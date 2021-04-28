---
description: CPL_INQUIRE 訊息傳送至主控台應用程式的 CPlApplet 函式，以要求應用程式所支援之對話方塊的相關資訊。
title: 'CPL_INQUIRE 訊息 (Cpl. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: daca87b7-f1ee-40f4-95d2-3150b595151e
api_name:
- CPL_INQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f9962ff94e8bf80041d7b61ecf97220d573131fb
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108104466"
---
# <a name="cpl_inquire-message"></a><span data-ttu-id="10420-103">CPL \_ 查詢訊息</span><span class="sxs-lookup"><span data-stu-id="10420-103">CPL\_INQUIRE message</span></span>

<span data-ttu-id="10420-104">傳送至主控台應用程式的 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式，以要求應用程式所支援之對話方塊的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="10420-104">Sent to the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function of a Control Panel application to request information about a dialog box that the application supports.</span></span>

## <a name="parameters"></a><span data-ttu-id="10420-105">參數</span><span class="sxs-lookup"><span data-stu-id="10420-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10420-106">*uAppNum*</span><span class="sxs-lookup"><span data-stu-id="10420-106">*uAppNum*</span></span> 
</dt> <dd>

<span data-ttu-id="10420-107">對話方塊編號。</span><span class="sxs-lookup"><span data-stu-id="10420-107">The dialog box number.</span></span> <span data-ttu-id="10420-108">此數位必須在0到1的範圍內，小於 (GETCOUNT 的值，以回應 [**cpl \_**](cpl-getcount.md) \_ GETCOUNT – 1) 。</span><span class="sxs-lookup"><span data-stu-id="10420-108">This number must be in the range zero through one less than the value returned in response to the [**CPL\_GETCOUNT**](cpl-getcount.md) message (CPL\_GETCOUNT – 1).</span></span>

</dd> <dt>

<span data-ttu-id="10420-109">*lpcpli*</span><span class="sxs-lookup"><span data-stu-id="10420-109">*lpcpli*</span></span> 
</dt> <dd>

