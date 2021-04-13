---
title: IMediaRendererActionInformation IsPlayAvailable 方法
description: 抓取值，指出 DMR 目前是否接受接受 PlayAsync 和 PlayAtSpeedAsync 方法。
ms.assetid: 969C55FA-872D-4063-B85C-573C8DA5593C
keywords:
- IsPlayAvailable 方法媒體串流 API
- IsPlayAvailable 方法媒體串流 API，IMediaRendererActionInformation 介面
- IMediaRendererActionInformation 介面媒體串流 API，IsPlayAvailable 方法
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPlayAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 87fa3a2005772a4d948bafe32d2a0e10cc5a6914
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375197"
---
# <a name="imediarendereractioninformationisplayavailable-method"></a><span data-ttu-id="6a9df-106">IMediaRendererActionInformation：： IsPlayAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="6a9df-106">IMediaRendererActionInformation::IsPlayAvailable method</span></span>

<span data-ttu-id="6a9df-107">抓取值，指出 DMR 目前是否接受接受 [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) 和 [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) 方法。</span><span class="sxs-lookup"><span data-stu-id="6a9df-107">Retrieves a value that indicates whether the DMR is currently accepting the accepting the [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) and [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) methods.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a9df-108">語法</span><span class="sxs-lookup"><span data-stu-id="6a9df-108">Syntax</span></span>


```C++
HRESULT IsPlayAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="6a9df-109">參數</span><span class="sxs-lookup"><span data-stu-id="6a9df-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a9df-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6a9df-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6a9df-111">如果 DMR 目前接受接受 [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync)和 [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync)方法，則布林值為 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="6a9df-111">A boolean value that is **True** if the DMR is currently accepting the accepting the [**PlayAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playasync) and [**PlayAtSpeedAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-playatspeedasync) methods and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a9df-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="6a9df-112">Return value</span></span>

<span data-ttu-id="6a9df-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="6a9df-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="6a9df-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="6a9df-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="6a9df-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="6a9df-115">Return code</span></span>                                                                          | <span data-ttu-id="6a9df-116">Description</span><span class="sxs-lookup"><span data-stu-id="6a9df-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="6a9df-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="6a9df-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="6a9df-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="6a9df-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="6a9df-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6a9df-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a9df-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="6a9df-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

