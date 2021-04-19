---
description: 用來指出已知資料行識別碼的列舉;這些都是所有執行都應該支援的資料行識別碼。
MS-HAID: vspixengine.EVENTCOLUMNID
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: EVENTCOLUMNID 列舉
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 908CC94B-DD06-4FEC-9DC8-B61D03D34F6E
api_name:
- EVENTCOLUMNID
api_type:
- HeaderDef
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7bf01eda2c43df3f0ec9553f61341406c541cac9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106966608"
---
# <a name="span-idvspixengineeventcolumnidspaneventcolumnid-enumeration"></a><span data-ttu-id="0e0fa-103"><span id="vspixengine.eventcolumnid"></span>EVENTCOLUMNID 列舉</span><span class="sxs-lookup"><span data-stu-id="0e0fa-103"><span id="vspixengine.eventcolumnid"></span>EVENTCOLUMNID enumeration</span></span>

<span data-ttu-id="0e0fa-104">用來指出已知資料行識別碼的列舉;這些都是所有執行都應該支援的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e0fa-104">An enum used to indicate well-known column IDs; these are column IDs that all implementations should support.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e0fa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e0fa-105">Syntax</span></span>


```C++
};
```

## <a name="constants"></a><span data-ttu-id="0e0fa-106">常數</span><span class="sxs-lookup"><span data-stu-id="0e0fa-106">Constants</span></span>

<span data-ttu-id="0e0fa-107"><span id="EventColumnID_EVENTTYPE"></span><span id="eventcolumnid_eventtype"></span><span id="EVENTCOLUMNID_EVENTTYPE"></span>**EventColumnID 的 \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="0e0fa-107"><span id="EventColumnID_EVENTTYPE"></span><span id="eventcolumnid_eventtype"></span><span id="EVENTCOLUMNID_EVENTTYPE"></span>**EventColumnID\_EVENTTYPE**</span></span>  
<span data-ttu-id="0e0fa-108">對應到事件種類資料行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e0fa-108">An ID that corresponds to the Event Type column.</span></span>

<span data-ttu-id="0e0fa-109"><span id="EventColumnID_EID"></span><span id="eventcolumnid_eid"></span><span id="EVENTCOLUMNID_EID"></span>**EventColumnID \_ EID**</span><span class="sxs-lookup"><span data-stu-id="0e0fa-109"><span id="EventColumnID_EID"></span><span id="eventcolumnid_eid"></span><span id="EVENTCOLUMNID_EID"></span>**EventColumnID\_EID**</span></span>  
<span data-ttu-id="0e0fa-110">對應至事件識別碼資料行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e0fa-110">An ID that corresponds to the Event ID column.</span></span>

<span data-ttu-id="0e0fa-111"><span id="EventColumnID_PARENTEID"></span><span id="eventcolumnid_parenteid"></span><span id="EVENTCOLUMNID_PARENTEID"></span>**EventColumnID \_ PARENTEID**</span><span class="sxs-lookup"><span data-stu-id="0e0fa-111"><span id="EventColumnID_PARENTEID"></span><span id="eventcolumnid_parenteid"></span><span id="EVENTCOLUMNID_PARENTEID"></span>**EventColumnID\_PARENTEID**</span></span>  
<span data-ttu-id="0e0fa-112">對應至父事件識別碼資料行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e0fa-112">An ID that corresponds to the Parent Event ID column.</span></span>

<span data-ttu-id="0e0fa-113"><span id="EventColumnID_EVENTNAME"></span><span id="eventcolumnid_eventname"></span><span id="EVENTCOLUMNID_EVENTNAME"></span>**EventColumnID \_ 事件名稱**</span><span class="sxs-lookup"><span data-stu-id="0e0fa-113"><span id="EventColumnID_EVENTNAME"></span><span id="eventcolumnid_eventname"></span><span id="EVENTCOLUMNID_EVENTNAME"></span>**EventColumnID\_EVENTNAME**</span></span>  
<span data-ttu-id="0e0fa-114">對應至事件名稱資料行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e0fa-114">An ID that corresponds to the Event Name column.</span></span>

<span data-ttu-id="0e0fa-115"><span id="EventColumnID_FRAME"></span><span id="eventcolumnid_frame"></span><span id="EVENTCOLUMNID_FRAME"></span>**EventColumnID \_ 框架**</span><span class="sxs-lookup"><span data-stu-id="0e0fa-115"><span id="EventColumnID_FRAME"></span><span id="eventcolumnid_frame"></span><span id="EVENTCOLUMNID_FRAME"></span>**EventColumnID\_FRAME**</span></span>  
<span data-ttu-id="0e0fa-116">對應至框架資料行的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e0fa-116">An ID that corresponds to the Frame column.</span></span>

