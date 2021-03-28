---
description: 當控制主控台的應用程式關閉時，傳送至主控台應用程式的 CPlApplet 函式。 控制應用程式會針對應用程式支援的每個對話方塊傳送一次訊息。
title: 'CPL_STOP 訊息 (Cpl. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 4f632b91-8200-42a3-90cc-a98889704ca4
api_name:
- CPL_STOP
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 78f8926d85b35b8cf5e55188c6cd76b014b3c4c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972041"
---
# <a name="cpl_stop-message"></a><span data-ttu-id="79531-104">CPL \_ 停止訊息</span><span class="sxs-lookup"><span data-stu-id="79531-104">CPL\_STOP message</span></span>

<span data-ttu-id="79531-105">當控制主控台的應用程式關閉時，傳送至主控台應用程式的 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式。</span><span class="sxs-lookup"><span data-stu-id="79531-105">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application when the controlling application of the Control Panel closes.</span></span> <span data-ttu-id="79531-106">控制應用程式會針對應用程式支援的每個對話方塊傳送一次訊息。</span><span class="sxs-lookup"><span data-stu-id="79531-106">The controlling application sends the message once for each dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="79531-107">參數</span><span class="sxs-lookup"><span data-stu-id="79531-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79531-108">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="79531-108">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="79531-109">對話方塊編號。</span><span class="sxs-lookup"><span data-stu-id="79531-109">The dialog box number.</span></span>

</dd> <dt>

<span data-ttu-id="79531-110">*lData*</span><span class="sxs-lookup"><span data-stu-id="79531-110">*lData*</span></span> 
</dt> <dd>

<span data-ttu-id="79531-111">主控台應用程式載入至對話方塊之 [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)或 [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa)結構的 **lpData** 成員的值。</span><span class="sxs-lookup"><span data-stu-id="79531-111">The value that the Control Panel application loaded into the **lpData** member of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) or [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure for the dialog box.</span></span> <span data-ttu-id="79531-112">應用程式會載入 **lpData** 成員，以回應 [**CPL \_ INQUIRE**](cpl-inquire.md) 或 [**cpl \_ NEWINQUIRE**](cpl-newinquire.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="79531-112">The application loads the **lpData** member in response to the [**CPL\_INQUIRE**](cpl-inquire.md) or [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79531-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="79531-113">Return value</span></span>

<span data-ttu-id="79531-114">如果 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式成功處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="79531-114">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="79531-115">備註</span><span class="sxs-lookup"><span data-stu-id="79531-115">Remarks</span></span>

<span data-ttu-id="79531-116">為了回應這則訊息，主控台的應用程式必須在指定的對話方塊中執行清除。</span><span class="sxs-lookup"><span data-stu-id="79531-116">In response to this message, a Control Panel application must perform cleanup for the given dialog box.</span></span>

## <a name="requirements"></a><span data-ttu-id="79531-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="79531-117">Requirements</span></span>



| <span data-ttu-id="79531-118">需求</span><span class="sxs-lookup"><span data-stu-id="79531-118">Requirement</span></span> | <span data-ttu-id="79531-119">值</span><span class="sxs-lookup"><span data-stu-id="79531-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="79531-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="79531-120">Minimum supported client</span></span><br/> | <span data-ttu-id="79531-121">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79531-121">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="79531-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="79531-122">Minimum supported server</span></span><br/> | <span data-ttu-id="79531-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="79531-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="79531-124">標頭</span><span class="sxs-lookup"><span data-stu-id="79531-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="79531-125"><dt>Cpl。h</dt></span><span class="sxs-lookup"><span data-stu-id="79531-125"><dt>Cpl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79531-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="79531-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79531-127">**CPL \_ 結束**</span><span class="sxs-lookup"><span data-stu-id="79531-127">**CPL\_EXIT**</span></span>](cpl-exit.md)
</dt> <dt>

[<span data-ttu-id="79531-128">**CPL \_ GETCOUNT**</span><span class="sxs-lookup"><span data-stu-id="79531-128">**CPL\_GETCOUNT**</span></span>](cpl-getcount.md)
</dt> </dl>

 

 
