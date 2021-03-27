---
description: 當事件發生時可能會影響 appbar 的大小和位置時，通知 appbar。
ms.assetid: 1016a362-4d2b-410e-aec9-c1cc8f497778
title: 'ABN_POSCHANGED 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24b0a800b1c112cba18fbadbba79a999ec83c77e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972085"
---
# <a name="abn_poschanged-message"></a><span data-ttu-id="2ea35-103">ABN \_ POSCHANGED 訊息</span><span class="sxs-lookup"><span data-stu-id="2ea35-103">ABN\_POSCHANGED message</span></span>

<span data-ttu-id="2ea35-104">當事件發生時可能會影響 appbar 的大小和位置時，通知 appbar。</span><span class="sxs-lookup"><span data-stu-id="2ea35-104">Notifies an appbar when an event has occurred that may affect the appbar's size and position.</span></span> <span data-ttu-id="2ea35-105">事件包括工作列大小、位置和可見度狀態的變更，以及在螢幕相同側邊的其他 appbar 的新增、移除或調整大小。</span><span class="sxs-lookup"><span data-stu-id="2ea35-105">Events include changes in the taskbar's size, position, and visibility state, as well as the addition, removal, or resizing of another appbar on the same side of the screen.</span></span>


```C++
ABN_POSCHANGED
```



## <a name="parameters"></a><span data-ttu-id="2ea35-106">參數</span><span class="sxs-lookup"><span data-stu-id="2ea35-106">Parameters</span></span>

<span data-ttu-id="2ea35-107">此訊息沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2ea35-107">This message has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2ea35-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="2ea35-108">Return value</span></span>

<span data-ttu-id="2ea35-109">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="2ea35-109">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ea35-110">備註</span><span class="sxs-lookup"><span data-stu-id="2ea35-110">Remarks</span></span>

<span data-ttu-id="2ea35-111">Appbar 應該藉由傳送 [**ABM \_ QUERYPOS**](abm-querypos.md) 和 [**ABM \_ SETPOS**](abm-setpos.md) 訊息來回應此通知訊息。</span><span class="sxs-lookup"><span data-stu-id="2ea35-111">An appbar should respond to this notification message by sending the [**ABM\_QUERYPOS**](abm-querypos.md) and [**ABM\_SETPOS**](abm-setpos.md) messages.</span></span> <span data-ttu-id="2ea35-112">如果它的位置已變更，則 appbar 應該呼叫 [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) 函式，將其本身移至新的位置。</span><span class="sxs-lookup"><span data-stu-id="2ea35-112">If its position has changed, the appbar should call the [**MoveWindow**](/windows/desktop/api/winuser/nf-winuser-movewindow) function to move itself to the new position.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ea35-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="2ea35-113">Requirements</span></span>



| <span data-ttu-id="2ea35-114">需求</span><span class="sxs-lookup"><span data-stu-id="2ea35-114">Requirement</span></span> | <span data-ttu-id="2ea35-115">值</span><span class="sxs-lookup"><span data-stu-id="2ea35-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2ea35-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2ea35-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2ea35-117">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ea35-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="2ea35-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2ea35-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2ea35-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2ea35-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2ea35-120">標頭</span><span class="sxs-lookup"><span data-stu-id="2ea35-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2ea35-121"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="2ea35-121"><dt>Shellapi.h</dt></span></span> </dl> |



 

