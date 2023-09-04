# Errors Reference

As described in [response-format.md](response-format.md "mention"), errors have a code and a message. The following ones are present in the application:

<table><thead><tr><th width="115.33333333333331">Code</th><th width="193">Name</th><th>Message</th></tr></thead><tbody><tr><td>999</td><td>DefaultError</td><td>An exception occured.</td></tr><tr><td>998</td><td>CustomMessage</td><td><em>&#x3C;a custom message></em></td></tr><tr><td>997</td><td>ForbiddenError</td><td>You are not authorized to call this action.</td></tr><tr><td>996</td><td>Cancelled</td><td>The request has been cancelled.</td></tr><tr><td>995</td><td>NotFound</td><td>The specified resource was not found.</td></tr><tr><td>994</td><td>Validation</td><td>One or more validation errors occurred.</td></tr><tr><td>500</td><td>InternalServerError</td><td>Internal server error.</td></tr></tbody></table>
