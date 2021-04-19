---
description: 服務提供者設計人員應該嘗試保持同步作業的執行時間短。
ms.assetid: eb264ab7-15bb-4cd5-8af8-f979f02a7a39
title: 同步要求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3684b1fa8ea2bca1b7fb777663f2c4e50ffd36a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981683"
---
# <a name="synchronous-requests"></a><span data-ttu-id="9dcf0-103">同步要求</span><span class="sxs-lookup"><span data-stu-id="9dcf0-103">Synchronous Requests</span></span>

<span data-ttu-id="9dcf0-104">服務提供者設計人員應該嘗試保持同步作業的執行時間短。</span><span class="sxs-lookup"><span data-stu-id="9dcf0-104">Service provider designers should try to keep the execution time of synchronous operations short.</span></span> <span data-ttu-id="9dcf0-105">例如，在初始化期間會呼叫「開啟」作業，以準備服務提供者和 TAPI，以在裝置上進行後續作業。</span><span class="sxs-lookup"><span data-stu-id="9dcf0-105">For example, there is an "Open" operation called at initialization time that prepares the service provider and TAPI for subsequent operations on a device.</span></span> <span data-ttu-id="9dcf0-106">在用戶端電腦與專用伺服器之間分割其執行的服務提供者，可能有合理的信賴度，可與其遠端伺服器通訊。</span><span class="sxs-lookup"><span data-stu-id="9dcf0-106">A service provider whose implementation is split between the client computer and a dedicated server may have reasonable confidence that it can communicate with its remote server.</span></span> <span data-ttu-id="9dcf0-107">它的實作為「開啟」可能只會配置並初始化資料結構，以代表裝置並傳回，以延遲端對端通訊，直到要求一些實際作業為止。</span><span class="sxs-lookup"><span data-stu-id="9dcf0-107">Its implementation of "Open" might just allocate and initialize data structures to represent the device and return, postponing end-to-end communication until some real operation is requested.</span></span>

<span data-ttu-id="9dcf0-108">任何此類同步作業的「開放式」執行，稍後都會遇到資源限制或遠端通訊失敗。</span><span class="sxs-lookup"><span data-stu-id="9dcf0-108">Any such "optimistic" implementation of a synchronous operation can later encounter resource limitations or remote communication failures.</span></span> <span data-ttu-id="9dcf0-109">一般來說，即使是「保守」方法，也無法完全避免這些問題;服務提供者設計師必須在可靠性與效能之間選擇最佳的取捨。</span><span class="sxs-lookup"><span data-stu-id="9dcf0-109">In general, even a "conservative" approach cannot entirely prevent these problems; service-provider designers must choose the best tradeoff between reliability and performance.</span></span> <span data-ttu-id="9dcf0-110">如果可能的話，應該盡可能適當地處理這種情況。</span><span class="sxs-lookup"><span data-stu-id="9dcf0-110">A failure of this kind should be handled gracefully wherever possible.</span></span> <span data-ttu-id="9dcf0-111">從 TSPI 裝置的觀點來看，它們應該仍適用于「簿記」目的，即使它們傳回任何所要求作業的失敗狀態也一樣。</span><span class="sxs-lookup"><span data-stu-id="9dcf0-111">From the point of view of TSPI devices, they should remain valid for "bookkeeping" purposes even if they return failure status for any operation requested.</span></span>

<span data-ttu-id="9dcf0-112">若要為同步要求執行開放式方法，不應花費正確的作業語義。</span><span class="sxs-lookup"><span data-stu-id="9dcf0-112">Implementing an optimistic approach for synchronous requests should not be done at the expense of correct semantics for the operation.</span></span> <span data-ttu-id="9dcf0-113">回到「開啟」範例，如果開啟裝置必須競爭並保留很少的 nonsharable 資源（例如通訊埠），即使是很耗時的資源，也應該這麼做。</span><span class="sxs-lookup"><span data-stu-id="9dcf0-113">Returning to the "Open" example, if opening a device needs to compete for and reserve a scarce, nonsharable resource such as communication ports, it should probably do so even if it is time-consuming.</span></span>

<span data-ttu-id="9dcf0-114">**TAPI 2.x：** 以同步方式完成的作業會在應用程式所進行的函式呼叫中執行所有處理。</span><span class="sxs-lookup"><span data-stu-id="9dcf0-114">**TAPI 2.x:** An operation that completes synchronously performs all of its processing in the function call made by the application.</span></span> <span data-ttu-id="9dcf0-115">函數會根據其成功或失敗傳回不同的值：</span><span class="sxs-lookup"><span data-stu-id="9dcf0-115">The function returns different values depending on its success or failure:</span></span>

-   <span data-ttu-id="9dcf0-116">**同步成功。**</span><span class="sxs-lookup"><span data-stu-id="9dcf0-116">**Synchronous Success.**</span></span> <span data-ttu-id="9dcf0-117">如果已成功執行對應至函式的要求或服務，則函式會傳回零，表示成功。</span><span class="sxs-lookup"><span data-stu-id="9dcf0-117">If the request or service corresponding to the function has been carried out successfully, the function returns zero, indicating success.</span></span> <span data-ttu-id="9dcf0-118">當做函式呼叫的結果來撰寫的任何值都是可靠的，可以立即使用。</span><span class="sxs-lookup"><span data-stu-id="9dcf0-118">Any values written as a result of the function call are reliable and can be used immediately.</span></span>
-   <span data-ttu-id="9dcf0-119">**同步失敗。**</span><span class="sxs-lookup"><span data-stu-id="9dcf0-119">**Synchronous Failure.**</span></span> <span data-ttu-id="9dcf0-120">如果函式偵測到錯誤，但未執行要求，則會傳回負的錯誤號碼來識別錯誤。</span><span class="sxs-lookup"><span data-stu-id="9dcf0-120">If the function detects an error and the request is not carried out, a negative error number is returned to identify the error.</span></span>

 

 



