---
description: 動態連結程式庫 (DLL) 是一個模組，其中包含可供其他模組 (應用程式或 DLL) 使用的函式和資料。
ms.assetid: 09e35b46-86a1-44ed-ab6d-207857b2605c
title: 'Dynamic-Link 程式庫 (動態連結程式庫) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8068cd0b8f1d5431c5638a10350d9a1ae7060aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691568"
---
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a>Dynamic-Link 程式庫 (動態連結程式庫) 

*動態連結程式庫* (DLL) 是一個模組，其中包含可供其他模組 (應用程式或 DLL) 使用的函式和資料。

DLL 可以定義兩種類型的函數：已匯出和內部。 匯出的函式可供其他模組呼叫，以及從定義的 DLL 內呼叫。 內建函式通常只能從定義它們的 DLL 內呼叫。 雖然 DLL 可以匯出資料，但其資料通常只會由其功能使用。 不過，沒有任何專案可以防止另一個模組讀取或寫入該位址。

Dll 提供一種方法來模組化應用程式，讓您可以更輕鬆地更新和重複使用其功能。 當數個應用程式同時使用相同的功能時，Dll 也有助於減少記憶體額外負荷，因為雖然每個應用程式都會收到自己的 DLL 資料複本，但應用程式會共用 DLL 程式碼。

Windows 應用程式開發介面 (API) 會實作為一組 Dll，因此任何使用 Windows API 的進程都會使用動態連結。

-   [關於 Dynamic-Link 程式庫](about-dynamic-link-libraries.md)
-   [使用 Dynamic-Link 程式庫](using-dynamic-link-libraries.md)
-   [動態連結程式庫參考](dynamic-link-library-reference.md)

> [!Note]  
> 如果您是在電腦上使用 DLL 時遇到困難的使用者，您應該將發佈 DLL 之軟體廠商的客戶支援聯絡。 如果您覺得您需要支援 Microsoft 產品 (包括 Windows) ，請前往我們的技術支援網站，網址為 [support.microsoft.com](https://support.microsoft.com)。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Dll (Visual C++) ](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
