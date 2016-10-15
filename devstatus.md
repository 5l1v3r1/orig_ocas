#Understanding Status thru tests
This section is an attempt to explain what is implemented so far 
and what needs to be done next.
It will use tests as a way to do this.
Tests that pass show functioning code.
Work to be done is shown thru tests that are incomplete, non-existent, or failing.
Status is:
- P - tests written, code written, tests pass
- F - tests written, tests fail
- N - tests not written
- ? - some other state that needs explaining

## 1. Sanity

- P - test get to /ok correctly processed
   * status=200, body=ok
- P - test get to /status simply processed 
   * status=200, body=meaningless for now until real status code added
- P - test get to /openc2 correctly processed (rejected with 405 return)
- P - test no-http-body correctly processed (rejected with 400 return)
- P - test media-type-not-json correctly processed (rejected with 415 return)
- P - test bad json correctly processed (rejected with 400 return)

## 2. Simple single command validator

### 2.1 Action Sanity
- ? - test all actions 'simply' processed
   * 200 return after validated action process spun up
   * but without target/actuator/modifier semantics
   * P - action=scan
   * N - action= remaining 36 actions
- P - test action=nonsense correctly processed (rejected with 400 return)
   * note this is not exhautive test of all invalid actions

### 2.2 Target Sanity
- N - test target=network connection simply processed
- N - test (first few) targets simply processed

### 2.3 Actuator Sanity
- N - test actuator=network-firewall simply processed
- N - test (first few) actuators simply processed
- N - test (first one, few) modifiers simply processed

### 2.4 Command Specifics
- N - test following command and response
   * action =  deny
   * target = network connection
   * actuator = network firewall
   * modifiers = (fill out correctly for reply requested, command_id)
- N - test following command
   * action =  fill in
   * target = fill in
   * actuator = fill in
   * modifiers = (fill out correctly for reply requested, command_id)
- N - test all X targets simply processed
- N - test all X actuators simply processed
- N - test all X modifiers simply processed

## 3. Simple single command simulator
what goes here?

## 4. Simple single command simulator
what goes here?

## 5. Playbook simulator
what goes here?
