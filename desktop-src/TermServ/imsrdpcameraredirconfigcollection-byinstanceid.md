---
title: IMsRdpCameraRedirConfigCollection ByInstanceId 屬性
description: 從集合中傳回對應至指定實例識別碼的 IMsRdpCameraRedirConfig 物件。
ms.tgt_platform: multiple
keywords:
- ByInstanceId 屬性遠端桌面服務
- ByInstanceId 屬性遠端桌面服務，IMsRdpCameraRedirConfigCollection 介面
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務，ByInstanceId 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByInstanceId
- IMsRdpCameraRedirConfigCollection.get_ByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d90cb7d2f309a3df9e354ace04a840b667e5569b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104467393"
---
# <a name="imsrdpcameraredirconfigcollectionbyinstanceid-property"></a><span data-ttu-id="09b55-106">IMsRdpCameraRedirConfigCollection：： ByInstanceId 屬性</span><span class="sxs-lookup"><span data-stu-id="09b55-106">IMsRdpCameraRedirConfigCollection::ByInstanceId property</span></span>

<span data-ttu-id="09b55-107">從集合中傳回對應至指定實例識別碼的 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="09b55-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the specified instance ID.</span></span>

<span data-ttu-id="09b55-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="09b55-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="09b55-109">語法</span><span class="sxs-lookup"><span data-stu-id="09b55-109">Syntax</span></span>

```C++
HRESULT get_ByInstanceId(
    [in]          BSTR instanceId,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="09b55-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="09b55-110">Property value</span></span>

<span data-ttu-id="09b55-111">對應到指定實例識別碼的 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="09b55-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified instance ID.</span></span>

## <a name="requirements"></a><span data-ttu-id="09b55-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="09b55-112">Requirements</span></span>

| <span data-ttu-id="09b55-113">需求</span><span class="sxs-lookup"><span data-stu-id="09b55-113">Requirement</span></span> | <span data-ttu-id="09b55-114">值</span><span class="sxs-lookup"><span data-stu-id="09b55-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="09b55-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="09b55-115">Minimum supported client</span></span>| <span data-ttu-id="09b55-116">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="09b55-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="09b55-117">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="09b55-117">Type library</span></span>            | <span data-ttu-id="09b55-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="09b55-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="09b55-119">DLL</span><span class="sxs-lookup"><span data-stu-id="09b55-119">DLL</span></span>                  | <span data-ttu-id="09b55-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="09b55-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="09b55-121">IID</span><span class="sxs-lookup"><span data-stu-id="09b55-121">IID</span></span>                      | <span data-ttu-id="09b55-122">IID \_ IMsRdpCameraRedirConfigCollection 定義為 AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="09b55-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="09b55-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="09b55-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09b55-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="09b55-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>