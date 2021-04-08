---
title: IBasicDevice ModelNumber 方法
description: 抓取裝置的模型編號。
ms.assetid: C4199135-0C6C-4427-8152-224D7D29C270
keywords:
- ModelNumber 方法媒體串流 API
- ModelNumber 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，ModelNumber 方法
topic_type:
- apiref
api_name:
- IBasicDevice.ModelNumber
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8034e67e5f3c552f0af83678d75e33881f1318f4
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103841219"
---
# <a name="ibasicdevicemodelnumber-method"></a><span data-ttu-id="dceda-106">IBasicDevice：： ModelNumber 方法</span><span class="sxs-lookup"><span data-stu-id="dceda-106">IBasicDevice::ModelNumber method</span></span>

<span data-ttu-id="dceda-107">抓取裝置的模型編號。</span><span class="sxs-lookup"><span data-stu-id="dceda-107">Retrieves the device s model number.</span></span>

## <a name="syntax"></a><span data-ttu-id="dceda-108">語法</span><span class="sxs-lookup"><span data-stu-id="dceda-108">Syntax</span></span>


```C++
HRESULT ModelNumber(
  [out] HSTRING *value
);
```



## <a name="parameters"></a><span data-ttu-id="dceda-109">參數</span><span class="sxs-lookup"><span data-stu-id="dceda-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dceda-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dceda-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dceda-111">接收裝置的模型編號指標。</span><span class="sxs-lookup"><span data-stu-id="dceda-111">Receives a pointer to the device s model number.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dceda-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="dceda-112">Return value</span></span>

<span data-ttu-id="dceda-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="dceda-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="dceda-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="dceda-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="dceda-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="dceda-115">Return code</span></span>                                                                          | <span data-ttu-id="dceda-116">Description</span><span class="sxs-lookup"><span data-stu-id="dceda-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="dceda-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="dceda-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="dceda-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="dceda-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="dceda-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dceda-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dceda-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="dceda-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





