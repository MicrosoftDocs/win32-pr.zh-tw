---
title: 'RBN_HEIGHTCHANGE (Commctrl 的通知碼) '
description: 當 Rebar 控制項的高度變更時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: cf90e38c-ac3e-4bef-b047-0956ae5041d1
keywords:
- RBN_HEIGHTCHANGE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- RBN_HEIGHTCHANGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe0601e8cb22ec9b86768741c5b455aa7f21eef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934314"
---
# <a name="rbn_heightchange-notification-code"></a><span data-ttu-id="92f2d-105">RBN \_ HEIGHTCHANGE 通知碼</span><span class="sxs-lookup"><span data-stu-id="92f2d-105">RBN\_HEIGHTCHANGE notification code</span></span>

<span data-ttu-id="92f2d-106">當 Rebar 控制項的高度變更時傳送。</span><span class="sxs-lookup"><span data-stu-id="92f2d-106">Sent by a rebar control when its height has changed.</span></span> <span data-ttu-id="92f2d-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="92f2d-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_HEIGHTCHANGE

    lpnmhdr = (LPNMHDR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="92f2d-108">參數</span><span class="sxs-lookup"><span data-stu-id="92f2d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92f2d-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="92f2d-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="92f2d-110">[**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr)結構的指標，其中包含此通知的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="92f2d-110">Pointer to an [**NMHDR**](/windows/desktop/api/richedit/ns-richedit-nmhdr) structure that contains additional information about this notification.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92f2d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="92f2d-111">Return value</span></span>

<span data-ttu-id="92f2d-112">未使用此通知的傳回值。</span><span class="sxs-lookup"><span data-stu-id="92f2d-112">The return value for this notification is not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="92f2d-113">備註</span><span class="sxs-lookup"><span data-stu-id="92f2d-113">Remarks</span></span>

<span data-ttu-id="92f2d-114">使用 [**CCS \_ 垂直**](common-control-styles.md) 樣式的 Rebar 控制項，會在其寬度變更時傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="92f2d-114">Rebar controls that use the [**CCS\_VERT**](common-control-styles.md) style send this notification code when their width changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="92f2d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="92f2d-115">Requirements</span></span>



| <span data-ttu-id="92f2d-116">需求</span><span class="sxs-lookup"><span data-stu-id="92f2d-116">Requirement</span></span> | <span data-ttu-id="92f2d-117">值</span><span class="sxs-lookup"><span data-stu-id="92f2d-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="92f2d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92f2d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="92f2d-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92f2d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="92f2d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92f2d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="92f2d-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92f2d-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="92f2d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="92f2d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="92f2d-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="92f2d-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





