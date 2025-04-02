<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DataEntryPro - Earn Money Online</title>
    <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
    <style>
        :root {
            --primary-color: #4e73df;
            --secondary-color: #1cc88a;
            --dark-color: #5a5c69;
            --light-color: #f8f9fc;
        }
        
        body {
            font-family: 'Nunito', sans-serif;
            background-color: var(--light-color);
        }
        
        .hero-section {
            background: linear-gradient(135deg, var(--primary-color) 0%, #224abe 100%);
            color: white;
            padding: 5rem 0;
        }
        
        .feature-card {
            border-radius: 10px;
            transition: transform 0.3s;
            margin-bottom: 20px;
        }
        
        .feature-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 20px rgba(0,0,0,0.1);
        }
        
        .nav-pills .nav-link.active {
            background-color: var(--primary-color);
        }
        
        .btn-primary {
            background-color: var(--primary-color);
            border-color: var(--primary-color);
        }
        
        .btn-success {
            background-color: var(--secondary-color);
            border-color: var(--secondary-color);
        }
        
        .pricing-card {
            border: none;
            border-radius: 10px;
            transition: all 0.3s;
        }
        
        .pricing-card:hover {
            transform: scale(1.03);
        }
        
        .pricing-header {
            background-color: var(--primary-color);
            color: white;
            border-top-left-radius: 10px;
            border-top-right-radius: 10px;
        }
        
        .dashboard-sidebar {
            background-color: var(--primary-color);
            min-height: 100vh;
            color: white;
        }
        
        .dashboard-content {
            background-color: var(--light-color);
        }
        
        .wallet-card {
            border-radius: 10px;
            box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        }
        
        .error-highlight {
            border: 2px solid #e74a3b !important;
        }
        
        /* New styles for page-based dashboard */
        .page-container {
            display: none;
        }
        
        .logged-in-only {
            display: none;
        }
        
        .logged-out-only {
            display: block;
        }
        
        .logged-in .logged-in-only {
            display: block;
        }
        
        .logged-in .logged-out-only {
            display: none;
        }
        
        .logged-in #landingPage {
            display: none;
        }
        
        .logged-in #dashboardPage, .logged-in #startWorkPage {
            display: block;
        }
        
        .entry-counter {
            font-size: 1.2rem;
            font-weight: bold;
            color: var(--primary-color);
        }
    </style>
