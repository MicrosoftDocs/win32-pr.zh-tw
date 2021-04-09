---
title: IMsRdpCameraRedirConfig >symboliclink 屬性
description: 取得相機之 **KSCATEGORY_VIDEO_CAMERA** 介面的符號連結。
ms.tgt_platform: multiple
keywords:
- '>symboliclink 屬性遠端桌面服務'
- '>symboliclink 屬性遠端桌面服務，IMsRdpCameraRedirConfig 介面'
- IMsRdpCameraRedirConfig 介面遠端桌面服務，>symboliclink 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.SymbolicLink
- IMsRdpCameraRedirConfig.SymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 439ead6fa0868887cc5965205b22236abb5aada6
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "103845659"
---
# <a name="imsrdpcameraredirconfigsymboliclink-property"></a><span data-ttu-id="ba8fa-106">IMsRdpCameraRedirConfig：： >symboliclink 屬性</span><span class="sxs-lookup"><span data-stu-id="ba8fa-106">IMsRdpCameraRedirConfig::SymbolicLink property</span></span>

<span data-ttu-id="ba8fa-107">取得相機之 **KSCATEGORY_VIDEO_CAMERA** 介面的符號連結。</span><span class="sxs-lookup"><span data-stu-id="ba8fa-107">Gets the symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

<span data-ttu-id="ba8fa-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="ba8fa-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba8fa-109">語法</span><span class="sxs-lookup"><span data-stu-id="ba8fa-109">Syntax</span></span>

```C++
HRESULT get_SymbolicLink(
    [out, retval] BSTR* pSymbolicLink
);
```

## <a name="property-value"></a><span data-ttu-id="ba8fa-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="ba8fa-110">Property value</span></span>

<span data-ttu-id="ba8fa-111">攝影機 **KSCATEGORY_VIDEO_CAMERA** 介面的符號連結。</span><span class="sxs-lookup"><span data-stu-id="ba8fa-111">The symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba8fa-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="ba8fa-112">Requirements</span></span>

| <span data-ttu-id="ba8fa-113">需求</span><span class="sxs-lookup"><span data-stu-id="ba8fa-113">Requirement</span></span> | <span data-ttu-id="ba8fa-114">值</span><span class="sxs-lookup"><span data-stu-id="ba8fa-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="ba8fa-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ba8fa-115">Minimum supported client</span></span>| <span data-ttu-id="ba8fa-116">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="ba8fa-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="ba8fa-117">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="ba8fa-117">Type library</span></span>            | <span data-ttu-id="ba8fa-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="ba8fa-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="ba8fa-119">DLL</span><span class="sxs-lookup"><span data-stu-id="ba8fa-119">DLL</span></span>                  | <span data-ttu-id="ba8fa-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="ba8fa-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="ba8fa-121">IID</span><span class="sxs-lookup"><span data-stu-id="ba8fa-121">IID</span></span>                      | <span data-ttu-id="ba8fa-122">IID \_ IMsRdpCameraRedirConfig 定義為 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="ba8fa-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="ba8fa-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ba8fa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba8fa-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="ba8fa-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>