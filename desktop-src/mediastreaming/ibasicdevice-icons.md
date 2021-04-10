---
title: IBasicDevice 圖示方法
description: 傳回 IDeviceIcon 介面的向量。
ms.assetid: 0C083AF3-FE22-4A8E-87B7-0FFA7B65ADBD
keywords:
- 圖示方法媒體串流 API
- 圖示方法媒體串流 API，IBasicDevice 介面
- IBasicDevice 介面媒體串流 API，圖示方法
topic_type:
- apiref
api_name:
- IBasicDevice.Icons
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3fb6e4b708b4e38ffb39f152308cec7b885a772f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103681779"
---
# <a name="ibasicdeviceicons-method"></a><span data-ttu-id="656a7-106">IBasicDevice：：圖示方法</span><span class="sxs-lookup"><span data-stu-id="656a7-106">IBasicDevice::Icons method</span></span>

<span data-ttu-id="656a7-107">傳回 [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) 介面的向量。</span><span class="sxs-lookup"><span data-stu-id="656a7-107">Returns a vector of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interfaces.</span></span>

## <a name="syntax"></a><span data-ttu-id="656a7-108">語法</span><span class="sxs-lookup"><span data-stu-id="656a7-108">Syntax</span></span>


```C++
HRESULT Icons(
  [out] IVector< IDeviceIcon > **value
);
```



## <a name="parameters"></a><span data-ttu-id="656a7-109">參數</span><span class="sxs-lookup"><span data-stu-id="656a7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="656a7-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="656a7-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="656a7-111">接收 [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) 介面指標的可列舉集合。</span><span class="sxs-lookup"><span data-stu-id="656a7-111">Receives an enumerable collection of [**IDeviceIcon**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-ideviceicon) interface pointers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="656a7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="656a7-112">Return value</span></span>

<span data-ttu-id="656a7-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="656a7-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="656a7-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="656a7-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="656a7-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="656a7-115">Return code</span></span>                                                                          | <span data-ttu-id="656a7-116">Description</span><span class="sxs-lookup"><span data-stu-id="656a7-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="656a7-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="656a7-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="656a7-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="656a7-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="656a7-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="656a7-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="656a7-120">**IBasicDevice**</span><span class="sxs-lookup"><span data-stu-id="656a7-120">**IBasicDevice**</span></span>](ibasicdevice.md)
</dt> </dl>

 

