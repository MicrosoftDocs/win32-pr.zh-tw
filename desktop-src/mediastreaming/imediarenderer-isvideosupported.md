---
title: IMediaRenderer IsVideoSupported 方法
description: 抓取值，指出 DMR 是否能夠播放影片內容。
ms.assetid: AE9A14D0-A7A2-4A71-9454-06A05C7D85F9
keywords:
- IsVideoSupported 方法媒體串流 API
- IsVideoSupported 方法媒體串流 API，IMediaRenderer 介面
- IMediaRenderer 介面媒體串流 API，IsVideoSupported 方法
topic_type:
- apiref
api_name:
- IMediaRenderer.IsVideoSupported
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9808841bf60a384d6a4566e75f53248b0f86338c
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312999"
---
# <a name="imediarendererisvideosupported-method"></a><span data-ttu-id="e51aa-106">IMediaRenderer：： IsVideoSupported 方法</span><span class="sxs-lookup"><span data-stu-id="e51aa-106">IMediaRenderer::IsVideoSupported method</span></span>

<span data-ttu-id="e51aa-107">抓取值，指出 DMR 是否能夠播放影片內容。</span><span class="sxs-lookup"><span data-stu-id="e51aa-107">Retrieves a value that indicates whether the DMR is capable of playing video content.</span></span>

## <a name="syntax"></a><span data-ttu-id="e51aa-108">語法</span><span class="sxs-lookup"><span data-stu-id="e51aa-108">Syntax</span></span>


```C++
HRESULT IsVideoSupported(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="e51aa-109">參數</span><span class="sxs-lookup"><span data-stu-id="e51aa-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e51aa-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e51aa-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e51aa-111">布林值，如果 DMR 能夠播放影片內容則為 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="e51aa-111">A boolean value that is **True** if the DMR is capable of playing video content and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e51aa-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="e51aa-112">Return value</span></span>

<span data-ttu-id="e51aa-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="e51aa-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="e51aa-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="e51aa-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="e51aa-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="e51aa-115">Return code</span></span>                                                                          | <span data-ttu-id="e51aa-116">Description</span><span class="sxs-lookup"><span data-stu-id="e51aa-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="e51aa-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="e51aa-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="e51aa-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="e51aa-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="e51aa-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e51aa-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e51aa-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="e51aa-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

 





