---
title: IWMDRMDevice SetLicenseResponse 方法
description: SetLicenseResponse 方法會設定授權回應。
ms.assetid: 1ef3ba9d-d14c-4a20-92d6-0bcb604fd9e2
keywords:
- SetLicenseResponse 方法 windows Media 裝置管理員
- SetLicenseResponse 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，SetLicenseResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetLicenseResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f32a2d27fabe45081b13d658e49171af035b8cc6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982589"
---
# <a name="iwmdrmdevicesetlicenseresponse-method"></a><span data-ttu-id="d88d7-106">IWMDRMDevice：： SetLicenseResponse 方法</span><span class="sxs-lookup"><span data-stu-id="d88d7-106">IWMDRMDevice::SetLicenseResponse method</span></span>

<span data-ttu-id="d88d7-107">**SetLicenseResponse** 方法會設定授權回應。</span><span class="sxs-lookup"><span data-stu-id="d88d7-107">The **SetLicenseResponse** method sets the license response.</span></span>

## <a name="syntax"></a><span data-ttu-id="d88d7-108">語法</span><span class="sxs-lookup"><span data-stu-id="d88d7-108">Syntax</span></span>


```C++
HRESULT SetLicenseResponse(
  [in] BYTE  *pbResponse,
  [in] DWORD cbResponse
);
```



## <a name="parameters"></a><span data-ttu-id="d88d7-109">參數</span><span class="sxs-lookup"><span data-stu-id="d88d7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d88d7-110">*pbResponse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d88d7-110">*pbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d88d7-111">指定要設定的回應。</span><span class="sxs-lookup"><span data-stu-id="d88d7-111">Specifies the response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="d88d7-112">*cbResponse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d88d7-112">*cbResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d88d7-113">回應的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d88d7-113">Size of the response, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d88d7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d88d7-114">Return value</span></span>

<span data-ttu-id="d88d7-115">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="d88d7-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d88d7-116">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="d88d7-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d88d7-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d88d7-117">Return code</span></span>                                                                          | <span data-ttu-id="d88d7-118">Description</span><span class="sxs-lookup"><span data-stu-id="d88d7-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d88d7-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d88d7-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d88d7-120">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="d88d7-120">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d88d7-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="d88d7-121">Requirements</span></span>



| <span data-ttu-id="d88d7-122">需求</span><span class="sxs-lookup"><span data-stu-id="d88d7-122">Requirement</span></span> | <span data-ttu-id="d88d7-123">值</span><span class="sxs-lookup"><span data-stu-id="d88d7-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d88d7-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d88d7-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d88d7-125"><dt>WMDDRMSP .idl</dt></span><span class="sxs-lookup"><span data-stu-id="d88d7-125"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="d88d7-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="d88d7-126">Library</span></span><br/> | <dl> <span data-ttu-id="d88d7-127"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d88d7-127"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d88d7-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d88d7-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d88d7-129">**IWMDRMDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="d88d7-129">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





