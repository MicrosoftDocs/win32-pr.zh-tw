---
title: IMsRdpCameraRedirConfig InstanceId 屬性
description: 取得相機的實例識別碼。
ms.tgt_platform: multiple
keywords:
- InstanceId 屬性遠端桌面服務
- InstanceId 屬性遠端桌面服務，IMsRdpCameraRedirConfig 介面
- IMsRdpCameraRedirConfig 介面遠端桌面服務，InstanceId 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.InstanceId
- IMsRdpCameraRedirConfig.get_InstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 42654e84f64b25a051a78963339ca95d4ebf760f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104187366"
---
# <a name="imsrdpcameraredirconfiginstanceid-property"></a><span data-ttu-id="999ff-106">IMsRdpCameraRedirConfig：： InstanceId 屬性</span><span class="sxs-lookup"><span data-stu-id="999ff-106">IMsRdpCameraRedirConfig::InstanceId property</span></span>

<span data-ttu-id="999ff-107">取得相機的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="999ff-107">Gets the instance ID of the camera.</span></span>

<span data-ttu-id="999ff-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="999ff-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="999ff-109">語法</span><span class="sxs-lookup"><span data-stu-id="999ff-109">Syntax</span></span>

```C++
HRESULT get_InstanceId(
    [out, retval] BSTR* pInstanceId
);
```

## <a name="property-value"></a><span data-ttu-id="999ff-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="999ff-110">Property value</span></span>

<span data-ttu-id="999ff-111">攝影機的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="999ff-111">The instance ID of the camera.</span></span>

## <a name="requirements"></a><span data-ttu-id="999ff-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="999ff-112">Requirements</span></span>

| <span data-ttu-id="999ff-113">需求</span><span class="sxs-lookup"><span data-stu-id="999ff-113">Requirement</span></span> | <span data-ttu-id="999ff-114">值</span><span class="sxs-lookup"><span data-stu-id="999ff-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="999ff-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="999ff-115">Minimum supported client</span></span>| <span data-ttu-id="999ff-116">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="999ff-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="999ff-117">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="999ff-117">Type library</span></span>            | <span data-ttu-id="999ff-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="999ff-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="999ff-119">DLL</span><span class="sxs-lookup"><span data-stu-id="999ff-119">DLL</span></span>                  | <span data-ttu-id="999ff-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="999ff-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="999ff-121">IID</span><span class="sxs-lookup"><span data-stu-id="999ff-121">IID</span></span>                      | <span data-ttu-id="999ff-122">IID \_ IMsRdpCameraRedirConfig 定義為 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="999ff-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="999ff-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="999ff-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="999ff-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="999ff-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>