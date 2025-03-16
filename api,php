<?php

use Illuminate\Support\Facades\Route;
use App\Http\Controllers\AuthController;
use App\Http\Controllers\ProductController;
use App\Http\Controllers\CartController;
use App\Http\Controllers\OrderController;
use App\Http\Controllers\PaymentController;

// Authentication Routes
Route::post('/register', [AuthController::class, 'register']);
Route::post('/login', [AuthController::class, 'login']);
Route::post('/logout', [AuthController::class, 'logout'])->middleware('auth:sanctum');

// Product Routes
Route::get('/products', [ProductController::class, 'index']);
Route::get('/products/{id}', [ProductController::class, 'show']);
Route::post('/products', [ProductController::class, 'store'])->middleware('auth:sanctum');
Route::put('/products/{id}', [ProductController::class, 'update'])->middleware('auth:sanctum');
Route::delete('/products/{id}', [ProductController::class, 'destroy'])->middleware('auth:sanctum');

// Cart Routes
Route::get('/cart', [CartController::class, 'index'])->middleware('auth:sanctum');
Route::post('/cart/add', [CartController::class, 'add'])->middleware('auth:sanctum');
Route::post('/cart/remove', [CartController::class, 'remove'])->middleware('auth:sanctum');

// Order Routes
Route::get('/orders', [OrderController::class, 'index'])->middleware('auth:sanctum');
Route::post('/orders', [OrderController::class, 'store'])->middleware('auth:sanctum');
Route::get('/orders/{id}', [OrderController::class, 'show'])->middleware('auth:sanctum');

// Payment Routes
Route::post('/payment/paypal', [PaymentController::class, 'paypal'])->middleware('auth:sanctum');
Route::post('/payment/stripe', [PaymentController::class, 'stripe'])->middleware('auth:sanctum');
