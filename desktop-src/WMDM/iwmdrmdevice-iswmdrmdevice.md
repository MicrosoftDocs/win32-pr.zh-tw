---
title: IWMDRMDevice IsWMDRMDevice 方法
description: IsWMDRMDevice 方法會判斷裝置是否支援可攜式裝置的 Windows Media DRM 10。
ms.assetid: 247e7a77-e805-4848-893f-f5522c161232
keywords:
- IsWMDRMDevice 方法 windows Media 裝置管理員
- IsWMDRMDevice 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，IsWMDRMDevice 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.IsWMDRMDevice
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca9cb79598ea41a996748e383c8fdfc63364dd6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984037"
---
# <a name="iwmdrmdeviceiswmdrmdevice-method"></a><span data-ttu-id="ad183-106">IWMDRMDevice：： IsWMDRMDevice 方法</span><span class="sxs-lookup"><span data-stu-id="ad183-106">IWMDRMDevice::IsWMDRMDevice method</span></span>

<span data-ttu-id="ad183-107">**IsWMDRMDevice** 方法會判斷裝置是否支援可攜式裝置的 WINDOWS Media DRM 10。</span><span class="sxs-lookup"><span data-stu-id="ad183-107">The **IsWMDRMDevice** method determines whether the device supports Windows Media DRM 10 for Portable Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad183-108">語法</span><span class="sxs-lookup"><span data-stu-id="ad183-108">Syntax</span></span>


```C++
HRESULT IsWMDRMDevice(
  [out] DWORD *pdwVersion
);
```



## <a name="parameters"></a><span data-ttu-id="ad183-109">參數</span><span class="sxs-lookup"><span data-stu-id="ad183-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad183-110">*pdwVersion* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ad183-110">*pdwVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad183-111">適用于可攜式裝置的 Windows Media DRM 10 版本，其值為0x00010000。</span><span class="sxs-lookup"><span data-stu-id="ad183-111">Version of Windows Media DRM 10 for Portable Devices, which has value of 0x00010000.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad183-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="ad183-112">Return value</span></span>

<span data-ttu-id="ad183-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="ad183-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ad183-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="ad183-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ad183-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ad183-115">Return code</span></span>                                                                          | <span data-ttu-id="ad183-116">Description</span><span class="sxs-lookup"><span data-stu-id="ad183-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ad183-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ad183-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ad183-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="ad183-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ad183-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad183-119">Requirements</span></span>



| <span data-ttu-id="ad183-120">需求</span><span class="sxs-lookup"><span data-stu-id="ad183-120">Requirement</span></span> | <span data-ttu-id="ad183-121">值</span><span class="sxs-lookup"><span data-stu-id="ad183-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad183-122">標頭</span><span class="sxs-lookup"><span data-stu-id="ad183-122">Header</span></span><br/>  | <dl> <span data-ttu-id="ad183-123"><dt>WMDDRMSP .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ad183-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="ad183-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="ad183-124">Library</span></span><br/> | <dl> <span data-ttu-id="ad183-125"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ad183-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad183-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad183-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad183-127">**IWMDRMDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="ad183-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





