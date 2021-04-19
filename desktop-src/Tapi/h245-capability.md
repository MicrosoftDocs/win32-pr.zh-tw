---
description: H245 \_ 功能列舉描述音訊和影片格式支援。
ms.assetid: 76aeb3a1-3233-4425-b9db-efacbedc309e
title: 'H245_CAPABILITY 列舉 (H323priv .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7a6f81f87480f221f87680d9cf086120deb2de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990818"
---
# <a name="h245_capability-enumeration"></a><span data-ttu-id="18214-103">H245 \_ 功能列舉</span><span class="sxs-lookup"><span data-stu-id="18214-103">H245\_CAPABILITY enumeration</span></span>

<span data-ttu-id="18214-104">\[**H245 \_功能** 無法在 Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="18214-104">\[**H245\_CAPABILITY** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="18214-105">RTC 用戶端 API 提供類似的功能。\]</span><span class="sxs-lookup"><span data-stu-id="18214-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="18214-106">**H245 \_ 功能** 列舉描述音訊和影片格式支援。</span><span class="sxs-lookup"><span data-stu-id="18214-106">The **H245\_CAPABILITY** enum describes audio and video format support.</span></span>

## <a name="syntax"></a><span data-ttu-id="18214-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="18214-107">Syntax</span></span>


```C++
} H245_CAPABILITY;
```



## <a name="constants"></a><span data-ttu-id="18214-108">常數</span><span class="sxs-lookup"><span data-stu-id="18214-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="18214-109"><span id="HC_G711"></span><span id="hc_g711"></span>**HC \_ G711**</span><span class="sxs-lookup"><span data-stu-id="18214-109"><span id="HC_G711"></span><span id="hc_g711"></span>**HC\_G711**</span></span>
</dt> <dd>

<span data-ttu-id="18214-110">支援 g.711 音訊通訊協定。</span><span class="sxs-lookup"><span data-stu-id="18214-110">The G.711 audio protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="18214-111"><span id="HC_G723"></span><span id="hc_g723"></span>**HC \_ G723**</span><span class="sxs-lookup"><span data-stu-id="18214-111"><span id="HC_G723"></span><span id="hc_g723"></span>**HC\_G723**</span></span>
</dt> <dd>

<span data-ttu-id="18214-112">支援723音訊通訊協定。</span><span class="sxs-lookup"><span data-stu-id="18214-112">The G.723 audio protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="18214-113"><span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC \_ H263QCIF**</span><span class="sxs-lookup"><span data-stu-id="18214-113"><span id="HC_H263QCIF"></span><span id="hc_h263qcif"></span>**HC\_H263QCIF**</span></span>
</dt> <dd>

<span data-ttu-id="18214-114">支援 h. video 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="18214-114">The H.263 video protocol is supported.</span></span>

</dd> <dt>

<span data-ttu-id="18214-115"><span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC \_ H261QCIF**</span><span class="sxs-lookup"><span data-stu-id="18214-115"><span id="HC_H261QCIF"></span><span id="hc_h261qcif"></span>**HC\_H261QCIF**</span></span>
</dt> <dd>

<span data-ttu-id="18214-116">支援 h. video 通訊協定。</span><span class="sxs-lookup"><span data-stu-id="18214-116">The H.263 video protocol is supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="18214-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="18214-117">Requirements</span></span>



| <span data-ttu-id="18214-118">需求</span><span class="sxs-lookup"><span data-stu-id="18214-118">Requirement</span></span> | <span data-ttu-id="18214-119">值</span><span class="sxs-lookup"><span data-stu-id="18214-119">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="18214-120">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="18214-120">TAPI version</span></span><br/> | <span data-ttu-id="18214-121">需要 TAPI 3.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="18214-121">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="18214-122">標頭</span><span class="sxs-lookup"><span data-stu-id="18214-122">Header</span></span><br/>       | <dl> <span data-ttu-id="18214-123"><dt>H323priv。h</dt></span><span class="sxs-lookup"><span data-stu-id="18214-123"><dt>H323priv.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="18214-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18214-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18214-125">**IH323LineEx::SetDefaultCapabilityPreferrence**</span><span class="sxs-lookup"><span data-stu-id="18214-125">**IH323LineEx::SetDefaultCapabilityPreferrence**</span></span>](ih323lineex-setdefaultcapabilitypreferrence.md)
</dt> </dl>

 

 




