---
title: 'IWMDRMNetTransmitter SetLicenseChallenge 方法 (Wmdrmsdk .h) '
description: SetLicenseChallenge 方法會處理 Windows Media DRM 針對網路裝置接收者傳送的授權挑戰。
ms.assetid: 3d4cd029-a8f5-49fc-ba8c-d8615ff94366
keywords:
- SetLicenseChallenge 方法 windows Media 格式
- SetLicenseChallenge 方法 windows Media Format，IWMDRMNetTransmitter 介面
- IWMDRMNetTransmitter 介面 windows Media Format，SetLicenseChallenge 方法
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.SetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94b83ca615896039a592d147fe8c14d15493cec0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990119"
---
# <a name="iwmdrmnettransmittersetlicensechallenge-method"></a><span data-ttu-id="835ae-106">IWMDRMNetTransmitter：： SetLicenseChallenge 方法</span><span class="sxs-lookup"><span data-stu-id="835ae-106">IWMDRMNetTransmitter::SetLicenseChallenge method</span></span>

<span data-ttu-id="835ae-107">**SetLicenseChallenge** 方法會處理 WINDOWS Media DRM 針對網路裝置接收者傳送的授權挑戰。</span><span class="sxs-lookup"><span data-stu-id="835ae-107">The **SetLicenseChallenge** method processes a license challenge sent by a Windows Media DRM for Network Devices receiver.</span></span>

## <a name="syntax"></a><span data-ttu-id="835ae-108">語法</span><span class="sxs-lookup"><span data-stu-id="835ae-108">Syntax</span></span>


```C++
HRESULT SetLicenseChallenge(
  [in] BYTE  *pbLicenseChallenge,
  [in] DWORD cbLicenseChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="835ae-109">參數</span><span class="sxs-lookup"><span data-stu-id="835ae-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="835ae-110">*pbLicenseChallenge* \[在\]</span><span class="sxs-lookup"><span data-stu-id="835ae-110">*pbLicenseChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="835ae-111">接收者傳送的授權挑戰資料指標。</span><span class="sxs-lookup"><span data-stu-id="835ae-111">Pointer to the license challenge data that was sent by a receiver.</span></span>

</dd> <dt>

<span data-ttu-id="835ae-112">*cbLicenseChallenge* \[在\]</span><span class="sxs-lookup"><span data-stu-id="835ae-112">*cbLicenseChallenge* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="835ae-113">授權挑戰的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="835ae-113">Size of license challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="835ae-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="835ae-114">Return value</span></span>

<span data-ttu-id="835ae-115">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="835ae-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="835ae-116">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="835ae-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="835ae-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="835ae-117">Return code</span></span>                                                                          | <span data-ttu-id="835ae-118">Description</span><span class="sxs-lookup"><span data-stu-id="835ae-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="835ae-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="835ae-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="835ae-120">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="835ae-120">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="835ae-121">備註</span><span class="sxs-lookup"><span data-stu-id="835ae-121">Remarks</span></span>

<span data-ttu-id="835ae-122">如果這個方法成功，則對 **IWMDRMNetTransmitter** 其他方法的後續呼叫將會使用處理過的挑戰中的資訊。</span><span class="sxs-lookup"><span data-stu-id="835ae-122">If this method succeeds, subsequent calls to the other methods of **IWMDRMNetTransmitter** will use the information in the processed challenge.</span></span>

## <a name="requirements"></a><span data-ttu-id="835ae-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="835ae-123">Requirements</span></span>



| <span data-ttu-id="835ae-124">需求</span><span class="sxs-lookup"><span data-stu-id="835ae-124">Requirement</span></span> | <span data-ttu-id="835ae-125">值</span><span class="sxs-lookup"><span data-stu-id="835ae-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="835ae-126">標頭</span><span class="sxs-lookup"><span data-stu-id="835ae-126">Header</span></span><br/> | <dl> <span data-ttu-id="835ae-127"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="835ae-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="835ae-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="835ae-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="835ae-129">**IWMDRMNetTransmitter 介面**</span><span class="sxs-lookup"><span data-stu-id="835ae-129">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





