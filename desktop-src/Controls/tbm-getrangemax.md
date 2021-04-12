---
title: 'TBM_GETRANGEMAX 訊息 (Commctrl .h) '
description: 抓取捲軸中滑杆的最大位置。
ms.assetid: c0ae5f96-f4ce-46cd-84d0-9e7c473441a0
keywords:
- TBM_GETRANGEMAX message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETRANGEMAX
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bdd9687b617759ab8b8fdea59ed06d7fcd78b6d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025124"
---
# <a name="tbm_getrangemax-message"></a><span data-ttu-id="cfecf-104">TBM \_ GETRANGEMAX 訊息</span><span class="sxs-lookup"><span data-stu-id="cfecf-104">TBM\_GETRANGEMAX message</span></span>

<span data-ttu-id="cfecf-105">抓取捲軸中滑杆的最大位置。</span><span class="sxs-lookup"><span data-stu-id="cfecf-105">Retrieves the maximum position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="cfecf-106">參數</span><span class="sxs-lookup"><span data-stu-id="cfecf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfecf-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="cfecf-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="cfecf-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="cfecf-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="cfecf-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="cfecf-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="cfecf-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="cfecf-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfecf-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="cfecf-111">Return value</span></span>

<span data-ttu-id="cfecf-112">傳回32位值，這個值會指定在最小至最大滑杆位置的最大捲軸範圍內的最大位置。</span><span class="sxs-lookup"><span data-stu-id="cfecf-112">Returns a 32-bit value that specifies the maximum position in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfecf-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfecf-113">Requirements</span></span>



| <span data-ttu-id="cfecf-114">需求</span><span class="sxs-lookup"><span data-stu-id="cfecf-114">Requirement</span></span> | <span data-ttu-id="cfecf-115">值</span><span class="sxs-lookup"><span data-stu-id="cfecf-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cfecf-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cfecf-116">Minimum supported client</span></span><br/> | <span data-ttu-id="cfecf-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfecf-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="cfecf-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cfecf-118">Minimum supported server</span></span><br/> | <span data-ttu-id="cfecf-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfecf-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cfecf-120">標頭</span><span class="sxs-lookup"><span data-stu-id="cfecf-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfecf-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="cfecf-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfecf-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfecf-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="cfecf-123">**參考**</span><span class="sxs-lookup"><span data-stu-id="cfecf-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="cfecf-124">**TBM \_ GETRANGEMIN**</span><span class="sxs-lookup"><span data-stu-id="cfecf-124">**TBM\_GETRANGEMIN**</span></span>](tbm-getrangemin.md)
</dt> <dt>

[<span data-ttu-id="cfecf-125">**TBM \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="cfecf-125">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="cfecf-126">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="cfecf-126">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





