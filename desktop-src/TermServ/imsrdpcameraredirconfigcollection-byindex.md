---
title: IMsRdpCameraRedirConfigCollection ByIndex 屬性
description: 依物件在集合中的索引傳回 IMsRdpCameraRedirConfig 物件。
ms.tgt_platform: multiple
keywords:
- ByIndex 屬性遠端桌面服務
- ByIndex 屬性遠端桌面服務，IMsRdpCameraRedirConfigCollection 介面
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務，ByIndex 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByIndex
- IMsRdpCameraRedirConfigCollection.get_ByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 68c179023e93295ee846da22357d5f8efb75b15c
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "106973121"
---
# <a name="imsrdpcameraredirconfigcollectionbyindex-property"></a><span data-ttu-id="825a2-106">IMsRdpCameraRedirConfigCollection：： ByIndex 屬性</span><span class="sxs-lookup"><span data-stu-id="825a2-106">IMsRdpCameraRedirConfigCollection::ByIndex property</span></span>

<span data-ttu-id="825a2-107">依物件在集合中的索引傳回 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="825a2-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object by its index in the collection.</span></span>

<span data-ttu-id="825a2-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="825a2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="825a2-109">語法</span><span class="sxs-lookup"><span data-stu-id="825a2-109">Syntax</span></span>

```C++
HRESULT get_ByIndex(
    [in]            ULONG index,
    [out, retval]   IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="825a2-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="825a2-110">Property value</span></span>

<span data-ttu-id="825a2-111">對應至指定之索引的 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="825a2-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified index.</span></span>

## <a name="requirements"></a><span data-ttu-id="825a2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="825a2-112">Requirements</span></span>

| <span data-ttu-id="825a2-113">需求</span><span class="sxs-lookup"><span data-stu-id="825a2-113">Requirement</span></span> | <span data-ttu-id="825a2-114">值</span><span class="sxs-lookup"><span data-stu-id="825a2-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="825a2-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="825a2-115">Minimum supported client</span></span>| <span data-ttu-id="825a2-116">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="825a2-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="825a2-117">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="825a2-117">Type library</span></span>            | <span data-ttu-id="825a2-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="825a2-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="825a2-119">DLL</span><span class="sxs-lookup"><span data-stu-id="825a2-119">DLL</span></span>                  | <span data-ttu-id="825a2-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="825a2-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="825a2-121">IID</span><span class="sxs-lookup"><span data-stu-id="825a2-121">IID</span></span>                      | <span data-ttu-id="825a2-122">IID \_ IMsRdpCameraRedirConfigCollection 定義為 AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="825a2-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="825a2-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="825a2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="825a2-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="825a2-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>