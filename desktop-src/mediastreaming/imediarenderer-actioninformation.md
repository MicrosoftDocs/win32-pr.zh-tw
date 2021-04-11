---
title: IMediaRenderer Actioninformation .action 方法
description: 抓取目前可在 DMR 上叫用哪些方法的相關資訊。
ms.assetid: 7681FF92-DD13-4BBC-B860-E2BDFDA74FB9
keywords:
- Actioninformation .action 方法媒體串流 API
- Actioninformation .action 方法媒體串流 API，IMediaRenderer 介面
- IMediaRenderer 介面媒體串流 API，Actioninformation .action 方法
topic_type:
- apiref
api_name:
- IMediaRenderer.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 346e43d6aaf3503c21f6a7586db5a731f0a7c478
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023391"
---
# <a name="imediarendereractioninformation-method"></a><span data-ttu-id="60028-106">IMediaRenderer：： Actioninformation .action 方法</span><span class="sxs-lookup"><span data-stu-id="60028-106">IMediaRenderer::ActionInformation method</span></span>

<span data-ttu-id="60028-107">抓取目前可在 DMR 上叫用哪些方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="60028-107">Retrieves information about which methods can currently be invoked on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="60028-108">語法</span><span class="sxs-lookup"><span data-stu-id="60028-108">Syntax</span></span>


```C++
HRESULT ActionInformation(
  [out] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a><span data-ttu-id="60028-109">參數</span><span class="sxs-lookup"><span data-stu-id="60028-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60028-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="60028-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60028-111">接收 [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) 介面的參考。</span><span class="sxs-lookup"><span data-stu-id="60028-111">Receives a reference to an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60028-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="60028-112">Return value</span></span>

<span data-ttu-id="60028-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="60028-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="60028-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="60028-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="60028-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="60028-115">Return code</span></span>                                                                          | <span data-ttu-id="60028-116">Description</span><span class="sxs-lookup"><span data-stu-id="60028-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="60028-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="60028-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="60028-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="60028-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="60028-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60028-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60028-120">**IMediaRenderer**</span><span class="sxs-lookup"><span data-stu-id="60028-120">**IMediaRenderer**</span></span>](imediarenderer.md)
</dt> </dl>

 

