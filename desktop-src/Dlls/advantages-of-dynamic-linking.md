---
description: 動態連結具有下列優於靜態連結的優點。
ms.assetid: adfd941d-1a36-4dd8-af1f-b105466e0668
title: 動態連結的優點
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1764e25a051522600bd6b485b75f414f8a280e0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979005"
---
# <a name="advantages-of-dynamic-linking"></a><span data-ttu-id="8972e-103">動態連結的優點</span><span class="sxs-lookup"><span data-stu-id="8972e-103">Advantages of Dynamic Linking</span></span>

<span data-ttu-id="8972e-104">動態連結具有下列優於靜態連結的優點：</span><span class="sxs-lookup"><span data-stu-id="8972e-104">Dynamic linking has the following advantages over static linking:</span></span>

-   <span data-ttu-id="8972e-105">在相同基底位址上載入相同 DLL 的多個進程，會在實體記憶體中共用一個 DLL 的單一複本。</span><span class="sxs-lookup"><span data-stu-id="8972e-105">Multiple processes that load the same DLL at the same base address share a single copy of the DLL in physical memory.</span></span> <span data-ttu-id="8972e-106">這樣做可節省系統記憶體並減少交換。</span><span class="sxs-lookup"><span data-stu-id="8972e-106">Doing this saves system memory and reduces swapping.</span></span>
-   <span data-ttu-id="8972e-107">當 DLL 中的函式變更時，使用這些函式的應用程式不需要重新編譯或重新連結，只要函式引數、呼叫慣例和傳回值都不會變更。</span><span class="sxs-lookup"><span data-stu-id="8972e-107">When the functions in a DLL change, the applications that use them do not need to be recompiled or relinked as long as the function arguments, calling conventions, and return values do not change.</span></span> <span data-ttu-id="8972e-108">相反地，靜態連結的物件程式碼需要在函式變更時重新連結應用程式。</span><span class="sxs-lookup"><span data-stu-id="8972e-108">In contrast, statically linked object code requires that the application be relinked when the functions change.</span></span>
-   <span data-ttu-id="8972e-109">DLL 可以提供上市後支援。</span><span class="sxs-lookup"><span data-stu-id="8972e-109">A DLL can provide after-market support.</span></span> <span data-ttu-id="8972e-110">例如，您可以修改顯示驅動程式 DLL，以支援一開始發行應用程式時無法使用的顯示。</span><span class="sxs-lookup"><span data-stu-id="8972e-110">For example, a display driver DLL can be modified to support a display that was not available when the application was initially shipped.</span></span>
-   <span data-ttu-id="8972e-111">只要程式遵循函式所使用的相同呼叫慣例，以不同程式設計語言撰寫的程式就可以呼叫相同的 DLL 函式。</span><span class="sxs-lookup"><span data-stu-id="8972e-111">Programs written in different programming languages can call the same DLL function as long as the programs follow the same calling convention that the function uses.</span></span> <span data-ttu-id="8972e-112">呼叫慣例 (例如 C、Pascal 或標準呼叫) 控制呼叫函式必須將引數推送至堆疊的順序、函式或呼叫的函式是否負責清除堆疊，以及是否在暫存器中傳遞任何引數。</span><span class="sxs-lookup"><span data-stu-id="8972e-112">The calling convention (such as C, Pascal, or standard call) controls the order in which the calling function must push the arguments onto the stack, whether the function or the calling function is responsible for cleaning up the stack, and whether any arguments are passed in registers.</span></span> <span data-ttu-id="8972e-113">如需詳細資訊，請參閱編譯器隨附的檔。</span><span class="sxs-lookup"><span data-stu-id="8972e-113">For more information, see the documentation included with your compiler.</span></span>

<span data-ttu-id="8972e-114">使用 Dll 的潛在缺點是應用程式不是獨立的，這取決於是否存在個別的 DLL 模組。</span><span class="sxs-lookup"><span data-stu-id="8972e-114">A potential disadvantage to using DLLs is that the application is not self-contained; it depends on the existence of a separate DLL module.</span></span> <span data-ttu-id="8972e-115">如果系統需要在處理常式啟動時找不到的 DLL，並將錯誤訊息提供給使用者，則系統會使用載入時間動態連結來終止進程。</span><span class="sxs-lookup"><span data-stu-id="8972e-115">The system terminates processes using load-time dynamic linking if they require a DLL that is not found at process startup and gives an error message to the user.</span></span> <span data-ttu-id="8972e-116">在這種情況下，系統不會使用執行時間動態連結來終止進程，但是程式無法使用遺失 DLL 所匯出的函式。</span><span class="sxs-lookup"><span data-stu-id="8972e-116">The system does not terminate a process using run-time dynamic linking in this situation, but functions exported by the missing DLL are not available to the program.</span></span>

 

 



