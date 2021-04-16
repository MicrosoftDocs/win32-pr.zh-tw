---
title: 類別和伺服器
description: 類別和伺服器
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d319fd985b812692e6d0bfc421c4bb9da2a2605c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382965"
---
# <a name="classes-and-servers"></a>類別和伺服器

COM 使用 **HKEY \_ 類別 \_ ROOT** 進行全電腦設定，但也允許個別使用者設定 clsid，以提供更高的安全性和彈性。 COM 先諮詢 **HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ 類別** ，然後才在 **HKEY \_ 類別 \_ 根目錄** 下進行搜尋。 COM 會將電腦範圍資訊與 **HKEY \_ 類別 \_ 根目錄 \\ CLSID** 下的 clsid 保持相關，並將每個使用者的類別資訊保留在 **HKEY 的 \_ 目前 \_ 使用者 \\ 軟體 \\ 類別 \\ clsid**。

COM 伺服器支援自我註冊。 針對同進程伺服器，這表示 DLL 必須匯出下列函數：

-   [**DllRegisterServer**](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [**DllUnregisterServer**](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

您必須使用模組定義檔、連結器參數或編譯器指示詞，明確地匯出這些函數。 類別存放區會在下載檔案至用戶端電腦之後，使用這些函數來設定本機登錄。 除了類別存放區之外，其他環境也會使用這些函數將伺服器安裝在主機電腦上。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[註冊 COM 應用程式](registering-com-applications.md)
</dt> </dl>

 

 