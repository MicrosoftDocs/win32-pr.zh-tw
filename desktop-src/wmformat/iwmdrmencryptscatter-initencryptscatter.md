---
title: 'IWMDRMEncryptScatter InitEncryptScatter 方法 (Wmdrmsdk .h) '
description: InitEncryptScatter 方法會初始化 IWMDRMEncryptScatter 介面以供使用。
ms.assetid: c5f2fa14-9465-4c53-bc42-ffcec34af083
keywords:
- InitEncryptScatter 方法 windows Media 格式
- InitEncryptScatter 方法 windows Media Format，IWMDRMEncryptScatter 介面
- IWMDRMEncryptScatter 介面 windows Media Format，InitEncryptScatter 方法
topic_type:
- apiref
api_name:
- IWMDRMEncryptScatter.InitEncryptScatter
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef788ecbe85defc7d3593f0c12c035e516f095eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997700"
---
# <a name="iwmdrmencryptscatterinitencryptscatter-method"></a><span data-ttu-id="821cc-106">IWMDRMEncryptScatter：： InitEncryptScatter 方法</span><span class="sxs-lookup"><span data-stu-id="821cc-106">IWMDRMEncryptScatter::InitEncryptScatter method</span></span>

<span data-ttu-id="821cc-107">**InitEncryptScatter** 方法會初始化 **IWMDRMEncryptScatter** 介面以供使用。</span><span class="sxs-lookup"><span data-stu-id="821cc-107">The **InitEncryptScatter** method initializes the **IWMDRMEncryptScatter** interface for use.</span></span>

## <a name="syntax"></a><span data-ttu-id="821cc-108">語法</span><span class="sxs-lookup"><span data-stu-id="821cc-108">Syntax</span></span>


```C++
HRESULT InitEncryptScatter(
  [in] DWORD                      cStreams,
  [in] WMDRM_ENCRYPT_SCATTER_INFO *rgInfos
);
```



## <a name="parameters"></a><span data-ttu-id="821cc-109">參數</span><span class="sxs-lookup"><span data-stu-id="821cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="821cc-110">*cStreams* \[在\]</span><span class="sxs-lookup"><span data-stu-id="821cc-110">*cStreams* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="821cc-111">*RgInfos* 陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="821cc-111">Number of elements in the *rgInfos* array.</span></span> <span data-ttu-id="821cc-112">這也是要加密的資料中包含的資料流程數目。</span><span class="sxs-lookup"><span data-stu-id="821cc-112">This is also the number of streams that are included in the data to be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="821cc-113">*rgInfos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="821cc-113">*rgInfos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="821cc-114">一或多個 [**WMDRM \_ 加密 \_ 散佈 \_ 資訊**](wmdrm-encrypt-scatter-info.md) 結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="821cc-114">Array of one or more [**WMDRM\_ENCRYPT\_SCATTER\_INFO**](wmdrm-encrypt-scatter-info.md) structures.</span></span> <span data-ttu-id="821cc-115">每個元素都包含資料流程的加密資訊。</span><span class="sxs-lookup"><span data-stu-id="821cc-115">Each element contains encryption information for a stream.</span></span> <span data-ttu-id="821cc-116">此陣列中的元素數目必須等於 *cStreams* 的值。</span><span class="sxs-lookup"><span data-stu-id="821cc-116">The number of elements in this array must be equal to the value of *cStreams*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="821cc-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="821cc-117">Return value</span></span>

<span data-ttu-id="821cc-118">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="821cc-118">The method returns an **HRESULT**.</span></span> <span data-ttu-id="821cc-119">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="821cc-119">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="821cc-120">傳回碼</span><span class="sxs-lookup"><span data-stu-id="821cc-120">Return code</span></span>                                                                          | <span data-ttu-id="821cc-121">Description</span><span class="sxs-lookup"><span data-stu-id="821cc-121">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="821cc-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="821cc-122"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="821cc-123">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="821cc-123">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="821cc-124">備註</span><span class="sxs-lookup"><span data-stu-id="821cc-124">Remarks</span></span>

<span data-ttu-id="821cc-125">無。</span><span class="sxs-lookup"><span data-stu-id="821cc-125">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="821cc-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="821cc-126">Requirements</span></span>



| <span data-ttu-id="821cc-127">需求</span><span class="sxs-lookup"><span data-stu-id="821cc-127">Requirement</span></span> | <span data-ttu-id="821cc-128">值</span><span class="sxs-lookup"><span data-stu-id="821cc-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="821cc-129">標頭</span><span class="sxs-lookup"><span data-stu-id="821cc-129">Header</span></span><br/> | <dl> <span data-ttu-id="821cc-130"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="821cc-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="821cc-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="821cc-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="821cc-132">**EncryptScatter**</span><span class="sxs-lookup"><span data-stu-id="821cc-132">**EncryptScatter**</span></span>](iwmdrmencryptscatter-encryptscatter.md)
</dt> <dt>

[<span data-ttu-id="821cc-133">**IWMDRMEncryptScatter 介面**</span><span class="sxs-lookup"><span data-stu-id="821cc-133">**IWMDRMEncryptScatter Interface**</span></span>](iwmdrmencryptscatter.md)
</dt> </dl>

 

 





