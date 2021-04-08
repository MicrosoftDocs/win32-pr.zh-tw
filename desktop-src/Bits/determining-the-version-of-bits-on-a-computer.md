---
title: 判斷電腦上的位版本
description: 若要判斷用戶端電腦上的位版本，請檢查 QMgr.dll 的版本。
ms.assetid: b6057ae4-3bf0-4304-ae50-5da5e82a0bed
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c94e151608511ec59e52befdef6e4f63e44476e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671440"
---
# <a name="determining-the-version-of-bits-on-a-computer"></a>判斷電腦上的位版本

若要判斷用戶端電腦上的位版本，請檢查 QMgr.dll 的版本。 若要尋找 DLL 的版本號碼：

-   在% windir% System32 中找出 QMgr.dll \\ 。
-   以滑鼠右鍵按一下 QMgr.dll，然後按一下 [ **屬性**]。
-   按一下 [ **版本** ] 索引標籤。
-   記下版本號碼。

您也可以使用下列 PowerShell 程式碼來判斷您系統上的 .dll 版本：

`get-item "C:\Windows\System32\qmgr.dll" | Select-Object -ExpandProperty VersionInfo`

如果 DLL 也存在於% windir% \\ System32 \\ 位中，請重複上述步驟。 BITS 使用具有較高版本號碼的 DLL。

下表列出 BITS 的版本及其對應的 QMgr.dll 檔案版本號碼。



| BITS 版本 | QMgr.dll 檔案版本號碼 |
|--------------|------------------------------|
| BITS 10。1    | 7.8. xxxx                |
| BITS 5。0     | 7.7. xxxx                |
| BITS 4。0     | 7.5. xxxx                |
| BITS 3。0     | 7.0. xxxx                |
| BITS 2.5     | 6.7. xxxx                |
| BITS 2。0     | 6.6. xxxx                |
| BITS 1。5     | 6.5. xxxx                |
| BITS 1。2     | 6.2. xxxx                |
| BITS 1。0     | 6.0. xxxx                |



 

您也可以使用符號類別識別碼來判斷電腦上已註冊的位版本。 下表列出 BITS 的版本及其對應的符號類別識別碼。 如果未註冊類別， **CoCreateInstance** 函數會傳回 **REGDB \_ E \_ CLASSNOTREG** 。



| BITS 版本  | 符號類別識別碼         |
|---------------|-----------------------------------|
| BITS 10。1     | CLSID \_ BackgroundCopyManager10 \_ 1 |
| BITS 5。0      | CLSID \_ BackgroundCopyManager5 \_ 0  |
| BITS 4。0      | CLSID \_ BackgroundCopyManager4 \_ 0  |
| BITS 3。0      | CLSID \_ BackgroundCopyManager3 \_ 0  |
| BITS 2.5      | CLSID \_ BackgroundCopyManager2 \_ 5  |
| BITS 2。0      | CLSID \_ BackgroundCopyManager2 \_ 0  |
| BITS 1。5      | CLSID \_ BackgroundCopyManager1 \_ 5  |
| 位1.2、1。0 | CLSID \_ BackgroundCopyManager      |



 

 

 




