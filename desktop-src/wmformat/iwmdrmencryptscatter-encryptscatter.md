---
title: 'IWMDRMEncryptScatter EncryptScatter 方法 (Wmdrmsdk .h) '
description: EncryptScatter 方法會 unscrambles 和加密資料。
ms.assetid: e7f87aac-387b-4483-956e-bfbca0cec0f2
keywords:
- EncryptScatter 方法 windows Media 格式
- EncryptScatter 方法 windows Media Format，IWMDRMEncryptScatter 介面
- IWMDRMEncryptScatter 介面 windows Media Format，EncryptScatter 方法
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.EncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58b2d1d6182aed55b60aa1cedfbce5dd870691bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997443"
---
# <a name="iwmdrmencryptscatterencryptscatter-method"></a><span data-ttu-id="8479e-106">IWMDRMEncryptScatter：： EncryptScatter 方法</span><span class="sxs-lookup"><span data-stu-id="8479e-106">IWMDRMEncryptScatter::EncryptScatter method</span></span>

<span data-ttu-id="8479e-107">**EncryptScatter** 方法會 unscrambles 和加密資料。</span><span class="sxs-lookup"><span data-stu-id="8479e-107">The **EncryptScatter** method unscrambles and encrypts data.</span></span>

## <a name="syntax"></a><span data-ttu-id="8479e-108">語法</span><span class="sxs-lookup"><span data-stu-id="8479e-108">Syntax</span></span>


```C++
HRESULT EncryptScatter(
  [in]  DWORD                       cBlocks,
  [in]  WMDRM_ENCRYPT_SCATTER_BLOCK *rgBlocks,
  [in]  WMDRMCryptoData             *pWMCryptoData,
  [in]  DWORD                       cbOutput,
  [out] BYTE                        *pbOutput
);
```



## <a name="parameters"></a><span data-ttu-id="8479e-109">參數</span><span class="sxs-lookup"><span data-stu-id="8479e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8479e-110">*cBlocks* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8479e-110">*cBlocks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8479e-111">*RgBlocks* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="8479e-111">Number of elements in the *rgBlocks* array.</span></span>

</dd> <dt>

<span data-ttu-id="8479e-112">*rgBlocks* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8479e-112">*rgBlocks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8479e-113">一或多個 [**WMDRM \_ 加密 \_ 散佈 \_ 區塊**](wmdrm-encrypt-scatter-block.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="8479e-113">Array of one or more [**WMDRM\_ENCRYPT\_SCATTER\_BLOCK**](wmdrm-encrypt-scatter-block.md) structures.</span></span> <span data-ttu-id="8479e-114">每個元素會描述要 unscrambled 和加密的資料區塊。</span><span class="sxs-lookup"><span data-stu-id="8479e-114">Each element describes a block of data to be unscrambled and encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="8479e-115">*pWMCryptoData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8479e-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8479e-116">包含加密參數之 [**WMDRMCryptoData**](wmdrmcryptodata.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="8479e-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure that contains encryption parameters.</span></span> <span data-ttu-id="8479e-117">設定為 **Null** 以使用預設參數。</span><span class="sxs-lookup"><span data-stu-id="8479e-117">Set to **NULL** to use the default parameters.</span></span>

</dd> <dt>

<span data-ttu-id="8479e-118">*cbOutput* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8479e-118">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8479e-119">傳遞為 *pbOutput* 的輸出資料緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="8479e-119">Size of the output data buffer passed as *pbOutput*.</span></span>

</dd> <dt>

<span data-ttu-id="8479e-120">*pbOutput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8479e-120">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8479e-121">輸出緩衝區。</span><span class="sxs-lookup"><span data-stu-id="8479e-121">Output buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8479e-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="8479e-122">Return value</span></span>

<span data-ttu-id="8479e-123">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="8479e-123">The method returns an **HRESULT**.</span></span> <span data-ttu-id="8479e-124">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="8479e-124">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="8479e-125">傳回碼</span><span class="sxs-lookup"><span data-stu-id="8479e-125">Return code</span></span>                                                                          | <span data-ttu-id="8479e-126">Description</span><span class="sxs-lookup"><span data-stu-id="8479e-126">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="8479e-127"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="8479e-127"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="8479e-128">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="8479e-128">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8479e-129">備註</span><span class="sxs-lookup"><span data-stu-id="8479e-129">Remarks</span></span>

<span data-ttu-id="8479e-130">無。</span><span class="sxs-lookup"><span data-stu-id="8479e-130">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="8479e-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="8479e-131">Requirements</span></span>



| <span data-ttu-id="8479e-132">需求</span><span class="sxs-lookup"><span data-stu-id="8479e-132">Requirement</span></span> | <span data-ttu-id="8479e-133">值</span><span class="sxs-lookup"><span data-stu-id="8479e-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8479e-134">標頭</span><span class="sxs-lookup"><span data-stu-id="8479e-134">Header</span></span><br/> | <dl> <span data-ttu-id="8479e-135"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="8479e-135"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8479e-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8479e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8479e-137">**InitEncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="8479e-137">**InitEncryptScatter**</span></span>](iwmdrmencryptscatter-initencryptscatter.md)
</dt> <dt>

[<span data-ttu-id="8479e-138">**IWMDRMEncryptScatter 介面**</span><span class="sxs-lookup"><span data-stu-id="8479e-138">**IWMDRMEncryptScatter Interface**</span></span>](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





