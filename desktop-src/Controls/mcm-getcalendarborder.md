---
title: 'MCM_GETCALENDARBORDER 訊息 (Commctrl .h) '
description: 取得框線的大小（以圖元為單位）。 您可以使用 MonthCal GetCurrentView 宏明確地傳送此訊息 \_ 。
ms.assetid: 68366ee1-7511-46a5-aab0-a42fb80c265f
keywords:
- MCM_GETCALENDARBORDER message Windows 控制項
topic_type:
- apiref
api_name:
- MCM_GETCALENDARBORDER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 581eeb5c060f725d3f884f4c19d7d3da3023c63a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508919"
---
# <a name="mcm_getcalendarborder-message"></a><span data-ttu-id="77361-105">MCM \_ GETCALENDARBORDER 訊息</span><span class="sxs-lookup"><span data-stu-id="77361-105">MCM\_GETCALENDARBORDER message</span></span>

<span data-ttu-id="77361-106">取得框線的大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="77361-106">Gets the size of the border, in pixels.</span></span> <span data-ttu-id="77361-107">您可以使用 [**MonthCal \_ GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) 宏明確地傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="77361-107">You can send this message explicitly or by using the [**MonthCal\_GetCurrentView**](/windows/desktop/api/Commctrl/nf-commctrl-monthcal_getcurrentview) macro.</span></span>

## <a name="parameters"></a><span data-ttu-id="77361-108">參數</span><span class="sxs-lookup"><span data-stu-id="77361-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77361-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="77361-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77361-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="77361-110">Must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="77361-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="77361-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="77361-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="77361-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77361-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="77361-113">Return value</span></span>

<span data-ttu-id="77361-114">框線大小（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="77361-114">Border size, in pixels.</span></span>

## <a name="requirements"></a><span data-ttu-id="77361-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="77361-115">Requirements</span></span>



| <span data-ttu-id="77361-116">需求</span><span class="sxs-lookup"><span data-stu-id="77361-116">Requirement</span></span> | <span data-ttu-id="77361-117">值</span><span class="sxs-lookup"><span data-stu-id="77361-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77361-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77361-118">Minimum supported client</span></span><br/> | <span data-ttu-id="77361-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77361-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="77361-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77361-120">Minimum supported server</span></span><br/> | <span data-ttu-id="77361-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="77361-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="77361-122">標頭</span><span class="sxs-lookup"><span data-stu-id="77361-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="77361-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="77361-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





