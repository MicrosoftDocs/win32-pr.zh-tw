---
title: 'IWMDRMNetReceiver GetLicenseChallenge 方法 (Wmdrmsdk .h) '
description: GetLicenseChallenge 方法會產生網路裝置的 Windows Media DRM 授權挑戰，可在要求受保護的內容時傳送給發送器。
ms.assetid: c13b9e9e-b076-411b-a106-b602544faaba
keywords:
- GetLicenseChallenge 方法 windows Media 格式
- GetLicenseChallenge 方法 windows Media Format，IWMDRMNetReceiver 介面
- IWMDRMNetReceiver 介面 windows Media Format，GetLicenseChallenge 方法
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetLicenseChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f58b85b8dc5edd6c23e809dda8c18bf30137f6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994199"
---
# <a name="iwmdrmnetreceivergetlicensechallenge-method"></a><span data-ttu-id="f100e-106">IWMDRMNetReceiver：： GetLicenseChallenge 方法</span><span class="sxs-lookup"><span data-stu-id="f100e-106">IWMDRMNetReceiver::GetLicenseChallenge method</span></span>

<span data-ttu-id="f100e-107">**GetLicenseChallenge** 方法會產生網路裝置的 WINDOWS Media DRM 授權挑戰，可在要求受保護的內容時傳送給發送器。</span><span class="sxs-lookup"><span data-stu-id="f100e-107">The **GetLicenseChallenge** method generates a Windows Media DRM for Network Devices license challenge that can be sent to a transmitter when requesting protected content.</span></span>

## <a name="syntax"></a><span data-ttu-id="f100e-108">語法</span><span class="sxs-lookup"><span data-stu-id="f100e-108">Syntax</span></span>


```C++
HRESULT GetLicenseChallenge(
  [in]  BSTR  bstrAction,
  [out] BYTE  **ppbLicenseChallenge,
  [out] DWORD *pcbLicenseChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="f100e-109">參數</span><span class="sxs-lookup"><span data-stu-id="f100e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f100e-110">*bstrAction* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f100e-110">*bstrAction* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f100e-111">要產生挑戰的動作。</span><span class="sxs-lookup"><span data-stu-id="f100e-111">Action for which to generate the challenge.</span></span>

</dd> <dt>

<span data-ttu-id="f100e-112">*ppbLicenseChallenge* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f100e-112">*ppbLicenseChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f100e-113">設定為所產生挑戰位址之指標的位址。</span><span class="sxs-lookup"><span data-stu-id="f100e-113">Address of a pointer that is set to the address of the generated challenge.</span></span> <span data-ttu-id="f100e-114">完成這項資料之後，您必須呼叫 **CoTaskMemFree** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="f100e-114">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="f100e-115">*pcbLicenseChallenge* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f100e-115">*pcbLicenseChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f100e-116">接收授權挑戰大小的變數位址（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f100e-116">Address of a variable that receives the size of the license challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f100e-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="f100e-117">Return value</span></span>

<span data-ttu-id="f100e-118">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="f100e-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="f100e-119">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="f100e-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="f100e-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="f100e-120">Return code</span></span>                                                                          | <span data-ttu-id="f100e-121">Description</span><span class="sxs-lookup"><span data-stu-id="f100e-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="f100e-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f100e-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="f100e-123">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="f100e-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f100e-124">備註</span><span class="sxs-lookup"><span data-stu-id="f100e-124">Remarks</span></span>

<span data-ttu-id="f100e-125">無。</span><span class="sxs-lookup"><span data-stu-id="f100e-125">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="f100e-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="f100e-126">Requirements</span></span>



| <span data-ttu-id="f100e-127">需求</span><span class="sxs-lookup"><span data-stu-id="f100e-127">Requirement</span></span> | <span data-ttu-id="f100e-128">值</span><span class="sxs-lookup"><span data-stu-id="f100e-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f100e-129">標頭</span><span class="sxs-lookup"><span data-stu-id="f100e-129">Header</span></span><br/> | <dl> <span data-ttu-id="f100e-130"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="f100e-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f100e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f100e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f100e-132">**IWMDRMNetReceiver 介面**</span><span class="sxs-lookup"><span data-stu-id="f100e-132">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="f100e-133">**IWMDRMNetReceiver：:P rocessLicenseResponse**</span><span class="sxs-lookup"><span data-stu-id="f100e-133">**IWMDRMNetReceiver::ProcessLicenseResponse**</span></span>](iwmdrmnetreceiver-processlicenseresponse.md)
</dt> </dl>

 

 





