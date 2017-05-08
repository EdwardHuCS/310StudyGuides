# Lecture 17 Engineering Secure Software
__Lecture 17: security properties, confidentiality, avaliblitiy, integrity, secure design principles, focused on good things to enhance security, 10 different design principles, security/implementation, common vulnerabilities in web app and mobile code, examples, definitions, countermeasures for each security vulnerability, definitions and process of penetration testing__

## Security Properties
CIA
- Confidentiality
    - keep data contained
- Integrity
    - keep data secure
- Availibility
    - keep data available
- Privacy
    - prevent access to data
- Anonymity
    - keep system nameless and unidentifable
- Non-repudiation
- Safety
- Liveness
## Secure Design Principles
- Economy of Mechanism
    - Keep the design as simple and small as possible
- Fail-safe Defaults
    - The principle of fail-safe defaults states that, unless a subject is given explicit access to an object, it should be denied access to that object
- Complete Mediation
    - Every access to every object must be checked for authority. This principle, when systematically applied, is the primary underpinning of the protection system
- Open Design
    - The principle of open design states that the security of a mechanism should not depend on the secrecy of its design or implementation.
- Separation of Privilege
    - The principle of separation of privilege states that a system should not grant permission based on a single condition.
- Least Privilege
- Least Common Mechanism
    - The principle of least common mechanism states that mechanisms used to access resources should not be shared.
- Pyschological Acceptability
    - The principle of psychological acceptability states that security mechanisms should not make the resource more difficult to access than if the security mechanisms were not present.
- Work Factor
    - Stronger security measures pose more work for the attacker
- Compromise Recording
    - The system should keep records of attacks even if the attacks aren’t necessarily blocked
## Common Vulnerabilities
1. Injection
    - tricking an application into including unintended commands in data
2. Broken Authentication and Session Management
    - http is stateless protocol, Session ID is used to track state, but is exposed in browser and logs
3. Cross Site Scripting
    - user enters script into web page that stores data on server
    - script runs inside victim's browser window with full access to dom and cookies
4. Insecure direct object references
    - user notices his acct parameter is 1, changes to 2
    - eliminate direct object reference
5. Security misconfig
6. Sensitive Data Exposure
    - storing and transmitting sensitive data insecurely
7. Missing function level access control
    - user can elevate to admin or manager
8. Cross Site Request Forgery
    - attack where victim's browser is tricked into issuing a command to vulnerable web app
9. Using known vulnerable components
10. Unvalidated redirects and forwards
    - send link to victim
## Penetration Testing
1. Info gathering
2. Attack generation
3. response analysis
4. report