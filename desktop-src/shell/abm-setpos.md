---
description: 設定 appbar 的大小和螢幕位置。
ms.assetid: b3c56278-b9a2-4e08-bf98-7b3e4c8bd082
title: 'ABM_SETPOS 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6886249f42638745ca038aa1f216ddc995f0e7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511071"
---
# <a name="abm_setpos-message"></a><span data-ttu-id="7e06a-103">ABM \_ SETPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="7e06a-103">ABM\_SETPOS message</span></span>

<span data-ttu-id="7e06a-104">設定 appbar 的大小和螢幕位置。</span><span class="sxs-lookup"><span data-stu-id="7e06a-104">Sets the size and screen position of an appbar.</span></span> <span data-ttu-id="7e06a-105">此訊息會指定螢幕邊緣和 appbar 的周框。</span><span class="sxs-lookup"><span data-stu-id="7e06a-105">The message specifies a screen edge and the bounding rectangle for the appbar.</span></span> <span data-ttu-id="7e06a-106">系統可能會調整周框，讓 appbar 不會干擾 Windows 工作列或其他任何透過像 appbars。</span><span class="sxs-lookup"><span data-stu-id="7e06a-106">The system may adjust the bounding rectangle so that the appbar does not interfere with the Windows taskbar or any other appbars.</span></span>


```C++
SHAppBarMessage(ABM_SETPOS, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="7e06a-107">參數</span><span class="sxs-lookup"><span data-stu-id="7e06a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e06a-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="7e06a-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="7e06a-109">[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="7e06a-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="7e06a-110">**UEdge** 成員會指定螢幕邊緣，而 **rc** 成員會包含周框。</span><span class="sxs-lookup"><span data-stu-id="7e06a-110">The **uEdge** member specifies a screen edge, and the **rc** member contains the bounding rectangle.</span></span> <span data-ttu-id="7e06a-111">當 [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) 函式傳回時， **rc** 會包含已核准的周框。</span><span class="sxs-lookup"><span data-stu-id="7e06a-111">When the [**SHAppBarMessage**](/windows/desktop/api/Shellapi/nf-shellapi-shappbarmessage) function returns, **rc** contains the approved bounding rectangle.</span></span> <span data-ttu-id="7e06a-112">傳送此訊息時，您必須指定 **cbSize**、 **hWnd**、 **uEdge** 和 **rc** 成員;所有其他成員都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="7e06a-112">You must specify the **cbSize**, **hWnd**, **uEdge**, and **rc** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e06a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="7e06a-113">Return value</span></span>

<span data-ttu-id="7e06a-114">一律傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="7e06a-114">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7e06a-115">備註</span><span class="sxs-lookup"><span data-stu-id="7e06a-115">Remarks</span></span>

<span data-ttu-id="7e06a-116">這則訊息會導致系統將 [**ABN \_ POSCHANGED**](abn-poschanged.md) 通知訊息傳送至所有透過像 appbars。</span><span class="sxs-lookup"><span data-stu-id="7e06a-116">This message causes the system to send the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message to all appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="7e06a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="7e06a-117">Requirements</span></span>



| <span data-ttu-id="7e06a-118">需求</span><span class="sxs-lookup"><span data-stu-id="7e06a-118">Requirement</span></span> | <span data-ttu-id="7e06a-119">值</span><span class="sxs-lookup"><span data-stu-id="7e06a-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7e06a-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7e06a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7e06a-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e06a-121">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7e06a-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7e06a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7e06a-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7e06a-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="7e06a-124">標頭</span><span class="sxs-lookup"><span data-stu-id="7e06a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7e06a-125"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="7e06a-125"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




