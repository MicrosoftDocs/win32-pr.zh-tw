---
title: 'IWMDRMNetReceiver ProcessRegistrationResponse 方法 (Wmdrmsdk .h) '
description: ProcessRegistrationResponse 方法會在回復註冊挑戰時，處理傳輸器所傳送的註冊回應。
ms.assetid: d0260e93-0a5e-494b-a723-bb62206ed55b
keywords:
- ProcessRegistrationResponse 方法 windows Media 格式
- ProcessRegistrationResponse 方法 windows Media Format，IWMDRMNetReceiver 介面
- IWMDRMNetReceiver 介面 windows Media Format，ProcessRegistrationResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessRegistrationResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a77b01f443d57825d82b7cf9556d7585745bb99e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977162"
---
# <a name="iwmdrmnetreceiverprocessregistrationresponse-method"></a><span data-ttu-id="35f35-106">IWMDRMNetReceiver：:P rocessRegistrationResponse 方法</span><span class="sxs-lookup"><span data-stu-id="35f35-106">IWMDRMNetReceiver::ProcessRegistrationResponse method</span></span>

<span data-ttu-id="35f35-107">**ProcessRegistrationResponse** 方法會在回復註冊挑戰時，處理傳輸器所傳送的註冊回應。</span><span class="sxs-lookup"><span data-stu-id="35f35-107">The **ProcessRegistrationResponse** method processes a registration response sent by the transmitter in reply to a registration challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="35f35-108">語法</span><span class="sxs-lookup"><span data-stu-id="35f35-108">Syntax</span></span>


```C++
HRESULT ProcessRegistrationResponse(
  [in]  BYTE     *pbRegistrationResponse,
  [in]  DWORD    cbRegistrationResponse,
  [out] IUnknown **ppunkCancellationCookie
);
```



## <a name="parameters"></a><span data-ttu-id="35f35-109">參數</span><span class="sxs-lookup"><span data-stu-id="35f35-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35f35-110">*pbRegistrationResponse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35f35-110">*pbRegistrationResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35f35-111">從傳輸器收到的註冊回應。</span><span class="sxs-lookup"><span data-stu-id="35f35-111">Registration response received from the transmitter.</span></span>

</dd> <dt>

<span data-ttu-id="35f35-112">*cbRegistrationResponse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35f35-112">*cbRegistrationResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35f35-113">註冊回應的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="35f35-113">Size of the registration response in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="35f35-114">*ppunkCancellationCookie* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="35f35-114">*ppunkCancellationCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="35f35-115">指標，接收識別此非同步呼叫之物件的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="35f35-115">Pointer that receives a pointer to the **IUnknown** interface of an object that identifies this asynchronous call.</span></span> <span data-ttu-id="35f35-116">這個介面指標可透過呼叫 [**IWMDRMEventGenerator：： CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) 方法，用來取消非同步呼叫。</span><span class="sxs-lookup"><span data-stu-id="35f35-116">This interface pointer can be used to cancel the asynchronous call by calling the [**IWMDRMEventGenerator::CancelAsyncOperation**](iwmdrmeventgenerator-cancelasyncoperation.md) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35f35-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="35f35-117">Return value</span></span>

<span data-ttu-id="35f35-118">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="35f35-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="35f35-119">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="35f35-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="35f35-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="35f35-120">Return code</span></span>                                                                          | <span data-ttu-id="35f35-121">Description</span><span class="sxs-lookup"><span data-stu-id="35f35-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="35f35-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="35f35-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="35f35-123">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="35f35-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="35f35-124">備註</span><span class="sxs-lookup"><span data-stu-id="35f35-124">Remarks</span></span>

<span data-ttu-id="35f35-125">這個方法會以非同步方式執行;當處理完成時，MEProximityCompleted 事件會傳送至 **IMFMediaEventGenerator** 介面。</span><span class="sxs-lookup"><span data-stu-id="35f35-125">This method executes asynchronously; when processing is complete, the MEProximityCompleted event is sent to the **IMFMediaEventGenerator** interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="35f35-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="35f35-126">Requirements</span></span>



| <span data-ttu-id="35f35-127">需求</span><span class="sxs-lookup"><span data-stu-id="35f35-127">Requirement</span></span> | <span data-ttu-id="35f35-128">值</span><span class="sxs-lookup"><span data-stu-id="35f35-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="35f35-129">標頭</span><span class="sxs-lookup"><span data-stu-id="35f35-129">Header</span></span><br/> | <dl> <span data-ttu-id="35f35-130"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="35f35-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35f35-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35f35-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35f35-132">**IWMDRMNetReceiver 介面**</span><span class="sxs-lookup"><span data-stu-id="35f35-132">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="35f35-133">**IWMDRMNetReceiver::GetRegistrationChallenge**</span><span class="sxs-lookup"><span data-stu-id="35f35-133">**IWMDRMNetReceiver::GetRegistrationChallenge**</span></span>](iwmdrmnetreceiver-getregistrationchallenge.md)
</dt> </dl>

 

 





