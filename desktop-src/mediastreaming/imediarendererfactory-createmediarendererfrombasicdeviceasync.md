---
title: IMediaRendererFactory CreateMediaRendererFromBasicDeviceAsync 方法
description: 以非同步方式建立物件的新實例，這個實例會使用指定的 IBasicDevice 介面來執行 IMediaRenderer 介面。
ms.assetid: 14A83789-0F3C-467B-8EFD-3BB421C54217
keywords:
- CreateMediaRendererFromBasicDeviceAsync 方法媒體串流 API
- CreateMediaRendererFromBasicDeviceAsync 方法媒體串流 API，IMediaRendererFactory 介面
- IMediaRendererFactory 介面媒體串流 API，CreateMediaRendererFromBasicDeviceAsync 方法
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererFromBasicDeviceAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7e4ee614cca9a03ca203ecde9203e019fab38ab4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023377"
---
# <a name="imediarendererfactorycreatemediarendererfrombasicdeviceasync-method"></a><span data-ttu-id="a339d-106">IMediaRendererFactory：： CreateMediaRendererFromBasicDeviceAsync 方法</span><span class="sxs-lookup"><span data-stu-id="a339d-106">IMediaRendererFactory::CreateMediaRendererFromBasicDeviceAsync method</span></span>

<span data-ttu-id="a339d-107">以非同步方式建立物件的新實例，這個實例會使用指定的 [**IBasicDevice**](ibasicdevice.md)介面來執行 [**IMediaRenderer**](imediarenderer.md)介面。</span><span class="sxs-lookup"><span data-stu-id="a339d-107">Asynchronously creates a new instance of an object that implements the [**IMediaRenderer**](imediarenderer.md) interface using the specified [**IBasicDevice**](ibasicdevice.md) interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="a339d-108">語法</span><span class="sxs-lookup"><span data-stu-id="a339d-108">Syntax</span></span>


```C++
HRESULT CreateMediaRendererFromBasicDeviceAsync(
  [in]          IBasicDevice                 *basicDevice,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="a339d-109">參數</span><span class="sxs-lookup"><span data-stu-id="a339d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a339d-110">*basicDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a339d-110">*basicDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a339d-111">[**IBasicDevice**](ibasicdevice.md)介面的指標，代表將建立 [**IMediaRenderer**](imediarenderer.md)實例的裝置。</span><span class="sxs-lookup"><span data-stu-id="a339d-111">A pointer to an [**IBasicDevice**](ibasicdevice.md) interface representing the device for which an instance of [**IMediaRenderer**](imediarenderer.md) will be created.</span></span>

</dd> <dt>

<span data-ttu-id="a339d-112">*值* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="a339d-112">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a339d-113">接收 [**CreateMediaRendererOperation**](createmediarendereroperation.md) 物件的參考，這個物件是用來從非同步作業取得結果。</span><span class="sxs-lookup"><span data-stu-id="a339d-113">Receives a reference to a [**CreateMediaRendererOperation**](createmediarendereroperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a339d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a339d-114">Return value</span></span>

<span data-ttu-id="a339d-115">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="a339d-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="a339d-116">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="a339d-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="a339d-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="a339d-117">Return code</span></span>                                                                          | <span data-ttu-id="a339d-118">Description</span><span class="sxs-lookup"><span data-stu-id="a339d-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="a339d-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a339d-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="a339d-120">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="a339d-120">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="a339d-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a339d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a339d-122">**IMediaRendererFactory**</span><span class="sxs-lookup"><span data-stu-id="a339d-122">**IMediaRendererFactory**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

