---
title: IMediaRendererActionInformation IsSeekAvailable 方法
description: 抓取值，這個值表示 DMR 目前是否接受 SeekAsync 方法。
ms.assetid: F0817184-70F2-43AC-A2BE-A15F4B195085
keywords:
- IsSeekAvailable 方法媒體串流 API
- IsSeekAvailable 方法媒體串流 API，IMediaRendererActionInformation 介面
- IMediaRendererActionInformation 介面媒體串流 API，IsSeekAvailable 方法
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSeekAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 700afb72efbab01bbd3a8f5e15fa444eb6b06272
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842236"
---
# <a name="imediarendereractioninformationisseekavailable-method"></a><span data-ttu-id="4c008-106">IMediaRendererActionInformation：： IsSeekAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="4c008-106">IMediaRendererActionInformation::IsSeekAvailable method</span></span>

<span data-ttu-id="4c008-107">抓取值，這個值表示 DMR 目前是否接受 [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) 方法。</span><span class="sxs-lookup"><span data-stu-id="4c008-107">Retrieves a value that indicates whether the DMR is currently accepting the [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c008-108">語法</span><span class="sxs-lookup"><span data-stu-id="4c008-108">Syntax</span></span>


```C++
HRESULT IsSeekAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="4c008-109">參數</span><span class="sxs-lookup"><span data-stu-id="4c008-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c008-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="4c008-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c008-111">如果 DMR 目前接受 [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync)方法，則布林值為 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="4c008-111">A boolean value that is **True** if the DMR is currently accepting the [**SeekAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-seekasync) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c008-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c008-112">Return value</span></span>

<span data-ttu-id="4c008-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="4c008-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="4c008-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="4c008-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="4c008-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4c008-115">Return code</span></span>                                                                          | <span data-ttu-id="4c008-116">Description</span><span class="sxs-lookup"><span data-stu-id="4c008-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="4c008-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="4c008-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="4c008-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="4c008-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="4c008-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c008-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c008-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="4c008-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

