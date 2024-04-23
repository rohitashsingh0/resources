import React, { useEffect, useState } from "react";
import { Link } from "react-router-dom";

const MainNavbar = () => {
  const [isScrolled, setIsScrolled] = useState(false);

  useEffect(() => {
    const handleScroll = () => {
      if (window.scrollY > 50) {
        setIsScrolled(true);
      } else {
        setIsScrolled(false);
      }
    };

    window.addEventListener("scroll", handleScroll);

    return () => {
      window.removeEventListener("scroll", handleScroll);
    };
  }, []);

  return (
    <>

            <section className={`header-section ${isScrolled ? "nav-scroll" : ""}`}>
</>
)

export default MainNavbar;
