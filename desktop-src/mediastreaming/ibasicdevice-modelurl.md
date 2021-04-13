---
title: IBasicDevice ModelUrl 方法
description: 抓取裝置的模型 URL。
ms.assetid: 093D306B-5DFC-4A68-803D-3DDE195A8B85
keywords:
- ModelUrl 方法媒體串流 API
- ModelUrl 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，ModelUrl 方法
topic_type:
- apiref
api_name:
- IBasicDevice.ModelUrl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f616d1a122f5fe6025c80742df61eb86d41514a
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312452"
---
# <a name="ibasicdevicemodelurl-method"></a><span data-ttu-id="159dc-106">IBasicDevice：： ModelUrl 方法</span><span class="sxs-lookup"><span data-stu-id="159dc-106">IBasicDevice::ModelUrl method</span></span>

<span data-ttu-id="159dc-107">抓取裝置的模型 URL。</span><span class="sxs-lookup"><span data-stu-id="159dc-107">Retrieves the device s model URL.</span></span>

## <a name="syntax"></a><span data-ttu-id="159dc-108">語法</span><span class="sxs-lookup"><span data-stu-id="159dc-108">Syntax</span></span>


```C++
HRESULT ModelUrl(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="159dc-109">參數</span><span class="sxs-lookup"><span data-stu-id="159dc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="159dc-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="159dc-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="159dc-111">接收裝置的模型 URL 指標。</span><span class="sxs-lookup"><span data-stu-id="159dc-111">Receives a pointer to the device s model URL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="159dc-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="159dc-112">Return value</span></span>

<span data-ttu-id="159dc-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="159dc-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="159dc-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="159dc-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="159dc-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="159dc-115">Return code</span></span>                                                                          | <span data-ttu-id="159dc-116">Description</span><span class="sxs-lookup"><span data-stu-id="159dc-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="159dc-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="159dc-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="159dc-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="159dc-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="159dc-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="159dc-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="159dc-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="159dc-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





