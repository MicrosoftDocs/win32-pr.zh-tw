---
title: 'LM_GETIDEALSIZE 訊息 (Commctrl .h) '
description: LM_GETIDEALSIZE 訊息-針對控制項目前寬度的連結，取得其慣用高度。
ms.assetid: 63aad7eb-26ee-41d2-90d4-65fdcf0f182a
keywords:
- LM_GETIDEALSIZE message Windows 控制項
topic_type:
- apiref
api_name:
- LM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 761fb5f6e5f7a2e2e9b1b9cc862b9a8f2c0fcd1f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112386"
---
# <a name="lm_getidealsize-message"></a><span data-ttu-id="a28cb-104">LM \_ GETIDEALSIZE 訊息</span><span class="sxs-lookup"><span data-stu-id="a28cb-104">LM\_GETIDEALSIZE message</span></span>

<span data-ttu-id="a28cb-105">抓取控制項目前寬度之連結的慣用高度。</span><span class="sxs-lookup"><span data-stu-id="a28cb-105">Retrieves the preferred height of a link for the control's current width.</span></span>

## <a name="parameters"></a><span data-ttu-id="a28cb-106">參數</span><span class="sxs-lookup"><span data-stu-id="a28cb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a28cb-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a28cb-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="a28cb-108">連結的最大寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="a28cb-108">Maximum width of the link, in pixels.</span></span></dd> <dt>

<span data-ttu-id="a28cb-109">*lParam* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a28cb-109">*lParam* \[out\]</span></span>
</dt> <dd><span data-ttu-id="a28cb-110">當這個訊息傳回時，會包含 <a href="/previous-versions//dd145106(v=vs.85)">**大小**</a> 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="a28cb-110">When this message returns, contains a pointer to a <a href="/previous-versions//dd145106(v=vs.85)">**SIZE**</a> structure.</span></span> <span data-ttu-id="a28cb-111">此結構的 **cy** 成員表示指定寬度之控制項的理想高度。</span><span class="sxs-lookup"><span data-stu-id="a28cb-111">The **cy** member of this structure indicates the ideal height of the control for the given width.</span></span> <span data-ttu-id="a28cb-112">它會將 **cx** 成員調整為實際需要的空間量。</span><span class="sxs-lookup"><span data-stu-id="a28cb-112">It adjusts the **cx** member to the amount of space actually needed.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a28cb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a28cb-113">Return value</span></span>

<span data-ttu-id="a28cb-114">整數，表示連結文字的慣用高度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="a28cb-114">Integer that represents the preferred height of the link text, in pixels.</span></span>

## <a name="remarks"></a><span data-ttu-id="a28cb-115">備註</span><span class="sxs-lookup"><span data-stu-id="a28cb-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="a28cb-116">若要使用此 API，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="a28cb-116">To use this API, you must provide a manifest that specifies Comclt32.dll version 6.0.</span></span> <span data-ttu-id="a28cb-117">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="a28cb-117">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a28cb-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="a28cb-118">Requirements</span></span>



| <span data-ttu-id="a28cb-119">需求</span><span class="sxs-lookup"><span data-stu-id="a28cb-119">Requirement</span></span> | <span data-ttu-id="a28cb-120">值</span><span class="sxs-lookup"><span data-stu-id="a28cb-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a28cb-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a28cb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a28cb-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a28cb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a28cb-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a28cb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a28cb-124">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a28cb-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a28cb-125">標頭</span><span class="sxs-lookup"><span data-stu-id="a28cb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a28cb-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a28cb-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

