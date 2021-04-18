---
description: '\_當應用程式目前有開啟行的代理程式處理常式上的 ACD 代理程式狀態變更時，就會傳送 LINE AGENTSTATUSEX 訊息。 此訊息是使用 lineProxyMessage 函式產生的。'
ms.assetid: a0709367-9105-43af-9772-0161d94c098a
title: 'LINE_AGENTSTATUSEX 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c9ff1a39fd6aacf69922693a54198426d267720
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976187"
---
# <a name="line_agentstatusex-message"></a><span data-ttu-id="d8075-104">行 \_ AGENTSTATUSEX 訊息</span><span class="sxs-lookup"><span data-stu-id="d8075-104">LINE\_AGENTSTATUSEX message</span></span>

<span data-ttu-id="d8075-105">當應用程式目前有開啟行的代理程式處理常式上的 ACD 代理程式狀態變更時，就會傳送 **LINE \_ AGENTSTATUSEX** 訊息。</span><span class="sxs-lookup"><span data-stu-id="d8075-105">The **LINE\_AGENTSTATUSEX** message is sent when the status of an ACD agent changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="d8075-106">此訊息是使用 [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) 函式產生的。</span><span class="sxs-lookup"><span data-stu-id="d8075-106">This message is generated using [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="d8075-107">參數</span><span class="sxs-lookup"><span data-stu-id="d8075-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8075-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="d8075-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="d8075-109">應用程式線路裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d8075-109">The application's handle to the line device.</span></span> <span data-ttu-id="d8075-110">這與代理程式處理常式相關。</span><span class="sxs-lookup"><span data-stu-id="d8075-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="d8075-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="d8075-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="d8075-112">開啟行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="d8075-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="d8075-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="d8075-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="d8075-114">狀態已變更之代理程式的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d8075-114">The handle of the agent whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="d8075-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="d8075-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="d8075-116">指定已變更的佇列狀態。</span><span class="sxs-lookup"><span data-stu-id="d8075-116">Specifies the queue status that has changed.</span></span> <span data-ttu-id="d8075-117">可以是一或多個 [**LINEQUEUESTATUS \_ 常數**](linequeuestatus--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="d8075-117">Can be one or more of the [**LINEQUEUESTATUS\_ constants**](linequeuestatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d8075-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="d8075-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="d8075-119">如果 *dwParam2* 包含 LINEAGENTSTATUSEX \_ 狀態位， *dwParam3* 就會指出代理程式狀態的新值，也就是其中一個 [**LINEAGENTSTATEEX \_ 常數**](lineagentstateex--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="d8075-119">If *dwParam2* includes the LINEAGENTSTATUSEX \_STATE bit, *dwParam3* indicates the new value of the agent state, which is one of the [**LINEAGENTSTATEEX\_ constants**](lineagentstateex--constants.md).</span></span>

<span data-ttu-id="d8075-120">否則， *dwParam3* 會設為零。</span><span class="sxs-lookup"><span data-stu-id="d8075-120">Otherwise, *dwParam3* is set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d8075-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8075-121">Requirements</span></span>



| <span data-ttu-id="d8075-122">需求</span><span class="sxs-lookup"><span data-stu-id="d8075-122">Requirement</span></span> | <span data-ttu-id="d8075-123">值</span><span class="sxs-lookup"><span data-stu-id="d8075-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d8075-124">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="d8075-124">TAPI version</span></span><br/> | <span data-ttu-id="d8075-125">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="d8075-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="d8075-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d8075-126">Header</span></span><br/>       | <dl> <span data-ttu-id="d8075-127"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="d8075-127"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8075-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8075-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8075-129">**lineGetAgentInfo**</span><span class="sxs-lookup"><span data-stu-id="d8075-129">**lineGetAgentInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentinfo)
</dt> <dt>

[<span data-ttu-id="d8075-130">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="d8075-130">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




