<!-- GuestLayout.vue -->
<template>
    <div class="layout-container">
      <nav class="navbar">
        <div class="container">
          <a href="/" class="home-link">Home</a>
          <div class="auth-links">
            <a href="/login" class="login-link">Login</a>
            <a href="/register" class="register-link">Register</a>
          </div>
        </div>
      </nav>
  
      <div class="content-container">
        <slot />
      </div>
    </div>
  </template>
  
  <script setup>
  import { Link } from '@inertiajs/vue3';
  </script>
  
  <style scoped>
  .layout-container {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-top: 1.5rem;
    background-color: #000000;
  }
  
  .navbar {
    background-color: #3b82f6; 
    width: 100%;
    padding: 1rem 0;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }
  
  .container {
    max-width: 1280px;
    margin-left: auto;
    margin-right: auto;
    display: flex;
    justify-content: space-between;
  }
  
  .home-link {
    color: white;
    font-weight: bold;
    font-size: 1.125rem; 
    text-decoration: none;
  }
  
  .auth-links a {
    color: white;
    margin-right: 1rem;
    text-decoration: none;
  }
  
  .auth-links a:last-child {
    margin-right: 0;
  }
  
  .content-container {
    width: 100%;
    max-width: 28rem; 
    margin-top: 1.5rem;
    padding: 1.5rem;
    background-color: white;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    border-radius: 0.375rem; 
    overflow: hidden;
    background-color: #374151; 
  }
  </style>
  