</head>
<body>
    <!-- Navigation -->
    <nav class="navbar navbar-expand-lg navbar-dark bg-dark">
        <div class="container">
            <a class="navbar-brand" href="#" id="homeLink">DataEntryPro</a>
            <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse" id="navbarNav">
                <ul class="navbar-nav me-auto logged-out-only">
                    <li class="nav-item">
                        <a class="nav-link" href="#about">About Us</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#how-it-works">How It Works</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#pricing">Pricing</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#demo">Demo</a>
                    </li>
                </ul>
                <ul class="navbar-nav me-auto logged-in-only">
                    <li class="nav-item">
                        <a class="nav-link" href="#" id="dashboardNavLink">Dashboard</a>
                    </li>
                    <li class="nav-item">
                        <a class="nav-link" href="#" id="startWorkNavLink">Start Work</a>
                    </li>
                </ul>
                <div class="d-flex" id="authButtons">
                    <button class="btn btn-outline-light me-2 logged-out-only" data-bs-toggle="modal" data-bs-target="#loginModal">Login</button>
                    <button class="btn btn-primary logged-out-only" data-bs-toggle="modal" data-bs-target="#registerModal">Register</button>
                    <div class="d-flex logged-in-only" id="userSection">
                    <button class="btn btn-danger" id="logoutBtn">Logout</button>
                    </div>
                </div>
            </div>
        </div>
    </nav>

    <!-- Landing Page (Visible when logged out) -->
    <div id="landingPage">
        <!-- Hero Section -->
        <section class="hero-section text-center">
            <div class="container">
                <h1 class="display-4 fw-bold mb-4">Earn Money with Data Entry</h1>
                <p class="lead mb-5">Join thousands of people earning money from home by completing simple data entry tasks</p>
                <button class="btn btn-light btn-lg me-2" data-bs-toggle="modal" data-bs-target="#registerModal">Get Started</button>
            </div>
        </section>

        <!-- About Us Section -->
        <section id="about" class="py-5">
            <div class="container">
                <div class="row align-items-center">
                    <div class="col-lg-6">
                        <h2 class="fw-bold mb-4">About Us</h2>
                        <p class="lead">DataEntryPro is a leading platform connecting businesses with remote data entry professionals.</p>
                        <p>Founded in 2015, we've helped over 50,000 people earn supplemental income from home while providing businesses with accurate data entry services.</p>
                        <p>Our mission is to create flexible earning opportunities for anyone with basic computer skills and an internet connection.</p>
                    </div>
                    <div class="col-lg-6">
                        <img src="https://images.unsplash.com/photo-1551288049-bebda4e38f71?ixlib=rb-1.2.1&auto=format&fit=crop&w=500&q=60" alt="About Us" class="img-fluid rounded shadow">
                    </div>
                </div>
            </div>
        </section>

        <!-- How It Works Section -->
        <section id="how-it-works" class="py-5 bg-light">
            <div class="container">
                <h2 class="text-center fw-bold mb-5">How It Works</h2>
                <div class="row">
                    <div class="col-md-4">
                        <div class="card feature-card h-100">
                            <div class="card-body text-center">
                                <div class="bg-primary bg-gradient text-white rounded-circle p-3 mb-3 mx-auto" style="width: 70px; height: 70px;">
                                    <i class="fas fa-user-plus fa-2x"></i>
                                </div>
                                <h5>1. Register</h5>
                                <p>Create your free account and complete your profile</p>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div class="card feature-card h-100">
                            <div class="card-body text-center">
                                <div class="bg-primary bg-gradient text-white rounded-circle p-3 mb-3 mx-auto" style="width: 70px; height: 70px;">
                                    <i class="fas fa-tasks fa-2x"></i>
                                </div>
                                <h5>2. Complete Tasks</h5>
                                <p>Enter data accurately according to the instructions</p>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div class="card feature-card h-100">
                            <div class="card-body text-center">
                                <div class="bg-primary bg-gradient text-white rounded-circle p-3 mb-3 mx-auto" style="width: 70px; height: 70px;">
                                    <i class="fas fa-money-bill-wave fa-2x"></i>
                                </div>
                                <h5>3. Earn Money</h5>
                                <p>Get paid for each approved data entry submission</p>
                            </div>
                        </div>
                    </div>
                </div>
                
                <div class="row mt-5">
                    <div class="col-md-6">
                        <div class="card">
                            <div class="card-header bg-primary text-white">
                                <h5 class="mb-0">Earning Details</h5>
                            </div>
                            <div class="card-body">
                                <ul class="list-group list-group-flush">
                                    <li class="list-group-item d-flex justify-content-between align-items-center">
                                        Free Plan
                                        <span class="badge bg-primary rounded-pill">₹0.50 per entry (10/day max)</span>
                                    </li>
                                    <li class="list-group-item d-flex justify-content-between align-items-center">
                                        Premium Plan (3 months)
                                        <span class="badge bg-primary rounded-pill">₹1 per entry (50/day max)</span>
                                    </li>
                                    <li class="list-group-item d-flex justify-content-between align-items-center">
                                        Premium Plan (1 year)
                                        <span class="badge bg-primary rounded-pill">₹3 per entry (50/day max)</span>
                                    </li>
                                    <li class="list-group-item d-flex justify-content-between align-items-center">
                                        Referral Bonus
                                        <span class="badge bg-success rounded-pill">10% of premium plans</span>
                                    </li>
                                </ul>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-6">
                        <div class="card">
                            <div class="card-header bg-primary text-white">
                                <h5 class="mb-0">Payment Information</h5>
                            </div>
                            <div class="card-body">
                                <ul class="list-group list-group-flush">
                                    <li class="list-group-item">Minimum withdrawal: ₹300 (Earning Wallet)</li>
                                    <li class="list-group-item">No minimum for Bonus Wallet</li>
                                    <li class="list-group-item">Withdrawals processed within 3-5 business days</li>
                                    <li class="list-group-item">Bank details required for withdrawal</li>
                                    <li class="list-group-item">Track withdrawal status in dashboard</li>
                                </ul>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Demo Video Section -->
        <section id="demo" class="py-5">
            <div class="container">
                <h2 class="text-center fw-bold mb-5">See How It Works</h2>
                <div class="row justify-content-center">
                    <div class="col-lg-8">
                        <div class="ratio ratio-16x9">
                            <iframe src="https://www.youtube.com/embed/example" allowfullscreen></iframe>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Pricing Section -->
        <section id="pricing" class="py-5 bg-light">
            <div class="container">
                <h2 class="text-center fw-bold mb-5">Choose Your Plan</h2>
                <div class="row">
                    <div class="col-md-4">
                        <div class="card pricing-card mb-4">
                            <div class="card-header pricing-header text-center py-3">
                                <h4 class="my-0 fw-normal">Free</h4>
                            </div>
                            <div class="card-body">
                                <h1 class="card-title pricing-card-title text-center">₹0<small class="text-muted fw-light">/mo</small></h1>
                                <ul class="list-unstyled mt-3 mb-4">
                                    <li><i class="fas fa-check text-success me-2"></i> ₹0.50 per entry</li>
                                    <li><i class="fas fa-check text-success me-2"></i> Max 10 entries per day</li>
                                    <li><i class="fas fa-check text-success me-2"></i> 60-second ads after each entry</li>
                                    <li><i class="fas fa-check text-success me-2"></i> Basic support</li>
                                    <li><i class="fas fa-times text-danger me-2"></i> No referral bonus</li>
                                </ul>
                                <button type="button" class="btn btn-lg btn-outline-primary w-100">Current Plan</button>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div class="card pricing-card mb-4">
                            <div class="card-header pricing-header text-center py-3">
                                <h4 class="my-0 fw-normal">Premium</h4>
                            </div>
                            <div class="card-body">
                                <h1 class="card-title pricing-card-title text-center">₹2999<small class="text-muted fw-light">/3mo</small></h1>
                                <ul class="list-unstyled mt-3 mb-4">
                                    <li><i class="fas fa-check text-success me-2"></i> ₹1 per entry</li>
                                    <li><i class="fas fa-check text-success me-2"></i> Max 50 entries per day</li>
                                    <li><i class="fas fa-check text-success me-2"></i> No ads for 3 months</li>
                                    <li><i class="fas fa-check text-success me-2"></i> Priority support</li>
                                    <li><i class="fas fa-check text-success me-2"></i> 10% referral bonus</li>
                                </ul>
                                <button type="button" class="btn btn-lg btn-primary w-100">Upgrade</button>
                            </div>
                        </div>
                    </div>
                    <div class="col-md-4">
                        <div class="card pricing-card mb-4">
                            <div class="card-header pricing-header text-center py-3">
                                <h4 class="my-0 fw-normal">Professional</h4>
                            </div>
                            <div class="card-body">
                                <h1 class="card-title pricing-card-title text-center">₹9999<small class="text-muted fw-light">/year</small></h1>
                                <ul class="list-unstyled mt-3 mb-4">
                                    <li><i class="fas fa-check text-success me-2"></i> ₹3 per entry</li>
                                    <li><i class="fas fa-check text-success me-2"></i> Max 50 entries per day</li>
                                    <li><i class="fas fa-check text-success me-2"></i> No ads for 1 year</li>
                                    <li><i class="fas fa-check text-success me-2"></i> 24/7 priority support</li>
                                    <li><i class="fas fa-check text-success me-2"></i> 10% referral bonus</li>
                                </ul>
                                <button type="button" class="btn btn-lg btn-primary w-100">Upgrade</button>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </section>

        <!-- Footer -->
        <footer class="bg-dark text-white py-4">
            <div class="container">
                <div class="row">
                    <div class="col-md-6">
                        <h5>DataEntryPro</h5>
                        <p>Earn money from home with simple data entry tasks.</p>
                    </div>
                    <div class="col-md-3">
                        <h5>Quick Links</h5>
                        <ul class="list-unstyled">
                            <li><a href="#about" class="text-white">About Us</a></li>
                            <li><a href="#how-it-works" class="text-white">How It Works</a></li>
                            <li><a href="#pricing" class="text-white">Pricing</a></li>
                        </ul>
                    </div>
                    <div class="col-md-3">
                        <h5>Contact</h5>
                        <ul class="list-unstyled">
                            <li><i class="fas fa-envelope me-2"></i> support@dataentrypro.com</li>
                            <li><i class="fas fa-phone me-2"></i> +91 1234567890</li>
                        </ul>
                    </div>
                </div>
                <hr>
                <div class="text-center">
                    <p class="mb-0">&copy; 2023 DataEntryPro. All rights reserved.</p>
                </div>
            </div>
        </footer>
    </div>

    <!-- Dashboard Page (Visible when logged in) -->
    <div id="dashboardPage" class="page-container">
        <div class="container-fluid">
            <div class="row">
                <!-- Sidebar -->
                <div class="col-md-3 col-lg-2 dashboard-sidebar p-0">
                    <div class="p-4">
                        <div class="text-center mb-4">
                            <img src="https://via.placeholder.com/100" class="rounded-circle mb-2" alt="Profile">
                            <h5 id="dashboardUsername">John Doe</h5>
                            <p class="text-white-50 small" id="userPlanDisplay">Free Plan</p>
                        </div>
                        <ul class="nav flex-column">
                            <li class="nav-item">
                                <a class="nav-link active text-white" href="#" data-section="dashboard"><i class="fas fa-tachometer-alt me-2"></i> Dashboard</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link text-white" href="#" data-section="startWork"><i class="fas fa-keyboard me-2"></i> Start Work</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link text-white" href="#" data-section="wallet"><i class="fas fa-wallet me-2"></i> Wallet</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link text-white" href="#" data-section="bankDetails"><i class="fas fa-university me-2"></i> Bank Details</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link text-white" href="#" data-section="withdrawals"><i class="fas fa-money-bill-wave me-2"></i> Withdrawals</a>
                            </li>
                            <li class="nav-item">
                                <a class="nav-link text-white" href="#" data-section="referrals"><i class="fas fa-user-friends me-2"></i> Referrals</a>
                            </li>
                        </ul>
                    </div>
                </div>
                
                <!-- Main Content -->
                <div class="col-md-9 col-lg-10 dashboard-content p-4">
                    <!-- Dashboard Section -->
                    <div id="dashboardSection">
                        <h4 class="mb-4">Overview</h4>
                        <div class="row mb-4">
                            <div class="col-md-4">
                                <div class="card bg-primary text-white mb-4">
                                    <div class="card-body">
                                        <h6 class="card-title">Total Entries</h6>
                                        <h2 class="mb-0" id="totalEntries">0</h2>
                                    </div>
                                </div>
                            </div>
                            <div class="col-md-4">
                                <div class="card bg-success text-white mb-4">
                                    <div class="card-body">
                                        <h6 class="card-title">Total Earnings</h6>
                                        <h2 class="mb-0" id="totalEarnings">₹0</h2>
                                    </div>
                                </div>
                            </div>
                            <div class="col-md-4">
                                <div class="card bg-info text-white mb-4">
                                    <div class="card-body">
                                        <h6 class="card-title">Total Withdrawals</h6>
                                        <h2 class="mb-0" id="totalWithdrawals">₹0</h2>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="card mb-4">
                            <div class="card-header">
                                <h5 class="mb-0">Today's Progress</h5>
                            </div>
                            <div class="card-body">
                                <div class="row">
                                    <div class="col-md-6">
                                        <div class="mb-3">
                                            <h6>Entries Completed Today</h6>
                                            <div class="progress">
                                                <div class="progress-bar" id="dailyProgressBar" role="progressbar" style="width: 0%"></div>
                                            </div>
                                            <div class="mt-2 text-center">
                                                <span id="entriesCompleted">0</span> / <span id="maxDailyEntries">10</span> entries
                                            </div>
                                        </div>
                                    </div>
                                    <div class="col-md-6">
                                        <div class="mb-3">
                                            <h6>Estimated Earnings Today</h6>
                                            <h3 id="dailyEarnings">₹0</h3>
                                        </div>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="card mb-4">
                            <div class="card-header">
                                <h5 class="mb-0">Recent Data Entry Earnings</h5>
                            </div>
                            <div class="card-body">
                                <div class="table-responsive">
                                    <table class="table table-hover">
                                        <thead>
                                            <tr>
                                                <th>Date</th>
                                                <th>Entries</th>
                                                <th>Rate</th>
                                                <th>Amount</th>
                                                <th>Status</th>
                                            </tr>
                                        </thead>
                                        <tbody id="dataEntryEarnings">
                                            <tr>
                                                <td colspan="5" class="text-center">No entries yet</td>
                                            </tr>
                                        </tbody>
                                    </table>
                                </div>
                            </div>
                        </div>
                        <div class="card">
                            <div class="card-header">
                                <h5 class="mb-0">Referral Program</h5>
                            </div>
                            <div class="card-body">
                                <p>Earn 10% of any premium plan purchased by your referrals!</p>
                                <div class="input-group mb-3">
                                    <input type="text" class="form-control" id="referralLink" value="https://dataentrypro.com/ref/username123" readonly>
                                    <button class="btn btn-primary" type="button" id="copyReferralBtn">Copy</button>
                                </div>
                                <div class="alert alert-info">
                                    <i class="fas fa-info-circle me-2"></i> Share your referral link with friends and earn bonuses when they join with premium plans.
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Start Work Page -->
    <div id="startWorkPage" class="page-container">
        <div class="container-fluid">
            <div class="row">
                <!-- Sidebar -->
                <div class="col-md-3 col-lg-2 dashboard-sidebar p-0">
                    <div class="p-4">
                        <div class="text-center mb-4">
                            <img src="https://via.placeholder.com/100" class="rounded-circle mb-2" alt="Profile">
                            <h5 id="workPageUsername">John Doe</h5>
                            <p class="text-white-50 small" id="workPagePlan">Free Plan</p>
                        </div>
                        <ul class="nav flex-column">
                            <li class="nav-item">
                                <a class="nav-link text-white" href="#" id="backToDashboard"><i class="fas fa-arrow-left me-2"></i> Back to Dashboard</a>
                            </li>
                        </ul>
                    </div>
                </div>
                
                <!-- Main Content -->
                <div class="col-md-9 col-lg-10 dashboard-content p-4">
                    <div class="d-flex justify-content-between align-items-center mb-4">
                        <h4>Data Entry Form</h4>
                        <div>
                            <span class="badge bg-primary me-2" id="currentRateBadge">Rate: ₹0.50 per entry</span>
                            <span class="entry-counter" id="entriesCounter">Entries today: 0/10</span>
                        </div>
                    </div>
                    <div class="alert alert-info mb-4">
                        <i class="fas fa-info-circle me-2"></i> Please enter the information accurately. Errors will be highlighted in red.
                    </div>
                    <form id="dataEntryForm">
                        <div class="row">
                            <div class="col-md-6 mb-3">
                                <label class="form-label">1. Company Name (Enter the full legal name of the company)</label>
                                <input type="text" class="form-control" data-field="companyName" required>
                            </div>
                            <div class="col-md-6 mb-3">
                                <label class="form-label">2. City (Enter the city where the company is located)</label>
                                <input type="text" class="form-control" data-field="city" required>
                            </div>
                        </div>
                        <div class="row">
                            <div class="col-md-6 mb-3">
                                <label class="form-label">3. Country (Enter the country where the company is based)</label>
                                <input type="text" class="form-control" data-field="country" required>
                            </div>
                            <div class="col-md-6 mb-3">
                                <label class="form-label">4. Zip Code (Enter the postal/zip code of the company)</label>
                                <input type="text" class="form-control" data-field="zipCode" required>
                            </div>
                        </div>
                        <div class="row">
                            <div class="col-md-6 mb-3">
                                <label class="form-label">5. Business ID (Enter the official business registration ID)</label>
                                <input type="text" class="form-control" data-field="businessId" required>
                            </div>
                        </div>
                        <div class="d-grid gap-2 mt-4">
                            <button type="submit" class="btn btn-primary btn-lg" id="submitEntryBtn">Submit Entry</button>
                        </div>
                    </form>
                </div>
            </div>
        </div>
    </div>

    <!-- Login Modal -->
    <div class="modal fade" id="loginModal" tabindex="-1" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title">Login to Your Account</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="loginForm">
                        <div class="mb-3">
                            <label for="loginEmail" class="form-label">Email address</label>
                            <input type="email" class="form-control" id="loginEmail" required>
                        </div>
                        <div class="mb-3">
                            <label for="loginPassword" class="form-label">Password</label>
                            <input type="password" class="form-control" id="loginPassword" required>
                        </div>
                        <div class="mb-3 form-check">
                            <input type="checkbox" class="form-check-input" id="rememberMe">
                            <label class="form-check-label" for="rememberMe">Remember me</label>
                        </div>
                        <button type="submit" class="btn btn-primary w-100">Login</button>
                    </form>
                    <div class="text-center mt-3">
                        <p>Don't have an account? <a href="#" data-bs-toggle="modal" data-bs-target="#registerModal" data-bs-dismiss="modal">Register</a></p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Register Modal -->
    <div class="modal fade" id="registerModal" tabindex="-1" aria-hidden="true">
        <div class="modal-dialog">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title">Create Your Account</h5>
                    <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
                </div>
                <div class="modal-body">
                    <form id="registerForm">
                        <div class="mb-3">
                            <label for="registerName" class="form-label">Full Name</label>
                            <input type="text" class="form-control" id="registerName" required>
                        </div>
                        <div class="mb-3">
                            <label for="registerEmail" class="form-label">Email address</label>
                            <input type="email" class="form-control" id="registerEmail" required>
                        </div>
                        <div class="mb-3">
                            <label for="registerPhone" class="form-label">Phone Number</label>
                            <input type="tel" class="form-control" id="registerPhone" required>
                        </div>
                        <div class="mb-3">
                            <label for="registerPassword" class="form-label">Password</label>
                            <input type="password" class="form-control" id="registerPassword" required>
                        </div>
                        <div class="mb-3">
                            <label for="registerConfirmPassword" class="form-label">Confirm Password</label>
                            <input type="password" class="form-control" id="registerConfirmPassword" required>
                        </div>
                        <div class="mb-3">
                            <label for="referralCode" class="form-label">Referral Code (Optional)</label>
                            <input type="text" class="form-control" id="referralCode">
                        </div>
                        <div class="mb-3 form-check">
                            <input type="checkbox" class="form-check-input" id="agreeTerms" required>
                            <label class="form-check-label" for="agreeTerms">I agree to the <a href="#">Terms and Conditions</a></label>
                        </div>
                        <button type="submit" class="btn btn-primary w-100">Register</button>
                    </form>
                    <div class="text-center mt-3">
                        <p>Already have an account? <a href="#" data-bs-toggle="modal" data-bs-target="#loginModal" data-bs-dismiss="modal">Login</a></p>
                    </div>
                </div>
            </div>
        </div>
    </div>

    <!-- Ad Modal -->
    <div class="modal fade" id="adModal" tabindex="-1" aria-hidden="true" data-bs-backdrop="static" data-bs-keyboard="false">
        <div class="modal-dialog modal-dialog-centered">
            <div class="modal-content">
                <div class="modal-header">
                    <h5 class="modal-title">Advertisement</h5>
                </div>
                <div class="modal-body text-center">
                    <p>Please watch this short advertisement to continue</p>
                    <div class="ratio ratio-16x9 mb-3">
                        <iframe src="https://www.youtube.com/embed/example" allowfullscreen></iframe>
                    </div>
                    <div class="progress mb-3">
                        <div class="progress-bar" id="adProgress" role="progressbar" style="width: 0%"></div>
                    </div>
                    <p id="adCountdown">60 seconds remaining</p>
                </div>
                <div class="modal-footer">
                    <button class="btn btn-primary" id="continueAfterAdBtn" disabled>Continue to Next Task</button>
                </div>
            </div>
        </div>
    </div>

    <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
    <script>
        // Simulate user authentication state
        let isLoggedIn = false;
        let currentUser = null;
        
        // DOM Elements
        const authButtons = document.getElementById('authButtons');
        const userSection = document.getElementById('userSection');
        const usernameDisplay = document.getElementById('usernameDisplay');
        const logoutBtn = document.getElementById('logoutBtn');
        const homeLink = document.getElementById('homeLink');
        const dashboardNavLink = document.getElementById('dashboardNavLink');
        const startWorkNavLink = document.getElementById('startWorkNavLink');
        const backToDashboard = document.getElementById('backToDashboard');
        const dashboardPage = document.getElementById('dashboardPage');
        const startWorkPage = document.getElementById('startWorkPage');
        const landingPage = document.getElementById('landingPage');
        
        // Update UI based on login state
        function updateUI() {
            if (isLoggedIn) {
                document.body.classList.add('logged-in');
                showDashboardPage();
                updateUserData();
            } else {
                document.body.classList.remove('logged-in');
                showLandingPage();
            }
        }
        
        function showLandingPage() {
            landingPage.style.display = 'block';
            dashboardPage.style.display = 'none';
            startWorkPage.style.display = 'none';
        }
        
        function showDashboardPage() {
            landingPage.style.display = 'none';
            dashboardPage.style.display = 'block';
            startWorkPage.style.display = 'none';
            updateDashboardData();
        }
        
        function showStartWorkPage() {
            landingPage.style.display = 'none';
            dashboardPage.style.display = 'none';
            startWorkPage.style.display = 'block';
            updateWorkPageData();
        }
        
        // Login function
        document.getElementById('loginForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const email = document.getElementById('loginEmail').value;
            const password = document.getElementById('loginPassword').value;
            
            // Simulate login (in a real app, this would be an API call)
            if (email && password) {
                isLoggedIn = true;
                currentUser = {
                    name: email.split('@')[0],
                    email: email,
                    plan: 'free',
                    entries: 0,
                    earnings: 0,
                    withdrawals: 0,
                    referrals: 0,
                    activeReferrals: 0,
                    referralBonus: 0,
                    earningWallet: 0,
                    bonusWallet: 0,
                    hasBankDetails: false,
                    dataEntryHistory: [],
                    entriesToday: 0,
                    lastEntryDate: null
                };
                
                // Update UI
                updateUI();
                
                // Close modal
                bootstrap.Modal.getInstance(document.getElementById('loginModal')).hide();
            }
        });
        
        // Register function
        document.getElementById('registerForm').addEventListener('submit', function(e) {
            e.preventDefault();
            const name = document.getElementById('registerName').value;
            const email = document.getElementById('registerEmail').value;
            const password = document.getElementById('registerPassword').value;
            
            // Simulate registration (in a real app, this would be an API call)
            if (name && email && password) {
                isLoggedIn = true;
                currentUser = {
                    name: name,
                    email: email,
                    plan: 'free',
                    entries: 0,
                    earnings: 0,
                    withdrawals: 0,
                    referrals: 0,
                    activeReferrals: 0,
                    referralBonus: 0,
                    earningWallet: 0,
                    bonusWallet: 0,
                    hasBankDetails: false,
                    dataEntryHistory: [],
                    entriesToday: 0,
                    lastEntryDate: null
                };
                
                // Update UI
                updateUI();
                
                // Close modal
                bootstrap.Modal.getInstance(document.getElementById('registerModal')).hide();
            }
        });
        
        // Logout function
        logoutBtn.addEventListener('click', function() {
            isLoggedIn = false;
            currentUser = null;
            updateUI();
        });
        
        // Navigation
        homeLink.addEventListener('click', function(e) {
            if (isLoggedIn) {
                e.preventDefault();
                showDashboardPage();
            }
        });
        
        dashboardNavLink.addEventListener('click', function(e) {
            e.preventDefault();
            showDashboardPage();
        });
        
        startWorkNavLink.addEventListener('click', function(e) {
            e.preventDefault();
            showStartWorkPage();
        });
        
        backToDashboard.addEventListener('click', function(e) {
            e.preventDefault();
            showDashboardPage();
        });
        
        function updateUserData() {
            if (!currentUser) return;
            
            // Update user display
            document.getElementById('usernameDisplay').textContent = currentUser.name;
            document.getElementById('dashboardUsername').textContent = currentUser.name;
            document.getElementById('workPageUsername').textContent = currentUser.name;
            
            // Update plan display
            const planDisplay = currentUser.plan === 'free' ? 'Free Plan' : 
                              currentUser.plan === 'premium3' ? 'Premium Plan (3 months)' : 'Professional Plan (1 year)';
            document.getElementById('userPlanDisplay').textContent = planDisplay;
            document.getElementById('workPagePlan').textContent = planDisplay;
            
            // Update rate badge
            const rate = currentUser.plan === 'free' ? '₹0.50' : 
                         currentUser.plan === 'premium3' ? '₹1' : '₹3';
            document.getElementById('currentRateBadge').textContent = `Rate: ${rate} per entry`;
            
            // Update max daily entries
            const maxEntries = currentUser.plan === 'free' ? 10 : 50;
            document.getElementById('maxDailyEntries').textContent = maxEntries;
            document.getElementById('entriesCounter').textContent = `Entries today: ${currentUser.entriesToday}/${maxEntries}`;
            
            // Update progress bar
            const progressPercent = (currentUser.entriesToday / maxEntries) * 100;
            document.getElementById('dailyProgressBar').style.width = `${progressPercent}%`;
        }
        
        function updateDashboardData() {
            if (!currentUser) return;
            
            updateUserData();
            
            // Update dashboard stats
            document.getElementById('totalEntries').textContent = currentUser.entries;
            document.getElementById('totalEarnings').textContent = `₹${currentUser.earnings}`;
            document.getElementById('totalWithdrawals').textContent = `₹${currentUser.withdrawals}`;
            document.getElementById('earningWalletBalance').textContent = `₹${currentUser.earningWallet}`;
            document.getElementById('bonusWalletBalance').textContent = `₹${currentUser.bonusWallet}`;
            document.getElementById('totalReferrals').textContent = currentUser.referrals;
            document.getElementById('activeReferrals').textContent = currentUser.activeReferrals;
            document.getElementById('totalReferralBonus').textContent = `₹${currentUser.referralBonus}`;
            document.getElementById('entriesCompleted').textContent = currentUser.entriesToday;
            
            // Calculate daily earnings
            const rate = currentUser.plan === 'free' ? 0.5 : 
                         currentUser.plan === 'premium3' ? 1 : 3;
            document.getElementById('dailyEarnings').textContent = `₹${(currentUser.entriesToday * rate).toFixed(2)}`;
            
            // Update data entry earnings table
            const dataEntryEarnings = document.getElementById('dataEntryEarnings');
            if (currentUser.dataEntryHistory.length === 0) {
                dataEntryEarnings.innerHTML = '<tr><td colspan="5" class="text-center">No entries yet</td></tr>';
            } else {
                dataEntryEarnings.innerHTML = currentUser.dataEntryHistory.map(entry => `
                    <tr>
                        <td>${entry.date}</td>
                        <td>${entry.count}</td>
                        <td>₹${entry.rate} per entry</td>
                        <td>₹${entry.amount}</td>
                        <td><span class="badge bg-success">Paid</span></td>
                    </tr>
                `).join('');
            }
        }
        
        function updateWorkPageData() {
            if (!currentUser) return;
            
            updateUserData();
            
            // Enable/disable submit button based on daily limit
            const maxEntries = currentUser.plan === 'free' ? 10 : 50;
            document.getElementById('submitEntryBtn').disabled = currentUser.entriesToday >= maxEntries;
        }
        
        // Data entry form submission
        document.getElementById('dataEntryForm').addEventListener('submit', function(e) {
            e.preventDefault();
            
            // Check if user has reached daily limit
            const maxEntries = currentUser.plan === 'free' ? 10 : 50;
            if (currentUser.entriesToday >= maxEntries) {
                alert(`You've reached your daily limit of ${maxEntries} entries.`);
                return;
            }
            
            // Validate form
            let hasError = false;
            const inputs = this.querySelectorAll('input[required]');
            
            inputs.forEach(input => {
                if (!input.value.trim()) {
                    input.classList.add('error-highlight');
                    hasError = true;
                } else {
                    input.classList.remove('error-highlight');
                }
            });
            
            if (hasError) {
                alert('Please fill in all required fields');
                return;
            }
            
            // Get current date
            const today = new Date();
            const entryDate = today.toLocaleDateString();
            
            // Calculate earnings based on plan
            const rate = currentUser.plan === 'free' ? 0.5 : 
                         currentUser.plan === 'premium3' ? 1 : 3;
            const earnings = rate;
            
            // Update user data
            currentUser.entries++;
            currentUser.entriesToday++;
            currentUser.earningWallet += earnings;
            currentUser.earnings += earnings;
            currentUser.lastEntryDate = today;
            
            // Add to data entry history
            const existingEntry = currentUser.dataEntryHistory.find(e => e.date === entryDate);
            if (existingEntry) {
                existingEntry.count++;
                existingEntry.amount += earnings;
            } else {
                currentUser.dataEntryHistory.push({
                    date: entryDate,
                    count: 1,
                    rate: rate,
                    amount: earnings
                });
            }
            
            // Show ad for free plan users
            if (currentUser.plan === 'free') {
                const adModal = new bootstrap.Modal(document.getElementById('adModal'));
                const adCountdown = document.getElementById('adCountdown');
                const adProgress = document.getElementById('adProgress');
                const continueBtn = document.getElementById('continueAfterAdBtn');
                
                let seconds = 60;
                adModal.show();
                
                const timer = setInterval(() => {
                    seconds--;
                    adCountdown.textContent = `${seconds} seconds remaining`;
                    adProgress.style.width = `${(60 - seconds) / 60 * 100}%`;
                    
                    if (seconds <= 0) {
                        clearInterval(timer);
                        continueBtn.disabled = false;
                        adCountdown.textContent = 'Ad completed!';
                    }
                }, 1000);
                
                continueBtn.addEventListener('click', function() {
                    adModal.hide();
                    // Reset form for next entry
                    document.getElementById('dataEntryForm').reset();
                    updateWorkPageData();
                }, { once: true });
            } else {
                // Reset form for next entry
                this.reset();
                updateWorkPageData();
            }
            
            // Update dashboard data if visible
            if (dashboardPage.style.display === 'block') {
                updateDashboardData();
            }
        });
        
        // Initialize UI
        updateUI();
    </script>
</body>
</html>
