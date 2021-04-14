---
title: IBasicDevice DiscoveredOnCurrentNetwork 方法
description: 抓取值，指出裝置是否在目前的網路上。
ms.assetid: E64D4E49-9790-4647-9A01-2C28C407F238
keywords:
- DiscoveredOnCurrentNetwork 方法媒體串流 API
- DiscoveredOnCurrentNetwork 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，DiscoveredOnCurrentNetwork 方法
topic_type:
- apiref
api_name:
- IBasicDevice.DiscoveredOnCurrentNetwork
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6e79a012413b3b3d78a9c4617f01ca6cc01cf7e1
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104372928"
---
# <a name="ibasicdevicediscoveredoncurrentnetwork-method"></a><span data-ttu-id="3aa3b-106">IBasicDevice：:D iscoveredOnCurrentNetwork 方法</span><span class="sxs-lookup"><span data-stu-id="3aa3b-106">IBasicDevice::DiscoveredOnCurrentNetwork method</span></span>

<span data-ttu-id="3aa3b-107">抓取值，指出裝置是否在目前的網路上。</span><span class="sxs-lookup"><span data-stu-id="3aa3b-107">Retrieves a value that indicates if the device is on the current network.</span></span>

## <a name="syntax"></a><span data-ttu-id="3aa3b-108">語法</span><span class="sxs-lookup"><span data-stu-id="3aa3b-108">Syntax</span></span>


```C++
HRESULT DiscoveredOnCurrentNetwork(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="3aa3b-109">參數</span><span class="sxs-lookup"><span data-stu-id="3aa3b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3aa3b-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3aa3b-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3aa3b-111">如果裝置位於目前的網路上 **，則接收** 布林值的指標。</span><span class="sxs-lookup"><span data-stu-id="3aa3b-111">Receives a pointer to a boolean value that is **True** if the device is on the current network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3aa3b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3aa3b-112">Return value</span></span>

<span data-ttu-id="3aa3b-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="3aa3b-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3aa3b-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="3aa3b-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3aa3b-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3aa3b-115">Return code</span></span>                                                                          | <span data-ttu-id="3aa3b-116">Description</span><span class="sxs-lookup"><span data-stu-id="3aa3b-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3aa3b-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3aa3b-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3aa3b-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="3aa3b-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="3aa3b-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3aa3b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3aa3b-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="3aa3b-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





