---
title: IMediaRendererActionInformation IsPauseAvailable 方法
description: 抓取值，這個值表示 DMR 目前是否接受 PauseAsync 方法。
ms.assetid: 095A664F-D974-410D-8741-87A171EDD071
keywords:
- IsPauseAvailable 方法媒體串流 API
- IsPauseAvailable 方法媒體串流 API，IMediaRendererActionInformation 介面
- IMediaRendererActionInformation 介面媒體串流 API，IsPauseAvailable 方法
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsPauseAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9eb0b750f5a04528aef830d87376c276bdaf6674
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842239"
---
# <a name="imediarendereractioninformationispauseavailable-method"></a><span data-ttu-id="d4c95-106">IMediaRendererActionInformation：： IsPauseAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="d4c95-106">IMediaRendererActionInformation::IsPauseAvailable method</span></span>

<span data-ttu-id="d4c95-107">抓取值，這個值表示 DMR 目前是否接受 [**PauseAsync**](imediarenderer-pauseasync.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="d4c95-107">Retrieves a value that indicates whether the DMR is currently accepting the [**PauseAsync**](imediarenderer-pauseasync.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4c95-108">語法</span><span class="sxs-lookup"><span data-stu-id="d4c95-108">Syntax</span></span>


```C++
HRESULT IsPauseAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="d4c95-109">參數</span><span class="sxs-lookup"><span data-stu-id="d4c95-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4c95-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d4c95-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c95-111">如果 DMR 目前接受 [**PauseAsync**](imediarenderer-pauseasync.md)方法，則布林值為 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="d4c95-111">A boolean value that is **True** if the DMR is currently accepting the [**PauseAsync**](imediarenderer-pauseasync.md) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4c95-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d4c95-112">Return value</span></span>

<span data-ttu-id="d4c95-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="d4c95-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="d4c95-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="d4c95-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="d4c95-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="d4c95-115">Return code</span></span>                                                                          | <span data-ttu-id="d4c95-116">Description</span><span class="sxs-lookup"><span data-stu-id="d4c95-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="d4c95-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="d4c95-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="d4c95-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="d4c95-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="d4c95-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4c95-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c95-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="d4c95-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

