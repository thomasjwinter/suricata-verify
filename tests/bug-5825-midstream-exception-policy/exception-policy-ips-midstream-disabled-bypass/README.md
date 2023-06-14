# Test

Check that the midstream exception policy is properly applied in case Suricata
has stream midstream pick-up sessions disabled. In this test the exception policy
for midstream sessions is set to ``bypass``. This test is for IPS mode.

# Behavior

We expect to see no alerts nor ``http`` events logged, as the flow won't be inspected.
Flow will be bypassed.

# Pcap

Pcap comes from the test ``exception-policy-midstream-03`` and is the result of a
curl to www.testmyids.com.