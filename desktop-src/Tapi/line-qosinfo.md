---
description: TSPI LINE \_ QOSINFO message 會導致 TAPI 引發 QOS 事件。 如需其他資訊，請參閱 ITQOSEvent。
ms.assetid: b2844d12-c524-42ab-aeb9-8daf4e07a436
title: 'LINE_QOSINFO 訊息 (Tspi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d35ff19601ab6acd9a3d8e8aebf1e59b06a4f17e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995771"
---
# <a name="line_qosinfo-message"></a><span data-ttu-id="e3fb5-104">行 \_ QOSINFO 訊息</span><span class="sxs-lookup"><span data-stu-id="e3fb5-104">LINE\_QOSINFO message</span></span>

<span data-ttu-id="e3fb5-105">TSPI **LINE \_ QOSINFO** MESSAGE 會導致 TAPI 引發 QOS 事件。</span><span class="sxs-lookup"><span data-stu-id="e3fb5-105">The TSPI **LINE\_QOSINFO** message causes TAPI to fire a QOS event.</span></span> <span data-ttu-id="e3fb5-106">如需其他資訊，請參閱 [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) 。</span><span class="sxs-lookup"><span data-stu-id="e3fb5-106">See [**ITQOSEvent**](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent) for additional information.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="e3fb5-107">參數</span><span class="sxs-lookup"><span data-stu-id="e3fb5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e3fb5-108">*htLine*</span><span class="sxs-lookup"><span data-stu-id="e3fb5-108">*htLine*</span></span> 
</dt> <dd>

<span data-ttu-id="e3fb5-109">線路的 TAPI 控制碼。</span><span class="sxs-lookup"><span data-stu-id="e3fb5-109">The TAPI handle for the line.</span></span>

</dd> <dt>

<span data-ttu-id="e3fb5-110">*htCall*</span><span class="sxs-lookup"><span data-stu-id="e3fb5-110">*htCall*</span></span> 
</dt> <dd>

<span data-ttu-id="e3fb5-111">呼叫的 TAPI 控制碼。</span><span class="sxs-lookup"><span data-stu-id="e3fb5-111">The TAPI handle for the call.</span></span>

</dd> <dt>

<span data-ttu-id="e3fb5-112">*dwMsg*</span><span class="sxs-lookup"><span data-stu-id="e3fb5-112">*dwMsg*</span></span> 
</dt> <dd>

<span data-ttu-id="e3fb5-113">值行 \_ QOSINFO。</span><span class="sxs-lookup"><span data-stu-id="e3fb5-113">The value LINE\_QOSINFO.</span></span>

</dd> <dt>

<span data-ttu-id="e3fb5-114">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="e3fb5-114">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="e3fb5-115">[**QOS \_ 事件**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)列舉值的成員，可識別事件的類型。</span><span class="sxs-lookup"><span data-stu-id="e3fb5-115">A member of the [**QOS\_EVENT**](/windows/win32/api/tapi3if/ne-tapi3if-qos_event) enumerator that identifies the type of event.</span></span>

</dd> <dt>

<span data-ttu-id="e3fb5-116">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="e3fb5-116">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="e3fb5-117">用來識別與這個事件相關聯之呼叫媒體的 [媒體類型](./tapiprotocol--constants.md) 常數。</span><span class="sxs-lookup"><span data-stu-id="e3fb5-117">A [media type](./tapiprotocol--constants.md) constant that identifies the media of the call associated with this event.</span></span>

</dd> <dt>

<span data-ttu-id="e3fb5-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="e3fb5-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="e3fb5-119">未使用的。</span><span class="sxs-lookup"><span data-stu-id="e3fb5-119">Unused.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e3fb5-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="e3fb5-120">Requirements</span></span>



| <span data-ttu-id="e3fb5-121">需求</span><span class="sxs-lookup"><span data-stu-id="e3fb5-121">Requirement</span></span> | <span data-ttu-id="e3fb5-122">值</span><span class="sxs-lookup"><span data-stu-id="e3fb5-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="e3fb5-123">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="e3fb5-123">TAPI version</span></span><br/> | <span data-ttu-id="e3fb5-124">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="e3fb5-124">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="e3fb5-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e3fb5-125">Header</span></span><br/>       | <dl> <span data-ttu-id="e3fb5-126"><dt>Tspi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e3fb5-126"><dt>Tspi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3fb5-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3fb5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3fb5-128">**QOS \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="e3fb5-128">**QOS\_EVENT**</span></span>](/windows/win32/api/tapi3if/ne-tapi3if-qos_event)
</dt> <dt>

[<span data-ttu-id="e3fb5-129">**ITQOSEvent**</span><span class="sxs-lookup"><span data-stu-id="e3fb5-129">**ITQOSEvent**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itqosevent)
</dt> </dl>

 

