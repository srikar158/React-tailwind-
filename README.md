npx create-react-app react-props-tailwind
cd react-props-tailwind
npm install -D tailwindcss postcss autoprefixer
npx tailwindc/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["./src/**/*.{js,jsx,ts,tsx}"],
  theme: {
    extend: {},
  },
  plugins: [],
};
ss init -p
@tailwind base;
@tailwind components;
@tailwind utilities;
import './index.css';
src/
 ┣ components/
 ┃ ┣ Header.js
 ┃ ┣ Card.js
 ┃ ┣ Message.js
 ┃ ┗ Footer.js
 ┗ App.js
import React from "react";

const Header = ({ title }) => {
  return (
    <header className="bg-blue-600 text-white p-4 text-center text-xl font-bold rounded">
      {title}
    </header>
  );
};

export default Header;
import React from "react";

const Card = ({ name, age }) => {
  return (
    <div className="bg-white shadow-md rounded p-4 m-4 border border-gray-200">
      <h2 className="text-lg font-semibold text-gray-700">Name: {name}</h2>
      <p className="text-gray-500">Age: {age}</p>
    </div>
  );
};

export default Card;
import React from "react";

const Message = ({ msg }) => {
  return (
    <div className="bg-green-100 text-green-800 border border-green-300 rounded p-2 m-2 text-center">
      {msg}
    </div>
  );
};

export default Message;

import React from "react";

const Footer = () => {
  return (
    <footer className="bg-gray-800 text-white text-center p-3 rounded mt-4">
      &copy; 2025 My React App
    </footer>
  );
};

export default Footer;
import React from "react";
import Header from "./components/Header";
import Card from "./components/Card";
import Message from "./components/Message";
import Footer from "./components/Footer";

function App() {
  const user = {
    name: "Chinnu",
    age: 21,
    message: "Welcome to React with Tailwind CSS!"
  };

  return (
    <div className="min-h-screen bg-gray-100 p-4">
      <Header title="React + Tailwind Demo" />
      <Message msg={user.message} />
      <Card name={user.name} age={user.age} />
      <Footer />
    </div>
  );
}

export default App;
npm start
