---
title: 'IWMDRMDecrypt 解密方法 (Wmdrmsdk .h) '
description: 解密方法會就地解密資料緩衝區。
ms.assetid: ca0a5b2f-d25f-423e-8956-fca264399083
keywords:
- 解密方法 windows 媒體格式
- 解密方法 windows Media Format，IWMDRMDecrypt 介面
- IWMDRMDecrypt 介面 windows 媒體格式，解密方法
topic_type:
- apiref
api_name:
- IWMDRMDecrypt.Decrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb3c1437bc4b4d2f442c61e54f238f176adf66b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986577"
---
# <a name="iwmdrmdecryptdecrypt-method"></a><span data-ttu-id="b2046-106">IWMDRMDecrypt：:D ecrypt 方法</span><span class="sxs-lookup"><span data-stu-id="b2046-106">IWMDRMDecrypt::Decrypt method</span></span>

<span data-ttu-id="b2046-107">**解密** 方法會就地解密資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="b2046-107">The **Decrypt** method decrypts a data buffer in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2046-108">語法</span><span class="sxs-lookup"><span data-stu-id="b2046-108">Syntax</span></span>


```C++
HRESULT Decrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a><span data-ttu-id="b2046-109">參數</span><span class="sxs-lookup"><span data-stu-id="b2046-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2046-110">*>pbdata* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="b2046-110">*pbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="b2046-111">要解密的資料。</span><span class="sxs-lookup"><span data-stu-id="b2046-111">Data to be decrypted.</span></span> <span data-ttu-id="b2046-112">如果方法成功，此資料會在傳回時解密。</span><span class="sxs-lookup"><span data-stu-id="b2046-112">If the method succeeds, this data is decrypted on return.</span></span>

</dd> <dt>

<span data-ttu-id="b2046-113">*cbData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b2046-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2046-114">資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="b2046-114">Size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="b2046-115">*pWMCryptoData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b2046-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2046-116">[**WMDRMCryptoData**](wmdrmcryptodata.md)結構的指標，其中包含額外的參數。</span><span class="sxs-lookup"><span data-stu-id="b2046-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure containing extra parameters.</span></span> <span data-ttu-id="b2046-117">如果內容是使用預設參數進行加密，則可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="b2046-117">Can be **NULL** if the content was encrypted using the default parameters.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2046-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="b2046-118">Return value</span></span>

<span data-ttu-id="b2046-119">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="b2046-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="b2046-120">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="b2046-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="b2046-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="b2046-121">Return code</span></span>                                                                          | <span data-ttu-id="b2046-122">Description</span><span class="sxs-lookup"><span data-stu-id="b2046-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="b2046-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="b2046-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="b2046-124">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="b2046-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b2046-125">備註</span><span class="sxs-lookup"><span data-stu-id="b2046-125">Remarks</span></span>

<span data-ttu-id="b2046-126">無。</span><span class="sxs-lookup"><span data-stu-id="b2046-126">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2046-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="b2046-127">Requirements</span></span>



| <span data-ttu-id="b2046-128">需求</span><span class="sxs-lookup"><span data-stu-id="b2046-128">Requirement</span></span> | <span data-ttu-id="b2046-129">值</span><span class="sxs-lookup"><span data-stu-id="b2046-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b2046-130">標頭</span><span class="sxs-lookup"><span data-stu-id="b2046-130">Header</span></span><br/> | <dl> <span data-ttu-id="b2046-131"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="b2046-131"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2046-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b2046-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2046-133">**IWMDRMDecrypt 介面**</span><span class="sxs-lookup"><span data-stu-id="b2046-133">**IWMDRMDecrypt Interface**</span></span>](iwmdrmdecrypt.md)
</dt> <dt>

[<span data-ttu-id="b2046-134">**WMDRMCryptoData**</span><span class="sxs-lookup"><span data-stu-id="b2046-134">**WMDRMCryptoData**</span></span>](wmdrmcryptodata.md)
</dt> </dl>

 

 





