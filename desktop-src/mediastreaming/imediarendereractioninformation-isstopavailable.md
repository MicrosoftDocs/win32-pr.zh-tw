---
title: IMediaRendererActionInformation IsStopAvailable 方法
description: 抓取值，這個值表示 DMR 目前是否接受 StopAsync 方法。
ms.assetid: 6EE8F56D-2A5A-49B0-A9B2-0A7EE57D03FD
keywords:
- IsStopAvailable 方法媒體串流 API
- IsStopAvailable 方法媒體串流 API，IMediaRendererActionInformation 介面
- IMediaRendererActionInformation 介面媒體串流 API，IsStopAvailable 方法
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsStopAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5e0a031bafc9a755dfec2498f4e2a52cdd9ef5b1
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092702"
---
# <a name="imediarendereractioninformationisstopavailable-method"></a><span data-ttu-id="9420b-106">IMediaRendererActionInformation：： IsStopAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="9420b-106">IMediaRendererActionInformation::IsStopAvailable method</span></span>

<span data-ttu-id="9420b-107">抓取值，這個值表示 DMR 目前是否接受 [**StopAsync**](imediarenderer-stopasync.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="9420b-107">Retrieves a value that indicates whether the DMR is currently accepting the [**StopAsync**](imediarenderer-stopasync.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="9420b-108">語法</span><span class="sxs-lookup"><span data-stu-id="9420b-108">Syntax</span></span>


```C++
HRESULT IsStopAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="9420b-109">參數</span><span class="sxs-lookup"><span data-stu-id="9420b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9420b-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9420b-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9420b-111">如果 DMR 目前接受 [**StopAsync**](imediarenderer-stopasync.md)方法，則布林值為 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="9420b-111">A boolean value that is **True** if the DMR is currently accepting the [**StopAsync**](imediarenderer-stopasync.md) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9420b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="9420b-112">Return value</span></span>

<span data-ttu-id="9420b-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="9420b-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="9420b-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="9420b-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="9420b-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="9420b-115">Return code</span></span>                                                                          | <span data-ttu-id="9420b-116">Description</span><span class="sxs-lookup"><span data-stu-id="9420b-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="9420b-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="9420b-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="9420b-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="9420b-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="9420b-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9420b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9420b-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="9420b-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