<span data-ttu-id="0e0fa-117"><span id="EventColumnID_EVENTSTRING"></span><span id="eventcolumnid_eventstring"></span><span id="EVENTCOLUMNID_EVENTSTRING"></span>**EventColumnID \_ EVENTSTRING**</span><span class="sxs-lookup"><span data-stu-id="0e0fa-117"><span id="EventColumnID_EVENTSTRING"></span><span id="eventcolumnid_eventstring"></span><span id="EVENTCOLUMNID_EVENTSTRING"></span>**EventColumnID\_EVENTSTRING**</span></span>  
<span data-ttu-id="0e0fa-118">識別碼，對應至要針對事件剖析的完整字串。</span><span class="sxs-lookup"><span data-stu-id="0e0fa-118">An ID that corresponds to the full string to be parsed for the event.</span></span>

<span data-ttu-id="0e0fa-119"><span id="EventColumnID_THISPTR"></span><span id="eventcolumnid_thisptr"></span><span id="EVENTCOLUMNID_THISPTR"></span>**EventColumnID \_ THISPTR**</span><span class="sxs-lookup"><span data-stu-id="0e0fa-119"><span id="EventColumnID_THISPTR"></span><span id="eventcolumnid_thisptr"></span><span id="EVENTCOLUMNID_THISPTR"></span>**EventColumnID\_THISPTR**</span></span>  
<span data-ttu-id="0e0fa-120">對應至這個指標之資源控制碼的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e0fa-120">An ID that corresponds to the resource handle for the this pointer.</span></span>

<span data-ttu-id="0e0fa-121"><span id="EventColumnID_STARTMOMENTHANDLE"></span><span id="eventcolumnid_startmomenthandle"></span><span id="EVENTCOLUMNID_STARTMOMENTHANDLE"></span>**EventColumnID \_ STARTMOMENTHANDLE**</span><span class="sxs-lookup"><span data-stu-id="0e0fa-121"><span id="EventColumnID_STARTMOMENTHANDLE"></span><span id="eventcolumnid_startmomenthandle"></span><span id="EVENTCOLUMNID_STARTMOMENTHANDLE"></span>**EventColumnID\_STARTMOMENTHANDLE**</span></span>  
<span data-ttu-id="0e0fa-122">對應到這個事件之時間控制碼的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e0fa-122">An ID that corresponds to the moment handle for this event.</span></span>

<span data-ttu-id="0e0fa-123"><span id="EventColumnID_InfoQueueMessages"></span><span id="eventcolumnid_infoqueuemessages"></span><span id="EVENTCOLUMNID_INFOQUEUEMESSAGES"></span>**EventColumnID \_ InfoQueueMessages**</span><span class="sxs-lookup"><span data-stu-id="0e0fa-123"><span id="EventColumnID_InfoQueueMessages"></span><span id="eventcolumnid_infoqueuemessages"></span><span id="EVENTCOLUMNID_INFOQUEUEMESSAGES"></span>**EventColumnID\_InfoQueueMessages**</span></span>  
<span data-ttu-id="0e0fa-124">對應至在 SDK 層中產生之任何訊息的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e0fa-124">An ID that corresponds to any message that this generated in the SDK layers.</span></span>

<span data-ttu-id="0e0fa-125"><span id="EventColumnID_ThreadId"></span><span id="eventcolumnid_threadid"></span><span id="EVENTCOLUMNID_THREADID"></span>**EventColumnID \_ ThreadId**</span><span class="sxs-lookup"><span data-stu-id="0e0fa-125"><span id="EventColumnID_ThreadId"></span><span id="eventcolumnid_threadid"></span><span id="EVENTCOLUMNID_THREADID"></span>**EventColumnID\_ThreadId**</span></span>  
<span data-ttu-id="0e0fa-126">對應至執行緒識別碼的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0e0fa-126">An ID that corresponds to the Thread ID.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e0fa-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="0e0fa-127">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="0e0fa-128">標頭</span><span class="sxs-lookup"><span data-stu-id="0e0fa-128">Header</span></span></p></td><td><span data-ttu-id="0e0fa-129">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="0e0fa-129">Vspixengine.h</span></span></td></tr></tbody></table>

 

 



