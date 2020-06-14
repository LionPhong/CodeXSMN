# CodeXSMN
 Prevent sending early termination of appop use If a package starts a particular appop both as active and noted, once one of them is finished (usually noted after 5s), a message will be sent to callbacks indicating the end of the use. However, the app op may still be active. This could result in the removal of indicators prematurely from notifications. This change prevents that from happening by checking if the app op is still in use by that combination uid/package (either active or noted) and not notifying listeners if that's the case. Test: atest AppOpsControllerTest Test: use app from bug report. Observe that notification does not lose the microphone indicator Bug: 144092031 Merged-In: I180e7c257e6171e7686ba7eda9bf02249358ed0 Change-Id: I94473c3ccf1318dac29f067dade91e540e20285e (cherry picked from commit 1a459638398446938a20b32fa0fbc63ad4bd505f) packages/SystemUI/src/com/android/systemui/appops/AppOpsControllerImpl.java[diff]packages/SystemUI/tests/src/com/android/systemui/appops/AppOpsControllerTest.java[diff]

2 files changed

tree: a4184bd4a1e739e4b275fe9f0a8153eac6e6f1ff



