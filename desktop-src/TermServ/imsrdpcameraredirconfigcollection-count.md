---
title: IMsRdpCameraRedirConfigCollection Count 屬性
description: 傳回集合中的 IMsRdpCameraRedirConfig 物件數目。
ms.tgt_platform: multiple
keywords:
- Count 屬性遠端桌面服務
- Count 屬性遠端桌面服務，IMsRdpCameraRedirConfigCollection 介面
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務，Count 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.Count
- IMsRdpCameraRedirConfigCollection.get_Count
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 31927428b709136de87f436ad92cc6a78fa9795a
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104467398"
---
# <a name="imsrdpcameraredirconfigcollectioncount-property"></a><span data-ttu-id="bad09-106">IMsRdpCameraRedirConfigCollection：： Count 屬性</span><span class="sxs-lookup"><span data-stu-id="bad09-106">IMsRdpCameraRedirConfigCollection::Count property</span></span>

<span data-ttu-id="bad09-107">傳回集合中的 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="bad09-107">Returns the number of [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) objects in the collection.</span></span>

<span data-ttu-id="bad09-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="bad09-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bad09-109">語法</span><span class="sxs-lookup"><span data-stu-id="bad09-109">Syntax</span></span>

```C++
HRESULT get_Count(
    [out, retval] ULONG *pCount
);
```

## <a name="property-value"></a><span data-ttu-id="bad09-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="bad09-110">Property value</span></span>

<span data-ttu-id="bad09-111">集合中的 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="bad09-111">The number of [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) objects in the collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="bad09-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="bad09-112">Requirements</span></span>

| <span data-ttu-id="bad09-113">需求</span><span class="sxs-lookup"><span data-stu-id="bad09-113">Requirement</span></span> | <span data-ttu-id="bad09-114">值</span><span class="sxs-lookup"><span data-stu-id="bad09-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="bad09-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bad09-115">Minimum supported client</span></span>| <span data-ttu-id="bad09-116">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="bad09-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="bad09-117">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bad09-117">Type library</span></span>            | <span data-ttu-id="bad09-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="bad09-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="bad09-119">DLL</span><span class="sxs-lookup"><span data-stu-id="bad09-119">DLL</span></span>                  | <span data-ttu-id="bad09-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="bad09-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="bad09-121">IID</span><span class="sxs-lookup"><span data-stu-id="bad09-121">IID</span></span>                      | <span data-ttu-id="bad09-122">IID \_ IMsRdpCameraRedirConfigCollection 定義為 AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="bad09-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="bad09-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bad09-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bad09-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="bad09-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>