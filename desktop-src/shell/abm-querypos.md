---
description: 要求 appbar 的大小和螢幕位置。
ms.assetid: 061a30fb-a68a-464e-ad8c-0bda672b57d9
title: 'ABM_QUERYPOS 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08f25ef636b2c55d8442df49f86a59b537694c31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318123"
---
# <a name="abm_querypos-message"></a><span data-ttu-id="c9166-103">ABM \_ QUERYPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="c9166-103">ABM\_QUERYPOS message</span></span>

<span data-ttu-id="c9166-104">要求 appbar 的大小和螢幕位置。</span><span class="sxs-lookup"><span data-stu-id="c9166-104">Requests a size and screen position for an appbar.</span></span> <span data-ttu-id="c9166-105">提出要求時，訊息會提出 appbar 的螢幕邊緣和周框。</span><span class="sxs-lookup"><span data-stu-id="c9166-105">When the request is made, the message proposes a screen edge and a bounding rectangle for the appbar.</span></span> <span data-ttu-id="c9166-106">系統會調整周框，讓 appbar 不會干擾 Windows 工作列或任何其他透過像 appbars。</span><span class="sxs-lookup"><span data-stu-id="c9166-106">The system adjusts the bounding rectangle so that the appbar does not interfere with the Windows taskbar or any other appbars.</span></span>


```C++
SHAppBarMessage(ABM_QUERYPOS, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="c9166-107">參數</span><span class="sxs-lookup"><span data-stu-id="c9166-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9166-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="c9166-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="c9166-109">[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="c9166-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="c9166-110">**UEdge** 成員會指定螢幕邊緣，而 **rc** 成員會包含建議的周框。</span><span class="sxs-lookup"><span data-stu-id="c9166-110">The **uEdge** member specifies a screen edge, and the **rc** member contains the proposed bounding rectangle.</span></span> <span data-ttu-id="c9166-111">當 [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) 函式傳回時， **rc** 會包含已核准的周框。</span><span class="sxs-lookup"><span data-stu-id="c9166-111">When the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function returns, **rc** contains the approved bounding rectangle.</span></span> <span data-ttu-id="c9166-112">傳送此訊息時，您必須指定 **cbSize**、 **hWnd**、 **uEdge** 和 **rc** 成員;所有其他成員都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="c9166-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9166-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9166-113">Return value</span></span>

<span data-ttu-id="c9166-114">一律傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="c9166-114">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9166-115">備註</span><span class="sxs-lookup"><span data-stu-id="c9166-115">Remarks</span></span>

<span data-ttu-id="c9166-116">Appbar 應該會在傳送 [**ABM \_ SETPOS**](abm-setpos.md) 訊息之前傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c9166-116">An appbar should send this message before sending the [**ABM\_SETPOS**](abm-setpos.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9166-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9166-117">Requirements</span></span>



| <span data-ttu-id="c9166-118">需求</span><span class="sxs-lookup"><span data-stu-id="c9166-118">Requirement</span></span> | <span data-ttu-id="c9166-119">值</span><span class="sxs-lookup"><span data-stu-id="c9166-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9166-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9166-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c9166-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9166-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c9166-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9166-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c9166-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9166-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c9166-124">標頭</span><span class="sxs-lookup"><span data-stu-id="c9166-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9166-125"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9166-125"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




