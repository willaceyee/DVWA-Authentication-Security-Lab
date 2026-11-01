# Remediation verification checklist

These are proposed checks for a corrected training application. They have **not** been executed against an implemented fix in this repository.

| Control | Verification goal |
| --- | --- |
| Login throttling | A bounded sequence of failed attempts triggers the documented server-side limit |
| Progressive delay | The intended delay is enforced by the server and can be measured |
| Temporary lockout | Recovery follows the specified policy, with assessment of account denial-of-service risk |
| MFA | Correct use of a password alone does not bypass the additional required factor |
| Failure monitoring | Repeated failures produce useful security events without recording plaintext passwords |
| Consistent failure messages | Responses avoid disclosing whether an account exists |
| Legitimate access | A valid user can authenticate normally after the defined recovery conditions |

Set thresholds and acceptance criteria before retesting. Record observations and distinguish a proposed defense from a verified one. The control rationale follows [OWASP authentication guidance](https://cheatsheetseries.owasp.org/cheatsheets/Authentication_Cheat_Sheet.html).
