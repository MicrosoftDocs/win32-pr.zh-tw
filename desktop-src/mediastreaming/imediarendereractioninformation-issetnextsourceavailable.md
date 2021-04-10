---
title: IMediaRendererActionInformation IsSetNextSourceAvailable 方法
description: 抓取值，這個值表示 DMR 目前是否接受 SetNextSourceFromUriAsync 方法、SetNextSourceFromStreamAsync 方法或 SetNextSourceFromMediaSourceAsync 方法。
ms.assetid: 7588E992-4070-4E0F-8C4B-7DFC097A5076
keywords:
- IsSetNextSourceAvailable 方法媒體串流 API
- IsSetNextSourceAvailable 方法媒體串流 API，IMediaRendererActionInformation 介面
- IMediaRendererActionInformation 介面媒體串流 API，IsSetNextSourceAvailable 方法
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsSetNextSourceAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 265a9a96d5229e47008c60813fd6c0e3bc567800
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682005"
---
# <a name="imediarendereractioninformationissetnextsourceavailable-method"></a><span data-ttu-id="3c2d2-106">IMediaRendererActionInformation：： IsSetNextSourceAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="3c2d2-106">IMediaRendererActionInformation::IsSetNextSourceAvailable method</span></span>

<span data-ttu-id="3c2d2-107">抓取值，這個值表示 DMR 目前是否接受 [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) 方法、 [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) 方法或 [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) 方法。</span><span class="sxs-lookup"><span data-stu-id="3c2d2-107">Retrieves a value that indicates whether the DMR is currently accepting the [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) method, the [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) method or the [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c2d2-108">語法</span><span class="sxs-lookup"><span data-stu-id="3c2d2-108">Syntax</span></span>


```C++
HRESULT IsSetNextSourceAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="3c2d2-109">參數</span><span class="sxs-lookup"><span data-stu-id="3c2d2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c2d2-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3c2d2-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2d2-111">如果 DMR 目前接受 [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync)方法、 [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync)方法或 [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync)方法，則布林值為 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="3c2d2-111">A boolean value that is **True** if the DMR is currently accepting the [**SetNextSourceFromUriAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromuriasync) method, the [**SetNextSourceFromStreamAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefromstreamasync) method or the [**SetNextSourceFromMediaSourceAsync**](/previous-versions/windows/desktop/api/windows.media.streaming/nf-windows-media-streaming-imediarenderer-setnextsourcefrommediasourceasync) method and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c2d2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c2d2-112">Return value</span></span>

<span data-ttu-id="3c2d2-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="3c2d2-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="3c2d2-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="3c2d2-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="3c2d2-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="3c2d2-115">Return code</span></span>                                                                          | <span data-ttu-id="3c2d2-116">Description</span><span class="sxs-lookup"><span data-stu-id="3c2d2-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="3c2d2-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="3c2d2-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="3c2d2-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="3c2d2-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="3c2d2-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c2d2-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c2d2-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="3c2d2-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

