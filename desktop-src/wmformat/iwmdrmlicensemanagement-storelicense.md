---
title: 'IWMDRMLicenseManagement StoreLicense 方法 (Wmdrmsdk .h) '
description: StoreLicense 方法包含在本機授權存放區的本機 DRM 子系統以外產生的授權。
ms.assetid: 2190ff8c-8969-4f03-9f90-331bff8f4da2
keywords:
- StoreLicense 方法 windows Media 格式
- StoreLicense 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，StoreLicense 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.StoreLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fcfde6347e099ceb9fc168e1183cbd62c90f9b9c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990120"
---
# <a name="iwmdrmlicensemanagementstorelicense-method"></a><span data-ttu-id="d43d7-106">IWMDRMLicenseManagement：： StoreLicense 方法</span><span class="sxs-lookup"><span data-stu-id="d43d7-106">IWMDRMLicenseManagement::StoreLicense method</span></span>

<span data-ttu-id="d43d7-107">**StoreLicense** 方法包含在本機授權存放區的本機 DRM 子系統以外產生的授權。</span><span class="sxs-lookup"><span data-stu-id="d43d7-107">The **StoreLicense** method includes a license that was generated outside of the local DRM subsystem in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="d43d7-108">語法</span><span class="sxs-lookup"><span data-stu-id="d43d7-108">Syntax</span></span>


```C++
HRESULT StoreLicense(
  [in] BSTR bstrLicenseResponse
);
```



## <a name="parameters"></a><span data-ttu-id="d43d7-109">參數</span><span class="sxs-lookup"><span data-stu-id="d43d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d43d7-110">*bstrLicenseResponse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d43d7-110">*bstrLicenseResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d43d7-111">要解碼並新增至本機授權存放區的授權回應字串。</span><span class="sxs-lookup"><span data-stu-id="d43d7-111">License response string to be decoded and added to the local license store.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d43d7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d43d7-112">Return value</span></span>

<span data-ttu-id="d43d7-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="d43d7-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d43d7-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="d43d7-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d43d7-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d43d7-115">Return code</span></span>                                                                          | <span data-ttu-id="d43d7-116">Description</span><span class="sxs-lookup"><span data-stu-id="d43d7-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d43d7-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d43d7-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d43d7-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="d43d7-118">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d43d7-119">備註</span><span class="sxs-lookup"><span data-stu-id="d43d7-119">Remarks</span></span>

<span data-ttu-id="d43d7-120">您可以使用此方法，將您建立的 XMR 授權新增至本機授權存放區。</span><span class="sxs-lookup"><span data-stu-id="d43d7-120">You can use this method to add XMR licenses that you have created to the local license store.</span></span>

## <a name="requirements"></a><span data-ttu-id="d43d7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d43d7-121">Requirements</span></span>



| <span data-ttu-id="d43d7-122">需求</span><span class="sxs-lookup"><span data-stu-id="d43d7-122">Requirement</span></span> | <span data-ttu-id="d43d7-123">值</span><span class="sxs-lookup"><span data-stu-id="d43d7-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d43d7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d43d7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d43d7-125"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="d43d7-125"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="d43d7-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="d43d7-126">Library</span></span><br/> | <dl> <span data-ttu-id="d43d7-127"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d43d7-127"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d43d7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d43d7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d43d7-129">**IWMDRMLicenseManagement 介面**</span><span class="sxs-lookup"><span data-stu-id="d43d7-129">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





