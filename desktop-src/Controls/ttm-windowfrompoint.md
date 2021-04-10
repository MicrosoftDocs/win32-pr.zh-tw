---
title: 'TTM_WINDOWFROMPOINT 訊息 (Commctrl .h) '
description: 允許子類別程式使工具提示顯示滑鼠游標下方以外的視窗文字。
ms.assetid: f3bf6917-1745-4e4f-a9c1-8fe86b2b3906
keywords:
- TTM_WINDOWFROMPOINT message Windows 控制項
topic_type:
- apiref
api_name:
- TTM_WINDOWFROMPOINT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68679f6b6c2477a8279c22f11d0d300e44c8370d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686097"
---
# <a name="ttm_windowfrompoint-message"></a><span data-ttu-id="504dc-104">TTM \_ WINDOWFROMPOINT 訊息</span><span class="sxs-lookup"><span data-stu-id="504dc-104">TTM\_WINDOWFROMPOINT message</span></span>

<span data-ttu-id="504dc-105">允許子類別程式使工具提示顯示滑鼠游標下方以外的視窗文字。</span><span class="sxs-lookup"><span data-stu-id="504dc-105">Allows a subclass procedure to cause a tooltip to display text for a window other than the one beneath the mouse cursor.</span></span>

## <a name="parameters"></a><span data-ttu-id="504dc-106">參數</span><span class="sxs-lookup"><span data-stu-id="504dc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="504dc-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="504dc-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="504dc-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="504dc-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="504dc-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="504dc-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="504dc-110">[**點**](/previous-versions//dd162805(v=vs.85))結構的指標，該結構定義要檢查的點。</span><span class="sxs-lookup"><span data-stu-id="504dc-110">Pointer to a [**POINT**](/previous-versions//dd162805(v=vs.85)) structure that defines the point to be checked.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="504dc-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="504dc-111">Return value</span></span>

<span data-ttu-id="504dc-112">傳回值是包含點之視窗的控制碼，如果指定的點沒有視窗存在，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="504dc-112">The return value is the handle to the window that contains the point, or **NULL** if no window exists at the specified point.</span></span>

## <a name="remarks"></a><span data-ttu-id="504dc-113">備註</span><span class="sxs-lookup"><span data-stu-id="504dc-113">Remarks</span></span>

<span data-ttu-id="504dc-114">此訊息的目的是要由子類別化工具提示的應用程式來處理。</span><span class="sxs-lookup"><span data-stu-id="504dc-114">This message is intended to be processed by an application that subclasses a tooltip.</span></span> <span data-ttu-id="504dc-115">它並不適合應用程式傳送。</span><span class="sxs-lookup"><span data-stu-id="504dc-115">It is not intended to be sent by an application.</span></span> <span data-ttu-id="504dc-116">工具提示會在顯示視窗的文字之前，將此訊息傳送給自己。</span><span class="sxs-lookup"><span data-stu-id="504dc-116">A tooltip sends this message to itself before displaying the text for a window.</span></span> <span data-ttu-id="504dc-117">藉由變更 *lParam* 所指定之點的座標，子類別程式可能會導致工具提示顯示非滑鼠游標下的視窗文字。</span><span class="sxs-lookup"><span data-stu-id="504dc-117">By changing the coordinates of the point specified by *lParam*, the subclass procedure can cause the tooltip to display text for a window other than the one beneath the mouse cursor.</span></span>

## <a name="requirements"></a><span data-ttu-id="504dc-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="504dc-118">Requirements</span></span>



| <span data-ttu-id="504dc-119">需求</span><span class="sxs-lookup"><span data-stu-id="504dc-119">Requirement</span></span> | <span data-ttu-id="504dc-120">值</span><span class="sxs-lookup"><span data-stu-id="504dc-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="504dc-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="504dc-121">Minimum supported client</span></span><br/> | <span data-ttu-id="504dc-122">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="504dc-122">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="504dc-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="504dc-123">Minimum supported server</span></span><br/> | <span data-ttu-id="504dc-124">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="504dc-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="504dc-125">標頭</span><span class="sxs-lookup"><span data-stu-id="504dc-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="504dc-126"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="504dc-126"><dt>Commctrl.h</dt></span></span> </dl> |



 

