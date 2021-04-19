---
description: '\_當應用程式目前已開啟的那一行上的 ACD 代理程式狀態變更時，就會傳送 TAPI 線路 AGENTSTATUS 訊息。 應用程式可以叫用 lineGetAgentStatus 來判斷代理程式目前的狀態。'
ms.assetid: 48f5d9bc-f20d-4364-8ec1-0b4bdc9cfcb4
title: 'LINE_AGENTSTATUS 訊息 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b98242745e2f025f95cfe06fbe22c8956a02b0e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991148"
---
# <a name="line_agentstatus-message"></a><span data-ttu-id="0b704-104">行 \_ AGENTSTATUS 訊息</span><span class="sxs-lookup"><span data-stu-id="0b704-104">LINE\_AGENTSTATUS message</span></span>

<span data-ttu-id="0b704-105">當應用程式目前已開啟的那一行上的 ACD 代理程式狀態變更時，就會傳送 TAPI **線路 \_ AGENTSTATUS** 訊息。</span><span class="sxs-lookup"><span data-stu-id="0b704-105">The TAPI **LINE\_AGENTSTATUS** message is sent when the status of an ACD agent changes on a line the application currently has open.</span></span> <span data-ttu-id="0b704-106">應用程式可以叫用 [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) 來判斷代理程式目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="0b704-106">The application can invoke [**lineGetAgentStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa) to determine the current status of the agent.</span></span>


```C++
            
```



## <a name="parameters"></a><span data-ttu-id="0b704-107">參數</span><span class="sxs-lookup"><span data-stu-id="0b704-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b704-108">*hDevice*</span><span class="sxs-lookup"><span data-stu-id="0b704-108">*hDevice*</span></span> 
</dt> <dd>

<span data-ttu-id="0b704-109">應用程式狀態已變更之線路裝置的應用程式控制碼。</span><span class="sxs-lookup"><span data-stu-id="0b704-109">The application's handle to the line device on which the agent status has changed.</span></span>

</dd> <dt>

<span data-ttu-id="0b704-110">*dwCallbackInstance*</span><span class="sxs-lookup"><span data-stu-id="0b704-110">*dwCallbackInstance*</span></span> 
</dt> <dd>

<span data-ttu-id="0b704-111">開啟呼叫的行時所提供的回呼實例。</span><span class="sxs-lookup"><span data-stu-id="0b704-111">The callback instance supplied when opening the call's line.</span></span>

</dd> <dt>

<span data-ttu-id="0b704-112">*dwParam1*</span><span class="sxs-lookup"><span data-stu-id="0b704-112">*dwParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="0b704-113">代理程式狀態變更所在行的位址識別碼。</span><span class="sxs-lookup"><span data-stu-id="0b704-113">Identifier of the address on the line on which the agent status changed.</span></span> <span data-ttu-id="0b704-114">位址識別碼會永久與位址相關聯;識別碼在作業系統升級之間會維持不變。</span><span class="sxs-lookup"><span data-stu-id="0b704-114">An address identifier is permanently associated with an address; the identifier remains constant across operating system upgrades.</span></span>

</dd> <dt>

<span data-ttu-id="0b704-115">*dwParam2*</span><span class="sxs-lookup"><span data-stu-id="0b704-115">*dwParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="0b704-116">指定已變更的代理程式狀態;可以是 [**LINEAGENTSTATUS \_ 常數**](lineagentstatus--constants.md)的組合。</span><span class="sxs-lookup"><span data-stu-id="0b704-116">Specifies the agent status that has changed; can be a combination of [**LINEAGENTSTATUS\_ constants**](lineagentstatus--constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b704-117">*dwParam3*</span><span class="sxs-lookup"><span data-stu-id="0b704-117">*dwParam3*</span></span> 
</dt> <dd>

<span data-ttu-id="0b704-118">如果 *dwParam2* 包含 LINEAGENTSTATUS \_ 狀態位，則 *dwParam3* 會在 [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)中指出 **dwState** 成員的新值。</span><span class="sxs-lookup"><span data-stu-id="0b704-118">If *dwParam2* includes the LINEAGENTSTATUS\_STATE bit, then *dwParam3* indicates the new value of the **dwState** member in [**LINEAGENTSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus).</span></span> <span data-ttu-id="0b704-119">否則，此參數會設定為零。</span><span class="sxs-lookup"><span data-stu-id="0b704-119">Otherwise, this parameter is set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0b704-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="0b704-120">Return value</span></span>

<span data-ttu-id="0b704-121">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="0b704-121">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0b704-122">備註</span><span class="sxs-lookup"><span data-stu-id="0b704-122">Remarks</span></span>

<span data-ttu-id="0b704-123">**LINE \_ AGENTSTATUS** 訊息不會傳送至支援舊版 TAPI 的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0b704-123">The **LINE\_AGENTSTATUS** message is not sent to applications that support older versions of TAPI.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b704-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b704-124">Requirements</span></span>



| <span data-ttu-id="0b704-125">需求</span><span class="sxs-lookup"><span data-stu-id="0b704-125">Requirement</span></span> | <span data-ttu-id="0b704-126">值</span><span class="sxs-lookup"><span data-stu-id="0b704-126">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0b704-127">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="0b704-127">TAPI version</span></span><br/> | <span data-ttu-id="0b704-128">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="0b704-128">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="0b704-129">標頭</span><span class="sxs-lookup"><span data-stu-id="0b704-129">Header</span></span><br/>       | <dl> <span data-ttu-id="0b704-130"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="0b704-130"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b704-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b704-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b704-132">**LINEAGENTSTATUS**</span><span class="sxs-lookup"><span data-stu-id="0b704-132">**LINEAGENTSTATUS**</span></span>](/windows/desktop/api/Tapi/ns-tapi-lineagentstatus)
</dt> <dt>

[<span data-ttu-id="0b704-133">**lineGetAgentStatus**</span><span class="sxs-lookup"><span data-stu-id="0b704-133">**lineGetAgentStatus**</span></span>](/windows/desktop/api/Tapi/nf-tapi-linegetagentstatusa)
</dt> </dl>

 

 




