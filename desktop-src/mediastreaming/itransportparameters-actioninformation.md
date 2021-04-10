---
title: ITransportParameters Actioninformation .action 方法
description: 取得 IMediaRendererActionInformation 介面，以提供目前可在 DMR 上叫用之方法的相關資訊。
ms.assetid: 3EEB94E1-B6BC-4111-AEF1-D5724BD0A2E7
keywords:
- Actioninformation .action 方法媒體串流 API
- Actioninformation .action 方法媒體串流 API，ITransportParameters 介面
- ITransportParameters 介面媒體串流 API，Actioninformation .action 方法
topic_type:
- apiref
api_name:
- ITransportParameters.ActionInformation
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b194da50e71402b6af69eb4cc9d67902e8ae89a0
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023376"
---
# <a name="itransportparametersactioninformation-method"></a><span data-ttu-id="5e22a-106">ITransportParameters：： Actioninformation .action 方法</span><span class="sxs-lookup"><span data-stu-id="5e22a-106">ITransportParameters::ActionInformation method</span></span>

<span data-ttu-id="5e22a-107">取得 [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) 介面，以提供目前可在 DMR 上叫用之方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="5e22a-107">Obtains an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface that provides information about which methods can currently be invoked on the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="5e22a-108">語法</span><span class="sxs-lookup"><span data-stu-id="5e22a-108">Syntax</span></span>


```C++
HRESULT ActionInformation(
  [out, retval] IMediaRendererActionInformation **value
);
```



## <a name="parameters"></a><span data-ttu-id="5e22a-109">參數</span><span class="sxs-lookup"><span data-stu-id="5e22a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5e22a-110">*值* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="5e22a-110">*value* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5e22a-111">接收 [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) 介面的參考。</span><span class="sxs-lookup"><span data-stu-id="5e22a-111">Receives a reference to an [**IMediaRendererActionInformation**](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5e22a-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="5e22a-112">Return value</span></span>

<span data-ttu-id="5e22a-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="5e22a-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="5e22a-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="5e22a-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="5e22a-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="5e22a-115">Return code</span></span>                                                                          | <span data-ttu-id="5e22a-116">Description</span><span class="sxs-lookup"><span data-stu-id="5e22a-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5e22a-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="5e22a-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="5e22a-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="5e22a-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="5e22a-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5e22a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5e22a-120">**ITransportParameters**</span><span class="sxs-lookup"><span data-stu-id="5e22a-120">**ITransportParameters**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-itransportparameters)
</dt> </dl>

 

