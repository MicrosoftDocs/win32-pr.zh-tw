---
title: '[系統還原]'
description: 設定系統還原點，並監視程式的主要系統變更，讓系統回復為先前的狀態。 撰寫自動復原程式碼或 wmi 腳本，將系統狀態還原到已註冊的還原點。
ms.assetid: 6861eedc-2bd9-49c7-8682-ea557fa29d28
keywords:
- '[系統還原]'
- 系統還原，起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0bdc4555171ad867f6e6b925144d9ed673ffc3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104092892"
---
# <a name="system-restore"></a><span data-ttu-id="206cf-106">[系統還原]</span><span class="sxs-lookup"><span data-stu-id="206cf-106">System Restore</span></span>

## <a name="purpose"></a><span data-ttu-id="206cf-107">目的</span><span class="sxs-lookup"><span data-stu-id="206cf-107">Purpose</span></span>

<span data-ttu-id="206cf-108">系統還原會自動監視並記錄使用者電腦上的重要系統變更。</span><span class="sxs-lookup"><span data-stu-id="206cf-108">System Restore automatically monitors and records key system changes on a user's computer.</span></span> <span data-ttu-id="206cf-109">其設計目的是為了降低支援成本，並讓使用者復原可能造成系統問題的變更，或在系統以最佳方式執行時還原為一天，以提高客戶滿意度。</span><span class="sxs-lookup"><span data-stu-id="206cf-109">It is designed to reduce support costs and increase customer satisfaction by enabling a user to undo a change that may have caused a problem with the system, or revert to a day when the system was performing optimally.</span></span>

> [!Note]  
> <span data-ttu-id="206cf-110">下列檔是針對開發人員所設計的。</span><span class="sxs-lookup"><span data-stu-id="206cf-110">The following documentation is targeted for developers.</span></span> <span data-ttu-id="206cf-111">如果您是使用者尋找如何使用系統還原的相關資訊，請參閱 [系統還原是什麼？](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)</span><span class="sxs-lookup"><span data-stu-id="206cf-111">If you are an end-user looking for information on how to use System Restore, see [What Is System Restore?](https://windows.microsoft.com/windows/What-is-System-Restore#1TC=windows-7)</span></span>

 

## <a name="developer-audience"></a><span data-ttu-id="206cf-112">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="206cf-112">Developer audience</span></span>

<span data-ttu-id="206cf-113">系統還原 API 是設計來供 C/c + + 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="206cf-113">The System Restore API is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="206cf-114">使用指令碼介面需要熟悉 Windows Management Instrumentation (WMI) 。</span><span class="sxs-lookup"><span data-stu-id="206cf-114">A familiarity with Windows Management Instrumentation (WMI) is required to use the scripting interface.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="206cf-115">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="206cf-115">Run-time requirements</span></span>

<span data-ttu-id="206cf-116">自 Windows XP 起的用戶端作業系統支援系統還原 API。</span><span class="sxs-lookup"><span data-stu-id="206cf-116">The System Restore API is supported on client operating systems starting with Windows XP.</span></span> <span data-ttu-id="206cf-117">如需有關使用特定 API 專案所需之作業系統的詳細資訊，請參閱其檔的需求一節。</span><span class="sxs-lookup"><span data-stu-id="206cf-117">For information about which operating systems are required to use a particular API element, see the Requirements section of its documentation.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="206cf-118">本節內容</span><span class="sxs-lookup"><span data-stu-id="206cf-118">In this section</span></span>



| <span data-ttu-id="206cf-119">主題</span><span class="sxs-lookup"><span data-stu-id="206cf-119">Topic</span></span>                                                | <span data-ttu-id="206cf-120">描述</span><span class="sxs-lookup"><span data-stu-id="206cf-120">Description</span></span>                                                                    |
|------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="206cf-121">概觀</span><span class="sxs-lookup"><span data-stu-id="206cf-121">Overview</span></span>](about-system-restore.md)<br/>      | <span data-ttu-id="206cf-122">概述系統還原的運作方式。</span><span class="sxs-lookup"><span data-stu-id="206cf-122">An overview of how System Restore works.</span></span><br/>                            |
| [<span data-ttu-id="206cf-123">參考</span><span class="sxs-lookup"><span data-stu-id="206cf-123">Reference</span></span>](system-restore-reference.md)<br/> | <span data-ttu-id="206cf-124">系統還原函數、結構和類別的檔。</span><span class="sxs-lookup"><span data-stu-id="206cf-124">Documentation of System Restore functions, structures, and classes.</span></span><br/> |
| [<span data-ttu-id="206cf-125">範例</span><span class="sxs-lookup"><span data-stu-id="206cf-125">Samples</span></span>](using-system-restore.md)<br/>       | <span data-ttu-id="206cf-126">以 C 撰寫的範例程式。</span><span class="sxs-lookup"><span data-stu-id="206cf-126">A sample program written in C.</span></span><br/>                                      |



 

## <a name="related-topics"></a><span data-ttu-id="206cf-127">相關主題</span><span class="sxs-lookup"><span data-stu-id="206cf-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="206cf-128">WMI</span><span class="sxs-lookup"><span data-stu-id="206cf-128">WMI</span></span>](/windows/desktop/WmiSdk/wmi-start-page)
</dt> </dl>

 

