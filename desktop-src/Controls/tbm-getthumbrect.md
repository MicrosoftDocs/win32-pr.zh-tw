---
title: 'TBM_GETTHUMBRECT 訊息 (Commctrl .h) '
description: 抓取捲軸中滑杆的周框大小和位置。
ms.assetid: f53fd7af-36f8-4490-aa95-f1fa20f34efb
keywords:
- TBM_GETTHUMBRECT message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETTHUMBRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dce1bba8af9a65f297aa0515c1103c50daa1626d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025119"
---
# <a name="tbm_getthumbrect-message"></a><span data-ttu-id="ede6d-104">TBM \_ GETTHUMBRECT 訊息</span><span class="sxs-lookup"><span data-stu-id="ede6d-104">TBM\_GETTHUMBRECT message</span></span>

<span data-ttu-id="ede6d-105">抓取捲軸中滑杆的周框大小和位置。</span><span class="sxs-lookup"><span data-stu-id="ede6d-105">Retrieves the size and position of the bounding rectangle for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="ede6d-106">參數</span><span class="sxs-lookup"><span data-stu-id="ede6d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ede6d-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ede6d-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="ede6d-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="ede6d-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="ede6d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ede6d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ede6d-110">[**矩形**](/previous-versions//dd162897(v=vs.85))結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ede6d-110">Pointer to a [**RECT**](/previous-versions//dd162897(v=vs.85)) structure.</span></span> <span data-ttu-id="ede6d-111">此訊息會在 [協調器] 視窗的用戶端座標中，以 [程式提示] 滑杆的周框矩形來填滿此結構。</span><span class="sxs-lookup"><span data-stu-id="ede6d-111">The message fills this structure with the bounding rectangle of the trackbar's slider in client coordinates of the trackbar's window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ede6d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ede6d-112">Return value</span></span>

<span data-ttu-id="ede6d-113">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="ede6d-113">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ede6d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ede6d-114">Requirements</span></span>



| <span data-ttu-id="ede6d-115">需求</span><span class="sxs-lookup"><span data-stu-id="ede6d-115">Requirement</span></span> | <span data-ttu-id="ede6d-116">值</span><span class="sxs-lookup"><span data-stu-id="ede6d-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ede6d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ede6d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ede6d-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ede6d-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ede6d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ede6d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ede6d-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ede6d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ede6d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ede6d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ede6d-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ede6d-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

