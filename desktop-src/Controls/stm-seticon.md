---
title: 'STM_SETICON 訊息 (Winuser .h) '
description: 應用程式會傳送 STM \_ SETICON 訊息，以將圖示與圖示控制項產生關聯。
ms.assetid: 105b0667-8e23-47ed-9fb1-0792a22d7100
keywords:
- STM_SETICON message Windows 控制項
topic_type:
- apiref
api_name:
- STM_SETICON
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9c7e2a007c1f866a1c73b3a1c1a55b157add47
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024648"
---
# <a name="stm_seticon-message"></a><span data-ttu-id="f959e-104">STM \_ SETICON 訊息</span><span class="sxs-lookup"><span data-stu-id="f959e-104">STM\_SETICON message</span></span>

<span data-ttu-id="f959e-105">應用程式會傳送 **STM \_ SETICON** 訊息，以將圖示與圖示控制項產生關聯。</span><span class="sxs-lookup"><span data-stu-id="f959e-105">An application sends the **STM\_SETICON** message to associate an icon with an icon control.</span></span>

## <a name="parameters"></a><span data-ttu-id="f959e-106">參數</span><span class="sxs-lookup"><span data-stu-id="f959e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f959e-107">*wParam*</span><span class="sxs-lookup"><span data-stu-id="f959e-107">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f959e-108">要與圖示控制項相關聯之圖示的控制碼。</span><span class="sxs-lookup"><span data-stu-id="f959e-108">Handle to the icon to associate with the icon control.</span></span>

</dd> <dt>

<span data-ttu-id="f959e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f959e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f959e-110">不使用這個參數。</span><span class="sxs-lookup"><span data-stu-id="f959e-110">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f959e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f959e-111">Return value</span></span>

<span data-ttu-id="f959e-112">傳回值是先前與圖示控制項相關聯之圖示的控制碼; 如果發生錯誤，則為零。</span><span class="sxs-lookup"><span data-stu-id="f959e-112">The return value is a handle to the icon previously associated with the icon control, or zero if an error occurs.</span></span>

## <a name="requirements"></a><span data-ttu-id="f959e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="f959e-113">Requirements</span></span>



| <span data-ttu-id="f959e-114">需求</span><span class="sxs-lookup"><span data-stu-id="f959e-114">Requirement</span></span> | <span data-ttu-id="f959e-115">值</span><span class="sxs-lookup"><span data-stu-id="f959e-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f959e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f959e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="f959e-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f959e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="f959e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f959e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="f959e-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f959e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="f959e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="f959e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="f959e-121"><dt>Winuser (包含) 的 Windows。h </dt></span><span class="sxs-lookup"><span data-stu-id="f959e-121"><dt>Winuser.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f959e-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f959e-122">See also</span></span>

<dl> <dt>

<span data-ttu-id="f959e-123">**參考**</span><span class="sxs-lookup"><span data-stu-id="f959e-123">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="f959e-124">**STM \_ GETICON**</span><span class="sxs-lookup"><span data-stu-id="f959e-124">**STM\_GETICON**</span></span>](stm-geticon.md)
</dt> <dt>

<span data-ttu-id="f959e-125">**其他資源**</span><span class="sxs-lookup"><span data-stu-id="f959e-125">**Other Resources**</span></span>
</dt> <dt>

[<span data-ttu-id="f959e-126">**LoadIcon**</span><span class="sxs-lookup"><span data-stu-id="f959e-126">**LoadIcon**</span></span>](/windows/desktop/api/winuser/nf-winuser-loadicona)
</dt> </dl>

 

