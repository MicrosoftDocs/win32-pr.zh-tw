---
title: 'IWMDRMLicense CreateDecryptor 方法 (Wmdrmsdk .h) '
description: CreateDecryptor 方法會使用目前授權的設定來建立解密程式物件。
ms.assetid: 69b7f96b-a0d6-455e-8ef9-0faf9690cef1
keywords:
- CreateDecryptor 方法 windows Media 格式
- CreateDecryptor 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，CreateDecryptor 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateDecryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e987e7ffa3390462889b128f390934f05e64cdff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991521"
---
# <a name="iwmdrmlicensecreatedecryptor-method"></a><span data-ttu-id="c9ff5-106">IWMDRMLicense：： CreateDecryptor 方法</span><span class="sxs-lookup"><span data-stu-id="c9ff5-106">IWMDRMLicense::CreateDecryptor method</span></span>

<span data-ttu-id="c9ff5-107">**CreateDecryptor** 方法會使用目前授權的設定來建立解密程式物件。</span><span class="sxs-lookup"><span data-stu-id="c9ff5-107">The **CreateDecryptor** method creates a decryptor object using the settings of the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9ff5-108">語法</span><span class="sxs-lookup"><span data-stu-id="c9ff5-108">Syntax</span></span>


```C++
HRESULT CreateDecryptor(
  [out] IWMDRMDecrypt **ppDecryptor
);
```



## <a name="parameters"></a><span data-ttu-id="c9ff5-109">參數</span><span class="sxs-lookup"><span data-stu-id="c9ff5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9ff5-110">*ppDecryptor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c9ff5-110">*ppDecryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9ff5-111">接收新建立物件之 [**IWMDRMDecrypt**](iwmdrmdecrypt.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="c9ff5-111">Receives a pointer to the [**IWMDRMDecrypt**](iwmdrmdecrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9ff5-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c9ff5-112">Return value</span></span>

<span data-ttu-id="c9ff5-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="c9ff5-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="c9ff5-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="c9ff5-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="c9ff5-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="c9ff5-115">Return code</span></span>                                                                                                | <span data-ttu-id="c9ff5-116">Description</span><span class="sxs-lookup"><span data-stu-id="c9ff5-116">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="c9ff5-117"><dt>**NS \_ E \_ DRM \_ RIV \_ 太 \_ 小**</dt></span><span class="sxs-lookup"><span data-stu-id="c9ff5-117"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="c9ff5-118">需要更新的內容撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="c9ff5-118">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="c9ff5-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="c9ff5-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="c9ff5-120">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="c9ff5-120">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="c9ff5-121">備註</span><span class="sxs-lookup"><span data-stu-id="c9ff5-121">Remarks</span></span>

<span data-ttu-id="c9ff5-122">無。</span><span class="sxs-lookup"><span data-stu-id="c9ff5-122">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9ff5-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9ff5-123">Requirements</span></span>



| <span data-ttu-id="c9ff5-124">需求</span><span class="sxs-lookup"><span data-stu-id="c9ff5-124">Requirement</span></span> | <span data-ttu-id="c9ff5-125">值</span><span class="sxs-lookup"><span data-stu-id="c9ff5-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c9ff5-126">標頭</span><span class="sxs-lookup"><span data-stu-id="c9ff5-126">Header</span></span><br/> | <dl> <span data-ttu-id="c9ff5-127"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9ff5-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9ff5-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9ff5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9ff5-129">**CreateEncryptor**</span><span class="sxs-lookup"><span data-stu-id="c9ff5-129">**CreateEncryptor**</span></span>](iwmdrmlicense-createencryptor.md)
</dt> <dt>

[<span data-ttu-id="c9ff5-130">**IWMDRMLicense 介面**</span><span class="sxs-lookup"><span data-stu-id="c9ff5-130">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





