---
title: 'IWMDRMNetTransmitter GetLeafLicenseResponse 方法 (Wmdrmsdk .h) '
description: GetLeafLicenseResponse 方法會產生分葉授權回應訊息。
ms.assetid: b2893d22-b6f3-44d2-b6db-e2b07fbe098d
keywords:
- GetLeafLicenseResponse 方法 windows Media 格式
- GetLeafLicenseResponse 方法 windows Media Format，IWMDRMNetTransmitter 介面
- IWMDRMNetTransmitter 介面 windows Media Format，GetLeafLicenseResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMNetTransmitter.GetLeafLicenseResponse
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1bf2374966abfae4353a72755313c1cbbdfb7287
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982543"
---
# <a name="iwmdrmnettransmittergetleaflicenseresponse-method"></a><span data-ttu-id="0d8f9-106">IWMDRMNetTransmitter：： GetLeafLicenseResponse 方法</span><span class="sxs-lookup"><span data-stu-id="0d8f9-106">IWMDRMNetTransmitter::GetLeafLicenseResponse method</span></span>

<span data-ttu-id="0d8f9-107">**GetLeafLicenseResponse** 方法會產生分葉授權回應訊息。</span><span class="sxs-lookup"><span data-stu-id="0d8f9-107">The **GetLeafLicenseResponse** method generates a leaf license response message.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d8f9-108">語法</span><span class="sxs-lookup"><span data-stu-id="0d8f9-108">Syntax</span></span>


```C++
HRESULT GetLeafLicenseResponse(
  [in]  BSTR            bstrKID,
  [in]  WMDRMNET_POLICY *pPolicy,
  [out] IWMDRMEncrypt   **ppIWMDRMEncrypt,
  [out] BYTE            **ppbLicenseResponse,
  [out] DWORD           *pcbLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="0d8f9-109">參數</span><span class="sxs-lookup"><span data-stu-id="0d8f9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d8f9-110">*bstrKID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d8f9-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d8f9-111">要用於新分葉授權的 Base64 編碼金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="0d8f9-111">Base64-encoded key identifier to be used for the new leaf license.</span></span> <span data-ttu-id="0d8f9-112">金鑰識別碼應為隨機產生的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="0d8f9-112">The key identifier should be a randomly generated GUID value.</span></span>

</dd> <dt>

<span data-ttu-id="0d8f9-113">*pPolicy* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0d8f9-113">*pPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d8f9-114">[**WMDRMNET \_ 原則**](wmdrmnet-policy.md)結構的指標，該結構定義要用於分葉授權的原則。</span><span class="sxs-lookup"><span data-stu-id="0d8f9-114">Pointer to the [**WMDRMNET\_POLICY**](wmdrmnet-policy.md) structure that defines the policy to use for the leaf license.</span></span>

</dd> <dt>

<span data-ttu-id="0d8f9-115">*ppIWMDRMEncrypt* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0d8f9-115">*ppIWMDRMEncrypt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d8f9-116">接收 [**IWMDRMEncrypt**](iwmdrmencrypt.md) 介面指標的變數位址，該介面可用來加密新分葉授權的資料。</span><span class="sxs-lookup"><span data-stu-id="0d8f9-116">Address of a variable that receives a pointer to the [**IWMDRMEncrypt**](iwmdrmencrypt.md) interface that can be used to encrypt data for the new leaf license.</span></span>

</dd> <dt>

<span data-ttu-id="0d8f9-117">*ppbLicenseResponse* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0d8f9-117">*ppbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d8f9-118">接收產生的授權回應位址之變數的位址。</span><span class="sxs-lookup"><span data-stu-id="0d8f9-118">Address of a variable that receives the address of the generated license response.</span></span> <span data-ttu-id="0d8f9-119">完成這項資料之後，您必須呼叫 **CoTaskMemFree** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="0d8f9-119">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="0d8f9-120">*pcbLicenseResponse* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0d8f9-120">*pcbLicenseResponse* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d8f9-121">接收授權回應大小的變數位址（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="0d8f9-121">Address of a variable that receives the size of the license response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d8f9-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="0d8f9-122">Return value</span></span>

<span data-ttu-id="0d8f9-123">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="0d8f9-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="0d8f9-124">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="0d8f9-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="0d8f9-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="0d8f9-125">Return code</span></span>                                                                                                | <span data-ttu-id="0d8f9-126">Description</span><span class="sxs-lookup"><span data-stu-id="0d8f9-126">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="0d8f9-127"><dt>**NS \_ E \_ DRM \_ RIV \_ 太 \_ 小**</dt></span><span class="sxs-lookup"><span data-stu-id="0d8f9-127"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="0d8f9-128">需要更新的內容撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="0d8f9-128">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="0d8f9-129"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0d8f9-129"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="0d8f9-130">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="0d8f9-130">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="0d8f9-131">備註</span><span class="sxs-lookup"><span data-stu-id="0d8f9-131">Remarks</span></span>

<span data-ttu-id="0d8f9-132">無。</span><span class="sxs-lookup"><span data-stu-id="0d8f9-132">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d8f9-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d8f9-133">Requirements</span></span>



| <span data-ttu-id="0d8f9-134">需求</span><span class="sxs-lookup"><span data-stu-id="0d8f9-134">Requirement</span></span> | <span data-ttu-id="0d8f9-135">值</span><span class="sxs-lookup"><span data-stu-id="0d8f9-135">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0d8f9-136">標頭</span><span class="sxs-lookup"><span data-stu-id="0d8f9-136">Header</span></span><br/> | <dl> <span data-ttu-id="0d8f9-137"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="0d8f9-137"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d8f9-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d8f9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d8f9-139">**IWMDRMNetTransmitter 介面**</span><span class="sxs-lookup"><span data-stu-id="0d8f9-139">**IWMDRMNetTransmitter Interface**</span></span>](iwmdrmnettransmitter.md)
</dt> </dl>

 

 





