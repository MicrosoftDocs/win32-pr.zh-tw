---
title: IMediaRendererFactory CreateMediaRendererAsync 方法
description: 以非同步方式建立物件的新實例，這個實例會使用指定的唯一裝置名稱（ (UDN) ）來執行 IMediaRenderer 介面。
ms.assetid: FD1242F8-4C2E-4027-B1DE-5FD69557684C
keywords:
- CreateMediaRendererAsync 方法媒體串流 API
- CreateMediaRendererAsync 方法媒體串流 API，IMediaRendererFactory 介面
- IMediaRendererFactory 介面媒體串流 API，CreateMediaRendererAsync 方法
topic_type:
- apiref
api_name:
- IMediaRendererFactory.CreateMediaRendererAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b152e5889ad83440a48e178be0b89a97d2a9f664
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682003"
---
# <a name="imediarendererfactorycreatemediarendererasync-method"></a><span data-ttu-id="917cc-106">IMediaRendererFactory：： CreateMediaRendererAsync 方法</span><span class="sxs-lookup"><span data-stu-id="917cc-106">IMediaRendererFactory::CreateMediaRendererAsync method</span></span>

<span data-ttu-id="917cc-107">以非同步方式建立物件的新實例，這個實例會使用指定的唯一裝置名稱（ (UDN) ）來執行 [**IMediaRenderer**](imediarenderer.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="917cc-107">Asynchronously creates a new instance of an object that implements the [**IMediaRenderer**](imediarenderer.md) interface using the specified Unique Device Name (UDN).</span></span>

## <a name="syntax"></a><span data-ttu-id="917cc-108">語法</span><span class="sxs-lookup"><span data-stu-id="917cc-108">Syntax</span></span>


```C++
HRESULT CreateMediaRendererAsync(
  [in]          HSTRING                      deviceIdentifier,
  [out, retval] CreateMediaRendererOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="917cc-109">參數</span><span class="sxs-lookup"><span data-stu-id="917cc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="917cc-110">*deviceIdentifier* \[在\]</span><span class="sxs-lookup"><span data-stu-id="917cc-110">*deviceIdentifier* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="917cc-111">包含 UDN 的 HSTRING，此會識別要建立 [**IMediaRenderer**](imediarenderer.md) 實例的 DLNA DMR 裝置。</span><span class="sxs-lookup"><span data-stu-id="917cc-111">An HSTRING containing a UDN that identifies the DLNA DMR device for which an instance of [**IMediaRenderer**](imediarenderer.md) will be created.</span></span>

</dd> <dt>

<span data-ttu-id="917cc-112">*值* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="917cc-112">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="917cc-113">接收 [**CreateMediaRendererOperation**](createmediarendereroperation.md) 物件的參考，這個物件是用來從非同步作業取得結果。</span><span class="sxs-lookup"><span data-stu-id="917cc-113">Receives a reference to a [**CreateMediaRendererOperation**](createmediarendereroperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="917cc-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="917cc-114">Return value</span></span>

<span data-ttu-id="917cc-115">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="917cc-115">The method returns an **HRESULT**.</span></span> <span data-ttu-id="917cc-116">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="917cc-116">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="917cc-117">傳回碼</span><span class="sxs-lookup"><span data-stu-id="917cc-117">Return code</span></span>                                                                          | <span data-ttu-id="917cc-118">Description</span><span class="sxs-lookup"><span data-stu-id="917cc-118">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="917cc-119"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="917cc-119"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="917cc-120">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="917cc-120">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="917cc-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="917cc-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="917cc-122">**IMediaRendererFactory**</span><span class="sxs-lookup"><span data-stu-id="917cc-122">**IMediaRendererFactory**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendererfactory)
</dt> </dl>

 

