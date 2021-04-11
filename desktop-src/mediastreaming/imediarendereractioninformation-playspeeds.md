---
title: IMediaRendererActionInformation PlaySpeeds 方法
description: 抓取 DMR 所接受之 PlaySpeed 值的完整清單。
ms.assetid: 0AB63E39-6A26-4199-9978-A10866A7C805
keywords:
- PlaySpeeds 方法媒體串流 API
- PlaySpeeds 方法媒體串流 API，IMediaRendererActionInformation 介面
- IMediaRendererActionInformation 介面媒體串流 API，PlaySpeeds 方法
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.PlaySpeeds
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 31089dd7616c035ebde4079c51988b94d1c27562
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314986"
---
# <a name="imediarendereractioninformationplayspeeds-method"></a><span data-ttu-id="fd776-106">IMediaRendererActionInformation：:P laySpeeds 方法</span><span class="sxs-lookup"><span data-stu-id="fd776-106">IMediaRendererActionInformation::PlaySpeeds method</span></span>

<span data-ttu-id="fd776-107">抓取 DMR 所接受之 [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) 值的完整清單。</span><span class="sxs-lookup"><span data-stu-id="fd776-107">Retrieves the complete list of [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) values that are accepted by the DMR.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd776-108">語法</span><span class="sxs-lookup"><span data-stu-id="fd776-108">Syntax</span></span>


```C++
HRESULT PlaySpeeds(
  [out] IVector< PlaySpeed > **value
);
```



## <a name="parameters"></a><span data-ttu-id="fd776-109">參數</span><span class="sxs-lookup"><span data-stu-id="fd776-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fd776-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fd776-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fd776-111">接收 [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) 結構的向量，指定 DMR 接受之 **PlaySpeed** 值的完整清單。</span><span class="sxs-lookup"><span data-stu-id="fd776-111">Receives a vector of [**PlaySpeed**](/previous-versions/windows/desktop/api/windows.media.streaming/ns-windows-media-streaming-playspeed) structures specifying the complete list of **PlaySpeed** values that are accepted by the DMR.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fd776-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="fd776-112">Return value</span></span>

<span data-ttu-id="fd776-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="fd776-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="fd776-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="fd776-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="fd776-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="fd776-115">Return code</span></span>                                                                          | <span data-ttu-id="fd776-116">Description</span><span class="sxs-lookup"><span data-stu-id="fd776-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="fd776-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="fd776-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="fd776-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="fd776-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="fd776-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd776-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd776-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="fd776-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

