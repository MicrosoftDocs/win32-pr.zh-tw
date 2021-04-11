---
title: IBasicDevice Description 方法
description: 抓取裝置的描述。
ms.assetid: 9973AC46-E6BA-4931-BDEB-E64B147AB291
keywords:
- 描述方法媒體串流 API
- Description 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，Description 方法
topic_type:
- apiref
api_name:
- IBasicDevice.Description
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f094246d1424c458e624d4a49358b63a84b9b7d2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022348"
---
# <a name="ibasicdevicedescription-method"></a><span data-ttu-id="4f62d-106">IBasicDevice：:D 描述 e) 方法</span><span class="sxs-lookup"><span data-stu-id="4f62d-106">IBasicDevice::Description method</span></span>

<span data-ttu-id="4f62d-107">抓取裝置的描述。</span><span class="sxs-lookup"><span data-stu-id="4f62d-107">Retrieves a description of the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f62d-108">語法</span><span class="sxs-lookup"><span data-stu-id="4f62d-108">Syntax</span></span>


```C++
HRESULT Description(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="4f62d-109">參數</span><span class="sxs-lookup"><span data-stu-id="4f62d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f62d-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4f62d-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f62d-111">接收裝置描述的指標。</span><span class="sxs-lookup"><span data-stu-id="4f62d-111">Receives a pointer to the description of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f62d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4f62d-112">Return value</span></span>

<span data-ttu-id="4f62d-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="4f62d-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4f62d-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="4f62d-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4f62d-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4f62d-115">Return code</span></span>                                                                          | <span data-ttu-id="4f62d-116">Description</span><span class="sxs-lookup"><span data-stu-id="4f62d-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4f62d-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4f62d-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4f62d-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="4f62d-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="4f62d-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4f62d-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f62d-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="4f62d-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





