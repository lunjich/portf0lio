
const root = document.documentElement;
const themeToggle = document.getElementById("themeToggle");
const themeLabel = document.getElementById("themeLabel");
const themeColor = document.querySelector('meta[name="theme-color"]');

function applyTheme(theme) {
    root.setAttribute("data-theme", theme);

    const isDark = theme === "dark";

    themeLabel.textContent = isDark ? "Light mode" : "Dark mode";

    themeToggle.setAttribute("aria-pressed", String(isDark));
    themeToggle.setAttribute(
        "aria-label",
        isDark ? "Switch to light mode" : "Switch to dark mode"
    );

    themeColor.setAttribute(
        "content",
        isDark ? "#2D3A47" : "#FFF7E6"
    );
}

let savedTheme = null;

try {
    savedTheme = localStorage.getItem("portfolio-theme");
} catch (error) {
    savedTheme = null;
}

applyTheme(savedTheme === "dark" ? "dark" : "light");

themeToggle.addEventListener("click", function () {
    const nextTheme =
        root.getAttribute("data-theme") === "dark" ? "light" : "dark";

    applyTheme(nextTheme);

    try {
        localStorage.setItem("portfolio-theme", nextTheme);
    } catch (error) {
        // Theme switching still works if storage is unavailable.
    }
});

document.getElementById("year").textContent = new Date().getFullYear();
