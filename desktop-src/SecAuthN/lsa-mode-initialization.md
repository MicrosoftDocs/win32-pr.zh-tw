---
description: 當電腦系統啟動時，「本地安全機構」 (LSA) 會自動將所有已註冊的安全性支援提供者/驗證套件 (SSP/AP) Dll 載入其進程空間中。 下圖顯示初始化處理常式。
ms.assetid: 2d52cbbf-9e28-4c6f-8b4c-448b73c6dbf8
title: LSA 模式初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff4c55397e5970b8401e1429eba7d92a034e76ce0c999950131167580ded7e5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922122"
---
# <a name="lsa-mode-initialization"></a>LSA 模式初始化

當電腦系統啟動時，「[*本地安全機構*](../secgloss/l-gly.md)」 (LSA) 會自動將所有已註冊的 [*安全性支援提供者*](../secgloss/s-gly.md) / [*驗證套件*](../secgloss/a-gly.md) (SSP/AP) dll 載入其進程空間中。 下圖顯示初始化處理常式。

> [!Note]  
> "Kerberos" 代表 Microsoft [*Kerberos*](../secgloss/k-gly.md) SSP/ap，而「我的 SSP/ap」表示包含兩個自訂安全性封裝的自訂 SSP/ap。

 

![lsa 模式初始化](images/lsamode1.png)

在啟動時，LSA 會在每個 SSP/AP 中呼叫 [**SpLsaModeInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-splsamodeinitializefn) 函式，以取得 DLL 中每個 [*安全性套件*](../secgloss/s-gly.md) 所執行之函式的指標。 函數指標會傳遞至 SECPKG 函式 [**\_ \_ 資料表**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) 結構陣列中的 LSA。

![lsa 呼叫 splsamodeinitialize 來取得函式指標](images/lsamode2.png)

收到 SECPKG 函式 [**\_ \_ 資料表**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_function_table) 結構的集合之後，LSA 會呼叫每個安全性封裝的 [**SpInitialize**](/windows/desktop/api/Ntsecpkg/nc-ntsecpkg-spinitializefn) 函式。 LSA 會使用這個函式呼叫，將 Lsa SECPKG 函式 [**\_ \_ \_ 資料表**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-lsa_secpkg_function_table) 結構（其中包含可供安全性封裝使用的 lsa 支援函式的指標）傳遞給每個安全性封裝。 除了將指標儲存至 LSA 支援函式之外，自訂安全性封裝應該使用其 **SpInitialize** 函式的實執行任何初始化相關的處理。

如需可供 LSA 模式安全性封裝使用的 LSA 支援函式清單，請參閱 [SSP/ap 所呼叫的 Lsa 函數](authentication-functions.md)。

如需註冊 SSP/AP DLL 的詳細資訊，請參閱 [註冊 ssp/ap](registering-ssp-ap-dlls.md)dll。

 

 
