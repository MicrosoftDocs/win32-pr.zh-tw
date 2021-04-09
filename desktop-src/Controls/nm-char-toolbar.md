---
title: 'NM_CHAR (工具列) 通知碼 (Commctrl) '
description: 當工具列收到 WM \_ 字元訊息時傳送。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 7bf0b046-da8e-448f-94e1-62ba0989f7ba
keywords:
- NM_CHAR (工具列) 通知程式碼 Windows 控制項
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
ms.openlocfilehash: a5a68cb85130f22c8cda63920ada974453a36991
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844468"
---
# <a name="nm_char-toolbar-notification-code"></a><span data-ttu-id="f8ebe-105">NM \_ 字元 (工具列) 通知碼</span><span class="sxs-lookup"><span data-stu-id="f8ebe-105">NM\_CHAR (toolbar) notification code</span></span>

<span data-ttu-id="f8ebe-106">當工具列收到 [**WM \_ 字元**](/windows/desktop/inputdev/wm-char) 訊息時傳送。</span><span class="sxs-lookup"><span data-stu-id="f8ebe-106">Sent by a toolbar when it receives a [**WM\_CHAR**](/windows/desktop/inputdev/wm-char) message.</span></span> <span data-ttu-id="f8ebe-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="f8ebe-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
NM_CHAR

    lpnmc = (LPNMCHAR) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f8ebe-108">參數</span><span class="sxs-lookup"><span data-stu-id="f8ebe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8ebe-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f8ebe-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f8ebe-110">[**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar)結構的指標，其中包含造成通知碼之字元的其他相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f8ebe-110">Pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains additional information about the character that caused the notification code.</span></span> <span data-ttu-id="f8ebe-111">此結構的 **dwItemPrev** 成員包含目前作用中之專案的命令識別碼，如果沒有任何專案在作用中，則為-1。</span><span class="sxs-lookup"><span data-stu-id="f8ebe-111">The **dwItemPrev** member of this structure contains the command identifier of the item that is currently hot or -1 if no item is currently hot.</span></span> <span data-ttu-id="f8ebe-112">此結構的 **dwItemNext** 成員包含將變成經常性存取之專案的命令識別碼，如果索引鍵不符合任何專案的快速鍵，則為-1。</span><span class="sxs-lookup"><span data-stu-id="f8ebe-112">The **dwItemNext** member of this structure contains the command identifier of the item that will become hot or -1 if the key does not match any item's accelerator.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8ebe-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8ebe-113">Return value</span></span>

<span data-ttu-id="f8ebe-114">傳回 **TRUE** ，表示工具列不應處理字元和 **FALSE** ，讓工具列處理該字元。</span><span class="sxs-lookup"><span data-stu-id="f8ebe-114">Returns **TRUE** to indicate that the toolbar should not process the character and **FALSE** to have the toolbar process the character.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8ebe-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8ebe-115">Requirements</span></span>



| <span data-ttu-id="f8ebe-116">需求</span><span class="sxs-lookup"><span data-stu-id="f8ebe-116">Requirement</span></span> | <span data-ttu-id="f8ebe-117">值</span><span class="sxs-lookup"><span data-stu-id="f8ebe-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f8ebe-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f8ebe-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f8ebe-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8ebe-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8ebe-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f8ebe-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f8ebe-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f8ebe-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f8ebe-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f8ebe-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8ebe-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f8ebe-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

