---
description: '\_當應用程式目前有開啟行的代理程式處理常式上的 ACD 代理程式會話狀態有所變更時，就會傳送 LINE AGENTSESSIONSTATUS 訊息。 此訊息是使用 lineProxyMessage 函式所產生。'
ms.assetid: bb9d2292-8c41-4557-989e-6c5eb785313f
title: 'LINE_AGENTSESSIONSTATUS 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d53c14290dfb6bda3889e7d2b87d8d3ca5e651c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993590"
---
# <a name="line_agentsessionstatus-message"></a><span data-ttu-id="ab5d5-104">行 \_ AGENTSESSIONSTATUS 訊息</span><span class="sxs-lookup"><span data-stu-id="ab5d5-104">LINE\_AGENTSESSIONSTATUS message</span></span>

<span data-ttu-id="ab5d5-105">當應用程式目前有開啟行的代理程式處理常式上的 ACD 代理程式會話狀態有所變更時，就會傳送 **LINE \_ AGENTSESSIONSTATUS** 訊息。</span><span class="sxs-lookup"><span data-stu-id="ab5d5-105">The **LINE\_AGENTSESSIONSTATUS** message is sent when the status of an ACD agent session changes on an agent handler for which the application currently has an open line.</span></span> <span data-ttu-id="ab5d5-106">此訊息是使用 [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) 函式所產生。</span><span class="sxs-lookup"><span data-stu-id="ab5d5-106">This message is generated using the [**lineProxyMessage**](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage) function.</span></span>


```C++
        
```



## <a name="parameters"></a><span data-ttu-id="ab5d5-107">參數</span><span class="sxs-lookup"><span data-stu-id="ab5d5-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab5d5-108">*dwDevice*</span><span class="sxs-lookup"><span data-stu-id="ab5d5-108">*dwDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="ab5d5-109">應用程式的控制碼，指向代理程式會話狀態已變更的線路裝置。</span><span class="sxs-lookup"><span data-stu-id="ab5d5-109">The application's handle to the line device on which the agent session status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="ab5d5-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="ab5d5-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="ab5d5-111">開啟行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="ab5d5-111">The callback instance supplied when opening the line.</span></span>

</dd> <dt>

<span data-ttu-id="ab5d5-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="ab5d5-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="ab5d5-113">已變更其狀態的代理程式會話控制碼。</span><span class="sxs-lookup"><span data-stu-id="ab5d5-113">A handle of the agent session whose status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="ab5d5-114">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="ab5d5-114">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="ab5d5-115">指定已變更的代理程式會話狀態。</span><span class="sxs-lookup"><span data-stu-id="ab5d5-115">Specifies the agent session status that has changed.</span></span> <span data-ttu-id="ab5d5-116">可以是一或多 **行 \_ AGENTSESSIONSTATUS**。</span><span class="sxs-lookup"><span data-stu-id="ab5d5-116">Can be one or more of the **LINE\_AGENTSESSIONSTATUS**.</span></span>

</dd> <dt>

<span data-ttu-id="ab5d5-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="ab5d5-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="ab5d5-118">如果 *dwParam2* 包含 LINEAGENTSTATUSEX \_ 狀態位， *dwParam3* 就會指出代理程式狀態的新值，也就是其中一個 [**LINEAGENTSTATEEX \_ 常數**](lineagentstateex--constants.md)。</span><span class="sxs-lookup"><span data-stu-id="ab5d5-118">If *dwParam2* includes the LINEAGENTSTATUSEX\_STATE bit, *dwParam3* indicates the new value of the agent state, which is one of the [**LINEAGENTSTATEEX\_ constants**](lineagentstateex--constants.md).</span></span>

<span data-ttu-id="ab5d5-119">否則， *dwParam3* 會設為零。</span><span class="sxs-lookup"><span data-stu-id="ab5d5-119">Otherwise, *dwParam3* is set to zero.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ab5d5-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab5d5-120">Requirements</span></span>



| <span data-ttu-id="ab5d5-121">需求</span><span class="sxs-lookup"><span data-stu-id="ab5d5-121">Requirement</span></span> | <span data-ttu-id="ab5d5-122">值</span><span class="sxs-lookup"><span data-stu-id="ab5d5-122">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="ab5d5-123">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="ab5d5-123">TAPI version</span></span><br/> | <span data-ttu-id="ab5d5-124">需要 TAPI 2。2</span><span class="sxs-lookup"><span data-stu-id="ab5d5-124">Requires TAPI 2.2</span></span><br/>                                                      |
| <span data-ttu-id="ab5d5-125">標頭</span><span class="sxs-lookup"><span data-stu-id="ab5d5-125">Header</span></span><br/>       | <dl> <span data-ttu-id="ab5d5-126"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="ab5d5-126"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab5d5-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab5d5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab5d5-128">**lineGetAgentSessionInfo**</span><span class="sxs-lookup"><span data-stu-id="ab5d5-128">**lineGetAgentSessionInfo**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentsessioninfo)
</dt> <dt>

[<span data-ttu-id="ab5d5-129">**lineProxyMessage**</span><span class="sxs-lookup"><span data-stu-id="ab5d5-129">**lineProxyMessage**</span></span>](/windows/desktop/api/Tapi/nf-tapi-lineproxymessage)
</dt> </dl>

 

 




