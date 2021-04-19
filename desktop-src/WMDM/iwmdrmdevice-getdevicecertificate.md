---
title: IWMDRMDevice GetDeviceCertificate 方法
description: GetDeviceCertificate 方法會抓取裝置憑證。
ms.assetid: 9e345bf9-a158-4c0e-a9f1-e4ce3ec16b58
keywords:
- GetDeviceCertificate 方法 windows Media 裝置管理員
- GetDeviceCertificate 方法 windows Media 裝置管理員，IWMDRMDevice 介面
- IWMDRMDevice interface windows Media 裝置管理員，GetDeviceCertificate 方法
topic_type:
- apiref
api_name:
- IWMDRMDevice.GetDeviceCertificate
api_location:
- mssachlp.lib
- mssachlp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9ceecca32f2455d73ca1dce76a4f8a17613a1ee
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993941"
---
# <a name="iwmdrmdevicegetdevicecertificate-method"></a><span data-ttu-id="090d2-106">IWMDRMDevice：： GetDeviceCertificate 方法</span><span class="sxs-lookup"><span data-stu-id="090d2-106">IWMDRMDevice::GetDeviceCertificate method</span></span>

<span data-ttu-id="090d2-107">**GetDeviceCertificate** 方法會抓取裝置憑證。</span><span class="sxs-lookup"><span data-stu-id="090d2-107">The **GetDeviceCertificate** method retrieves the device certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="090d2-108">語法</span><span class="sxs-lookup"><span data-stu-id="090d2-108">Syntax</span></span>


```C++
HRESULT GetDeviceCertificate(
  [out] BSTR *pbstrDevCert
);
```



## <a name="parameters"></a><span data-ttu-id="090d2-109">參數</span><span class="sxs-lookup"><span data-stu-id="090d2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="090d2-110">*pbstrDevCert* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="090d2-110">*pbstrDevCert* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="090d2-111">包含已抓取裝置憑證之 **BSTR** 的指標。</span><span class="sxs-lookup"><span data-stu-id="090d2-111">Pointer to a **BSTR** containing the retrieved device certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="090d2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="090d2-112">Return value</span></span>

<span data-ttu-id="090d2-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="090d2-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="090d2-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="090d2-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="090d2-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="090d2-115">Return code</span></span>                                                                          | <span data-ttu-id="090d2-116">Description</span><span class="sxs-lookup"><span data-stu-id="090d2-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="090d2-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="090d2-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="090d2-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="090d2-118">The method succeeded.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="090d2-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="090d2-119">Requirements</span></span>



| <span data-ttu-id="090d2-120">需求</span><span class="sxs-lookup"><span data-stu-id="090d2-120">Requirement</span></span> | <span data-ttu-id="090d2-121">值</span><span class="sxs-lookup"><span data-stu-id="090d2-121">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="090d2-122">標頭</span><span class="sxs-lookup"><span data-stu-id="090d2-122">Header</span></span><br/>  | <dl> <span data-ttu-id="090d2-123"><dt>WMDDRMSP .idl</dt></span><span class="sxs-lookup"><span data-stu-id="090d2-123"><dt>WMDDRMSP.idl</dt></span></span> </dl> |
| <span data-ttu-id="090d2-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="090d2-124">Library</span></span><br/> | <dl> <span data-ttu-id="090d2-125"><dt>Mssachlp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="090d2-125"><dt>Mssachlp.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="090d2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="090d2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="090d2-127">**IWMDRMDevice 介面**</span><span class="sxs-lookup"><span data-stu-id="090d2-127">**IWMDRMDevice Interface**</span></span>](iwmdrmdevice.md)
</dt> </dl>

 

 





