---
title: IMediaRendererActionInformation IsVolumeAvailable 方法
description: 抓取指出 DMR 是否能夠調整音訊音量層級的值。
ms.assetid: 6DFDC37A-3304-4CDB-9928-C113D2F64ED0
keywords:
- IsVolumeAvailable 方法媒體串流 API
- IsVolumeAvailable 方法媒體串流 API，IMediaRendererActionInformation 介面
- IMediaRendererActionInformation 介面媒體串流 API，IsVolumeAvailable 方法
topic_type:
- apiref
api_name:
- IMediaRendererActionInformation.IsVolumeAvailable
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: bb8dc60c25cf3ec12e0ebeaa863e239c287d7c46
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104092666"
---
# <a name="imediarendereractioninformationisvolumeavailable-method"></a><span data-ttu-id="feb5e-106">IMediaRendererActionInformation：： IsVolumeAvailable 方法</span><span class="sxs-lookup"><span data-stu-id="feb5e-106">IMediaRendererActionInformation::IsVolumeAvailable method</span></span>

<span data-ttu-id="feb5e-107">抓取指出 DMR 是否能夠調整音訊音量層級的值。</span><span class="sxs-lookup"><span data-stu-id="feb5e-107">Retrieves a value that indicates whether the DMR is capable of adjusting the audio volume level.</span></span>

## <a name="syntax"></a><span data-ttu-id="feb5e-108">語法</span><span class="sxs-lookup"><span data-stu-id="feb5e-108">Syntax</span></span>


```C++
HRESULT IsVolumeAvailable(
  [out] boolean *value
);
```



## <a name="parameters"></a><span data-ttu-id="feb5e-109">參數</span><span class="sxs-lookup"><span data-stu-id="feb5e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="feb5e-110">*值* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="feb5e-110">*value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="feb5e-111">布林值，如果 DMR 能夠調整音訊音量層級，則為 **True** ，否則為 **False** 。</span><span class="sxs-lookup"><span data-stu-id="feb5e-111">A boolean value that is **True** if the DMR is capable of adjusting the audio volume level and **False** if it is not.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="feb5e-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="feb5e-112">Return value</span></span>

<span data-ttu-id="feb5e-113">方法會傳回 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="feb5e-113">The method returns an **HRESULT**.</span></span> <span data-ttu-id="feb5e-114">可能的值包括 (但不限於) 下表中的這些值。</span><span class="sxs-lookup"><span data-stu-id="feb5e-114">Possible values include, but are not limited to, those in the following table.</span></span>



| <span data-ttu-id="feb5e-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="feb5e-115">Return code</span></span>                                                                          | <span data-ttu-id="feb5e-116">Description</span><span class="sxs-lookup"><span data-stu-id="feb5e-116">Description</span></span>                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="feb5e-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="feb5e-117"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="feb5e-118">此方法已成功。</span><span class="sxs-lookup"><span data-stu-id="feb5e-118">The method succeeded.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="feb5e-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="feb5e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="feb5e-120">**IMediaRendererActionInformation**</span><span class="sxs-lookup"><span data-stu-id="feb5e-120">**IMediaRendererActionInformation**</span></span>](/previous-versions/windows/desktop/api/windows.media.streaming/nn-windows-media-streaming-imediarendereractioninformation)
</dt> </dl>

 

