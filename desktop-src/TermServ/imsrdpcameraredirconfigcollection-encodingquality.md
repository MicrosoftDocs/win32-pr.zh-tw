---
title: IMsRdpCameraRedirConfigCollection EncodingQuality 屬性
description: 指定編碼品質 (位速率) 。
ms.tgt_platform: multiple
keywords:
- EncodingQuality 屬性遠端桌面服務
- EncodingQuality 屬性遠端桌面服務，IMsRdpCameraRedirConfigCollection 介面
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務，EncodingQuality 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodingQuality
- IMsRdpCameraRedirConfigCollection.put_EncodingQuality
- IMsRdpCameraRedirConfigCollection.get_EncodingQuality
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d8044c2fb70233243a3a74d8dc5faac96873cb48
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104467396"
---
# <a name="imsrdpcameraredirconfigcollectionencodingquality-property"></a><span data-ttu-id="1ac52-106">IMsRdpCameraRedirConfigCollection：： EncodingQuality 屬性</span><span class="sxs-lookup"><span data-stu-id="1ac52-106">IMsRdpCameraRedirConfigCollection::EncodingQuality property</span></span>

<span data-ttu-id="1ac52-107">指定編碼品質 (位速率) 。</span><span class="sxs-lookup"><span data-stu-id="1ac52-107">Specifies the encoding quality (bit rate).</span></span>

<span data-ttu-id="1ac52-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="1ac52-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ac52-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ac52-109">Syntax</span></span>

```C++
HRESULT put_EncodingQuality(
    [in] CameraRedirEncodingQuality encodingQuality
);

HRESULT get_EncodingQuality(
    [out, retval] CameraRedirEncodingQuality* pEncodingQuality
);
```

## <a name="property-value"></a><span data-ttu-id="1ac52-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="1ac52-110">Property value</span></span>

<span data-ttu-id="1ac52-111">下列其中一個 **CameraRedirEncodingQuality** 列舉值，指定編碼品質 (位速率) 。</span><span class="sxs-lookup"><span data-stu-id="1ac52-111">One of the following **CameraRedirEncodingQuality** enum values that specifies the encoding quality (bit rate).</span></span>

| <span data-ttu-id="1ac52-112">列舉成員名稱</span><span class="sxs-lookup"><span data-stu-id="1ac52-112">Enum member name</span></span> | <span data-ttu-id="1ac52-113">值</span><span class="sxs-lookup"><span data-stu-id="1ac52-113">Value</span></span> |
|-----------------|--------|
| <span data-ttu-id="1ac52-114">encodingQualityLow</span><span class="sxs-lookup"><span data-stu-id="1ac52-114">encodingQualityLow</span></span> | <span data-ttu-id="1ac52-115">0x0000</span><span class="sxs-lookup"><span data-stu-id="1ac52-115">0x0000</span></span> |
| <span data-ttu-id="1ac52-116">encodingQualityMedium</span><span class="sxs-lookup"><span data-stu-id="1ac52-116">encodingQualityMedium</span></span> | <span data-ttu-id="1ac52-117">0x0001</span><span class="sxs-lookup"><span data-stu-id="1ac52-117">0x0001</span></span> |
| <span data-ttu-id="1ac52-118">encodingQualityHigh</span><span class="sxs-lookup"><span data-stu-id="1ac52-118">encodingQualityHigh</span></span> | <span data-ttu-id="1ac52-119">0x0002</span><span class="sxs-lookup"><span data-stu-id="1ac52-119">0x0002</span></span> |

## <a name="requirements"></a><span data-ttu-id="1ac52-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ac52-120">Requirements</span></span>

| <span data-ttu-id="1ac52-121">需求</span><span class="sxs-lookup"><span data-stu-id="1ac52-121">Requirement</span></span> | <span data-ttu-id="1ac52-122">值</span><span class="sxs-lookup"><span data-stu-id="1ac52-122">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="1ac52-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ac52-123">Minimum supported client</span></span>| <span data-ttu-id="1ac52-124">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="1ac52-124">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="1ac52-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="1ac52-125">Type library</span></span>            | <span data-ttu-id="1ac52-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="1ac52-126">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="1ac52-127">DLL</span><span class="sxs-lookup"><span data-stu-id="1ac52-127">DLL</span></span>                  | <span data-ttu-id="1ac52-128">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="1ac52-128">MsTscAx.dll</span></span>     |
| <span data-ttu-id="1ac52-129">IID</span><span class="sxs-lookup"><span data-stu-id="1ac52-129">IID</span></span>                      | <span data-ttu-id="1ac52-130">IID \_ IMsRdpCameraRedirConfigCollection 定義為 AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="1ac52-130">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="1ac52-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ac52-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ac52-132">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="1ac52-132">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>