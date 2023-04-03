# Bug recreate

 1. Run `pollapo install`
 2. Run `pb gen ts --entry-path=".pollapo"`

# Observed outcome

The file `out/messages/opentelemetry/proto/collector/trace/v1/ExportTraceServiceRequest.ts` is invalid TS (see Line 61):

```
    const value = wireValues.map((wireValue) => ).filter(x => x !== undefined);
```

The file `out/messages/opentelemetry/proto/trace/v1/Span.ts` is invalid TS (see Line 293):

```
    const value = wireValues.map((wireValue) => ).filter(x => x !== undefined);
```

There are possibly others, but you get the point.

# Expected outcome

All generated files are valid TS
