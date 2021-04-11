---
title: 'NM_HOVER (清單視圖) 通知碼 (Commctrl) '
description: 當滑鼠停留在專案上時，由清單視圖控制項所傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 0d4a2eee-9c98-43d1-bc05-226d91c0480a
keywords:
- NM_HOVER (清單視圖) 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_HOVER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e60606dfac73e13b0439ce861f37cb4ec941fda3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843076"
---
# <a name="nm_hover-list-view-notification-code"></a><span data-ttu-id="1e7ef-105">NM 將 \_ (清單視圖) 通知碼</span><span class="sxs-lookup"><span data-stu-id="1e7ef-105">NM\_HOVER (list view) notification code</span></span>

<span data-ttu-id="1e7ef-106">當滑鼠停留在專案上時，由清單視圖控制項所傳送。</span><span class="sxs-lookup"><span data-stu-id="1e7ef-106">Sent by a list-view control when the mouse hovers over an item.</span></span> <span data-ttu-id="1e7ef-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="1e7ef-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_HOVER

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="1e7ef-108">參數</span><span class="sxs-lookup"><span data-stu-id="1e7ef-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e7ef-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="1e7ef-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="1e7ef-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1e7ef-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e7ef-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1e7ef-111">Return value</span></span>

<span data-ttu-id="1e7ef-112">傳回零以允許清單視圖正常處理暫留，或非零，以防止暫止處理。</span><span class="sxs-lookup"><span data-stu-id="1e7ef-112">Return zero to allow the list view to process the hover normally, or nonzero to prevent the hover from being processed.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e7ef-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="1e7ef-113">Requirements</span></span>



| <span data-ttu-id="1e7ef-114">需求</span><span class="sxs-lookup"><span data-stu-id="1e7ef-114">Requirement</span></span> | <span data-ttu-id="1e7ef-115">值</span><span class="sxs-lookup"><span data-stu-id="1e7ef-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1e7ef-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1e7ef-116">Minimum supported client</span></span><br/> | <span data-ttu-id="1e7ef-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e7ef-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e7ef-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1e7ef-118">Minimum supported server</span></span><br/> | <span data-ttu-id="1e7ef-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1e7ef-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1e7ef-120">標頭</span><span class="sxs-lookup"><span data-stu-id="1e7ef-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e7ef-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="1e7ef-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





