---
title: DeviceController. CachedDevices 方法
description: 抓取 IBasicDevice 介面指標的集合，表示所有可探索的 DLNA 裝置的快取視圖。 |DeviceController. CachedDevices 方法
ms.assetid: 89CFA4BB-EDA8-461A-A3A0-A84CBDA99EA4
keywords:
- CachedDevices 方法媒體串流 API
- CachedDevices 方法媒體串流 API，DeviceController 介面
- DeviceController 介面媒體串流 API，CachedDevices 方法
topic_type:
- apiref
api_name:
- DeviceController.CachedDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c0bb39e03a9788e0c444f682b61d39fc1c65781b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981783"
---
# <a name="devicecontrollercacheddevices-method"></a><span data-ttu-id="42064-107">DeviceController. CachedDevices 方法</span><span class="sxs-lookup"><span data-stu-id="42064-107">DeviceController.CachedDevices method</span></span>

<span data-ttu-id="42064-108">抓取 [**IBasicDevice**](ibasicdevice.md) 介面指標的集合，表示所有可探索的 DLNA 裝置的快取視圖。</span><span class="sxs-lookup"><span data-stu-id="42064-108">Retrieves a collection of [**IBasicDevice**](ibasicdevice.md) interface pointers that represents the cached view of all discoverable DLNA devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="42064-109">語法</span><span class="sxs-lookup"><span data-stu-id="42064-109">Syntax</span></span>


```C++
HRESULT CachedDevices(
  [out] IVector< IBasicDevice > **value
);
```



## <a name="parameters"></a><span data-ttu-id="42064-110">參數</span><span class="sxs-lookup"><span data-stu-id="42064-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="42064-111">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="42064-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="42064-112">接收 [**IBasicDevice**](ibasicdevice.md) 介面指標的可列舉集合。</span><span class="sxs-lookup"><span data-stu-id="42064-112">Receives an enumerable collection of [**IBasicDevice**](ibasicdevice.md) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="42064-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="42064-113">Return value</span></span>

<span data-ttu-id="42064-114">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="42064-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="42064-115">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="42064-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="42064-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="42064-116">Return code</span></span>                                                                          | <span data-ttu-id="42064-117">Description</span><span class="sxs-lookup"><span data-stu-id="42064-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="42064-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="42064-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="42064-119">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="42064-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="42064-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="42064-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="42064-121">[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="42064-121">[**DeviceController**](/previous-versions/windows/desktop/legacy/hh828842(v=vs.85))</span></span>
</dt> </dl>

 

