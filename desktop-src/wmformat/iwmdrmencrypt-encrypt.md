---
title: 'IWMDRMEncrypt Encrypt 方法 (Wmdrmsdk .h) '
description: Encrypt 方法會就地加密資料緩衝區。
ms.assetid: 9626f53e-3602-4369-99ed-fbcd8d5f4d9e
keywords:
- 加密方法 windows Media 格式
- 加密方法 windows Media Format，IWMDRMEncrypt 介面
- IWMDRMEncrypt 介面 windows 媒體格式，加密方法
topic_type:
- apiref
api_name:
- IWMDRMEncrypt.Encrypt
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13380b321b540cbb5edce3c03e422b49c7b90e54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999084"
---
# <a name="iwmdrmencryptencrypt-method"></a><span data-ttu-id="4087f-106">IWMDRMEncrypt：： Encrypt 方法</span><span class="sxs-lookup"><span data-stu-id="4087f-106">IWMDRMEncrypt::Encrypt method</span></span>

<span data-ttu-id="4087f-107">**Encrypt** 方法會就地加密資料緩衝區。</span><span class="sxs-lookup"><span data-stu-id="4087f-107">The **Encrypt** method encrypts a data buffer in place.</span></span>

## <a name="syntax"></a><span data-ttu-id="4087f-108">語法</span><span class="sxs-lookup"><span data-stu-id="4087f-108">Syntax</span></span>


```C++
HRESULT Encrypt(
  [in, out] BYTE            *pbData,
  [in]      DWORD           cbData,
  [in]      WMDRMCryptoData *pWMCryptoData
);
```



## <a name="parameters"></a><span data-ttu-id="4087f-109">參數</span><span class="sxs-lookup"><span data-stu-id="4087f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4087f-110">*>pbdata* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="4087f-110">*pbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="4087f-111">要加密的資料。</span><span class="sxs-lookup"><span data-stu-id="4087f-111">Data to encrypt.</span></span> <span data-ttu-id="4087f-112">如果方法成功，資料會在傳回時加密。</span><span class="sxs-lookup"><span data-stu-id="4087f-112">If the method succeeds, the data is encrypted on return.</span></span>

</dd> <dt>

<span data-ttu-id="4087f-113">*cbData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4087f-113">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4087f-114">資料的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="4087f-114">Size of the data in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4087f-115">*pWMCryptoData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4087f-115">*pWMCryptoData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4087f-116">[**WMDRMCryptoData**](wmdrmcryptodata.md)結構的指標，其中包含額外的參數。</span><span class="sxs-lookup"><span data-stu-id="4087f-116">Pointer to a [**WMDRMCryptoData**](wmdrmcryptodata.md) structure containing extra parameters.</span></span> <span data-ttu-id="4087f-117">設定為 **Null** 以使用預設的加密值。</span><span class="sxs-lookup"><span data-stu-id="4087f-117">Set to **NULL** to use the default encryption values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4087f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="4087f-118">Return value</span></span>

<span data-ttu-id="4087f-119">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="4087f-119">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4087f-120">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="4087f-120">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4087f-121">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4087f-121">Return code</span></span>                                                                          | <span data-ttu-id="4087f-122">Description</span><span class="sxs-lookup"><span data-stu-id="4087f-122">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4087f-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4087f-123"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4087f-124">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="4087f-124">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="4087f-125">備註</span><span class="sxs-lookup"><span data-stu-id="4087f-125">Remarks</span></span>

<span data-ttu-id="4087f-126">無。</span><span class="sxs-lookup"><span data-stu-id="4087f-126">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="4087f-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="4087f-127">Requirements</span></span>



| <span data-ttu-id="4087f-128">需求</span><span class="sxs-lookup"><span data-stu-id="4087f-128">Requirement</span></span> | <span data-ttu-id="4087f-129">值</span><span class="sxs-lookup"><span data-stu-id="4087f-129">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4087f-130">標頭</span><span class="sxs-lookup"><span data-stu-id="4087f-130">Header</span></span><br/> | <dl> <span data-ttu-id="4087f-131"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="4087f-131"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4087f-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4087f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4087f-133">**IWMDRMEncrypt 介面**</span><span class="sxs-lookup"><span data-stu-id="4087f-133">**IWMDRMEncrypt Interface**</span></span>](iwmdrmencrypt.md)
</dt> <dt>

[<span data-ttu-id="4087f-134">**WMDRMCryptoData**</span><span class="sxs-lookup"><span data-stu-id="4087f-134">**WMDRMCryptoData**</span></span>](wmdrmcryptodata.md)
</dt> </dl>

 

 





