---
title: 'IWMDRMLicense GetLicenseProperty 方法 (Wmdrmsdk .h) '
description: GetLicenseProperty 方法會從目前的授權抓取屬性。
ms.assetid: 5431f849-b37e-40b7-8bdb-ee30948aeff1
keywords:
- GetLicenseProperty 方法 windows Media 格式
- GetLicenseProperty 方法 windows Media Format，IWMDRMLicense 介面
- IWMDRMLicense 介面 windows Media Format，GetLicenseProperty 方法
topic_type:
- apiref
api_name:
- IWMDRMLicense.GetLicenseProperty
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bf7fe91c57b9c69934f093cdd504b5e6d35efb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978623"
---
# <a name="iwmdrmlicensegetlicenseproperty-method"></a><span data-ttu-id="375e1-106">IWMDRMLicense：： GetLicenseProperty 方法</span><span class="sxs-lookup"><span data-stu-id="375e1-106">IWMDRMLicense::GetLicenseProperty method</span></span>

<span data-ttu-id="375e1-107">**GetLicenseProperty** 方法會從目前的授權抓取屬性。</span><span class="sxs-lookup"><span data-stu-id="375e1-107">The **GetLicenseProperty** method retrieves a property from the current license.</span></span>

## <a name="syntax"></a><span data-ttu-id="375e1-108">語法</span><span class="sxs-lookup"><span data-stu-id="375e1-108">Syntax</span></span>


```C++
HRESULT GetLicenseProperty(
  [in]  BSTR        bstrName,
  [out] PROPVARIANT *ppropVariant
);
```



## <a name="parameters"></a><span data-ttu-id="375e1-109">參數</span><span class="sxs-lookup"><span data-stu-id="375e1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="375e1-110">*bstrName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="375e1-110">*bstrName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="375e1-111">要取得之屬性的名稱。</span><span class="sxs-lookup"><span data-stu-id="375e1-111">Name of the property to retrieve.</span></span> <span data-ttu-id="375e1-112">設定為下表中的其中一個常數：</span><span class="sxs-lookup"><span data-stu-id="375e1-112">Set to one of the constants in the following table:</span></span>



| <span data-ttu-id="375e1-113">常數</span><span class="sxs-lookup"><span data-stu-id="375e1-113">Constant</span></span>                   | <span data-ttu-id="375e1-114">描述</span><span class="sxs-lookup"><span data-stu-id="375e1-114">Description</span></span>                                                                                                          |
|----------------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="375e1-115">g \_ wszWMDRMNet \_ 撤銷</span><span class="sxs-lookup"><span data-stu-id="375e1-115">g\_wszWMDRMNet\_Revocation</span></span> | <span data-ttu-id="375e1-116">用來取得目前授權的 Windows Media DRM for Network 裝置撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="375e1-116">Use to get the Windows Media DRM for Network Devices revocation list for the current license.</span></span>                        |
| <span data-ttu-id="375e1-117">g \_ wszWMDRM \_ SAPLEVEL</span><span class="sxs-lookup"><span data-stu-id="375e1-117">g\_wszWMDRM\_SAPLEVEL</span></span>      | <span data-ttu-id="375e1-118">使用可取得 (SAP) 層級所需的安全音訊路徑，以播放目前授權所涵蓋的內容。</span><span class="sxs-lookup"><span data-stu-id="375e1-118">Use to get the Secure Audio Path (SAP) level required to play content covered by the current license.</span></span>                |
| <span data-ttu-id="375e1-119">g \_ wszWMDRM \_ SAPRequired</span><span class="sxs-lookup"><span data-stu-id="375e1-119">g\_wszWMDRM\_SAPRequired</span></span>   | <span data-ttu-id="375e1-120">使用來確定目前的授權是否需要使用 SAP 來播放內容。</span><span class="sxs-lookup"><span data-stu-id="375e1-120">Use to ascertain whether the current license requires SAP be used to play the content.</span></span>                               |
| <span data-ttu-id="375e1-121">g \_ wszWMDRM \_ SOURCEID</span><span class="sxs-lookup"><span data-stu-id="375e1-121">g\_wszWMDRM\_SOURCEID</span></span>      | <span data-ttu-id="375e1-122">用來取得目前授權的來源識別碼。</span><span class="sxs-lookup"><span data-stu-id="375e1-122">Use to get the source identifier for the current license.</span></span>                                                            |
| <span data-ttu-id="375e1-123">g \_ wszWMDRM \_ 優先順序</span><span class="sxs-lookup"><span data-stu-id="375e1-123">g\_wszWMDRM\_PRIORITY</span></span>      | <span data-ttu-id="375e1-124">使用以取得目前授權的優先權。</span><span class="sxs-lookup"><span data-stu-id="375e1-124">Use to get the priority of the current license.</span></span> <span data-ttu-id="375e1-125">較高優先順序的授權會在較低優先順序的授權之前套用。</span><span class="sxs-lookup"><span data-stu-id="375e1-125">Higher priority licenses are applied before lower priority licenses.</span></span> |
| <span data-ttu-id="375e1-126">g \_ wszWMDRM \_ UplinkID</span><span class="sxs-lookup"><span data-stu-id="375e1-126">g\_wszWMDRM\_UplinkID</span></span>      | <span data-ttu-id="375e1-127">用來取得目前授權所屬授權鏈中根授權的金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="375e1-127">Use to get the key ID of the root license in the license chain that the current license belongs to.</span></span>                  |



 

