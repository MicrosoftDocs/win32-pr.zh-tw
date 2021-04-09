---
title: 'TBM_GETRANGEMIN 訊息 (Commctrl .h) '
description: 抓取捲軸中滑杆的最小位置。
ms.assetid: 64334aed-0403-4785-829e-693292734d10
keywords:
- TBM_GETRANGEMIN message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_GETRANGEMIN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fddef597f7b129f8334f75136f56404a8ef117fa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934408"
---
# <a name="tbm_getrangemin-message"></a><span data-ttu-id="9de74-104">TBM \_ GETRANGEMIN 訊息</span><span class="sxs-lookup"><span data-stu-id="9de74-104">TBM\_GETRANGEMIN message</span></span>

<span data-ttu-id="9de74-105">抓取捲軸中滑杆的最小位置。</span><span class="sxs-lookup"><span data-stu-id="9de74-105">Retrieves the minimum position for the slider in a trackbar.</span></span>

## <a name="parameters"></a><span data-ttu-id="9de74-106">參數</span><span class="sxs-lookup"><span data-stu-id="9de74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9de74-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="9de74-107">*wParam*</span></span> 
</dt> <dd><span data-ttu-id="9de74-108">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9de74-108">Must be zero.</span></span></dd> <dt>

<span data-ttu-id="9de74-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9de74-109">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="9de74-110">必須為零。</span><span class="sxs-lookup"><span data-stu-id="9de74-110">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9de74-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9de74-111">Return value</span></span>

<span data-ttu-id="9de74-112">傳回32位值，這個值會指定在最小至最大滑杆位置的最小值範圍中，最小位置。</span><span class="sxs-lookup"><span data-stu-id="9de74-112">Returns a 32-bit value that specifies the minimum position in the trackbar's range of minimum to maximum slider positions.</span></span>

## <a name="requirements"></a><span data-ttu-id="9de74-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9de74-113">Requirements</span></span>



| <span data-ttu-id="9de74-114">需求</span><span class="sxs-lookup"><span data-stu-id="9de74-114">Requirement</span></span> | <span data-ttu-id="9de74-115">值</span><span class="sxs-lookup"><span data-stu-id="9de74-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9de74-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9de74-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9de74-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9de74-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9de74-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9de74-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9de74-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9de74-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9de74-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9de74-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9de74-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9de74-121"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9de74-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9de74-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="9de74-123">**參考**</span><span class="sxs-lookup"><span data-stu-id="9de74-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="9de74-124">**TBM \_ GETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="9de74-124">**TBM\_GETRANGEMAX**</span></span>](tbm-getrangemax.md)
</dt> <dt>

[<span data-ttu-id="9de74-125">**TBM \_ SETRANGE**</span><span class="sxs-lookup"><span data-stu-id="9de74-125">**TBM\_SETRANGE**</span></span>](tbm-setrange.md)
</dt> <dt>

[<span data-ttu-id="9de74-126">**TBM \_ SETRANGEMAX**</span><span class="sxs-lookup"><span data-stu-id="9de74-126">**TBM\_SETRANGEMAX**</span></span>](tbm-setrangemax.md)
</dt> </dl>

 

 





