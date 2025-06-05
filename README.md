# ConnectFourGame
/* Updated CSS for horizontal scrolling inventory */

/* Inventory View - Enable horizontal scrolling */
.inventory-view {
  height: 100%;
  overflow-y: auto;
  padding: 8px;
  scroll-behavior: smooth; /* Add smooth scrolling */
}

.inventory-category {
  margin-bottom: 24px;
}

.inventory-category h3 {
  color: black;
  margin-bottom: 12px;
  font-size: 1.2rem;
}

/* Updated inventory-items for horizontal scrolling */
.inventory-items {
  display: flex;
  overflow-x: auto; /* Enable horizontal scrolling */
  overflow-y: hidden; /* Prevent vertical scrolling */
  gap: 12px;
  padding-bottom: 8px; /* Add some padding for scrollbar */
  scroll-behavior: smooth; /* Smooth horizontal scrolling */
  
  /* Custom scrollbar styling */
  scrollbar-width: thin;
  scrollbar-color: #bdc3c7 #f8f9fa;
}

/* Webkit scrollbar styling for better appearance */
.inventory-items::-webkit-scrollbar {
  height: 8px;
}

.inventory-items::-webkit-scrollbar-track {
  background: #f8f9fa;
  border-radius: 4px;
}

.inventory-items::-webkit-scrollbar-thumb {
  background: #bdc3c7;
  border-radius: 4px;
  transition: background 0.2s ease;
}

.inventory-items::-webkit-scrollbar-thumb:hover {
  background: #95a5a6;
}

/* Updated inventory-item for horizontal layout */
.inventory-item {
  flex: 0 0 auto; /* Prevent flex shrinking */
  height: 25vh;
  width: 15vw;
  min-width: 120px; /* Minimum width to prevent items from being too small */
  background-color: white;
  border-radius: 8px;
  overflow: hidden;
  cursor: pointer;
  transition: all 0.3s ease; /* Smooth transition for hover effects */
  border: 3px solid transparent;
}

.inventory-item:hover {
  transform: translateY(-4px) scale(1.02); /* Enhanced hover effect */
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.15);
}

.inventory-item.selected {
  border-color: #062031;
  box-shadow: 0 0 0 2px rgba(52, 152, 219, 0.3);
  transform: translateY(-2px); /* Slight elevation for selected items */
}

.inventory-item img {
  width: 100%;
  height: 100%;
  object-fit: contain;
  transition: transform 0.2s ease;
}

.inventory-item:hover img {
  transform: scale(1.05); /* Subtle image zoom on hover */
}

/* Enhanced empty inventory state */
.empty-inventory {
  color: #bdc3c7;
  font-style: italic;
  padding: 40px 20px;
  text-align: center;
  background-color: rgba(255, 255, 255, 0.1);
  border-radius: 8px;
  min-width: 200px;
  flex: 0 0 auto;
}

/* Mobile responsiveness updates */
@media (max-width: 768px) {
  .inventory-items {
    justify-content: flex-start; /* Change from center to flex-start for horizontal scroll */
  }
  
  .inventory-item {
    width: 120px; /* Fixed width for mobile */
    height: 150px; /* Fixed height for mobile */
    min-width: 120px;
  }
}

@media (max-width: 480px) {
  .inventory-item {
    width: 100px;
    height: 130px;
    min-width: 100px;
  }
  
  .inventory-items {
    gap: 8px; /* Reduce gap on smaller screens */
  }
}
