---
description: '\_當應用程式目前有開啟行的代理程式處理常式上的 ACD 佇列狀態變更時，就會傳送 LINE system.printing.printqueue.queuestatus 訊息。 此訊息是使用 lineProxyMessage 函式所產生。'
ms.assetid: 9baacfc5-f26c-41c7-a1f8-f48ec8aa844c
title: 'LINE_QUEUESTATUS 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a89785b92009a7531ae693545febaf153cf19bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983067"
---
# <a name="line_queuestatus-message"></a><span data-ttu-id="d4ed4-104">行 \_ system.printing.printqueue.queuestatus 訊息</span><span class="sxs-lookup"><span data-stu-id="d4ed4-104">LINE\_QUEUESTATUS message</span></span>

<span data-ttu-id="d4ed4-105">當應用程式目前有開啟行的代理程式處理常式上的 ACD 佇列狀態變更時，就會傳送 **LINE \_ system.printing.printqueue.queuestatus** 訊息。</span><span class="sxs-lookup"><span data-stu-id="d4ed4-105">The **LINE\_QUEUESTATUS** message is sent when the status of an ACD queue changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="d4ed4-106">此訊息是使用 [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) 函式所產生。</span><span class="sxs-lookup"><span data-stu-id="d4ed4-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="d4ed4-107">參數</span><span class="sxs-lookup"><span data-stu-id="d4ed4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4ed4-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="d4ed4-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="d4ed4-109">應用程式線路裝置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d4ed4-109">The application's handle to the line device.</span></span> <span data-ttu-id="d4ed4-110">這與代理程式處理常式相關。</span><span class="sxs-lookup"><span data-stu-id="d4ed4-110">This relates to the agent handler.</span></span>

</dd> <dt>

<span data-ttu-id="d4ed4-111">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="d4ed4-111">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="d4ed4-112">開啟行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="d4ed4-112">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="d4ed4-113">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="d4ed4-113">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="d4ed4-114">其狀態已變更之佇列的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d4ed4-114">The identifier of the queue whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="d4ed4-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="d4ed4-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="d4ed4-116">指定已變更的佇列狀態。</span><span class="sxs-lookup"><span data-stu-id="d4ed4-116">Specifies the queue status that has changed.</span></span> <span data-ttu-id="d4ed4-117">可以是一或多個 [**LINEQUEUESTATUS \_ 常數**](linequeuestatus--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="d4ed4-117">Can be one or more of the [**LINEQUEUESTATUS\_ constants**](linequeuestatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="d4ed4-118">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="d4ed4-118">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="d4ed4-119">保留的。</span><span class="sxs-lookup"><span data-stu-id="d4ed4-119">Reserved.</span></span> <span data-ttu-id="d4ed4-120">設定為零。</span><span class="sxs-lookup"><span data-stu-id="d4ed4-120">Set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d4ed4-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4ed4-121">Requirements</span></span>



| <span data-ttu-id="d4ed4-122">需求</span><span class="sxs-lookup"><span data-stu-id="d4ed4-122">Requirement</span></span> | <span data-ttu-id="d4ed4-123">值</span><span class="sxs-lookup"><span data-stu-id="d4ed4-123">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="d4ed4-124">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="d4ed4-124">TAPI version</span></span><br/> | <span data-ttu-id="d4ed4-125">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="d4ed4-125">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="d4ed4-126">標頭</span><span class="sxs-lookup"><span data-stu-id="d4ed4-126">Header</span></span><br/>       | <dl> <span data-ttu-id="d4ed4-127"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="d4ed4-127"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4ed4-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4ed4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4ed4-129">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="d4ed4-129">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