<span data-ttu-id="10420-110">[**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)結構的位址。</span><span class="sxs-lookup"><span data-stu-id="10420-110">The address of a [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure.</span></span> <span data-ttu-id="10420-111">應用程式必須在此結構中填入圖示的資源識別碼、簡短名稱、描述，以及與對話方塊相關聯的任何使用者定義值。</span><span class="sxs-lookup"><span data-stu-id="10420-111">The application must fill this structure with resource identifiers for the icon, short name, description, and any user-defined value associated with the dialog box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10420-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="10420-112">Return value</span></span>

<span data-ttu-id="10420-113">如果 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式成功處理此訊息，則應該傳回零。</span><span class="sxs-lookup"><span data-stu-id="10420-113">If the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function processes this message successfully, it should return zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="10420-114">備註</span><span class="sxs-lookup"><span data-stu-id="10420-114">Remarks</span></span>

<span data-ttu-id="10420-115">主控台針對您的應用程式所支援的每個對話方塊傳送 **CPL \_ 查詢** 訊息一次。</span><span class="sxs-lookup"><span data-stu-id="10420-115">The Control Panel sends the **CPL\_INQUIRE** message once for each dialog box supported by your application.</span></span> <span data-ttu-id="10420-116">主控台也會為每個對話方塊傳送 [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="10420-116">The Control Panel also sends a [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message for each dialog box.</span></span> <span data-ttu-id="10420-117">這些訊息會緊接在 [**CPL \_ GETCOUNT**](cpl-getcount.md) 訊息之後傳送。</span><span class="sxs-lookup"><span data-stu-id="10420-117">These messages are sent immediately after the [**CPL\_GETCOUNT**](cpl-getcount.md) message.</span></span> <span data-ttu-id="10420-118">不過，系統不保證會傳送 **cpl \_ 查詢** 和 **cpl \_ NEWINQUIRE** 訊息的順序。</span><span class="sxs-lookup"><span data-stu-id="10420-118">However, the system does not guarantee the order in which the **CPL\_INQUIRE** and **CPL\_NEWINQUIRE** messages are sent.</span></span>

<span data-ttu-id="10420-119">您可以在收到 **CPL \_ 查詢** 時執行對話方塊的初始化。</span><span class="sxs-lookup"><span data-stu-id="10420-119">You can perform initialization for the dialog box when you receive **CPL\_INQUIRE**.</span></span> <span data-ttu-id="10420-120">如果您必須配置記憶體，請這麼做以回應 [**CPL \_ INIT**](cpl-init.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="10420-120">If you must allocate memory, do so in response to the [**CPL\_INIT**](cpl-init.md) message.</span></span>

<span data-ttu-id="10420-121">[**CPL \_ NEWINQUIRE**](cpl-newinquire.md)訊息會以系統無法快取的形式傳回信息。</span><span class="sxs-lookup"><span data-stu-id="10420-121">The [**CPL\_NEWINQUIRE**](cpl-newinquire.md) message returns information in a form that the system cannot cache.</span></span> <span data-ttu-id="10420-122">基於這個理由，大部分的 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式都應該處理 **cpl \_ 查詢** 並忽略 **CPL \_ NEWINQUIRE**。</span><span class="sxs-lookup"><span data-stu-id="10420-122">For this reason, most [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) functions should process **CPL\_INQUIRE** and ignore **CPL\_NEWINQUIRE**.</span></span>

<span data-ttu-id="10420-123">唯一應該使用 [**CPL \_ NEWINQUIRE**](cpl-newinquire.md) 的應用程式，是需要變更其圖示或根據電腦狀態顯示字串的應用程式。</span><span class="sxs-lookup"><span data-stu-id="10420-123">The only applications that should use [**CPL\_NEWINQUIRE**](cpl-newinquire.md) are those that need to change their icon or display strings based on the state of the computer.</span></span> <span data-ttu-id="10420-124">在此情況下，您的 **cpl \_ 查詢** 處理常式應該 \_ \_ 為 [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo)結構的 **idIcon**、 **idName** 或 **idInfo** 成員指定 CPL 動態 RES 值，而不是指定有效的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="10420-124">In this case, your **CPL\_INQUIRE** handler should specify the CPL\_DYNAMIC\_RES value for the **idIcon**, **idName**, or **idInfo** members of the [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) structure, rather than specifying a valid resource identifier.</span></span> <span data-ttu-id="10420-125">這會導致主控台在每次需要圖示和顯示字串時傳送 **CPL \_ NEWINQUIRE** 訊息，讓您根據電腦目前的狀態指定資訊。</span><span class="sxs-lookup"><span data-stu-id="10420-125">This causes the Control Panel to send the **CPL\_NEWINQUIRE** message each time it needs the icon and display strings, allowing you to specify information based on the current state of the computer.</span></span> <span data-ttu-id="10420-126">這比使用快取的資訊來得慢很多。</span><span class="sxs-lookup"><span data-stu-id="10420-126">This is significantly slower than using cached information.</span></span>

## <a name="requirements"></a><span data-ttu-id="10420-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="10420-127">Requirements</span></span>



| <span data-ttu-id="10420-128">需求</span><span class="sxs-lookup"><span data-stu-id="10420-128">Requirement</span></span> | <span data-ttu-id="10420-129">值</span><span class="sxs-lookup"><span data-stu-id="10420-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="10420-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10420-130">Minimum supported client</span></span><br/> | <span data-ttu-id="10420-131">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10420-131">Windows XP \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="10420-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10420-132">Minimum supported server</span></span><br/> | <span data-ttu-id="10420-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10420-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="10420-134">標頭</span><span class="sxs-lookup"><span data-stu-id="10420-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="10420-135"><dt>Cpl。h</dt></span><span class="sxs-lookup"><span data-stu-id="10420-135"><dt>Cpl.h</dt></span></span> </dl> |



 

 
