---
description: 抓取 Windows 工作列的周框。
ms.assetid: 8072bb2d-05e6-4baa-a7f4-1377b94fdd45
title: 'ABM_GETTASKBARPOS 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb678b6e7ade1f148d2deb4b0de6c8953f019d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511072"
---
# <a name="abm_gettaskbarpos-message"></a><span data-ttu-id="26d08-103">ABM \_ GETTASKBARPOS 訊息</span><span class="sxs-lookup"><span data-stu-id="26d08-103">ABM\_GETTASKBARPOS message</span></span>

<span data-ttu-id="26d08-104">抓取 Windows 工作列的周框。</span><span class="sxs-lookup"><span data-stu-id="26d08-104">Retrieves the bounding rectangle of the Windows taskbar.</span></span>


```C++
fResult = (BOOL) SHAppBarMessage(ABM_GETTASKBARPOS, pabd);
```



## <a name="parameters"></a><span data-ttu-id="26d08-105">參數</span><span class="sxs-lookup"><span data-stu-id="26d08-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="26d08-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="26d08-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="26d08-107">[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標，其 **rc** 成員會收到工作列的周框（以螢幕座標為單位）。</span><span class="sxs-lookup"><span data-stu-id="26d08-107">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure whose **rc** member receives the bounding rectangle, in screen coordinates, of the taskbar.</span></span> <span data-ttu-id="26d08-108">傳送此訊息時，您必須指定 **cbSize** ;所有其他成員都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="26d08-108">You must specify the **cbSize** when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="26d08-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="26d08-109">Return value</span></span>

<span data-ttu-id="26d08-110">如果成功，則傳回 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="26d08-110">Returns **TRUE** if successful; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="26d08-111">備註</span><span class="sxs-lookup"><span data-stu-id="26d08-111">Remarks</span></span>

<span data-ttu-id="26d08-112">請注意，這只適用于系統工作列。</span><span class="sxs-lookup"><span data-stu-id="26d08-112">Note that this applies only to the system taskbar.</span></span> <span data-ttu-id="26d08-113">其他物件（特別是協力廠商軟體提供的工具列）也可以存在。</span><span class="sxs-lookup"><span data-stu-id="26d08-113">Other objects, particularly toolbars supplied with third-party software, also can be present.</span></span> <span data-ttu-id="26d08-114">如此一來，使用者就看不到 Windows 工作列所涵蓋的某些螢幕區域。</span><span class="sxs-lookup"><span data-stu-id="26d08-114">As a result, some of the screen area not covered by the Windows taskbar might not be visible to the user.</span></span> <span data-ttu-id="26d08-115">若要取出工作列和其他應用程式橫條未涵蓋的畫面區域，可供您的應用程式使用的工作區，請使用 [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) 函數。</span><span class="sxs-lookup"><span data-stu-id="26d08-115">To retrieve the area of the screen not covered by both the taskbar and other app bars the working area available to your application , use the [**GetMonitorInfo**](/windows/desktop/api/winuser/nf-winuser-getmonitorinfoa) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="26d08-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="26d08-116">Requirements</span></span>



| <span data-ttu-id="26d08-117">需求</span><span class="sxs-lookup"><span data-stu-id="26d08-117">Requirement</span></span> | <span data-ttu-id="26d08-118">值</span><span class="sxs-lookup"><span data-stu-id="26d08-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26d08-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="26d08-119">Minimum supported client</span></span><br/> | <span data-ttu-id="26d08-120">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26d08-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="26d08-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="26d08-121">Minimum supported server</span></span><br/> | <span data-ttu-id="26d08-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="26d08-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26d08-123">標頭</span><span class="sxs-lookup"><span data-stu-id="26d08-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="26d08-124"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="26d08-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

