---
title: 'MCN_VIEWCHANGE (Commctrl 的通知碼) '
description: 由月曆控制項在目前的視圖變更時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: ee35ac1d-9aeb-4d75-9cef-016487f23602
keywords:
- MCN_VIEWCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- MCN_VIEWCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: abbcad3fdda355ac2795dbe49a89fa4e7c2c5cad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464529"
---
# <a name="mcn_viewchange-notification-code"></a><span data-ttu-id="07e73-105">MCN \_ VIEWCHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="07e73-105">MCN\_VIEWCHANGE notification code</span></span>

<span data-ttu-id="07e73-106">由月曆控制項在目前的視圖變更時傳送。</span><span class="sxs-lookup"><span data-stu-id="07e73-106">Sent by a month calendar control when the current view changes.</span></span> <span data-ttu-id="07e73-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="07e73-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
MCN_VIEWCHANGE

    lpNMViewChange = (LPNMVIEWCHANGE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="07e73-108">參數</span><span class="sxs-lookup"><span data-stu-id="07e73-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07e73-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="07e73-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="07e73-110">[**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange)結構的指標，其中包含目前視圖的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="07e73-110">Pointer to an [**NMVIEWCHANGE**](/windows/win32/api/commctrl/ns-commctrl-nmviewchange) structure that contains information about the current view.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07e73-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="07e73-111">Return value</span></span>

<span data-ttu-id="07e73-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="07e73-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="07e73-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="07e73-113">Requirements</span></span>



| <span data-ttu-id="07e73-114">需求</span><span class="sxs-lookup"><span data-stu-id="07e73-114">Requirement</span></span> | <span data-ttu-id="07e73-115">值</span><span class="sxs-lookup"><span data-stu-id="07e73-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="07e73-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07e73-116">Minimum supported client</span></span><br/> | <span data-ttu-id="07e73-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07e73-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="07e73-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07e73-118">Minimum supported server</span></span><br/> | <span data-ttu-id="07e73-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="07e73-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="07e73-120">標頭</span><span class="sxs-lookup"><span data-stu-id="07e73-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="07e73-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="07e73-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





