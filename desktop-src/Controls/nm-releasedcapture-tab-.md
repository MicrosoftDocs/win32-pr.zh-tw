---
title: 'NM_RELEASEDCAPTURE (] 索引標籤) 通知碼 (Commctrl) '
description: 通知索引標籤控制項的父視窗，控制項正在放開滑鼠捕捉。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 17f87666-692c-4c2f-9ef5-6d2593e0de97
keywords:
- NM_RELEASEDCAPTURE (] 索引標籤) 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_RELEASEDCAPTURE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad9c9049b63afb18413aea9fa77b7947e97e93b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465865"
---
# <a name="nm_releasedcapture-tab-notification-code"></a><span data-ttu-id="9d8c1-105">NM \_ RELEASEDCAPTURE (tab) 通知碼</span><span class="sxs-lookup"><span data-stu-id="9d8c1-105">NM\_RELEASEDCAPTURE (tab) notification code</span></span>

<span data-ttu-id="9d8c1-106">通知索引標籤控制項的父視窗，控制項正在放開滑鼠捕捉。</span><span class="sxs-lookup"><span data-stu-id="9d8c1-106">Notifies a tab control's parent window that the control is releasing mouse capture.</span></span> <span data-ttu-id="9d8c1-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="9d8c1-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_RELEASEDCAPTURE

    lpnmh = (LPNMHDR) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="9d8c1-108">參數</span><span class="sxs-lookup"><span data-stu-id="9d8c1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d8c1-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="9d8c1-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="9d8c1-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9d8c1-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d8c1-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9d8c1-111">Return value</span></span>

<span data-ttu-id="9d8c1-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="9d8c1-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="9d8c1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d8c1-113">Requirements</span></span>



| <span data-ttu-id="9d8c1-114">需求</span><span class="sxs-lookup"><span data-stu-id="9d8c1-114">Requirement</span></span> | <span data-ttu-id="9d8c1-115">值</span><span class="sxs-lookup"><span data-stu-id="9d8c1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d8c1-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d8c1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="9d8c1-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d8c1-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="9d8c1-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d8c1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="9d8c1-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d8c1-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="9d8c1-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9d8c1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d8c1-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="9d8c1-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





