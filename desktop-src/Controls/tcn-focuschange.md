---
title: 'TCN_FOCUSCHANGE (Commctrl 的通知碼) '
description: 通知索引標籤控制項的父視窗，按鈕焦點已變更。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 7500faae-5386-465d-ae4a-285205bccc1f
keywords:
- TCN_FOCUSCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TCN_FOCUSCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80c7ef76daf7ff9731a3fe5d749141454df19c35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685499"
---
# <a name="tcn_focuschange-notification-code"></a><span data-ttu-id="5fd1e-105">TCN \_ FOCUSCHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="5fd1e-105">TCN\_FOCUSCHANGE notification code</span></span>

<span data-ttu-id="5fd1e-106">通知索引標籤控制項的父視窗，按鈕焦點已變更。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-106">Notifies a tab control's parent window that the button focus has changed.</span></span> <span data-ttu-id="5fd1e-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_FOCUSCHANGE

    lpnmh = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="5fd1e-108">參數</span><span class="sxs-lookup"><span data-stu-id="5fd1e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fd1e-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="5fd1e-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="5fd1e-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fd1e-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="5fd1e-111">Return value</span></span>

<span data-ttu-id="5fd1e-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="5fd1e-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="5fd1e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5fd1e-113">Requirements</span></span>



| <span data-ttu-id="5fd1e-114">需求</span><span class="sxs-lookup"><span data-stu-id="5fd1e-114">Requirement</span></span> | <span data-ttu-id="5fd1e-115">值</span><span class="sxs-lookup"><span data-stu-id="5fd1e-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd1e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5fd1e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5fd1e-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5fd1e-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5fd1e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5fd1e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5fd1e-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5fd1e-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5fd1e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="5fd1e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="5fd1e-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="5fd1e-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





