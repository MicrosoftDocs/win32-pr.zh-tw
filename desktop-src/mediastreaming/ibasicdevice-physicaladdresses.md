---
title: IBasicDevice PhysicalAddresses 方法
description: 傳回實體位址的向量。
ms.assetid: 85F48EE3-14A1-46DA-A3C3-F94A8A43CF92
keywords:
- PhysicalAddresses 方法媒體串流 API
- PhysicalAddresses 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，PhysicalAddresses 方法
topic_type:
- apiref
api_name:
- IBasicDevice.PhysicalAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2f1cd87435c78e1f6877d1bb6afd1b38981b05dc
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312447"
---
# <a name="ibasicdevicephysicaladdresses-method"></a><span data-ttu-id="bdcfd-106">IBasicDevice：:P hysicalAddresses 方法</span><span class="sxs-lookup"><span data-stu-id="bdcfd-106">IBasicDevice::PhysicalAddresses method</span></span>

<span data-ttu-id="bdcfd-107">傳回實體位址的向量。</span><span class="sxs-lookup"><span data-stu-id="bdcfd-107">Returns a vector of physical addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="bdcfd-108">語法</span><span class="sxs-lookup"><span data-stu-id="bdcfd-108">Syntax</span></span>


```C++
HRESULT PhysicalAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="bdcfd-109">參數</span><span class="sxs-lookup"><span data-stu-id="bdcfd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bdcfd-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="bdcfd-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bdcfd-111">接收實體位址指標的可列舉集合。</span><span class="sxs-lookup"><span data-stu-id="bdcfd-111">Receives an enumerable collection of pointers to physical addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bdcfd-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="bdcfd-112">Return value</span></span>

<span data-ttu-id="bdcfd-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="bdcfd-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="bdcfd-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="bdcfd-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="bdcfd-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="bdcfd-115">Return code</span></span>                                                                          | <span data-ttu-id="bdcfd-116">Description</span><span class="sxs-lookup"><span data-stu-id="bdcfd-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="bdcfd-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bdcfd-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="bdcfd-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="bdcfd-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="bdcfd-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bdcfd-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bdcfd-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="bdcfd-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





