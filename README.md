# CodeXSMN
 " login " "Phonglion "

 
If an AssetManager is closed and then finalized before assets that were opened with that AssetManager were finalized, nativeDestroy will be ran twice. Test that the fix the double destroy issue works as expected. Bug: 144028297 Test atest android.security.cts.AssetManagerTest Change-Id: Iecbb0cc60d1e2f93d7ec1fa263be2910de1a78a8 (cherry picked from commit 210730e5627e52b6f56a1765e242913908af72bd) tests/tests/security/src/android/security/cts/AssetManagerTest.java 
