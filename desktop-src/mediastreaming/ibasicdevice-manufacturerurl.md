---
title: IBasicDevice ManufacturerUrl 方法
description: 抓取裝置的製造商 URL。
ms.assetid: E8372D15-D8B5-49E4-950A-96B4A88B0450
keywords:
- ManufacturerUrl 方法媒體串流 API
- ManufacturerUrl 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，ManufacturerUrl 方法
topic_type:
- apiref
api_name:
- IBasicDevice.ManufacturerUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e41ca83c98507c65ead8d1faf2922ee84b45649
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022414"
---
# <a name="ibasicdevicemanufacturerurl-method"></a><span data-ttu-id="9c33a-106">IBasicDevice：： ManufacturerUrl 方法</span><span class="sxs-lookup"><span data-stu-id="9c33a-106">IBasicDevice::ManufacturerUrl method</span></span>

<span data-ttu-id="9c33a-107">抓取裝置的製造商 URL。</span><span class="sxs-lookup"><span data-stu-id="9c33a-107">Retrieves the device s manufacturer URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c33a-108">語法</span><span class="sxs-lookup"><span data-stu-id="9c33a-108">Syntax</span></span>


```C++
HRESULT ManufacturerUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="9c33a-109">參數</span><span class="sxs-lookup"><span data-stu-id="9c33a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9c33a-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9c33a-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9c33a-111">接收裝置製造商 URL 的指標。</span><span class="sxs-lookup"><span data-stu-id="9c33a-111">Receives a pointer to the device s manufacturer URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9c33a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9c33a-112">Return value</span></span>

<span data-ttu-id="9c33a-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="9c33a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9c33a-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="9c33a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9c33a-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9c33a-115">Return code</span></span>                                                                          | <span data-ttu-id="9c33a-116">Description</span><span class="sxs-lookup"><span data-stu-id="9c33a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9c33a-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="9c33a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9c33a-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="9c33a-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="9c33a-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c33a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c33a-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="9c33a-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





