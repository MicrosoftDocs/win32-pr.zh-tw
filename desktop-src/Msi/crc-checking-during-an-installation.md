---
description: Windows Installer 會提供) 檔案 (CRC 的迴圈重複檢查。
ms.assetid: c895488b-6e60-4175-8865-4ba4b0cb2d9a
title: 安裝期間的 CRC 檢查
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b80a9b1900abf6c294911803df155a4c75025f5ad5ef01609af7345b0431e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118379913"
---
# <a name="crc-checking-during-an-installation"></a>安裝期間的 CRC 檢查

Windows Installer 會提供) 檔案 (CRC 的迴圈重複檢查。 CRC 檢查是類似于總和檢查碼的錯誤檢查機制，可讓應用程式判斷檔案中的資訊是否已修改。 在 Windows Installer 完成複製檔案之後，它會從來源和目的地檔案取得 CRC 值。 安裝程式會將原始的 CRC 戳記簽入檔案中，並將其與從複本計算出來的 CRC 進行比較。 如果原始 CRC 值為非 null，且與複製上計算的 CRC 不同，CRC 檢查就會失敗。 如果原始 CRC 為 null，則不會執行任何檢查。

在下列情況下，Windows Installer 會對檔案執行 CRC 檢查：

-   如果已設定 [MSICHECKCRCS 屬性](msicheckcrcs.md) ，而且 **msidbFileAttributesChecksum** 包含在檔案 [資料表](file-table.md)中檔案記錄的 [屬性] 欄位中。 安裝、複製或移動檔案之後，安裝程式會進行 CRC 檢查一次。
-   如果 [ [MSICHECKCRCS] 屬性](msicheckcrcs.md) 已設定，而且 **msidbFileAttributesChecksum** 包含在檔案的記錄的 [屬性] 欄位中 [，則](file-table.md)安裝程式會在修補檔案之後進行 CRC 檢查。
-   如果 **msidbFileAttributesChecksum** 包含在檔案的記錄檔中的 [屬性] 欄位 [中，則](file-table.md)安裝程式會先進行 CRC 檢查，再系結影像。

如果檢查在系結映射之前失敗，安裝程式會報告記錄檔中的下列兩個錯誤，並繼續安裝，而不會系結檔案。



| 程式碼 | 訊息                                               |
|------|-------------------------------------------------------|
| 2941 | 無法計算檔2的 CRC \[ \] 。             |
| 2942 | 未在2個檔案上執行 BindImage 動作 \[ \] 。 |



 

如果在複製、複製或修補未壓縮檔案後檢查失敗，安裝程式會報告下列錯誤。 如果複製壓縮檔案之後的檢查失敗，也會報告此錯誤。 如果檔案具有 **msidbFileAttributesVital** 屬性，則會將該檔案視為重要的安裝，而且使用者會取得重試或取消安裝的選項。 如果檔案在檔案 [資料表](file-table.md)的 [屬性] 資料行中標示為 nonvital，使用者可能會忽略錯誤並繼續、重試或取消安裝。



| 程式碼 | 訊息                                         |
|------|-------------------------------------------------|
| 1331 | 無法正確複製2個檔案 \[ \] ： CRC 錯誤。 |



 

請注意，只會移動未壓縮檔案。 如果在移動未壓縮檔案後檢查失敗，安裝程式會顯示下列錯誤。 如果檔案具有 **msidbFileAttributesVital** 屬性，則會將該檔案視為對安裝很重要，且安裝會失敗。 如果檔案 [資料表](file-table.md)的 [屬性] 資料行中的檔案標示為 nonvital，使用者會取得取消或忽略錯誤的選項，並繼續進行安裝。



| 程式碼 | 訊息                                         |
|------|-------------------------------------------------|
| 1332 | 無法正確地移動 \[ 2 個檔案 \] ： CRC 錯誤。 |



 

如果在修補未壓縮檔案之後檢查失敗，安裝程式會顯示下列錯誤。 如果檔案具有 **msidbFileAttributesVital** 屬性，則會將該檔案視為對安裝很重要，且安裝會失敗。 如果檔案 [資料表](file-table.md)的 [屬性] 資料行中的檔案標示為 nonvital，使用者會取得取消或忽略錯誤的選項，並繼續進行安裝。



| 程式碼 | 訊息                                          |
|------|--------------------------------------------------|
| 1333 | 無法正確修補2個檔案 \[ \] ： CRC 錯誤。 |



 

 

 



