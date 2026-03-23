# Url-shortener-DBMS
(possible) Project for Database course

The project involves designing and implementing a comprehensive URL Shortener Service with advanced analytics, user management, and enterprise features.
 
The system allows users to convert long URLs into shorter, more shareable links while tracking click analytics, managing custom domains, and organizing links into campaigns.

## Project Scope
 
### System Objectives
 
1. **URL Shortening**: Convert long URLs into shorter, unique codes for easy sharing
2. **Analytics & Tracking**: Log and analyze user clicks, geographic data, device types, and referrer information
3. **User Management**: Support different user tiers (free/premium) with appropriate features
4. **Enterprise Features**: Custom domains, team collaboration, API access, and link management
5. **Data Integrity**: Maintain consistency through constraints, triggers, and audit trails
 
### Target Users
 
- **End Users**: Anyone wanting to shorten URLs and track analytics
- **Premium Users**: Businesses using custom domains and team features
- **Administrators**: System managers overseeing platform health, abuse prevention, and performance
- **Stakeholders**: Business analysts viewing reports and performance metrics
 
---
 
## Core Features
 
### User-Facing Operations
 
1. **Account Management**
   - User registration and authentication
   - Profile management (name, email, subscription tier)
   - API key generation
 
2. **Link Management**
   - Create short links from long URLs
   - View all user-created short links
   - Delete or disable links
   - Set expiration dates on links
   - Bulk URL shortening operations
 
3. **Analytics Dashboard**
   - View click count and traffic trends
   - Geographic analytics (which countries/regions access links)
   - Device analytics (mobile, desktop, tablet)
   - Referrer tracking (where clicks originate)
   - Time-series analytics (clicks over time)
 
4. **Campaign Organization**
   - Group related short links into campaigns
   - Track campaign performance
   - Generate campaign-level reports
 
5. **Premium Features**
   - Custom domain configuration (e.g., mycompany.io/abc123)
   - Team/workspace management
   - Advanced permissions and access control
   - Extended analytics and retention
 
6. **Admin Features**
   - Monitor platform usage and performance
   - Flag or block suspicious/spam links
   - View audit logs of system changes
   - Generate platform-wide reports
 
---
 
## Database Design
 
### Key Entities
 
1. **Users** - System user accounts with roles and subscription details
2. **Subscriptions** - Pricing tiers and feature limits
3. **Short_Links** - Generated short codes with metadata
4. **Original_URLs** - Long URLs stored for reference
5. **Click_Analytics** - Individual click events with details
6. **User_Campaigns** - Organizing links into groups
7. **Custom_Domains** - Premium custom domain configurations
8. **Link_Access_Control** - Team/workspace permissions
9. **API_Keys** - Programmatic access tokens
10. **Audit_Log** - Track all system modifications
11. **Spam_Reports** - User reports of suspicious links
12. **Geographic_Data** - Click location information
13. **Device_Analytics** - Device type breakdown per link
14. **Referrer_Tracking** - Source of traffic for clicks
 
### Database Relationships
 
- Users have many Short_Links (1:N)
- Short_Links belong to Campaigns (N:1)
- Short_Links have many Click_Analytics (1:N)
- Users can have multiple API_Keys (1:N)
- Premium Users have Custom_Domains (1:N)
- Teams share Links through Access_Control (M:N)
