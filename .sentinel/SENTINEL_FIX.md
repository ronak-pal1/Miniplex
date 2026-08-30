# Sentinel proposed fix

Automated fix proposed by Sentinel for incident inc-checkout-svc-60cf8e.

Root cause: See investigation logs

## Patch

```diff
--- a/Miniplex/client/src/components/Modals/PaymentModal.tsx
+++ b/Miniplex/client/src/components/Modals/PaymentModal.tsx
@@ -48,7 +48,7 @@
     setLoading(true);
     const res = await userApi.post("/book", {
       transactionId,
       movieIds,
-      userId: "gaeahaeha",
       auditorium: slotInfo?.audi,
       date: slotInfo?.date ? formatDate(slotInfo.date) : "",
       noOfPersons: slotInfo?.noOfPerons,
```
