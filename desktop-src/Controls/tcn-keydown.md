---
title: 'TCN_KEYDOWN (Commctrl 的通知碼) '
description: 通知索引標籤控制項的父視窗已按下按鍵。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 884e79cd-5732-44cd-8c7a-38bb9349ec7d
keywords:
- TCN_KEYDOWN 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TCN_KEYDOWN
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91a1e963b11faf8f75e50e86e8c120ea0b05f0dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967312"
---
# <a name="tcn_keydown-notification-code"></a><span data-ttu-id="577df-105">TCN \_ KEYDOWN 通知碼</span><span class="sxs-lookup"><span data-stu-id="577df-105">TCN\_KEYDOWN notification code</span></span>

<span data-ttu-id="577df-106">通知索引標籤控制項的父視窗已按下按鍵。</span><span class="sxs-lookup"><span data-stu-id="577df-106">Notifies a tab control's parent window that a key has been pressed.</span></span> <span data-ttu-id="577df-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="577df-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TCN_KEYDOWN 

    pnm = (NMTCKEYDOWN*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="577df-108">參數</span><span class="sxs-lookup"><span data-stu-id="577df-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="577df-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="577df-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="577df-110">[**NMTCKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="577df-110">Pointer to an [**NMTCKEYDOWN**](/windows/win32/api/commctrl/ns-commctrl-nmtckeydown) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="577df-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="577df-111">Return value</span></span>

<span data-ttu-id="577df-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="577df-112">No return value.</span></span>

## <a name="requirements"></a><span data-ttu-id="577df-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="577df-113">Requirements</span></span>



| <span data-ttu-id="577df-114">需求</span><span class="sxs-lookup"><span data-stu-id="577df-114">Requirement</span></span> | <span data-ttu-id="577df-115">值</span><span class="sxs-lookup"><span data-stu-id="577df-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="577df-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="577df-116">Minimum supported client</span></span><br/> | <span data-ttu-id="577df-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="577df-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="577df-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="577df-118">Minimum supported server</span></span><br/> | <span data-ttu-id="577df-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="577df-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="577df-120">標頭</span><span class="sxs-lookup"><span data-stu-id="577df-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="577df-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="577df-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





