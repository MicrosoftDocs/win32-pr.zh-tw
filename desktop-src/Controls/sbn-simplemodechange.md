---
title: 'SBN_SIMPLEMODECHANGE (Commctrl 的通知碼) '
description: 當簡單模式因為 SB 簡單訊息而變更時，由狀態列控制項傳送 \_ 。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: b2df8feb-5028-4488-a99b-4ceff5b48a92
keywords:
- SBN_SIMPLEMODECHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- SBN_SIMPLEMODECHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b998f0c39ecb00322bf5a423f99b3231338283f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967750"
---
# <a name="sbn_simplemodechange-notification-code"></a><span data-ttu-id="2ede9-105">SBN \_ SIMPLEMODECHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="2ede9-105">SBN\_SIMPLEMODECHANGE notification code</span></span>

<span data-ttu-id="2ede9-106">當簡單模式因為 [**SB \_ 簡單**](sb-simple.md) 訊息而變更時，由狀態列控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="2ede9-106">Sent by a status bar control when the simple mode changes due to a [**SB\_SIMPLE**](sb-simple.md) message.</span></span> <span data-ttu-id="2ede9-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="2ede9-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
SBN_SIMPLEMODECHANGE

    lpnmh = (NMHDR*) lParam;
```



## <a name="parameters"></a><span data-ttu-id="2ede9-108">參數</span><span class="sxs-lookup"><span data-stu-id="2ede9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ede9-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="2ede9-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="2ede9-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含通知碼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2ede9-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains information about the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ede9-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ede9-111">Return value</span></span>

<span data-ttu-id="2ede9-112">狀態列會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="2ede9-112">The return value is ignored by the status bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ede9-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ede9-113">Requirements</span></span>



| <span data-ttu-id="2ede9-114">需求</span><span class="sxs-lookup"><span data-stu-id="2ede9-114">Requirement</span></span> | <span data-ttu-id="2ede9-115">值</span><span class="sxs-lookup"><span data-stu-id="2ede9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ede9-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ede9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2ede9-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ede9-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="2ede9-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ede9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2ede9-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ede9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ede9-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2ede9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ede9-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ede9-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





