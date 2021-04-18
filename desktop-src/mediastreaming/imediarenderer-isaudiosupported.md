---
title: IMediaRenderer IsAudioSupported 方法
description: 抓取值，指出 DMR 是否能夠播放音訊內容。
ms.assetid: D5F0C4ED-5778-4388-A7BD-E3923145D663
keywords:
- IsAudioSupported 方法媒體串流 API
- IsAudioSupported 方法媒體串流 API，IMediaRenderer 介面
- IMediaRenderer 介面媒體串流 API，IsAudioSupported 方法
topic_type:
- apiref
api_name:
- IMediaRenderer.IsAudioSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4f7670d0a2818cf5518bee0b2586531caeea20fd
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106965614"
---
# <a name="imediarendererisaudiosupported-method"></a><span data-ttu-id="d21e6-106">IMediaRenderer：： IsAudioSupported 方法</span><span class="sxs-lookup"><span data-stu-id="d21e6-106">IMediaRenderer::IsAudioSupported method</span></span>

<span data-ttu-id="d21e6-107">抓取值，指出 DMR 是否能夠播放音訊內容。</span><span class="sxs-lookup"><span data-stu-id="d21e6-107">Retrieves a value that indicates whether the DMR is capable of playing audio content.</span></span>

## <a name="syntax"></a><span data-ttu-id="d21e6-108">語法</span><span class="sxs-lookup"><span data-stu-id="d21e6-108">Syntax</span></span>


```C++
HRESULT IsAudioSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="d21e6-109">參數</span><span class="sxs-lookup"><span data-stu-id="d21e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d21e6-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d21e6-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d21e6-111">布林值，如果 DMR 能夠播放音訊內容，則為 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="d21e6-111">A boolean value that is **True** if the DMR is capable of playing audio content and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d21e6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d21e6-112">Return value</span></span>

<span data-ttu-id="d21e6-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="d21e6-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d21e6-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="d21e6-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d21e6-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d21e6-115">Return code</span></span>                                                                          | <span data-ttu-id="d21e6-116">Description</span><span class="sxs-lookup"><span data-stu-id="d21e6-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d21e6-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d21e6-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d21e6-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="d21e6-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d21e6-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d21e6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d21e6-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="d21e6-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





