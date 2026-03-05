# Splunk Queries Used

## Privileged Logons

index=* EventCode=4672

## Successful Logons

index=* EventCode=4624

## Failed Logons

index=* EventCode=4625

## Process Creation (Sysmon)

index=* EventCode=1

## Network Connections (Sysmon)

index=* EventCode=3
