---
title: 'IWMDRMLicense CanPersist 方法 (Wmdrmsdk .h) '
description: CanPersist 方法會查詢授權是否可保存在本機授權存放區中。
ms.assetid: 040b30d8-4e47-44a3-8b09-e81cc30e8a53
keywords:
- CanPersist 方法 windows Media 格式
- CanPersist 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，CanPersist 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.CanPersist
api_location:
- Wmdrmsdk.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a7772dac73b99443626b1eeec6f5e90851f92c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998835"
---
# <a name="iwmdrmlicensecanpersist-method"></a><span data-ttu-id="64dd1-106">IWMDRMLicense：： CanPersist 方法</span><span class="sxs-lookup"><span data-stu-id="64dd1-106">IWMDRMLicense::CanPersist method</span></span>

<span data-ttu-id="64dd1-107">**CanPersist** 方法會查詢授權是否可保存在本機授權存放區中。</span><span class="sxs-lookup"><span data-stu-id="64dd1-107">The **CanPersist** method queries whether the license can be persisted on in a local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="64dd1-108">語法</span><span class="sxs-lookup"><span data-stu-id="64dd1-108">Syntax</span></span>


```C++
HRESULT CanPersist(
  [out] BOOL *pfCanPersist
);
```



## <a name="parameters"></a><span data-ttu-id="64dd1-109">參數</span><span class="sxs-lookup"><span data-stu-id="64dd1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64dd1-110">*pfCanPersist* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="64dd1-110">*pfCanPersist* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="64dd1-111">TRUE 表示可以保存授權。</span><span class="sxs-lookup"><span data-stu-id="64dd1-111">TRUE indicates that the license can be persisted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="64dd1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="64dd1-112">Return value</span></span>

<span data-ttu-id="64dd1-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="64dd1-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="64dd1-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="64dd1-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="64dd1-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="64dd1-115">Return code</span></span>                                                                          | <span data-ttu-id="64dd1-116">Description</span><span class="sxs-lookup"><span data-stu-id="64dd1-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="64dd1-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="64dd1-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="64dd1-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="64dd1-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="64dd1-119">備註</span><span class="sxs-lookup"><span data-stu-id="64dd1-119">Remarks</span></span>

<span data-ttu-id="64dd1-120">無。</span><span class="sxs-lookup"><span data-stu-id="64dd1-120">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="64dd1-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="64dd1-121">Requirements</span></span>



| <span data-ttu-id="64dd1-122">需求</span><span class="sxs-lookup"><span data-stu-id="64dd1-122">Requirement</span></span> | <span data-ttu-id="64dd1-123">值</span><span class="sxs-lookup"><span data-stu-id="64dd1-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="64dd1-124">標頭</span><span class="sxs-lookup"><span data-stu-id="64dd1-124">Header</span></span><br/> | <dl> <span data-ttu-id="64dd1-125"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="64dd1-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64dd1-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64dd1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64dd1-127">**IWMDRMLicense 介面**</span><span class="sxs-lookup"><span data-stu-id="64dd1-127">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





