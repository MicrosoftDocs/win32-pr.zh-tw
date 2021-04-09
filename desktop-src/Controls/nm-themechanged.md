---
title: 'NM_THEMECHANGED (Commctrl 的通知碼) '
description: 通知控制項的父視窗，主題已變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 5e6a039e-9c35-4476-8cf1-5aea8977ed2d
keywords:
- NM_THEMECHANGED 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_THEMECHANGED
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3dab2a133da2ff1fed0949f2bc97ce294168febc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025288"
---
# <a name="nm_themechanged-notification-code"></a><span data-ttu-id="381f5-105">NM \_ THEMECHANGED 通知碼</span><span class="sxs-lookup"><span data-stu-id="381f5-105">NM\_THEMECHANGED notification code</span></span>

<span data-ttu-id="381f5-106">通知控制項的父視窗，主題已變更。</span><span class="sxs-lookup"><span data-stu-id="381f5-106">Notifies a control's parent window that the theme has changed.</span></span> <span data-ttu-id="381f5-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="381f5-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_THEMECHANGED

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="381f5-108">參數</span><span class="sxs-lookup"><span data-stu-id="381f5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="381f5-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="381f5-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="381f5-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="381f5-110">A pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="381f5-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="381f5-111">Return value</span></span>

<span data-ttu-id="381f5-112">控制項會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="381f5-112">The return value is ignored by the control.</span></span>

## <a name="requirements"></a><span data-ttu-id="381f5-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="381f5-113">Requirements</span></span>



| <span data-ttu-id="381f5-114">需求</span><span class="sxs-lookup"><span data-stu-id="381f5-114">Requirement</span></span> | <span data-ttu-id="381f5-115">值</span><span class="sxs-lookup"><span data-stu-id="381f5-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="381f5-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="381f5-116">Minimum supported client</span></span><br/> | <span data-ttu-id="381f5-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="381f5-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="381f5-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="381f5-118">Minimum supported server</span></span><br/> | <span data-ttu-id="381f5-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="381f5-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="381f5-120">標頭</span><span class="sxs-lookup"><span data-stu-id="381f5-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="381f5-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="381f5-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





