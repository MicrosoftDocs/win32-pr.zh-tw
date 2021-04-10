---
title: 'NM_CLICK (syslink) 通知碼 (Commctrl .h) '
description: 通知控制項的父視窗，指出使用者已在控制項內按一下滑鼠左鍵的超連結。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: e92d7c92-f2c6-44aa-bce5-3bb07c184e7d
keywords:
- NM_CLICK (syslink) 通知程式碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_CLICK
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ea34682b0cfdfdf1206a133abe4fdb22b8af5cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106643"
---
# <a name="nm_click-syslink-notification-code"></a><span data-ttu-id="21037-105">NM \_ 按一下 (syslink) 通知碼</span><span class="sxs-lookup"><span data-stu-id="21037-105">NM\_CLICK (syslink) notification code</span></span>

<span data-ttu-id="21037-106">通知控制項的父視窗，指出使用者已在控制項內按一下滑鼠左鍵的超連結。</span><span class="sxs-lookup"><span data-stu-id="21037-106">Notifies a control's parent window that the user has clicked a hyperlink with the left mouse button within the control.</span></span> <span data-ttu-id="21037-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="21037-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CLICK

    pnmLink = (PNMLINK) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="21037-108">參數</span><span class="sxs-lookup"><span data-stu-id="21037-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21037-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="21037-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="21037-110">[**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="21037-110">Pointer to an [**NMLINK**](/windows/win32/api/commctrl/ns-commctrl-nmlink) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21037-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="21037-111">Return value</span></span>

<span data-ttu-id="21037-112">控制項會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="21037-112">The return value is ignored by the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="21037-113">備註</span><span class="sxs-lookup"><span data-stu-id="21037-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="21037-114">若要使用此通知碼，您必須提供指定 Comclt32.dll 版本6.0 的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="21037-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="21037-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="21037-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="21037-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="21037-116">Requirements</span></span>



| <span data-ttu-id="21037-117">需求</span><span class="sxs-lookup"><span data-stu-id="21037-117">Requirement</span></span> | <span data-ttu-id="21037-118">值</span><span class="sxs-lookup"><span data-stu-id="21037-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="21037-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21037-119">Minimum supported client</span></span><br/> | <span data-ttu-id="21037-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21037-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="21037-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21037-121">Minimum supported server</span></span><br/> | <span data-ttu-id="21037-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21037-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="21037-123">標頭</span><span class="sxs-lookup"><span data-stu-id="21037-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="21037-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="21037-124"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21037-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21037-125">See also</span></span>

<dl> <dt>

<span data-ttu-id="21037-126">**參考**</span><span class="sxs-lookup"><span data-stu-id="21037-126">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="21037-127">**NMLINK**</span><span class="sxs-lookup"><span data-stu-id="21037-127">**NMLINK**</span></span>](/windows/win32/api/commctrl/ns-commctrl-nmlink)
</dt> <dt>

[<span data-ttu-id="21037-128">**WM \_ 通知**</span><span class="sxs-lookup"><span data-stu-id="21037-128">**WM\_NOTIFY**</span></span>](wm-notify.md)
</dt> </dl>

 

 





