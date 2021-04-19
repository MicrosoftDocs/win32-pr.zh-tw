---
title: 'IWMDRMLicenseManagement CreateLicenseEnumeration 方法 (Wmdrmsdk .h) '
description: CreateLicenseEnumeration 方法會建立授權列舉值物件，讓您可以在本機授權存放區中取得授權的相關資訊。
ms.assetid: 48da1ef4-89bc-4cba-b5c9-0e202eb2986f
keywords:
- CreateLicenseEnumeration 方法 windows Media 格式
- CreateLicenseEnumeration 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，CreateLicenseEnumeration 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.CreateLicenseEnumeration
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bb75d21cc640da39c3679ac118ead629b24f719
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975968"
---
# <a name="iwmdrmlicensemanagementcreatelicenseenumeration-method"></a><span data-ttu-id="2c21f-106">IWMDRMLicenseManagement：： CreateLicenseEnumeration 方法</span><span class="sxs-lookup"><span data-stu-id="2c21f-106">IWMDRMLicenseManagement::CreateLicenseEnumeration method</span></span>

<span data-ttu-id="2c21f-107">**CreateLicenseEnumeration** 方法會建立授權列舉值物件，讓您可以在本機授權存放區中取得授權的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2c21f-107">The **CreateLicenseEnumeration** method creates a license enumerator object with which you can get information about licenses in the local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c21f-108">語法</span><span class="sxs-lookup"><span data-stu-id="2c21f-108">Syntax</span></span>


```C++
HRESULT CreateLicenseEnumeration(
  [in]  WMDRM_LICENSE_FILTER *pLicenseFilter,
  [out] IWMDRMLicense        **pEnumerator
);
```



## <a name="parameters"></a><span data-ttu-id="2c21f-109">參數</span><span class="sxs-lookup"><span data-stu-id="2c21f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2c21f-110">*pLicenseFilter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2c21f-110">*pLicenseFilter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2c21f-111">[**WMDRM \_ 授權 \_ 篩選**](wmdrm-license-filter.md)結構的指標，其中包含列舉值中授權清單的篩選參數。</span><span class="sxs-lookup"><span data-stu-id="2c21f-111">Pointer to a [**WMDRM\_LICENSE\_FILTER**](wmdrm-license-filter.md) structure containing the filtering parameters for the list of licenses in the enumerator.</span></span>

</dd> <dt>

<span data-ttu-id="2c21f-112">*pEnumerator* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2c21f-112">*pEnumerator* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2c21f-113">此指標會接收新建立的授權列舉值物件之 [**IWMDRMLicense**](iwmdrmlicense.md) 介面的位址。</span><span class="sxs-lookup"><span data-stu-id="2c21f-113">Pointer that receives the address of the [**IWMDRMLicense**](iwmdrmlicense.md) interface of the newly created license enumerator object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2c21f-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="2c21f-114">Return value</span></span>

<span data-ttu-id="2c21f-115">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="2c21f-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="2c21f-116">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="2c21f-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="2c21f-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="2c21f-117">Return code</span></span>                                                                                                | <span data-ttu-id="2c21f-118">Description</span><span class="sxs-lookup"><span data-stu-id="2c21f-118">Description</span></span>                                              |
|------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="2c21f-119"><dt>**NS \_ E \_ DRM \_ RIV \_ 太 \_ 小**</dt></span><span class="sxs-lookup"><span data-stu-id="2c21f-119"><dt>**NS\_E\_DRM\_RIV\_TOO\_SMALL**</dt></span></span> </dl> | <span data-ttu-id="2c21f-120">需要更新的內容撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="2c21f-120">An updated content revocation list is needed.</span></span><br/> |
| <dl> <span data-ttu-id="2c21f-121"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2c21f-121"><dt>**S\_OK**</dt></span></span> </dl>                       | <span data-ttu-id="2c21f-122">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="2c21f-122">The method succeeded.</span></span><br/>                         |



 

## <a name="remarks"></a><span data-ttu-id="2c21f-123">備註</span><span class="sxs-lookup"><span data-stu-id="2c21f-123">Remarks</span></span>

<span data-ttu-id="2c21f-124">無。</span><span class="sxs-lookup"><span data-stu-id="2c21f-124">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c21f-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c21f-125">Requirements</span></span>



| <span data-ttu-id="2c21f-126">需求</span><span class="sxs-lookup"><span data-stu-id="2c21f-126">Requirement</span></span> | <span data-ttu-id="2c21f-127">值</span><span class="sxs-lookup"><span data-stu-id="2c21f-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2c21f-128">標頭</span><span class="sxs-lookup"><span data-stu-id="2c21f-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2c21f-129"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="2c21f-129"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="2c21f-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="2c21f-130">Library</span></span><br/> | <dl> <span data-ttu-id="2c21f-131"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2c21f-131"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2c21f-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c21f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c21f-133">**列舉本機授權存放區中的授權**</span><span class="sxs-lookup"><span data-stu-id="2c21f-133">**Enumerating Licenses in the Local License Store**</span></span>](enumerating-licenses-in-the-local-license-store.md)
</dt> <dt>

[<span data-ttu-id="2c21f-134">**IWMDRMLicenseManagement 介面**</span><span class="sxs-lookup"><span data-stu-id="2c21f-134">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





