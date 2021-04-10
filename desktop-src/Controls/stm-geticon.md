---
title: 'STM_GETICON 訊息 (Winuser .h) '
description: 應用程式會傳送 STM \_ GETICON 訊息，以抓取與具有 SS 圖示樣式之靜態控制項相關聯的圖示控制碼 \_ 。
ms.assetid: e6b0a006-696b-401d-b894-b1db697c8939
keywords:
- STM_GETICON message Windows 控制項
topic_type:
- apiref
api_name:
- STM_GETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64f55d2a2f8315b99526e51a69891f6f0056e8b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094075"
---
# <a name="stm_geticon-message"></a><span data-ttu-id="2a682-104">STM \_ GETICON 訊息</span><span class="sxs-lookup"><span data-stu-id="2a682-104">STM\_GETICON message</span></span>

<span data-ttu-id="2a682-105">應用程式會傳送 **STM \_ GETICON** 訊息，以抓取與具有 SS 圖示樣式之靜態控制項相關聯的圖示控制碼 \_ 。</span><span class="sxs-lookup"><span data-stu-id="2a682-105">An application sends the **STM\_GETICON** message to retrieve a handle to the icon associated with a static control that has the SS\_ICON style.</span></span>

## <a name="parameters"></a><span data-ttu-id="2a682-106">參數</span><span class="sxs-lookup"><span data-stu-id="2a682-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a682-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="2a682-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a682-108">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="2a682-108">Not used; must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="2a682-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2a682-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2a682-110">未使用;必須為零。</span><span class="sxs-lookup"><span data-stu-id="2a682-110">Not used; must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a682-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a682-111">Return value</span></span>

<span data-ttu-id="2a682-112">傳回值是圖示的控制碼; 如果靜態控制項沒有相關聯的圖示或發生錯誤，則為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="2a682-112">The return value is a handle to the icon, or **NULL** if either the static control has no associated icon or if an error occurred.</span></span>

## <a name="requirements"></a><span data-ttu-id="2a682-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a682-113">Requirements</span></span>



| <span data-ttu-id="2a682-114">需求</span><span class="sxs-lookup"><span data-stu-id="2a682-114">Requirement</span></span> | <span data-ttu-id="2a682-115">值</span><span class="sxs-lookup"><span data-stu-id="2a682-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a682-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a682-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2a682-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a682-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2a682-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a682-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2a682-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2a682-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2a682-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2a682-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2a682-121"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="2a682-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a682-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a682-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a682-123">**STM \_ SETICON**</span><span class="sxs-lookup"><span data-stu-id="2a682-123">**STM\_SETICON**</span></span>](stm-seticon.md)
</dt> </dl>

 

 





