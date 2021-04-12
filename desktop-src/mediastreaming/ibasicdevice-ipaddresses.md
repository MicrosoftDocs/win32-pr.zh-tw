---
title: IBasicDevice IpAddresses 方法
description: 傳回 IP 位址的向量。
ms.assetid: F48B91DC-3AE2-462F-835B-292BF86904B3
keywords:
- IpAddresses 方法媒體串流 API
- IpAddresses 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，IpAddresses 方法
topic_type:
- apiref
api_name:
- IBasicDevice.IpAddresses
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0623b6e2e5d96cb0a400ab1e820424b7eecf46c9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104373012"
---
# <a name="ibasicdeviceipaddresses-method"></a><span data-ttu-id="e39f8-106">IBasicDevice：： IpAddresses 方法</span><span class="sxs-lookup"><span data-stu-id="e39f8-106">IBasicDevice::IpAddresses method</span></span>

<span data-ttu-id="e39f8-107">傳回 IP 位址的向量。</span><span class="sxs-lookup"><span data-stu-id="e39f8-107">Returns a vector of IP addresses.</span></span>

## <a name="syntax"></a><span data-ttu-id="e39f8-108">語法</span><span class="sxs-lookup"><span data-stu-id="e39f8-108">Syntax</span></span>


```C++
HRESULT IpAddresses(
  [out] IVector< HSTRING > **value
);
```



## <a name="parameters"></a><span data-ttu-id="e39f8-109">參數</span><span class="sxs-lookup"><span data-stu-id="e39f8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e39f8-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e39f8-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e39f8-111">接收 IP 位址指標的可列舉集合。</span><span class="sxs-lookup"><span data-stu-id="e39f8-111">Receives an enumerable collection of pointers to IP addresses.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e39f8-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e39f8-112">Return value</span></span>

<span data-ttu-id="e39f8-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="e39f8-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e39f8-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="e39f8-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e39f8-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e39f8-115">Return code</span></span>                                                                          | <span data-ttu-id="e39f8-116">Description</span><span class="sxs-lookup"><span data-stu-id="e39f8-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e39f8-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e39f8-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e39f8-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="e39f8-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="e39f8-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e39f8-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e39f8-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="e39f8-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





