---
title: 'IWMDRMLicense CreateEncryptor 方法 (Wmdrmsdk .h) '
description: CreateEncryptor 方法會使用目前授權的設定來建立加密程式物件。
ms.assetid: 570ba898-e846-4981-8ea8-ce16f2dad68a
keywords:
- CreateEncryptor 方法 windows Media 格式
- CreateEncryptor 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，CreateEncryptor 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.CreateEncryptor
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8031f412129f1d02cc4ef37c6af5f49a6c0b7532
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001825"
---
# <a name="iwmdrmlicensecreateencryptor-method"></a><span data-ttu-id="6cb24-106">IWMDRMLicense：： CreateEncryptor 方法</span><span class="sxs-lookup"><span data-stu-id="6cb24-106">IWMDRMLicense::CreateEncryptor method</span></span>

<span data-ttu-id="6cb24-107">**CreateEncryptor** 方法會使用目前授權的設定來建立加密程式物件。</span><span class="sxs-lookup"><span data-stu-id="6cb24-107">The **CreateEncryptor** method creates an encryptor object using the settings of the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cb24-108">語法</span><span class="sxs-lookup"><span data-stu-id="6cb24-108">Syntax</span></span>


```C++
HRESULT CreateEncryptor(
  [out] IWMDRMEncrypt **ppEncryptor
);
```



## <a name="parameters"></a><span data-ttu-id="6cb24-109">參數</span><span class="sxs-lookup"><span data-stu-id="6cb24-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cb24-110">*ppEncryptor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6cb24-110">*ppEncryptor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cb24-111">接收新建立物件之 [**IWMDRMEncrypt**](iwmdrmencrypt.md) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="6cb24-111">Receives a pointer to the [**IWMDRMEncrypt**](iwmdrmencrypt.md) interface of the newly created object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cb24-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6cb24-112">Return value</span></span>

<span data-ttu-id="6cb24-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="6cb24-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6cb24-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="6cb24-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6cb24-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6cb24-115">Return code</span></span>                                                                                                | <span data-ttu-id="6cb24-116">Description</span><span class="sxs-lookup"><span data-stu-id="6cb24-116">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="6cb24-117"><dt>**NS \_ E \_ DRM \_ RIV \_ 太 \_ 小**</dt></span><span class="sxs-lookup"><span data-stu-id="6cb24-117"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="6cb24-118">需要更新的內容撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="6cb24-118">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="6cb24-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6cb24-119"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="6cb24-120">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="6cb24-120">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="6cb24-121">備註</span><span class="sxs-lookup"><span data-stu-id="6cb24-121">Remarks</span></span>

<span data-ttu-id="6cb24-122">無。</span><span class="sxs-lookup"><span data-stu-id="6cb24-122">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cb24-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cb24-123">Requirements</span></span>



| <span data-ttu-id="6cb24-124">需求</span><span class="sxs-lookup"><span data-stu-id="6cb24-124">Requirement</span></span> | <span data-ttu-id="6cb24-125">值</span><span class="sxs-lookup"><span data-stu-id="6cb24-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6cb24-126">標頭</span><span class="sxs-lookup"><span data-stu-id="6cb24-126">Header</span></span><br/> | <dl> <span data-ttu-id="6cb24-127"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="6cb24-127"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cb24-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cb24-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cb24-129">**CreateDecryptor**</span><span class="sxs-lookup"><span data-stu-id="6cb24-129">**CreateDecryptor**</span></span>](iwmdrmlicense-createdecryptor.md)
</dt> <dt>

[<span data-ttu-id="6cb24-130">**IWMDRMLicense 介面**</span><span class="sxs-lookup"><span data-stu-id="6cb24-130">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





