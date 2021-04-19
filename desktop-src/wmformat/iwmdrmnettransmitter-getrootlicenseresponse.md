---
title: 'IWMDRMNetTransmitter GetRootLicenseResponse 方法 (Wmdrmsdk .h) '
description: GetRootLicenseResponse 方法會產生根授權回應訊息。
ms.assetid: c735ee52-f0e0-4404-881b-18ee9a7fa9f9
keywords:
- GetRootLicenseResponse 方法 windows Media 格式
- GetRootLicenseResponse 方法 windows Media Format，IWMDRMNetTransmitter 介面
- IWMDRMNetTransmitter 介面 windows Media Format，GetRootLicenseResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetRootLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3497a3eaedb872b7d2c9eb5d7782d01f8b35462
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992899"
---
# <a name="iwmdrmnettransmittergetrootlicenseresponse-method"></a><span data-ttu-id="42c11-106">IWMDRMNetTransmitter：： GetRootLicenseResponse 方法</span><span class="sxs-lookup"><span data-stu-id="42c11-106">IWMDRMNetTransmitter::GetRootLicenseResponse method</span></span>

<span data-ttu-id="42c11-107">**GetRootLicenseResponse** 方法會產生根授權回應訊息。</span><span class="sxs-lookup"><span data-stu-id="42c11-107">The **GetRootLicenseResponse** method generates a root license response message.</span></span>

## <a name="syntax"></a><span data-ttu-id="42c11-108">語法</span><span class="sxs-lookup"><span data-stu-id="42c11-108">Syntax</span></span>


```C++
HRESULT GetRootLicenseResponse(
  [in]  BSTR  bstrKID,
  [out] BYTE  **ppbLicenseResponse,
  [out] DWORD *pcbLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="42c11-109">參數</span><span class="sxs-lookup"><span data-stu-id="42c11-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42c11-110">*bstrKID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="42c11-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="42c11-111">以 Base64 編碼的金鑰識別碼，用於新的根授權。</span><span class="sxs-lookup"><span data-stu-id="42c11-111">Base64-encoded key identifier to be used for the new root license.</span></span> <span data-ttu-id="42c11-112">金鑰識別碼應為隨機產生的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="42c11-112">The key identifier should be a randomly generated GUID value.</span></span>

</dd> <dt>

<span data-ttu-id="42c11-113">*ppbLicenseResponse* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="42c11-113">*ppbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42c11-114">接收產生的授權回應位址之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="42c11-114">Address of a variable that receives the address of the generated license response.</span></span> <span data-ttu-id="42c11-115">完成這項資料之後，您必須呼叫 **CoTaskMemFree** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="42c11-115">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="42c11-116">*pcbLicenseResponse* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="42c11-116">*pcbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42c11-117">接收授權回應大小的變數位址（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="42c11-117">Address of a variable that receives the size of the license response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42c11-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="42c11-118">Return value</span></span>

<span data-ttu-id="42c11-119">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="42c11-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="42c11-120">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="42c11-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="42c11-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="42c11-121">Return code</span></span>                                                                                                | <span data-ttu-id="42c11-122">Description</span><span class="sxs-lookup"><span data-stu-id="42c11-122">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="42c11-123"><dt>**NS \_ E \_ DRM \_ RIV \_ 太 \_ 小**</dt></span><span class="sxs-lookup"><span data-stu-id="42c11-123"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="42c11-124">需要更新的內容撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="42c11-124">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="42c11-125"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="42c11-125"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="42c11-126">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="42c11-126">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="42c11-127">備註</span><span class="sxs-lookup"><span data-stu-id="42c11-127">Remarks</span></span>

<span data-ttu-id="42c11-128">產生的根授權會使用來自授權挑戰資料的資訊來建立，而該資料會藉由呼叫 [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md)針對介面進行處理。</span><span class="sxs-lookup"><span data-stu-id="42c11-128">The generated root license is created using the information from the license challenge data, which is processed for the interface by calling [**SetLicenseChallenge**](iwmdrmnettransmitter-setlicensechallenge.md).</span></span>

<span data-ttu-id="42c11-129">根授權是在產生分葉授權時使用，這是藉由呼叫 [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) 方法來完成。</span><span class="sxs-lookup"><span data-stu-id="42c11-129">The root license is used in the generation of leaf licenses, which is accomplished by calling the [**GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) method.</span></span> <span data-ttu-id="42c11-130">**IWMDRMNetTransmitter** 介面會維護該使用的根授權複本。</span><span class="sxs-lookup"><span data-stu-id="42c11-130">The **IWMDRMNetTransmitter** interface maintains a copy of the root license for that use.</span></span>

<span data-ttu-id="42c11-131">藉由呼叫這個方法所建立的根授權沒有任何原則，且已設定為無法在接收的裝置上保存。</span><span class="sxs-lookup"><span data-stu-id="42c11-131">The root license created by calling this method does not have any policies and is configured so that it cannot be persisted on the receiving device.</span></span>

## <a name="requirements"></a><span data-ttu-id="42c11-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="42c11-132">Requirements</span></span>



| <span data-ttu-id="42c11-133">需求</span><span class="sxs-lookup"><span data-stu-id="42c11-133">Requirement</span></span> | <span data-ttu-id="42c11-134">值</span><span class="sxs-lookup"><span data-stu-id="42c11-134">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="42c11-135">標頭</span><span class="sxs-lookup"><span data-stu-id="42c11-135">Header</span></span><br/> | <dl> <span data-ttu-id="42c11-136"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="42c11-136"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="42c11-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42c11-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="42c11-138">**IWMDRMNetTransmitter 介面**</span><span class="sxs-lookup"><span data-stu-id="42c11-138">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





