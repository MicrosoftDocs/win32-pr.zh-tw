---
title: 設定延伸模組 Dll
description: 在啟動時，NPS 會檢查登錄以取得要呼叫的協力廠商 Dll 清單。
ms.assetid: fbbd9031-3ebe-47b8-8d8b-e359fa7d4b67
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 737d53bd25a28321c333e890a019af881ae54fa1c5ae92299b1776689f9abb74
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119962508"
---
# <a name="setting-up-the-extension-dlls"></a>設定延伸模組 Dll

> [!Note]  
> 網際網路驗證服務 (IAS) 已重新命名網路原則伺服器 (NPS) 從 Windows Server 2008 開始。 本主題的內容適用于 IAS 和 NPS。 在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。

 

在啟動時，NPS 會檢查登錄以取得要呼叫的協力廠商 Dll 清單。

若要在 NPS 伺服器上設定驗證或授權 DLL，請在下列登錄機碼底下的值列出 Dll 的路徑：

**HKLM \\ System \\ CurrentControlSet \\ Services \\ AuthSrv \\ 參數\\**

如果 **AuthSrv** 和 **Parameters** 索引鍵不存在，請加以建立。

要在其中列出驗證延伸模組 Dll 的值為：

**ExtensionDLLs**

要在其中列出授權延伸模組 Dll 的值為：

**AuthorizationDLLs**

**ExtensionDLLs** 和 **AuthorizationDLLs** 值都必須是 **REG \_ 多重 \_ SZ** 類型。 此類型可讓您列出多個 Dll。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[叫用擴充 Dll](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> <dt>

[使用者識別屬性](/windows/desktop/Nps/ias-user-identification-attributes)
</dt> </dl>

 

 