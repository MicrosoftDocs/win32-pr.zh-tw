---
title: 'TBM_SETTHUMBLENGTH 訊息 (Commctrl .h) '
description: 設定捲軸中滑杆的長度。 如果 [FIXEDLENGTH] 沒有 [TB] 樣式，則會忽略此訊息 \_ 。
ms.assetid: 027fe341-a60a-4dbe-a48a-5ddaadef0b4a
keywords:
- TBM_SETTHUMBLENGTH message Windows 控制項
topic_type:
- apiref
api_name:
- TBM_SETTHUMBLENGTH
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d4ac33d2df43a267766e14ab95fb9729692bbee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509216"
---
# <a name="tbm_setthumblength-message"></a><span data-ttu-id="baa9c-105">TBM \_ SETTHUMBLENGTH 訊息</span><span class="sxs-lookup"><span data-stu-id="baa9c-105">TBM\_SETTHUMBLENGTH message</span></span>

<span data-ttu-id="baa9c-106">設定捲軸中滑杆的長度。</span><span class="sxs-lookup"><span data-stu-id="baa9c-106">Sets the length of the slider in a trackbar.</span></span> <span data-ttu-id="baa9c-107">如果 [FIXEDLENGTH] 沒有 [ [**tb] \_**](trackbar-control-styles.md) 樣式，則會忽略此訊息。</span><span class="sxs-lookup"><span data-stu-id="baa9c-107">This message is ignored if the trackbar does not have the [**TBS\_FIXEDLENGTH**](trackbar-control-styles.md) style.</span></span>

## <a name="parameters"></a><span data-ttu-id="baa9c-108">參數</span><span class="sxs-lookup"><span data-stu-id="baa9c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="baa9c-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="baa9c-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="baa9c-110">滑杆的長度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="baa9c-110">Length, in pixels, of the slider.</span></span>

</dd> <dt>

<span data-ttu-id="baa9c-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="baa9c-111">*lParam*</span></span> 
</dt> <dd><span data-ttu-id="baa9c-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="baa9c-112">Must be zero.</span></span></dd> </dl>

## <a name="return-value"></a><span data-ttu-id="baa9c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="baa9c-113">Return value</span></span>

<span data-ttu-id="baa9c-114">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="baa9c-114">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="baa9c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="baa9c-115">Requirements</span></span>



| <span data-ttu-id="baa9c-116">需求</span><span class="sxs-lookup"><span data-stu-id="baa9c-116">Requirement</span></span> | <span data-ttu-id="baa9c-117">值</span><span class="sxs-lookup"><span data-stu-id="baa9c-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="baa9c-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="baa9c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="baa9c-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="baa9c-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="baa9c-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="baa9c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="baa9c-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="baa9c-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="baa9c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="baa9c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="baa9c-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="baa9c-123"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="baa9c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="baa9c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="baa9c-125">**TBM \_ GETTHUMBLENGTH**</span><span class="sxs-lookup"><span data-stu-id="baa9c-125">**TBM\_GETTHUMBLENGTH**</span></span>](tbm-getthumblength.md)
</dt> </dl>

 

 





