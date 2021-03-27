---
description: 傳送以通知 CPlApplet，使用者已選擇與指定對話方塊相關聯的圖示。 CPlApplet 應該會顯示對應的對話方塊，並執行任何使用者指定的工作。
title: 'CPL_STARTWPARMS 訊息 (Cpl. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 04ac5117-39c9-4d3f-b32d-8f8d2b515be1
api_name:
- CPL_STARTWPARMS
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 790779c1c45acbc211fe36e28b2e55d5ae2e60da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943267"
---
# <a name="cpl_startwparms-message"></a><span data-ttu-id="8c4f8-104">CPL \_ STARTWPARMS 訊息</span><span class="sxs-lookup"><span data-stu-id="8c4f8-104">CPL\_STARTWPARMS message</span></span>

<span data-ttu-id="8c4f8-105">傳送以通知 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) ，使用者已選擇與指定對話方塊相關聯的圖示。</span><span class="sxs-lookup"><span data-stu-id="8c4f8-105">Sent to notify [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) that the user has chosen the icon associated with a given dialog box.</span></span> <span data-ttu-id="8c4f8-106">**CPlApplet** 應該會顯示對應的對話方塊，並執行任何使用者指定的工作。</span><span class="sxs-lookup"><span data-stu-id="8c4f8-106">**CPlApplet** should display the corresponding dialog box and carry out any user-specified tasks.</span></span>

## <a name="parameters"></a><span data-ttu-id="8c4f8-107">參數</span><span class="sxs-lookup"><span data-stu-id="8c4f8-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c4f8-108">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="8c4f8-108">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="8c4f8-109">對話方塊編號。</span><span class="sxs-lookup"><span data-stu-id="8c4f8-109">The dialog box number.</span></span> <span data-ttu-id="8c4f8-110">此數位必須在0到1的範圍內，小於 (GETCOUNT 的值，以回應 [**cpl \_**](cpl-getcount.md) \_ GETCOUNT – 1) 。</span><span class="sxs-lookup"><span data-stu-id="8c4f8-110">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="8c4f8-111">*lpszExtra*</span><span class="sxs-lookup"><span data-stu-id="8c4f8-111">*lpszExtra*</span></span> 
</dt> <dd>

<span data-ttu-id="8c4f8-112">字串，包含執行的其他指示。</span><span class="sxs-lookup"><span data-stu-id="8c4f8-112">A string with additional directions for execution.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c4f8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="8c4f8-113">Return value</span></span>

<span data-ttu-id="8c4f8-114">如果已處理訊息，則傳回 **TRUE** ，否則傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="8c4f8-114">Returns **TRUE** if the message was handled, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c4f8-115">備註</span><span class="sxs-lookup"><span data-stu-id="8c4f8-115">Remarks</span></span>

<span data-ttu-id="8c4f8-116">**CPL \_STARTWPARMS** 類似于 [**CPL \_ DBLCLK**](cpl-dblclk.md) ，但可讓您將字串傳遞至 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 而不是 **int**。您可以使用此字串作為提供詳細執行指示的彈性方式。</span><span class="sxs-lookup"><span data-stu-id="8c4f8-116">**CPL\_STARTWPARMS** is similar to [**CPL\_DBLCLK**](cpl-dblclk.md) but allows you to pass a string to [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) instead of an **int**. You can use this string as a flexible way to provide detailed directions for execution.</span></span>

## <a name="requirements"></a><span data-ttu-id="8c4f8-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c4f8-117">Requirements</span></span>



| <span data-ttu-id="8c4f8-118">需求</span><span class="sxs-lookup"><span data-stu-id="8c4f8-118">Requirement</span></span> | <span data-ttu-id="8c4f8-119">值</span><span class="sxs-lookup"><span data-stu-id="8c4f8-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8c4f8-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c4f8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8c4f8-121">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c4f8-121">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="8c4f8-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c4f8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8c4f8-123">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c4f8-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8c4f8-124">標頭</span><span class="sxs-lookup"><span data-stu-id="8c4f8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="8c4f8-125"><dt>Cpl。h</dt></span><span class="sxs-lookup"><span data-stu-id="8c4f8-125"><dt>Cpl.h</dt></span></span> </dl> |



 

 
