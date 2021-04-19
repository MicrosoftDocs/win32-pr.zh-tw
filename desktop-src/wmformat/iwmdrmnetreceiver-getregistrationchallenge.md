---
title: 'IWMDRMNetReceiver GetRegistrationChallenge 方法 (Wmdrmsdk .h) '
description: GetRegistrationChallenge 方法會產生網路裝置註冊挑戰訊息的 Windows Media DRM。
ms.assetid: 7b3641a1-ccc5-4e29-b0e9-808b111f8841
keywords:
- GetRegistrationChallenge 方法 windows Media 格式
- GetRegistrationChallenge 方法 windows Media Format，IWMDRMNetReceiver 介面
- IWMDRMNetReceiver 介面 windows Media Format，GetRegistrationChallenge 方法
topic_type:
- apiref
api_name:
- IWMDRMNetReceiver.GetRegistrationChallenge
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a292749e95ca6ba2dabc8f3829eae827dbdd8325
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001148"
---
# <a name="iwmdrmnetreceivergetregistrationchallenge-method"></a><span data-ttu-id="3b669-106">IWMDRMNetReceiver：： GetRegistrationChallenge 方法</span><span class="sxs-lookup"><span data-stu-id="3b669-106">IWMDRMNetReceiver::GetRegistrationChallenge method</span></span>

<span data-ttu-id="3b669-107">**GetRegistrationChallenge** 方法會產生網路裝置註冊挑戰訊息的 WINDOWS Media DRM。</span><span class="sxs-lookup"><span data-stu-id="3b669-107">The **GetRegistrationChallenge** method generates a Windows Media DRM for Network Devices registration challenge message.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b669-108">語法</span><span class="sxs-lookup"><span data-stu-id="3b669-108">Syntax</span></span>


```C++
HRESULT GetRegistrationChallenge(
  [out] BYTE  **ppbRegistrationChallenge,
  [out] DWORD *pcbRegistrationChallenge
);
```



## <a name="parameters"></a><span data-ttu-id="3b669-109">參數</span><span class="sxs-lookup"><span data-stu-id="3b669-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b669-110">*ppbRegistrationChallenge* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3b669-110">*ppbRegistrationChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b669-111">接收所產生之挑戰位址的指標位址。</span><span class="sxs-lookup"><span data-stu-id="3b669-111">Address of a pointer that receives the address of the generated challenge.</span></span> <span data-ttu-id="3b669-112">完成這項資料之後，您必須呼叫 **CoTaskMemFree** 來釋放記憶體。</span><span class="sxs-lookup"><span data-stu-id="3b669-112">When finished with this data, you must release the memory by calling **CoTaskMemFree**.</span></span>

</dd> <dt>

<span data-ttu-id="3b669-113">*pcbRegistrationChallenge* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3b669-113">*pcbRegistrationChallenge* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3b669-114">接收註冊挑戰大小的變數位址（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3b669-114">Address of a variable that receives the size of the registration challenge in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b669-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b669-115">Return value</span></span>

<span data-ttu-id="3b669-116">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="3b669-116">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3b669-117">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="3b669-117">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3b669-118">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3b669-118">Return code</span></span>                                                                          | <span data-ttu-id="3b669-119">Description</span><span class="sxs-lookup"><span data-stu-id="3b669-119">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3b669-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3b669-120"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3b669-121">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="3b669-121">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3b669-122">備註</span><span class="sxs-lookup"><span data-stu-id="3b669-122">Remarks</span></span>

<span data-ttu-id="3b669-123">無。</span><span class="sxs-lookup"><span data-stu-id="3b669-123">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b669-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b669-124">Requirements</span></span>



| <span data-ttu-id="3b669-125">需求</span><span class="sxs-lookup"><span data-stu-id="3b669-125">Requirement</span></span> | <span data-ttu-id="3b669-126">值</span><span class="sxs-lookup"><span data-stu-id="3b669-126">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3b669-127">標頭</span><span class="sxs-lookup"><span data-stu-id="3b669-127">Header</span></span><br/> | <dl> <span data-ttu-id="3b669-128"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="3b669-128"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b669-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b669-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b669-130">**IWMDRMNetReceiver 介面**</span><span class="sxs-lookup"><span data-stu-id="3b669-130">**IWMDRMNetReceiver Interface**</span></span>](iwmdrmnetreceiver.md)
</dt> <dt>

[<span data-ttu-id="3b669-131">**IWMDRMNetReceiver：:P rocessRegistrationResponse**</span><span class="sxs-lookup"><span data-stu-id="3b669-131">**IWMDRMNetReceiver::ProcessRegistrationResponse**</span></span>](iwmdrmnetreceiver-processregistrationresponse.md)
</dt> </dl>

 

 





