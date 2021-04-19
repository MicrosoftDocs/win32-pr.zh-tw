---
description: LINECALLHUBTRACKING \_ 位旗標常數描述所提供的呼叫中樞追蹤類型。
ms.assetid: ad3c8d2e-f074-4db0-bb72-fb2181cbf687
title: 'LINECALLHUBTRACKING_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bfae61e36551a7d186408c2c87e0727503540a5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992172"
---
# <a name="linecallhubtracking_-constants"></a><span data-ttu-id="48d4a-103">LINECALLHUBTRACKING \_ 常數</span><span class="sxs-lookup"><span data-stu-id="48d4a-103">LINECALLHUBTRACKING\_ Constants</span></span>

<span data-ttu-id="48d4a-104">**LINECALLHUBTRACKING \_** 位旗標常數描述所提供的呼叫中樞追蹤類型。</span><span class="sxs-lookup"><span data-stu-id="48d4a-104">The **LINECALLHUBTRACKING\_** bit-flag constants describe the type of call hub tracking provided.</span></span>

<dl> <dt>

<span data-ttu-id="48d4a-105"><span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**LINECALLHUBTRACKING \_ ALLCALLS**</span><span class="sxs-lookup"><span data-stu-id="48d4a-105"><span id="LINECALLHUBTRACKING_ALLCALLS"></span><span id="linecallhubtracking_allcalls"></span>**LINECALLHUBTRACKING\_ALLCALLS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48d4a-106">呼叫層級會在呼叫層級提供呼叫中樞追蹤。</span><span class="sxs-lookup"><span data-stu-id="48d4a-106">Call hub tracking is provided at the call level.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48d4a-107"><span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING \_ 無**</span><span class="sxs-lookup"><span data-stu-id="48d4a-107"><span id="LINECALLHUBTRACKING_NONE"></span><span id="linecallhubtracking_none"></span>**LINECALLHUBTRACKING\_NONE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48d4a-108">未提供任何呼叫中樞追蹤。</span><span class="sxs-lookup"><span data-stu-id="48d4a-108">No call hub tracking is provided.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="48d4a-109"><span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**LINECALLHUBTRACKING \_ PROVIDERLEVEL**</span><span class="sxs-lookup"><span data-stu-id="48d4a-109"><span id="LINECALLHUBTRACKING_PROVIDERLEVEL"></span><span id="linecallhubtracking_providerlevel"></span>**LINECALLHUBTRACKING\_PROVIDERLEVEL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="48d4a-110">呼叫中樞是在服務提供者層級進行追蹤。</span><span class="sxs-lookup"><span data-stu-id="48d4a-110">Call hubs are tracked at the service provider level.</span></span> <span data-ttu-id="48d4a-111">不會報告依通話變更的呼叫。</span><span class="sxs-lookup"><span data-stu-id="48d4a-111">Call by call changes are not reported.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="48d4a-112">備註</span><span class="sxs-lookup"><span data-stu-id="48d4a-112">Remarks</span></span>

<span data-ttu-id="48d4a-113">無延伸。</span><span class="sxs-lookup"><span data-stu-id="48d4a-113">No extensibility.</span></span> <span data-ttu-id="48d4a-114">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="48d4a-114">All 32 bits are reserved.</span></span>

<span data-ttu-id="48d4a-115">當此資料結構中發生變更時，會將 [**行 \_ CALLINFO**](line-callinfo.md) 訊息傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="48d4a-115">When changes occur in this data structure, a [**LINE\_CALLINFO**](line-callinfo.md) message is sent to the application.</span></span> <span data-ttu-id="48d4a-116">此訊息的參數是呼叫的控制碼，以及已變更之資訊專案的指示。</span><span class="sxs-lookup"><span data-stu-id="48d4a-116">The parameters to this message are a handle to the call and an indication of the information item that has changed.</span></span> <span data-ttu-id="48d4a-117">[**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)資料結構會指出所提供的追蹤類型。</span><span class="sxs-lookup"><span data-stu-id="48d4a-117">The [**LINECALLHUBTRACKINGINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo) data structure indicates which tracking type is provided.</span></span>

## <a name="requirements"></a><span data-ttu-id="48d4a-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="48d4a-118">Requirements</span></span>



| <span data-ttu-id="48d4a-119">需求</span><span class="sxs-lookup"><span data-stu-id="48d4a-119">Requirement</span></span> | <span data-ttu-id="48d4a-120">值</span><span class="sxs-lookup"><span data-stu-id="48d4a-120">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="48d4a-121">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="48d4a-121">TAPI version</span></span><br/> | <span data-ttu-id="48d4a-122">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="48d4a-122">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="48d4a-123">標頭</span><span class="sxs-lookup"><span data-stu-id="48d4a-123">Header</span></span><br/>       | <dl> <span data-ttu-id="48d4a-124"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="48d4a-124"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48d4a-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48d4a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48d4a-126">**行 \_ CALLINFO**</span><span class="sxs-lookup"><span data-stu-id="48d4a-126">**LINE\_CALLINFO**</span></span>](line-callinfo.md)
</dt> <dt>

[<span data-ttu-id="48d4a-127">**LINECALLHUBTRACKINGINFO**</span><span class="sxs-lookup"><span data-stu-id="48d4a-127">**LINECALLHUBTRACKINGINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallhubtrackinginfo)
</dt> <dt>

[<span data-ttu-id="48d4a-128">**LINECALLINFO**</span><span class="sxs-lookup"><span data-stu-id="48d4a-128">**LINECALLINFO**</span></span>](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)
</dt> </dl>

 

 




