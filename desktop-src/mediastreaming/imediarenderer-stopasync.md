---
title: IMediaRenderer StopAsync 方法
description: 指示 DMR 以非同步方式停止播放目前的內容。 |IMediaRenderer StopAsync 方法
ms.assetid: B6B0F3F2-E95E-4A58-9CBD-CF4CB24FDAD0
keywords:
- StopAsync 方法媒體串流 API
- StopAsync 方法媒體串流 API，IMediaRenderer 介面
- IMediaRenderer 介面媒體串流 API，StopAsync 方法
topic_type:
- apiref
api_name:
- IMediaRenderer.StopAsync
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a5f73d534fdd786038a242614a981f4915d92c13
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "103853895"
---
# <a name="imediarendererstopasync-method"></a><span data-ttu-id="ddae9-107">IMediaRenderer：： StopAsync 方法</span><span class="sxs-lookup"><span data-stu-id="ddae9-107">IMediaRenderer::StopAsync method</span></span>

<span data-ttu-id="ddae9-108">指示 DMR 以非同步方式停止播放目前的內容。</span><span class="sxs-lookup"><span data-stu-id="ddae9-108">Instructs the DMR asynchronously to stop playing the current content.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddae9-109">語法</span><span class="sxs-lookup"><span data-stu-id="ddae9-109">Syntax</span></span>


```C++
HRESULT StopAsync(
  [out] PlaybackOperation **value
);
```



## <a name="parameters"></a><span data-ttu-id="ddae9-110">參數</span><span class="sxs-lookup"><span data-stu-id="ddae9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ddae9-111">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ddae9-111">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ddae9-112">接收 [**PlaybackOperation**](playbackoperation.md) 物件的參考，這個物件是用來從非同步作業取得結果。</span><span class="sxs-lookup"><span data-stu-id="ddae9-112">Receives a reference to a [**PlaybackOperation**](playbackoperation.md) object that is used to get results from the asynchronous operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ddae9-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ddae9-113">Return value</span></span>

<span data-ttu-id="ddae9-114">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="ddae9-114">The method returns an **HRESULT**.</span></span> <span data-ttu-id="ddae9-115">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="ddae9-115">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="ddae9-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="ddae9-116">Return code</span></span>                                                                          | <span data-ttu-id="ddae9-117">Description</span><span class="sxs-lookup"><span data-stu-id="ddae9-117">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="ddae9-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="ddae9-118"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="ddae9-119">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="ddae9-119">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="ddae9-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ddae9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddae9-121">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="ddae9-121">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





