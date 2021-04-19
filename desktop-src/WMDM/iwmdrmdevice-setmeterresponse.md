---
title: IWMDRMDevice SetMeterResponse 方法
description: SetMeterResponse 方法會設定計量回應。
ms.assetid: 3f2e7d7c-6470-4d53-96b0-d3eebdb08329
keywords:
- SetMeterResponse 方法 windows Media 裝置管理員
- SetMeterResponse 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，SetMeterResponse 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.SetMeterResponse
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed70b158215eb831296ad083af8cd2c001cb38f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993318"
---
# <a name="iwmdrmdevicesetmeterresponse-method"></a><span data-ttu-id="39558-106">IWMDRMDevice：： SetMeterResponse 方法</span><span class="sxs-lookup"><span data-stu-id="39558-106">IWMDRMDevice::SetMeterResponse method</span></span>

<span data-ttu-id="39558-107">**SetMeterResponse** 方法會設定計量回應。</span><span class="sxs-lookup"><span data-stu-id="39558-107">The **SetMeterResponse** method sets the metering response.</span></span>

## <a name="syntax"></a><span data-ttu-id="39558-108">語法</span><span class="sxs-lookup"><span data-stu-id="39558-108">Syntax</span></span>


```C++
HRESULT SetMeterResponse(
  [in]  BYTE  *pbMeterResponse,
  [in]  DWORD cbMeterResponse,
  [out] DWORD *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="39558-109">參數</span><span class="sxs-lookup"><span data-stu-id="39558-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39558-110">*pbMeterResponse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39558-110">*pbMeterResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39558-111">要設定的計量回應。</span><span class="sxs-lookup"><span data-stu-id="39558-111">The metering response to be set.</span></span>

</dd> <dt>

<span data-ttu-id="39558-112">*cbMeterResponse* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39558-112">*cbMeterResponse* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39558-113">計量回應的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="39558-113">Size of the metering response, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="39558-114">*pdwFlags* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="39558-114">*pdwFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39558-115">回應旗標。</span><span class="sxs-lookup"><span data-stu-id="39558-115">Response flags.</span></span> <span data-ttu-id="39558-116">此值必須是下列其中一個旗標。</span><span class="sxs-lookup"><span data-stu-id="39558-116">This value must be one of the following flags.</span></span>



| <span data-ttu-id="39558-117">旗標</span><span class="sxs-lookup"><span data-stu-id="39558-117">Flag</span></span>                            | <span data-ttu-id="39558-118">描述</span><span class="sxs-lookup"><span data-stu-id="39558-118">Description</span></span>              |
|---------------------------------|--------------------------|
| <span data-ttu-id="39558-119">WMDRM \_ 計量 \_ 回應 \_ 全部</span><span class="sxs-lookup"><span data-stu-id="39558-119">WMDRM\_METER\_RESPONSE\_ALL</span></span>     | <span data-ttu-id="39558-120">所有計量回應。</span><span class="sxs-lookup"><span data-stu-id="39558-120">All meter responses.</span></span>     |
| <span data-ttu-id="39558-121">WMDRM \_ 計量 \_ 回應 \_ 部分</span><span class="sxs-lookup"><span data-stu-id="39558-121">WMDRM\_METER\_RESPONSE\_PARTIAL</span></span> | <span data-ttu-id="39558-122">部分計量回應。</span><span class="sxs-lookup"><span data-stu-id="39558-122">Partial meter responses.</span></span> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39558-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="39558-123">Return value</span></span>

<span data-ttu-id="39558-124">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="39558-124">The method returns an **HRESULT**.</span></span> <span data-ttu-id="39558-125">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="39558-125">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="39558-126">傳回碼</span><span class="sxs-lookup"><span data-stu-id="39558-126">Return code</span></span>                                                                          | <span data-ttu-id="39558-127">Description</span><span class="sxs-lookup"><span data-stu-id="39558-127">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="39558-128"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="39558-128"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="39558-129">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="39558-129">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="39558-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="39558-130">Requirements</span></span>



| <span data-ttu-id="39558-131">需求</span><span class="sxs-lookup"><span data-stu-id="39558-131">Requirement</span></span> | <span data-ttu-id="39558-132">值</span><span class="sxs-lookup"><span data-stu-id="39558-132">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="39558-133">標頭</span><span class="sxs-lookup"><span data-stu-id="39558-133">Header</span></span><br/>  | <dl> <span data-ttu-id="39558-134"><dt>WMDDRMSP .idl</dt></span><span class="sxs-lookup"><span data-stu-id="39558-134"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="39558-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="39558-135">Library</span></span><br/> | <dl> <span data-ttu-id="39558-136"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="39558-136"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39558-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39558-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39558-138">**IWMDRMDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="39558-138">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





