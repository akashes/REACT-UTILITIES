
import React, { useState } from 'react';
import { RxHamburgerMenu, RxCross2 } from "react-icons/rx";

const Header = () => {
    const [showMenu, setShowMenu] = useState(false);

    const toggleMenu = () => setShowMenu(prev => !prev);

    return (
        <div className="w-[100%] flex flex-col sm:flex-row justify-between px-6 py-5 bg-slate-200 relative">
            {/* Header with Logo & Menu Button */}
            <div className="flex justify-between w-full sm:w-auto">
                <h1 className="text-2xl font-semibold">MirrorSoft</h1>
                <button className="sm:hidden text-3xl p-2" onClick={toggleMenu}>
                    {showMenu ? <RxCross2 /> : <RxHamburgerMenu />}
                </button>
            </div>

            {/* Mobile Menu (Slide-in Sidebar) */}
            <div className={`fixed top-0 right-0 w-1/2 h-full bg-white shadow-lg z-50 transition-transform duration-500 ${showMenu ? "translate-x-0" : "translate-x-full"} sm:hidden`}>
                <button className="absolute top-5 right-5 text-3xl" onClick={toggleMenu}>
                    <RxCross2 />
                </button>
                <ul className="flex flex-col items-center gap-6 pt-20">
                    {["Home", "Services", "About", "Contact"].map((item) => (
                        <li key={item} className="text-xl hover:text-blue-600 transition">
                            <a href="#" onClick={() => setShowMenu(false)}>{item}</a>
                        </li>
                    ))}
                </ul>
            </div>

            {/* Desktop Menu */}
            <ul className="hidden sm:flex gap-6 items-center">
                {["Home", "Services", "About", "Contact"].map((item) => (
                    <li key={item} className="text-lg hover:text-blue-600 transition">
                        <a href="#">{item}</a>
                    </li>
                ))}
            </ul>

            {/* Overlay for Mobile Menu */}
            {showMenu && <div className="fixed inset-0 bg-black/40 sm:hidden" onClick={toggleMenu}></div>}
        </div>
    );
};

export default Header;
