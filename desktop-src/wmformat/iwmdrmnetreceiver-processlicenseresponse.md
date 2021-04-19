---
title: 'IWMDRMNetReceiver ProcessLicenseResponse 方法 (Wmdrmsdk .h) '
description: ProcessLicenseResponse 方法會處理傳輸器在回復至授權挑戰時傳送的授權回應。
ms.assetid: b6d04651-746b-474e-8a02-6b7cbee9db46
keywords:
- ProcessLicenseResponse 方法 windows Media 格式
- ProcessLicenseResponse 方法 windows Media Format，IWMDRMNetReceiver 介面
- IWMDRMNetReceiver 介面 windows Media Format，ProcessLicenseResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.ProcessLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45a09ebab81b71e21b9ef922423a7bbe67b20596
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983983"
---
# <a name="iwmdrmnetreceiverprocesslicenseresponse-method"></a><span data-ttu-id="3d512-106">IWMDRMNetReceiver：:P rocessLicenseResponse 方法</span><span class="sxs-lookup"><span data-stu-id="3d512-106">IWMDRMNetReceiver::ProcessLicenseResponse method</span></span>

<span data-ttu-id="3d512-107">**ProcessLicenseResponse** 方法會處理傳輸器在回復至授權挑戰時傳送的授權回應。</span><span class="sxs-lookup"><span data-stu-id="3d512-107">The **ProcessLicenseResponse** method processes the license response that is sent by the transmitter in reply to a license challenge.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d512-108">語法</span><span class="sxs-lookup"><span data-stu-id="3d512-108">Syntax</span></span>


```C++
HRESULT ProcessLicenseResponse(
  [in]  BYTE  *pbLicenseResponse,
  [in]  DWORD cbLicenseResponse,
  [out] BYTE  **ppbWMDRMNetLicenseRepresentation,
  [out] DWORD *pcbWMDRMNetLicenseRepresentation
);
```



## <a name="parameters"></a><span data-ttu-id="3d512-109">參數</span><span class="sxs-lookup"><span data-stu-id="3d512-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d512-110">*pbLicenseResponse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d512-110">*pbLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d512-111">從傳輸器收到的授權回應。</span><span class="sxs-lookup"><span data-stu-id="3d512-111">License response received from the transmitter.</span></span>

</dd> <dt>

<span data-ttu-id="3d512-112">*cbLicenseResponse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3d512-112">*cbLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d512-113">回應的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3d512-113">Size of the response in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="3d512-114">*ppbWMDRMNetLicenseRepresentation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3d512-114">*ppbWMDRMNetLicenseRepresentation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d512-115">變數的位址，此變數會接收授權回應訊息中所含授權之內部授權表示的位址。</span><span class="sxs-lookup"><span data-stu-id="3d512-115">Address of a variable that receives the address of the internal license representation for the license contained in the license response message.</span></span> <span data-ttu-id="3d512-116">完成這項資料之後，您必須呼叫 **CoTaskMemFree** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="3d512-116">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span> <span data-ttu-id="3d512-117">如果不需要授權標記法，此參數可以設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="3d512-117">This parameter may be set to **NULL** if the license representation is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="3d512-118">*pcbWMDRMNetLicenseRepresentation* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3d512-118">*pcbWMDRMNetLicenseRepresentation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d512-119">接收授權表示大小之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="3d512-119">Address of a variable that receives the size of the license representation.</span></span> <span data-ttu-id="3d512-120">如果 *ppbWMDRMNetLicenseRepresentation* 為 **null**，則必須設定為 **null** 。</span><span class="sxs-lookup"><span data-stu-id="3d512-120">Must be set to **NULL** if *ppbWMDRMNetLicenseRepresentation* is **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d512-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d512-121">Return value</span></span>

<span data-ttu-id="3d512-122">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="3d512-122">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3d512-123">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="3d512-123">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3d512-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3d512-124">Return code</span></span>                                                                                                | <span data-ttu-id="3d512-125">Description</span><span class="sxs-lookup"><span data-stu-id="3d512-125">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="3d512-126"><dt>**NS \_ E \_ DRM \_ RIV \_ 太 \_ 小**</dt></span><span class="sxs-lookup"><span data-stu-id="3d512-126"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="3d512-127">需要更新的內容撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="3d512-127">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="3d512-128"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3d512-128"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="3d512-129">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="3d512-129">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="3d512-130">備註</span><span class="sxs-lookup"><span data-stu-id="3d512-130">Remarks</span></span>

<span data-ttu-id="3d512-131">使用這個方法所處理的授權回應必須對應至用戶端電腦上所產生的最後一個授權挑戰。</span><span class="sxs-lookup"><span data-stu-id="3d512-131">The license response processed by using this method must correspond to the last license challenge generated on the client computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d512-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d512-132">Requirements</span></span>



| <span data-ttu-id="3d512-133">需求</span><span class="sxs-lookup"><span data-stu-id="3d512-133">Requirement</span></span> | <span data-ttu-id="3d512-134">值</span><span class="sxs-lookup"><span data-stu-id="3d512-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3d512-135">標頭</span><span class="sxs-lookup"><span data-stu-id="3d512-135">Header</span></span><br/> | <dl> <span data-ttu-id="3d512-136"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="3d512-136"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d512-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d512-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d512-138">**IWMDRMNetReceiver 介面**</span><span class="sxs-lookup"><span data-stu-id="3d512-138">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="3d512-139">**IWMDRMNetReceiver::GetLicenseChallenge**</span><span class="sxs-lookup"><span data-stu-id="3d512-139">**IWMDRMNetReceiver::GetLicenseChallenge**</span></span>](iwmdrmnetreceiver-getlicensechallenge.md)
</dt> </dl>

 

 





