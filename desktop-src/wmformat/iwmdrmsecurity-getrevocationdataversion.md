---
title: 'IWMDRMSecurity GetRevocationDataVersion 方法 (Wmdrmsdk .h) '
description: GetRevocationDataVersion 方法會抓取本機存放區中憑證撤銷清單的版本號碼。
ms.assetid: 2fa13b38-02c2-4c81-938b-409cadca00fb
keywords:
- GetRevocationDataVersion 方法 windows Media 格式
- GetRevocationDataVersion 方法 windows Media Format，IWMDRMSecurity 介面
- IWMDRMSecurity 介面 windows Media Format，GetRevocationDataVersion 方法
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetRevocationDataVersion
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 705f02622b7298134328b513aa038804995eb1c1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975986"
---
# <a name="iwmdrmsecuritygetrevocationdataversion-method"></a><span data-ttu-id="cf691-106">IWMDRMSecurity：： GetRevocationDataVersion 方法</span><span class="sxs-lookup"><span data-stu-id="cf691-106">IWMDRMSecurity::GetRevocationDataVersion method</span></span>

<span data-ttu-id="cf691-107">**GetRevocationDataVersion** 方法會抓取本機存放區中憑證撤銷清單的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="cf691-107">The **GetRevocationDataVersion** method retrieves the version number of a certificate revocation list in the local store.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf691-108">語法</span><span class="sxs-lookup"><span data-stu-id="cf691-108">Syntax</span></span>


```C++
HRESULT GetRevocationDataVersion(
  [in]  REFGUID   f_guidRevocationType,
  [out] ULONGLONG *f_pdwCRLVersion
);
```



## <a name="parameters"></a><span data-ttu-id="cf691-109">參數</span><span class="sxs-lookup"><span data-stu-id="cf691-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf691-110">*f \_ guidRevocationType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf691-110">*f\_guidRevocationType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf691-111">指定撤銷清單類型的 GUID。</span><span class="sxs-lookup"><span data-stu-id="cf691-111">GUID specifying the type of revocation list.</span></span> <span data-ttu-id="cf691-112">設定為下表中的其中一個常數。</span><span class="sxs-lookup"><span data-stu-id="cf691-112">Set to one of the constants in the following table.</span></span>



| <span data-ttu-id="cf691-113">GUID 常數</span><span class="sxs-lookup"><span data-stu-id="cf691-113">GUID constant</span></span>                 | <span data-ttu-id="cf691-114">Description</span><span class="sxs-lookup"><span data-stu-id="cf691-114">Description</span></span>                                                                      |
|-------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cf691-115">WMDRM \_ REVOCATIONTYPE \_ 應用程式</span><span class="sxs-lookup"><span data-stu-id="cf691-115">WMDRM\_REVOCATIONTYPE\_APP</span></span>    | <span data-ttu-id="cf691-116">指定應用程式憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="cf691-116">Specifies the application certificate revocation list.</span></span>                           |
| <span data-ttu-id="cf691-117">WMDRM \_ REVOCATIONTYPE \_ 裝置</span><span class="sxs-lookup"><span data-stu-id="cf691-117">WMDRM\_REVOCATIONTYPE\_DEVICE</span></span> | <span data-ttu-id="cf691-118">指定裝置憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="cf691-118">Specifies the device certificate revocation list.</span></span>                                |
| <span data-ttu-id="cf691-119">WMDRM \_ REVOCATIONTYPE \_ CARDEA</span><span class="sxs-lookup"><span data-stu-id="cf691-119">WMDRM\_REVOCATIONTYPE\_CARDEA</span></span> | <span data-ttu-id="cf691-120">指定「網路裝置的 Windows Media DRM」憑證撤銷清單。</span><span class="sxs-lookup"><span data-stu-id="cf691-120">Specifies the Windows Media DRM for Network Devices certificate revocation list.</span></span> |



 

</dd> <dt>

<span data-ttu-id="cf691-121">*f \_ pdwCRLVersion* \[ 輸出\]</span><span class="sxs-lookup"><span data-stu-id="cf691-121">*f\_pdwCRLVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf691-122">接收版本號碼的變數。</span><span class="sxs-lookup"><span data-stu-id="cf691-122">Variable that receives the version number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf691-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="cf691-123">Return value</span></span>

<span data-ttu-id="cf691-124">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="cf691-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="cf691-125">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="cf691-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="cf691-126">傳回碼</span><span class="sxs-lookup"><span data-stu-id="cf691-126">Return code</span></span>                                                                          | <span data-ttu-id="cf691-127">Description</span><span class="sxs-lookup"><span data-stu-id="cf691-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="cf691-128"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="cf691-129">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="cf691-129">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="cf691-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="cf691-130">Requirements</span></span>



| <span data-ttu-id="cf691-131">需求</span><span class="sxs-lookup"><span data-stu-id="cf691-131">Requirement</span></span> | <span data-ttu-id="cf691-132">值</span><span class="sxs-lookup"><span data-stu-id="cf691-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf691-133">標頭</span><span class="sxs-lookup"><span data-stu-id="cf691-133">Header</span></span><br/>  | <dl> <span data-ttu-id="cf691-134"><dt>Wmdrmsdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-134"><dt>Wmdrmsdk.h</dt></span></span> </dl>   |
| <span data-ttu-id="cf691-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="cf691-135">Library</span></span><br/> | <dl> <span data-ttu-id="cf691-136"><dt>Wmdrmsdk .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cf691-136"><dt>Wmdrmsdk.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf691-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf691-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf691-138">**自動化元件撤銷和更新**</span><span class="sxs-lookup"><span data-stu-id="cf691-138">**Automated Component Revocation and Renewal**</span></span>](automated-component-revocation-and-renewal.md)
</dt> <dt>

[<span data-ttu-id="cf691-139">**GetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="cf691-139">**GetRevocationData**</span></span>](iwmdrmsecurity-getrevocationdata.md)
</dt> <dt>

[<span data-ttu-id="cf691-140">**IWMDRMSecurity 介面**</span><span class="sxs-lookup"><span data-stu-id="cf691-140">**IWMDRMSecurity Interface**</span></span>](iwmdrmsecurity.md)
</dt> <dt>

[<span data-ttu-id="cf691-141">**SetRevocationData**</span><span class="sxs-lookup"><span data-stu-id="cf691-141">**SetRevocationData**</span></span>](iwmdrmsecurity-setrevocationdata.md)
</dt> </dl>

 

 





