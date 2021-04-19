---
title: 'NM_CHAR (Commctrl 的通知碼) '
description: '\_當處理字元鍵時，控制項會傳送 NM 字元通知碼。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。'
ms.assetid: b750f2a6-8642-4d76-96bb-bf58b00cd5c4
keywords:
- NM_CHAR 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- NM_CHAR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0910736bcb174c2f3ddb16174c153f4b22ac5bd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968391"
---
# <a name="nm_char-notification-code"></a><span data-ttu-id="40a4c-105">NM \_ CHAR 通知碼</span><span class="sxs-lookup"><span data-stu-id="40a4c-105">NM\_CHAR notification code</span></span>

<span data-ttu-id="40a4c-106">\_當處理字元鍵時，控制項會傳送 NM 字元通知碼。</span><span class="sxs-lookup"><span data-stu-id="40a4c-106">The NM\_CHAR notification code is sent by a control when a character key is processed.</span></span> <span data-ttu-id="40a4c-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="40a4c-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="40a4c-108">參數</span><span class="sxs-lookup"><span data-stu-id="40a4c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40a4c-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="40a4c-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="40a4c-110">[**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar)結構的指標，其中包含造成通知碼之字元的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="40a4c-110">A pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains additional information about the character that caused the notification code.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40a4c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="40a4c-111">Return value</span></span>

<span data-ttu-id="40a4c-112">大部分的控制項都會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="40a4c-112">The return value is ignored by most controls.</span></span> <span data-ttu-id="40a4c-113">如需詳細資訊，請參閱個別控制項的檔。</span><span class="sxs-lookup"><span data-stu-id="40a4c-113">For more information, see the documentation for the individual controls.</span></span>

## <a name="requirements"></a><span data-ttu-id="40a4c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="40a4c-114">Requirements</span></span>



| <span data-ttu-id="40a4c-115">需求</span><span class="sxs-lookup"><span data-stu-id="40a4c-115">Requirement</span></span> | <span data-ttu-id="40a4c-116">值</span><span class="sxs-lookup"><span data-stu-id="40a4c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="40a4c-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40a4c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="40a4c-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40a4c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="40a4c-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40a4c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="40a4c-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40a4c-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="40a4c-121">標頭</span><span class="sxs-lookup"><span data-stu-id="40a4c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="40a4c-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="40a4c-122"><dt>Commctrl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40a4c-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40a4c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40a4c-124">NM \_ 字元 (工具列) </span><span class="sxs-lookup"><span data-stu-id="40a4c-124">NM\_CHAR (toolbar)</span></span>](nm-char-toolbar.md)
</dt> </dl>

 

 





