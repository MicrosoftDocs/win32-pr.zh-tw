---
description: LINECALLSELECT \_ 位旗標常數描述要選取的呼叫。
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: 'LINECALLSELECT_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8330b4c4e4e14ac399595d10d4a208a3c67f5b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978497"
---
# <a name="linecallselect_-constants"></a><span data-ttu-id="e3165-103">LINECALLSELECT \_ 常數</span><span class="sxs-lookup"><span data-stu-id="e3165-103">LINECALLSELECT\_ Constants</span></span>

<span data-ttu-id="e3165-104">**LINECALLSELECT \_** 位旗標常數描述要選取的呼叫。</span><span class="sxs-lookup"><span data-stu-id="e3165-104">The **LINECALLSELECT\_** bit-flag constants describe which calls are to be selected.</span></span>

<dl> <dt>

<span data-ttu-id="e3165-105"><span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**LINECALLSELECT \_ 位址**</span><span class="sxs-lookup"><span data-stu-id="e3165-105"><span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**LINECALLSELECT\_ADDRESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3165-106">選取指定位址上的呼叫。</span><span class="sxs-lookup"><span data-stu-id="e3165-106">Selects call on the specified address.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3165-107"><span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**LINECALLSELECT \_ 呼叫**</span><span class="sxs-lookup"><span data-stu-id="e3165-107"><span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**LINECALLSELECT\_CALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3165-108">選取對指定之呼叫的相關呼叫。</span><span class="sxs-lookup"><span data-stu-id="e3165-108">Selects related calls to the specified call.</span></span> <span data-ttu-id="e3165-109">例如，在會議通話中的合作物件。</span><span class="sxs-lookup"><span data-stu-id="e3165-109">For example, the parties in a conference call.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3165-110"><span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**LINECALLSELECT \_ CALLID**</span><span class="sxs-lookup"><span data-stu-id="e3165-110"><span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**LINECALLSELECT\_CALLID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3165-111">選取對指定之呼叫識別碼的相關呼叫。</span><span class="sxs-lookup"><span data-stu-id="e3165-111">Selects related calls to the specified call identifier.</span></span> <span data-ttu-id="e3165-112">此旗標只會公開給協調 TAPI 3.0 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e3165-112">This flag is exposed only to applications that negotiate a TAPI version of 3.0 or higher.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3165-113"><span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT \_ DEVICEID**</span><span class="sxs-lookup"><span data-stu-id="e3165-113"><span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**LINECALLSELECT\_DEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3165-114">選取指定裝置識別碼上的呼叫。</span><span class="sxs-lookup"><span data-stu-id="e3165-114">Selects calls on the specified device identifier.</span></span> <span data-ttu-id="e3165-115">此旗標只會公開給協調 TAPI 2.1 版或更新版本的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e3165-115">This flag is exposed only to applications that negotiate a TAPI version of 2.1 or higher.</span></span> <span data-ttu-id="e3165-116">應用程式應該考慮使用 LINECALLSELECT \_ 行常數，而不是這一項。</span><span class="sxs-lookup"><span data-stu-id="e3165-116">Applications should consider using the LINECALLSELECT\_LINE constant instead of this one.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="e3165-117"><span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**LINECALLSELECT \_ 行**</span><span class="sxs-lookup"><span data-stu-id="e3165-117"><span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**LINECALLSELECT\_LINE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="e3165-118">選取指定線路裝置上的呼叫。</span><span class="sxs-lookup"><span data-stu-id="e3165-118">Selects calls on the specified line device.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e3165-119">備註</span><span class="sxs-lookup"><span data-stu-id="e3165-119">Remarks</span></span>

<span data-ttu-id="e3165-120">無延伸。</span><span class="sxs-lookup"><span data-stu-id="e3165-120">No extensibility.</span></span> <span data-ttu-id="e3165-121">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="e3165-121">All 32 bits are reserved.</span></span>

<span data-ttu-id="e3165-122">這個常數會在 [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) 中使用，並指定所要求之呼叫 (範圍) 的選取範圍。</span><span class="sxs-lookup"><span data-stu-id="e3165-122">This constant is used in [**lineGetNewCalls**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) and to specify a selection (scope) of the calls that are requested.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3165-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3165-123">Requirements</span></span>



| <span data-ttu-id="e3165-124">需求</span><span class="sxs-lookup"><span data-stu-id="e3165-124">Requirement</span></span> | <span data-ttu-id="e3165-125">值</span><span class="sxs-lookup"><span data-stu-id="e3165-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e3165-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="e3165-126">TAPI version</span></span><br/> | <span data-ttu-id="e3165-127">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="e3165-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="e3165-128">標頭</span><span class="sxs-lookup"><span data-stu-id="e3165-128">Header</span></span><br/>       | <dl> <span data-ttu-id="e3165-129"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="e3165-129"><dt>Tapi.h</dt></span></span> </dl> |



 

 




