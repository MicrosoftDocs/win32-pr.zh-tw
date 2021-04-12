---
title: 'TBM_GETPOS 訊息 (Commctrl .h) '
description: 抓取捲軸中滑杆的目前邏輯位置。 邏輯位置是在最小至最大滑杆位置的 [最大值] 範圍內的整數值。
ms.assetid: 6f082ab2-2f9a-4bc0-bfca-56f7b1a2d921
keywords:
- TBM_GETPOS message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETPOS
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 072ff9b8a107fe19afb1fee6107a2f05bad36025
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465368"
---
# <a name="tbm_getpos-message"></a><span data-ttu-id="5caad-105">TBM \_ GETPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="5caad-105">TBM\_GETPOS message</span></span>

<span data-ttu-id="5caad-106">抓取捲軸中滑杆的目前邏輯位置。</span><span class="sxs-lookup"><span data-stu-id="5caad-106">Retrieves the current logical position of the slider in a trackbar.</span></span> <span data-ttu-id="5caad-107">邏輯位置是在最小至最大滑杆位置的 [最大值] 範圍內的整數值。</span><span class="sxs-lookup"><span data-stu-id="5caad-107">The logical positions are the integer values in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="parameters"></a><span data-ttu-id="5caad-108">參數</span><span class="sxs-lookup"><span data-stu-id="5caad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5caad-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="5caad-109">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="5caad-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="5caad-110">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="5caad-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5caad-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="5caad-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="5caad-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5caad-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5caad-113">Return value</span></span>

<span data-ttu-id="5caad-114">傳回32位值，這個值會指定目前的捲軸滑杆的邏輯位置。</span><span class="sxs-lookup"><span data-stu-id="5caad-114">Returns a 32-bit value that specifies the current logical position of the trackbar's slider.</span></span>

## <a name="requirements"></a><span data-ttu-id="5caad-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="5caad-115">Requirements</span></span>



| <span data-ttu-id="5caad-116">需求</span><span class="sxs-lookup"><span data-stu-id="5caad-116">Requirement</span></span> | <span data-ttu-id="5caad-117">值</span><span class="sxs-lookup"><span data-stu-id="5caad-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5caad-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5caad-118">Minimum supported client</span></span><br/> | <span data-ttu-id="5caad-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5caad-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5caad-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5caad-120">Minimum supported server</span></span><br/> | <span data-ttu-id="5caad-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5caad-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5caad-122">標頭</span><span class="sxs-lookup"><span data-stu-id="5caad-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="5caad-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5caad-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5caad-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5caad-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5caad-125">**TBM \_ SETPOS**</span><span class="sxs-lookup"><span data-stu-id="5caad-125">**TBM\_SETPOS**</span></span>](tbm-setpos.md)
</dt> </dl>

 

 





