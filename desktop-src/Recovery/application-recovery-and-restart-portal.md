---
title: 應用程式復原和重新啟動
description: 撰寫自訂安裝程式，以自動重新開機已關機的應用程式以完成更新。 在結束程式之前，儲存資料並設定應用程式復原。
ms.assetid: 60b057dd-9724-4bc4-b1b0-eea7e8380ecb
keywords:
- restart
- recover
- recovery
- 可靠性
- 軟體可靠性
- 應用程式復原
- 應用程式重新開機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 862236fad876307b0662a8444775c78673b92983
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840687"
---
# <a name="application-recovery-and-restart"></a><span data-ttu-id="f73fa-111">應用程式復原和重新啟動</span><span class="sxs-lookup"><span data-stu-id="f73fa-111">Application Recovery and Restart</span></span>

## <a name="purpose"></a><span data-ttu-id="f73fa-112">目的</span><span class="sxs-lookup"><span data-stu-id="f73fa-112">Purpose</span></span>

<span data-ttu-id="f73fa-113">應用程式可以使用應用程式復原，並重新啟動 (ARR) ，以在應用程式因未處理的例外狀況或應用程式停止回應之前結束之前儲存資料和狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="f73fa-113">An application can use Application Recovery and Restart (ARR) to save data and state information before the application exits due to an unhandled exception or when the application stops responding.</span></span> <span data-ttu-id="f73fa-114">如果要求，也會重新開機應用程式。</span><span class="sxs-lookup"><span data-stu-id="f73fa-114">The application is also restarted, if requested.</span></span>

<span data-ttu-id="f73fa-115">如果安裝程式更新應用程式的元件，或電腦需要重新開機做為更新的結果，也可以重新開機應用程式。</span><span class="sxs-lookup"><span data-stu-id="f73fa-115">An application can also be restarted if an installer updates a component of the application, or if the computer needs to restart as the result of an update.</span></span> <span data-ttu-id="f73fa-116">請注意，為了支援在安裝程式更新應用程式後自動重新開機應用程式，應用程式和安裝程式都需要適當撰寫。</span><span class="sxs-lookup"><span data-stu-id="f73fa-116">Note that to support automatic application restart after an installer updates an application, both the application and installer need to be authored appropriately.</span></span> <span data-ttu-id="f73fa-117">如需詳細資訊，請參閱 [註冊應用程式重新開機](registering-for-application-restart.md)。</span><span class="sxs-lookup"><span data-stu-id="f73fa-117">For details, see [Registering for Application Restart](registering-for-application-restart.md).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="f73fa-118">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="f73fa-118">Developer audience</span></span>

<span data-ttu-id="f73fa-119">ARR 是針對 C 和 c + + 開發人員所設計。</span><span class="sxs-lookup"><span data-stu-id="f73fa-119">ARR is designed for C and C++ developers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f73fa-120">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="f73fa-120">Run-time requirements</span></span>

<span data-ttu-id="f73fa-121">從 Windows Vista 作業系統開始，可以使用 ARR。</span><span class="sxs-lookup"><span data-stu-id="f73fa-121">ARR is available starting with the Windows Vista operating system.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f73fa-122">本節內容</span><span class="sxs-lookup"><span data-stu-id="f73fa-122">In this section</span></span>



| <span data-ttu-id="f73fa-123">主題</span><span class="sxs-lookup"><span data-stu-id="f73fa-123">Topic</span></span>                                                                                                   | <span data-ttu-id="f73fa-124">描述</span><span class="sxs-lookup"><span data-stu-id="f73fa-124">Description</span></span>                                                           |
|---------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="f73fa-125">使用應用程式修復並重新啟動</span><span class="sxs-lookup"><span data-stu-id="f73fa-125">Using Application Recovery and Restart</span></span>](using-application-recovery-and-restart.md)<br/>         | <span data-ttu-id="f73fa-126">註冊修復和重新開機的程式指南。</span><span class="sxs-lookup"><span data-stu-id="f73fa-126">Procedural guide for registering for recovery and restart.</span></span><br/> |
| [<span data-ttu-id="f73fa-127">應用程式修復和重新開機參考</span><span class="sxs-lookup"><span data-stu-id="f73fa-127">Application Recovery and Restart Reference</span></span>](application-recovery-and-restart-reference.md)<br/> | <span data-ttu-id="f73fa-128">ARR API 的參考資訊。</span><span class="sxs-lookup"><span data-stu-id="f73fa-128">Reference information for the ARR API.</span></span> <br/>                    |



 

 

 





