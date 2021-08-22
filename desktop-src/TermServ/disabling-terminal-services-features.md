---
title: 停用遠端桌面服務功能
description: 為了加強安全性，您可以選擇停用遠端桌面服務功能。
ms.assetid: 93505e3a-a4f8-4b94-8dbb-646140b6fa58
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e994999293a23468da78724fdcec8b09f3be4a5f814b4e805923f1bff469267d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119401348"
---
# <a name="disabling-remote-desktop-services-features"></a>停用遠端桌面服務功能

為了加強安全性，您可以選擇停用遠端桌面服務功能，例如使用遠端桌面) 控制項連接至遠端桌面工作階段主機 (RD 工作階段主機 ActiveX 伺服器之用戶端的「剪貼簿重新導向」和「印表機重新導向」。

**停用遠端桌面服務功能**

1.  編輯用戶端電腦的登錄，並新增下列機碼：

    -   **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 終端機伺服器 \\ DisableClipboardRedirection**
    -   **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 終端機伺服器 \\ DisableDriveRedirection**
    -   **HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 終端機伺服器 \\ DisablePrinterRedirection**

2.  將兩個索引鍵的值設定為 **REG \_ DWORD** 1。

 

 




