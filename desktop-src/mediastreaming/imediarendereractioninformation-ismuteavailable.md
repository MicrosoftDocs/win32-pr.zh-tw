---
title: IMediaRendererActionInformation IsMuteAvailable 方法
description: 抓取值，指出 DMR 是否能夠將音訊靜音。
ms.assetid: F744C2D7-5518-4A9F-A71E-60CF0B312177
keywords:
- IsMuteAvailable 方法媒體串流 API
- IsMuteAvailable 方法媒體串流 API，IMediaRendererActionInformation 介面
- IMediaRendererActionInformation 介面媒體串流 API，IsMuteAvailable 方法
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsMuteAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 96751a7f2f1aedcd9e29be981ffadf6c43bf4008
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023363"
---
# <a name="imediarendereractioninformationismuteavailable-method"></a><span data-ttu-id="70155-106">IMediaRendererActionInformation：： IsMuteAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="70155-106">IMediaRendererActionInformation::IsMuteAvailable method</span></span>

<span data-ttu-id="70155-107">抓取值，指出 DMR 是否能夠將音訊靜音。</span><span class="sxs-lookup"><span data-stu-id="70155-107">Retrieves a value that indicates whether the DMR is capable of muting the audio.</span></span>

## <a name="syntax"></a><span data-ttu-id="70155-108">語法</span><span class="sxs-lookup"><span data-stu-id="70155-108">Syntax</span></span>


```C++
HRESULT IsMuteAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="70155-109">參數</span><span class="sxs-lookup"><span data-stu-id="70155-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70155-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="70155-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="70155-111">布林值，如果 DMR 能夠將音訊靜音，則為 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="70155-111">A boolean value that is **True** if the DMR is capable of muting the audio and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70155-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="70155-112">Return value</span></span>

<span data-ttu-id="70155-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="70155-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="70155-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="70155-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="70155-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="70155-115">Return code</span></span>                                                                          | <span data-ttu-id="70155-116">Description</span><span class="sxs-lookup"><span data-stu-id="70155-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="70155-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="70155-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="70155-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="70155-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="70155-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70155-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70155-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="70155-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

