---
description: CPL_NEWINQUIRE 訊息傳送至主控台應用程式的 CPlApplet 函式，以要求應用程式所支援之對話方塊的相關資訊。
title: 'CPL_NEWINQUIRE 訊息 (Cpl. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: af52889c-7180-4690-8ed1-a0eb0a9dff35
api_name:
- CPL_NEWINQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 90c5adf31c01fbab1b62aafd0714d165092f4e23
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104436"
---
# <a name="cpl_newinquire-message"></a><span data-ttu-id="67cc4-103">CPL \_ NEWINQUIRE 訊息</span><span class="sxs-lookup"><span data-stu-id="67cc4-103">CPL\_NEWINQUIRE message</span></span>

<span data-ttu-id="67cc4-104">傳送至主控台應用程式的 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式，以要求應用程式所支援之對話方塊的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="67cc4-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="67cc4-105">參數</span><span class="sxs-lookup"><span data-stu-id="67cc4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67cc4-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="67cc4-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="67cc4-107">對話方塊編號。</span><span class="sxs-lookup"><span data-stu-id="67cc4-107">The dialog box number.</span></span> <span data-ttu-id="67cc4-108">此數位必須在0到1的範圍內，小於 (GETCOUNT 的值，以回應 [**cpl \_**](cpl-getcount.md) \_ GETCOUNT – 1) 。</span><span class="sxs-lookup"><span data-stu-id="67cc4-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="67cc4-109">*lpncpli*</span><span class="sxs-lookup"><span data-stu-id="67cc4-109">*lpncpli*</span></span> 
</dt> <dd>

<span data-ttu-id="67cc4-110">[**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa)結構的位址。</span><span class="sxs-lookup"><span data-stu-id="67cc4-110">The address of a [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) structure.</span></span> <span data-ttu-id="67cc4-111">主控台應用程式應該以對話方塊的相關資訊來填滿此結構。</span><span class="sxs-lookup"><span data-stu-id="67cc4-111">The Control Panel application should fill this structure with information about the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67cc4-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="67cc4-112">Return value</span></span>

<span data-ttu-id="67cc4-113">如果 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式成功處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="67cc4-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="67cc4-114">備註</span><span class="sxs-lookup"><span data-stu-id="67cc4-114">Remarks</span></span>

<span data-ttu-id="67cc4-115">為了獲得更好的效能，大部分的應用程式應忽略 **cpl \_ NEWINQUIRE** ，並改為處理 [**cpl \_ 查詢**](cpl-inquire.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="67cc4-115">For better performance, most applications should ignore **CPL\_NEWINQUIRE** and process the [**CPL\_INQUIRE**](cpl-inquire.md) message instead.</span></span>

<span data-ttu-id="67cc4-116">主控台會針對您的應用程式所支援的每個對話方塊傳送 **CPL \_ NEWINQUIRE** 訊息一次。</span><span class="sxs-lookup"><span data-stu-id="67cc4-116">The Control Panel sends the **CPL\_NEWINQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="67cc4-117">主控台也會為每個對話方塊傳送 [**CPL \_ 查詢**](cpl-inquire.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="67cc4-117">The Control Panel also sends a [**CPL\_INQUIRE**](cpl-inquire.md) message for each dialog box.</span></span> <span data-ttu-id="67cc4-118">這些訊息會緊接在 [**CPL \_ GETCOUNT**](cpl-getcount.md) 訊息之後傳送。</span><span class="sxs-lookup"><span data-stu-id="67cc4-118">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="67cc4-119">不過，系統不保證會傳送 **cpl \_ 查詢** 和 **cpl \_ NEWINQUIRE** 訊息的順序。</span><span class="sxs-lookup"><span data-stu-id="67cc4-119">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="67cc4-120">您可以在收到 [**CPL \_ 查詢**](cpl-inquire.md)時執行對話方塊的初始化。</span><span class="sxs-lookup"><span data-stu-id="67cc4-120">You can perform initialization for the dialog box when you receive [**CPL\_INQUIRE**](cpl-inquire.md).</span></span> <span data-ttu-id="67cc4-121">如果您必須配置記憶體，請這麼做以回應 [**CPL \_ INIT**](cpl-init.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="67cc4-121">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="67cc4-122">[**CPL \_INQUIRE**](cpl-inquire.md) 是慣用的訊息。</span><span class="sxs-lookup"><span data-stu-id="67cc4-122">[**CPL\_INQUIRE**](cpl-inquire.md) is the preferred message.</span></span> <span data-ttu-id="67cc4-123">這是因為 **CPL \_ NEWINQUIRE** 會以系統無法快取的形式傳回信息。</span><span class="sxs-lookup"><span data-stu-id="67cc4-123">This is because **CPL\_NEWINQUIRE** returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="67cc4-124">因此，每次主控台需要資訊時，都必須載入處理 **CPL \_ NEWINQUIRE** 的應用程式，從而大幅降低效能。</span><span class="sxs-lookup"><span data-stu-id="67cc4-124">Consequently, applications that process **CPL\_NEWINQUIRE** must be loaded each time the Control Panel needs the information, resulting in a significant reduction in performance.</span></span>

<span data-ttu-id="67cc4-125">唯一應該使用 **CPL \_ NEWINQUIRE** 的應用程式，是需要變更其圖示或根據電腦狀態顯示字串的應用程式。</span><span class="sxs-lookup"><span data-stu-id="67cc4-125">The only applications that should use **CPL\_NEWINQUIRE** are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="67cc4-126">在此情況下，您的 [**cpl \_ 查詢**](cpl-inquire.md)處理常式應該 \_ \_ 為 [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)結構的 **idIcon**、 **idName** 或 **idInfo** 成員指定 CPL 動態 RES 值，而不是指定有效的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="67cc4-126">In this case, your [**CPL\_INQUIRE**](cpl-inquire.md) handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="67cc4-127">這會導致主控台在每次需要圖示和顯示字串時傳送 **CPL \_ NEWINQUIRE** 訊息，讓您根據電腦目前的狀態指定資訊。</span><span class="sxs-lookup"><span data-stu-id="67cc4-127">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="67cc4-128">當然，這比使用快取的資訊來得慢很多。</span><span class="sxs-lookup"><span data-stu-id="67cc4-128">Of course, this is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="67cc4-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="67cc4-129">Requirements</span></span>



| <span data-ttu-id="67cc4-130">需求</span><span class="sxs-lookup"><span data-stu-id="67cc4-130">Requirement</span></span> | <span data-ttu-id="67cc4-131">值</span><span class="sxs-lookup"><span data-stu-id="67cc4-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="67cc4-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67cc4-132">Minimum supported client</span></span><br/> | <span data-ttu-id="67cc4-133">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67cc4-133">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="67cc4-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67cc4-134">Minimum supported server</span></span><br/> | <span data-ttu-id="67cc4-135">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67cc4-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="67cc4-136">標頭</span><span class="sxs-lookup"><span data-stu-id="67cc4-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="67cc4-137"><dt>Cpl。h</dt></span><span class="sxs-lookup"><span data-stu-id="67cc4-137"><dt>Cpl.h</dt></span></span> </dl> |



 

 
