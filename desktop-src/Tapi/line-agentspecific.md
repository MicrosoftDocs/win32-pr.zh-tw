---
description: '\_當應用程式目前已開啟的那一行上的 ACD 代理程式狀態變更時，就會傳送 TAPI 線路 AGENTSPECIFIC 訊息。 應用程式可以叫用 lineGetAgentStatus 來判斷代理程式目前的狀態。'
ms.assetid: 67e1796c-02e5-4f81-8086-7c2ff3112ae0
title: 'LINE_AGENTSPECIFIC 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20ca03138ce00f11520e2e0f1df8e810e21d1186
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996227"
---
# <a name="line_agentspecific-message"></a><span data-ttu-id="6d640-104">行 \_ AGENTSPECIFIC 訊息</span><span class="sxs-lookup"><span data-stu-id="6d640-104">LINE\_AGENTSPECIFIC message</span></span>

<span data-ttu-id="6d640-105">當應用程式目前已開啟的那一行上的 ACD 代理程式狀態變更時，就會傳送 TAPI **線路 \_ AGENTSPECIFIC** 訊息。</span><span class="sxs-lookup"><span data-stu-id="6d640-105">The TAPI **LINE\_AGENTSPECIFIC** message is sent when the status of an ACD agent changes on a line the application currently has open.</span></span> <span data-ttu-id="6d640-106">應用程式可以叫用 [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) 來判斷代理程式目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="6d640-106">The application can invoke [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) to determine the current status of the agent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="6d640-107">參數</span><span class="sxs-lookup"><span data-stu-id="6d640-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d640-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="6d640-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="6d640-109">應用程式線路裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6d640-109">The application's handle to the line device.</span></span>

</dd> <dt>

<span data-ttu-id="6d640-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="6d640-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="6d640-111">開啟呼叫的行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="6d640-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="6d640-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="6d640-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="6d640-113">與訊息相關聯之處理常式延伸模組的 [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) 結構中，處理常式延伸模組識別碼陣列的索引。</span><span class="sxs-lookup"><span data-stu-id="6d640-113">The index into the array of handler extension identifiers in the [**LINEAGENTCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps) structure of the handler extension with which the message is associated.</span></span>

</dd> <dt>

<span data-ttu-id="6d640-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="6d640-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="6d640-115">特定于處理常式延伸模組。</span><span class="sxs-lookup"><span data-stu-id="6d640-115">Specific to the handler extension.</span></span> <span data-ttu-id="6d640-116">一般來說，這個值是用來讓應用程式叫用 [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) 函式，以提取有關訊息的進一步詳細資料。</span><span class="sxs-lookup"><span data-stu-id="6d640-116">Generally, this value is used to cause the application to invoke a [**lineAgentSpecific**](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific) function to fetch further details about the message.</span></span>

</dd> <dt>

<span data-ttu-id="6d640-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="6d640-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="6d640-118">特定于處理常式延伸模組。</span><span class="sxs-lookup"><span data-stu-id="6d640-118">Specific to the handler extension.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d640-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="6d640-119">Return value</span></span>

<span data-ttu-id="6d640-120">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="6d640-120">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d640-121">備註</span><span class="sxs-lookup"><span data-stu-id="6d640-121">Remarks</span></span>

<span data-ttu-id="6d640-122">**LINE \_ AGENTSPECIFIC** 訊息不會傳送至支援舊版 TAPI 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="6d640-122">The **LINE\_AGENTSPECIFIC** message is not sent to applications that support older versions of TAPI.</span></span>

## <a name="requirements"></a><span data-ttu-id="6d640-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6d640-123">Requirements</span></span>



| <span data-ttu-id="6d640-124">需求</span><span class="sxs-lookup"><span data-stu-id="6d640-124">Requirement</span></span> | <span data-ttu-id="6d640-125">值</span><span class="sxs-lookup"><span data-stu-id="6d640-125">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="6d640-126">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="6d640-126">TAPI version</span></span><br/> | <span data-ttu-id="6d640-127">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="6d640-127">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="6d640-128">標頭</span><span class="sxs-lookup"><span data-stu-id="6d640-128">Header</span></span><br/>       | <dl> <span data-ttu-id="6d640-129"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="6d640-129"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d640-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6d640-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d640-131">**LINEAGENTCAPS**</span><span class="sxs-lookup"><span data-stu-id="6d640-131">**LINEAGENTCAPS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineagentcaps)
</dt> <dt>

[<span data-ttu-id="6d640-132">**lineAgentSpecific**</span><span class="sxs-lookup"><span data-stu-id="6d640-132">**lineAgentSpecific**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineagentspecific)
</dt> <dt>

[<span data-ttu-id="6d640-133">**lineGetAgentStatus**</span><span class="sxs-lookup"><span data-stu-id="6d640-133">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




