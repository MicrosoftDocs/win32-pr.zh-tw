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
# <a name="dynamic-link-libraries-dynamic-link-libraries"></a><span data-ttu-id="1f3c3-103">Dynamic-Link 程式庫 (動態連結程式庫) </span><span class="sxs-lookup"><span data-stu-id="1f3c3-103">Dynamic-Link Libraries (Dynamic-Link Libraries)</span></span>

<span data-ttu-id="1f3c3-104">*動態連結程式庫* (DLL) 是一個模組，其中包含可供其他模組 (應用程式或 DLL) 使用的函式和資料。</span><span class="sxs-lookup"><span data-stu-id="1f3c3-104">A *dynamic-link library* (DLL) is a module that contains functions and data that can be used by another module (application or DLL).</span></span>

<span data-ttu-id="1f3c3-105">DLL 可以定義兩種類型的函數：已匯出和內部。</span><span class="sxs-lookup"><span data-stu-id="1f3c3-105">A DLL can define two kinds of functions: exported and internal.</span></span> <span data-ttu-id="1f3c3-106">匯出的函式可供其他模組呼叫，以及從定義的 DLL 內呼叫。</span><span class="sxs-lookup"><span data-stu-id="1f3c3-106">The exported functions are intended to be called by other modules, as well as from within the DLL where they are defined.</span></span> <span data-ttu-id="1f3c3-107">內建函式通常只能從定義它們的 DLL 內呼叫。</span><span class="sxs-lookup"><span data-stu-id="1f3c3-107">Internal functions are typically intended to be called only from within the DLL where they are defined.</span></span> <span data-ttu-id="1f3c3-108">雖然 DLL 可以匯出資料，但其資料通常只會由其功能使用。</span><span class="sxs-lookup"><span data-stu-id="1f3c3-108">Although a DLL can export data, its data is generally used only by its functions.</span></span> <span data-ttu-id="1f3c3-109">不過，沒有任何專案可以防止另一個模組讀取或寫入該位址。</span><span class="sxs-lookup"><span data-stu-id="1f3c3-109">However, there is nothing to prevent another module from reading or writing that address.</span></span>

<span data-ttu-id="1f3c3-110">Dll 提供一種方法來模組化應用程式，讓您可以更輕鬆地更新和重複使用其功能。</span><span class="sxs-lookup"><span data-stu-id="1f3c3-110">DLLs provide a way to modularize applications so that their functionality can be updated and reused more easily.</span></span> <span data-ttu-id="1f3c3-111">當數個應用程式同時使用相同的功能時，Dll 也有助於減少記憶體額外負荷，因為雖然每個應用程式都會收到自己的 DLL 資料複本，但應用程式會共用 DLL 程式碼。</span><span class="sxs-lookup"><span data-stu-id="1f3c3-111">DLLs also help reduce memory overhead when several applications use the same functionality at the same time, because although each application receives its own copy of the DLL data, the applications share the DLL code.</span></span>

<span data-ttu-id="1f3c3-112">Windows 應用程式開發介面 (API) 會實作為一組 Dll，因此任何使用 Windows API 的進程都會使用動態連結。</span><span class="sxs-lookup"><span data-stu-id="1f3c3-112">The Windows application programming interface (API) is implemented as a set of DLLs, so any process that uses the Windows API uses dynamic linking.</span></span>

-   [<span data-ttu-id="1f3c3-113">關於 Dynamic-Link 程式庫</span><span class="sxs-lookup"><span data-stu-id="1f3c3-113">About Dynamic-Link Libraries</span></span>](about-dynamic-link-libraries.md)
-   [<span data-ttu-id="1f3c3-114">使用 Dynamic-Link 程式庫</span><span class="sxs-lookup"><span data-stu-id="1f3c3-114">Using Dynamic-Link Libraries</span></span>](using-dynamic-link-libraries.md)
-   [<span data-ttu-id="1f3c3-115">動態連結程式庫參考</span><span class="sxs-lookup"><span data-stu-id="1f3c3-115">Dynamic-Link Library Reference</span></span>](dynamic-link-library-reference.md)

> [!Note]  
> <span data-ttu-id="1f3c3-116">如果您是在電腦上使用 DLL 時遇到困難的使用者，您應該將發佈 DLL 之軟體廠商的客戶支援聯絡。</span><span class="sxs-lookup"><span data-stu-id="1f3c3-116">If you are a user experiencing difficulty with a DLL on your computer, you should contact customer support for the software vendor that publishes the DLL.</span></span> <span data-ttu-id="1f3c3-117">如果您覺得您需要支援 Microsoft 產品 (包括 Windows) ，請前往我們的技術支援網站，網址為 [support.microsoft.com](https://support.microsoft.com)。</span><span class="sxs-lookup"><span data-stu-id="1f3c3-117">If you feel you are in need of support for a Microsoft product (including Windows), please go to our technical support site at [support.microsoft.com](https://support.microsoft.com).</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="1f3c3-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="1f3c3-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f3c3-119">Dll (Visual C++) </span><span class="sxs-lookup"><span data-stu-id="1f3c3-119">DLLs (Visual C++)</span></span>](/cpp/build/dlls-in-visual-cpp?view=vs-2019)
</dt> </dl>

 

 
