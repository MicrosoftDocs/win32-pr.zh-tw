---
title: IBasicDevice CanWakeDevices 方法
description: 抓取值，指出裝置是否可以喚醒。
ms.assetid: AAD0597C-AD33-40EE-A5DA-27AC66375D38
keywords:
- CanWakeDevices 方法媒體串流 API
- CanWakeDevices 方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，CanWakeDevices 方法
topic_type:
- apiref
api_name:
- IBasicDevice.CanWakeDevices
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 08a893ac880a426f604f2dc1c73173585e507cc0
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104022542"
---
# <a name="ibasicdevicecanwakedevices-method"></a><span data-ttu-id="4c247-106">IBasicDevice：： CanWakeDevices 方法</span><span class="sxs-lookup"><span data-stu-id="4c247-106">IBasicDevice::CanWakeDevices method</span></span>

<span data-ttu-id="4c247-107">抓取值，指出裝置是否可以喚醒。</span><span class="sxs-lookup"><span data-stu-id="4c247-107">Retrieves a value that indicates if the device can wake.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c247-108">語法</span><span class="sxs-lookup"><span data-stu-id="4c247-108">Syntax</span></span>


```C++
HRESULT CanWakeDevices(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="4c247-109">參數</span><span class="sxs-lookup"><span data-stu-id="4c247-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c247-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4c247-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c247-111">接收布林值的指標，如果裝置可以喚醒則為 **True** 。</span><span class="sxs-lookup"><span data-stu-id="4c247-111">Receives a pointer to a boolean value that is **True** if the device can wake.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c247-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c247-112">Return value</span></span>

<span data-ttu-id="4c247-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="4c247-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4c247-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="4c247-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4c247-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4c247-115">Return code</span></span>                                                                          | <span data-ttu-id="4c247-116">Description</span><span class="sxs-lookup"><span data-stu-id="4c247-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4c247-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4c247-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4c247-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="4c247-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="4c247-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c247-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c247-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="4c247-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

 





