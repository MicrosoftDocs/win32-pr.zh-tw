---
title: 'IWMDRMLicenseManagement DeleteLicense 方法 (Wmdrmsdk .h) '
description: DeleteLicense 方法會移除暫時本機授權存放區中的授權。
ms.assetid: 0aa7143a-845a-41a4-8b3c-a04c68ee280a
keywords:
- DeleteLicense 方法 windows Media 格式
- DeleteLicense 方法 windows Media Format，IWMDRMLicenseManagement 介面
- IWMDRMLicenseManagement 介面 windows Media Format，DeleteLicense 方法
topic_type:
- apiref
api_name:
- IWMDRMLicenseManagement.DeleteLicense
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d5b52f6277459f147285f46fc791669e56061a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981639"
---
# <a name="iwmdrmlicensemanagementdeletelicense-method"></a><span data-ttu-id="34037-106">IWMDRMLicenseManagement：:D eleteLicense 方法</span><span class="sxs-lookup"><span data-stu-id="34037-106">IWMDRMLicenseManagement::DeleteLicense method</span></span>

<span data-ttu-id="34037-107">**DeleteLicense** 方法會移除暫時本機授權存放區中的授權。</span><span class="sxs-lookup"><span data-stu-id="34037-107">The **DeleteLicense** method removes a license from the temporary local license store.</span></span>

## <a name="syntax"></a><span data-ttu-id="34037-108">語法</span><span class="sxs-lookup"><span data-stu-id="34037-108">Syntax</span></span>


```C++
HRESULT DeleteLicense(
  [in] BSTR  bstrKID,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="34037-109">參數</span><span class="sxs-lookup"><span data-stu-id="34037-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="34037-110">*bstrKID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="34037-110">*bstrKID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34037-111">金鑰識別碼 (要刪除的授權小孩) 。</span><span class="sxs-lookup"><span data-stu-id="34037-111">Key ID (KID) of the license to be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="34037-112">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="34037-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="34037-113">授權刪除選項旗標。</span><span class="sxs-lookup"><span data-stu-id="34037-113">License deletion option flags.</span></span> <span data-ttu-id="34037-114">設定為下表中的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="34037-114">Set to one of the values in the following table.</span></span>



| <span data-ttu-id="34037-115">值</span><span class="sxs-lookup"><span data-stu-id="34037-115">Value</span></span>                                    | <span data-ttu-id="34037-116">描述</span><span class="sxs-lookup"><span data-stu-id="34037-116">Description</span></span>                                                                                                                                                                                           |
|------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="34037-117">\_立即刪除 WMDRM 的 \_ 授權 \_</span><span class="sxs-lookup"><span data-stu-id="34037-117">WMDRM\_DELETE\_LICENSE\_IMMEDIATELY</span></span>      | <span data-ttu-id="34037-118">指定應立即從存放區移除授權。</span><span class="sxs-lookup"><span data-stu-id="34037-118">Specifies that the license should be removed from the store immediately.</span></span>                                                                                                                              |
| <span data-ttu-id="34037-119">\_清除的 WMDRM 刪除 \_ 授權 \_ 標記 \_ \_</span><span class="sxs-lookup"><span data-stu-id="34037-119">WMDRM\_DELETE\_LICENSE\_MARK\_FOR\_PURGE</span></span> | <span data-ttu-id="34037-120">指定應標示為要刪除的授權，但在呼叫 [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) 方法之前，不應該從存放區中移除。</span><span class="sxs-lookup"><span data-stu-id="34037-120">Specifies that the license should be marked for deletion, but should not be removed from the store until the [**CleanLicenseStore**](iwmdrmlicensemanagement-cleanlicensestore.md) method is called.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="34037-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="34037-121">Return value</span></span>

<span data-ttu-id="34037-122">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="34037-122">The method returns an **HRESULT**.</span></span> <span data-ttu-id="34037-123">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="34037-123">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="34037-124">傳回碼</span><span class="sxs-lookup"><span data-stu-id="34037-124">Return code</span></span>                                                                                            | <span data-ttu-id="34037-125">Description</span><span class="sxs-lookup"><span data-stu-id="34037-125">Description</span></span>                                                                                                         |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="34037-126"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="34037-126"><dt>**S\_OK**</dt></span></span> </dl>                   | <span data-ttu-id="34037-127">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="34037-127">The method succeeded.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="34037-128"><dt>**DRM \_ E \_ LICENSENOTFOUND**</dt></span><span class="sxs-lookup"><span data-stu-id="34037-128"><dt>**DRM\_E\_LICENSENOTFOUND**</dt></span></span> </dl> | <span data-ttu-id="34037-129">指定的授權不存在於存放區中。</span><span class="sxs-lookup"><span data-stu-id="34037-129">The specified license does not exist in the store.</span></span><br/> <span data-ttu-id="34037-130">-或-</span><span class="sxs-lookup"><span data-stu-id="34037-130">- OR -</span></span><br/> <span data-ttu-id="34037-131">找不到存放區。</span><span class="sxs-lookup"><span data-stu-id="34037-131">The store was not found.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="34037-132">備註</span><span class="sxs-lookup"><span data-stu-id="34037-132">Remarks</span></span>

<span data-ttu-id="34037-133">若要從永久本機授權存放區刪除授權，您必須使用授權撤銷。</span><span class="sxs-lookup"><span data-stu-id="34037-133">To delete licenses from the permanent local license store, you must use license revocation.</span></span>

## <a name="requirements"></a><span data-ttu-id="34037-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="34037-134">Requirements</span></span>



| <span data-ttu-id="34037-135">需求</span><span class="sxs-lookup"><span data-stu-id="34037-135">Requirement</span></span> | <span data-ttu-id="34037-136">值</span><span class="sxs-lookup"><span data-stu-id="34037-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="34037-137">標頭</span><span class="sxs-lookup"><span data-stu-id="34037-137">Header</span></span><br/>  | <dl> <span data-ttu-id="34037-138"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="34037-138"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="34037-139">程式庫</span><span class="sxs-lookup"><span data-stu-id="34037-139">Library</span></span><br/> | <dl> <span data-ttu-id="34037-140"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="34037-140"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="34037-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="34037-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="34037-142">**IWMDRMLicenseManagement 介面**</span><span class="sxs-lookup"><span data-stu-id="34037-142">**IWMDRMLicenseManagement Interface**</span></span>](iwmdrmlicensemanagement.md)
</dt> </dl>

 

 





