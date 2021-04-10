---
title: IReconcileInitiator 介面
description: 公開方法，這些方法會提供公事包調整器，以通知起始端的進度、設定終止物件，以及要求指定的檔版本。 啟動器負責執行這個介面。
ms.assetid: 1a32d67f-1ddc-49dc-af88-b8c41a50ac54
keywords:
- IReconcileInitiator 介面舊版 Windows 環境功能
- IReconcileInitiator 介面舊版 Windows 環境功能，說明
topic_type:
- apiref
api_name:
- IReconcileInitiator
api_location:
- Shell32.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759ad26fd87db7076811b9b31d6ef39df1479e3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685932"
---
# <a name="ireconcileinitiator-interface"></a><span data-ttu-id="36cc0-106">IReconcileInitiator 介面</span><span class="sxs-lookup"><span data-stu-id="36cc0-106">IReconcileInitiator interface</span></span>

<span data-ttu-id="36cc0-107">公開方法，這些方法會提供公事包調整器，以通知起始端的進度、設定終止物件，以及要求指定的檔版本。</span><span class="sxs-lookup"><span data-stu-id="36cc0-107">Exposes methods that provide the briefcase reconciler with the means to notify the initiator of its progress, to set a termination object, and to request a given version of a document.</span></span> <span data-ttu-id="36cc0-108">啟動器負責執行這個介面。</span><span class="sxs-lookup"><span data-stu-id="36cc0-108">The initiator is responsible for implementing this interface.</span></span>

## <a name="members"></a><span data-ttu-id="36cc0-109">成員</span><span class="sxs-lookup"><span data-stu-id="36cc0-109">Members</span></span>

<span data-ttu-id="36cc0-110">**IReconcileInitiator** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="36cc0-110">The **IReconcileInitiator** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="36cc0-111">**IReconcileInitiator** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="36cc0-111">**IReconcileInitiator** also has these types of members:</span></span>

-   [<span data-ttu-id="36cc0-112">方法</span><span class="sxs-lookup"><span data-stu-id="36cc0-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="36cc0-113">方法</span><span class="sxs-lookup"><span data-stu-id="36cc0-113">Methods</span></span>

<span data-ttu-id="36cc0-114">**IReconcileInitiator** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="36cc0-114">The **IReconcileInitiator** interface has these methods.</span></span>



| <span data-ttu-id="36cc0-115">方法</span><span class="sxs-lookup"><span data-stu-id="36cc0-115">Method</span></span>                                                                 | <span data-ttu-id="36cc0-116">描述</span><span class="sxs-lookup"><span data-stu-id="36cc0-116">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|:-----------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36cc0-117">**SetAbortCallback**</span><span class="sxs-lookup"><span data-stu-id="36cc0-117">**SetAbortCallback**</span></span>](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setabortcallback)       | <span data-ttu-id="36cc0-118">設定可讓啟動器以非同步方式終止對帳的物件。</span><span class="sxs-lookup"><span data-stu-id="36cc0-118">Sets the object through which the initiator can asynchronously terminate a reconciliation.</span></span> <span data-ttu-id="36cc0-119">公事包調整器通常會針對冗長或牽涉到使用者互動的對帳設定此物件。</span><span class="sxs-lookup"><span data-stu-id="36cc0-119">A briefcase reconciler typically sets this object for reconciliations that are lengthy or involve user interaction.</span></span> <br/>                                                                                              |
| [<span data-ttu-id="36cc0-120">**SetProgressFeedback**</span><span class="sxs-lookup"><span data-stu-id="36cc0-120">**SetProgressFeedback**</span></span>](/windows/win32/api/reconcil/nf-reconcil-ireconcileinitiator-setprogressfeedback) | <span data-ttu-id="36cc0-121">指出公事包調整器完成對帳所進行的進度量。</span><span class="sxs-lookup"><span data-stu-id="36cc0-121">Indicates the amount of progress the briefcase reconciler has made toward completing the reconciliation.</span></span> <span data-ttu-id="36cc0-122">此數量為分數，而且會計算為 *ulProgress* 和 *ulProgressMax* 參數的商。</span><span class="sxs-lookup"><span data-stu-id="36cc0-122">The amount is a fraction and is computed as the quotient of the *ulProgress* and *ulProgressMax* parameters.</span></span> <span data-ttu-id="36cc0-123">Reconcilers 應該在其對帳程式期間定期呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="36cc0-123">Reconcilers should call this method periodically during their reconciliation process.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="36cc0-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="36cc0-124">Requirements</span></span>



| <span data-ttu-id="36cc0-125">需求</span><span class="sxs-lookup"><span data-stu-id="36cc0-125">Requirement</span></span> | <span data-ttu-id="36cc0-126">值</span><span class="sxs-lookup"><span data-stu-id="36cc0-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36cc0-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="36cc0-127">Minimum supported client</span></span><br/> | <span data-ttu-id="36cc0-128">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36cc0-128">Windows XP \[desktop apps only\]</span></span><br/>                                                                   |
| <span data-ttu-id="36cc0-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="36cc0-129">Minimum supported server</span></span><br/> | <span data-ttu-id="36cc0-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="36cc0-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="36cc0-131">DLL</span><span class="sxs-lookup"><span data-stu-id="36cc0-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="36cc0-132"><dt>Shell32.dll (4.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="36cc0-132"><dt>Shell32.dll (version 4.0 or later)</dt></span></span> </dl> |



 

