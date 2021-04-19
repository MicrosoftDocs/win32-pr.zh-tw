---
title: IMsRdpCameraRedirConfig ParentInstanceId 屬性
description: 取得相機的父裝置實例識別碼。
ms.tgt_platform: multiple
keywords:
- ParentInstanceId 屬性遠端桌面服務
- ParentInstanceId 屬性遠端桌面服務，IMsRdpCameraRedirConfig 介面
- IMsRdpCameraRedirConfig 介面遠端桌面服務，ParentInstanceId 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.ParentInstanceId
- IMsRdpCameraRedirConfig.get_ParentInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e4a399659c33000207930bfe7d17818a2ad8438f
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "106971087"
---
# <a name="imsrdpcameraredirconfigparentinstanceid-property"></a><span data-ttu-id="e5ff2-106">IMsRdpCameraRedirConfig：:P arentInstanceId 屬性</span><span class="sxs-lookup"><span data-stu-id="e5ff2-106">IMsRdpCameraRedirConfig::ParentInstanceId property</span></span>

<span data-ttu-id="e5ff2-107">取得相機的父裝置實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5ff2-107">Gets the parent device instance ID of the camera.</span></span>

<span data-ttu-id="e5ff2-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="e5ff2-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5ff2-109">語法</span><span class="sxs-lookup"><span data-stu-id="e5ff2-109">Syntax</span></span>

```C++
HRESULT get_ParentInstanceId(
    [out, retval] BSTR* pParentInstanceId
);
```

## <a name="property-value"></a><span data-ttu-id="e5ff2-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="e5ff2-110">Property value</span></span>

<span data-ttu-id="e5ff2-111">相機的父裝置實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="e5ff2-111">The parent device instance ID of the camera.</span></span>

## <a name="requirements"></a><span data-ttu-id="e5ff2-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="e5ff2-112">Requirements</span></span>

| <span data-ttu-id="e5ff2-113">需求</span><span class="sxs-lookup"><span data-stu-id="e5ff2-113">Requirement</span></span> | <span data-ttu-id="e5ff2-114">值</span><span class="sxs-lookup"><span data-stu-id="e5ff2-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="e5ff2-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e5ff2-115">Minimum supported client</span></span>| <span data-ttu-id="e5ff2-116">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="e5ff2-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="e5ff2-117">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e5ff2-117">Type library</span></span>            | <span data-ttu-id="e5ff2-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="e5ff2-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="e5ff2-119">DLL</span><span class="sxs-lookup"><span data-stu-id="e5ff2-119">DLL</span></span>                  | <span data-ttu-id="e5ff2-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="e5ff2-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="e5ff2-121">IID</span><span class="sxs-lookup"><span data-stu-id="e5ff2-121">IID</span></span>                      | <span data-ttu-id="e5ff2-122">IID \_ IMsRdpCameraRedirConfig 定義為 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="e5ff2-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="e5ff2-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e5ff2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5ff2-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="e5ff2-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>