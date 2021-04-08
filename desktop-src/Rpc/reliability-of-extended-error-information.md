---
title: 擴充錯誤資訊的可靠性
description: 延伸的錯誤資訊不可靠。
ms.assetid: d4735a7b-ede0-4230-b10a-bf9772aca6a6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c20edfbaa68f2a9ce80893f4f47bba33ec5ce595
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671083"
---
# <a name="reliability-of-extended-error-information"></a><span data-ttu-id="8f843-103">擴充錯誤資訊的可靠性</span><span class="sxs-lookup"><span data-stu-id="8f843-103">Reliability of Extended Error Information</span></span>

<span data-ttu-id="8f843-104">延伸的錯誤資訊不可靠。</span><span class="sxs-lookup"><span data-stu-id="8f843-104">Extended error information is not reliable.</span></span> <span data-ttu-id="8f843-105">擴充的錯誤資訊無法用於建立程式碼邏輯。</span><span class="sxs-lookup"><span data-stu-id="8f843-105">Extended error information cannot be used for building code logic.</span></span> <span data-ttu-id="8f843-106">您可以檢查是否有延伸的錯誤資訊，如果有的話，要傾印、儲存或記錄這些資訊。</span><span class="sxs-lookup"><span data-stu-id="8f843-106">It is appropriate to check for the presence of extended error information, and if there, to dump, save, or log that information.</span></span> <span data-ttu-id="8f843-107">但請勿依賴資訊或其內容。</span><span class="sxs-lookup"><span data-stu-id="8f843-107">But do not rely on the information or its contents.</span></span>

<span data-ttu-id="8f843-108">下列原因說明擴充錯誤資訊不可靠的原因：</span><span class="sxs-lookup"><span data-stu-id="8f843-108">The following reasons explain why extended error information is not reliable:</span></span>

-   <span data-ttu-id="8f843-109">擴充錯誤記錄的順序和內容取決於系統的內部架構，而這些架構可能會變更。</span><span class="sxs-lookup"><span data-stu-id="8f843-109">The sequence and contents of the extended error records depends on the internal architecture of the system, which is subject to change.</span></span> <span data-ttu-id="8f843-110">某些作業可能會在目前的系統上 NPFS，但未來可能會通過 TCP。</span><span class="sxs-lookup"><span data-stu-id="8f843-110">A certain operation may go through NPFS on current systems, but tomorrow could go through TCP.</span></span> <span data-ttu-id="8f843-111">這些不同的元件會產生非常不同的錯誤碼，因此程式碼檢查原本就不可靠，因此不建議使用。</span><span class="sxs-lookup"><span data-stu-id="8f843-111">These different components generate very different error codes, and code checks therefore are inherently unreliable and not recommended.</span></span>
-   <span data-ttu-id="8f843-112">如先前所述，您可以停用擴充錯誤資訊的傳播。</span><span class="sxs-lookup"><span data-stu-id="8f843-112">The propagation of extended error information can be disabled, as explained previously.</span></span> <span data-ttu-id="8f843-113">如果包含偵測程式碼，應用程式可能會在特定環境中停止運作。</span><span class="sxs-lookup"><span data-stu-id="8f843-113">If detection code is included, the application will likely stop working in certain environments.</span></span>
-   <span data-ttu-id="8f843-114">擴充錯誤資訊的傳播會以最大的方式執行。</span><span class="sxs-lookup"><span data-stu-id="8f843-114">The propagation of extended error information is performed in a best effort manner.</span></span> <span data-ttu-id="8f843-115">如果電腦上沒有足夠的記憶體可處理或傳播鏈，則傳播或產生擴充的錯誤資訊可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="8f843-115">Propagation or generation of extended error information can fail if there isn't enough memory on the computer to process or propagate the chain.</span></span> <span data-ttu-id="8f843-116">在這種情況下，將會捨棄鏈。</span><span class="sxs-lookup"><span data-stu-id="8f843-116">Under such circumstances, the chain will be dropped.</span></span> <span data-ttu-id="8f843-117">某些通訊協定的錯誤長度有限，因為它們通常不包含許多資訊。</span><span class="sxs-lookup"><span data-stu-id="8f843-117">Some protocols have limited lengths for fault packets since they usually don't include much information.</span></span> <span data-ttu-id="8f843-118">如果鏈的長度超過允許的封包長度，RPC 執行時間就會開始從鏈中卸載資訊，以嘗試將鏈放入封包中。</span><span class="sxs-lookup"><span data-stu-id="8f843-118">If the length of the chain exceeds the allowed length of the packet, the RPC run time begins dropping information from the chain in an attempt to fit the chain into the packet.</span></span> <span data-ttu-id="8f843-119">執行時間會先卸載倒數第二記錄開始的記錄，直到只剩下第一個和最後一個記錄為止。</span><span class="sxs-lookup"><span data-stu-id="8f843-119">The run time first drops records, starting from the penultimate record, going backwards, until only the first and last records remain.</span></span> <span data-ttu-id="8f843-120">如果鏈仍無法放入封包中，則執行時間會卸載字串參數和電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="8f843-120">If the chain still doesn't fit into a packet, the run time drops string parameters and computer names.</span></span> <span data-ttu-id="8f843-121">如果已卸載字串參數，參數的類型會設為 none。</span><span class="sxs-lookup"><span data-stu-id="8f843-121">If a string parameter is dropped, the type of the parameter is set to none.</span></span> <span data-ttu-id="8f843-122">如果記錄已卸載，則會在下一筆記錄中設定 EEInfoNextRecordsMissing 旗標，並在上一筆記錄中設定 EEInfoPreviousRecordsMissing。</span><span class="sxs-lookup"><span data-stu-id="8f843-122">If a record is dropped, the EEInfoNextRecordsMissing flag is set in the next record, and EEInfoPreviousRecordsMissing is set in the previous record.</span></span>

 

 