</dd> <dt>

<span data-ttu-id="375e1-128">*ppropVariant* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="375e1-128">*ppropVariant* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="375e1-129">接收屬性值。</span><span class="sxs-lookup"><span data-stu-id="375e1-129">Receives the property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="375e1-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="375e1-130">Return value</span></span>

<span data-ttu-id="375e1-131">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="375e1-131">The method returns an **HRESULT**.</span></span> <span data-ttu-id="375e1-132">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="375e1-132">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="375e1-133">傳回碼</span><span class="sxs-lookup"><span data-stu-id="375e1-133">Return code</span></span>                                                                          | <span data-ttu-id="375e1-134">Description</span><span class="sxs-lookup"><span data-stu-id="375e1-134">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="375e1-135"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="375e1-135"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="375e1-136">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="375e1-136">The method succeeded.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="375e1-137">備註</span><span class="sxs-lookup"><span data-stu-id="375e1-137">Remarks</span></span>

<span data-ttu-id="375e1-138">無。</span><span class="sxs-lookup"><span data-stu-id="375e1-138">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="375e1-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="375e1-139">Requirements</span></span>



| <span data-ttu-id="375e1-140">需求</span><span class="sxs-lookup"><span data-stu-id="375e1-140">Requirement</span></span> | <span data-ttu-id="375e1-141">值</span><span class="sxs-lookup"><span data-stu-id="375e1-141">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="375e1-142">標頭</span><span class="sxs-lookup"><span data-stu-id="375e1-142">Header</span></span><br/>  | <dl> <span data-ttu-id="375e1-143"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="375e1-143"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="375e1-144">程式庫</span><span class="sxs-lookup"><span data-stu-id="375e1-144">Library</span></span><br/> | <dl> <span data-ttu-id="375e1-145"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="375e1-145"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="375e1-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="375e1-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="375e1-147">**GetLicense**</span><span class="sxs-lookup"><span data-stu-id="375e1-147">**GetLicense**</span></span>](iwmdrmlicense-getlicense.md)
</dt> <dt>

[<span data-ttu-id="375e1-148">**IWMDRMLicense 介面**</span><span class="sxs-lookup"><span data-stu-id="375e1-148">**IWMDRMLicense Interface**</span></span>](iwmdrmlicense.md)
</dt> </dl>

 

 





