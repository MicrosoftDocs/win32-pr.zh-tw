---
title: IMsRdpCameraRedirConfig 重新導向屬性
description: 指定是否將相機重新導向。
ms.tgt_platform: multiple
keywords:
- 重新導向的屬性遠端桌面服務
- 重新導向的屬性遠端桌面服務，IMsRdpCameraRedirConfig 介面
- IMsRdpCameraRedirConfig 介面遠端桌面服務，重新導向的屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.Redirected
- IMsRdpCameraRedirConfig.put_Redirected
- IMsRdpCameraRedirConfig.get_Redirected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: f81dc643f7911029df088bbb692d7c8c06fddac4
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104467400"
---
# <a name="imsrdpcameraredirconfigredirected-property"></a><span data-ttu-id="47bab-106">IMsRdpCameraRedirConfig：：重新導向的屬性</span><span class="sxs-lookup"><span data-stu-id="47bab-106">IMsRdpCameraRedirConfig::Redirected property</span></span>

<span data-ttu-id="47bab-107">指定是否將相機重新導向。</span><span class="sxs-lookup"><span data-stu-id="47bab-107">Specifies whether or not the camera is redirected.</span></span>

<span data-ttu-id="47bab-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="47bab-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="47bab-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="47bab-109">Syntax</span></span>

```C++
HRESULT put_Redirected(
    [in] VARIANT_BOOL fRedirected
);

HRESULT get_Redirected(
    [out, retval] VARIANT_BOOL* pfRedirected
);
```

## <a name="property-value"></a><span data-ttu-id="47bab-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="47bab-110">Property value</span></span>

<span data-ttu-id="47bab-111">值，指定是否重新導向相機。</span><span class="sxs-lookup"><span data-stu-id="47bab-111">A value that specifies whether or not the camera is redirected.</span></span>

## <a name="requirements"></a><span data-ttu-id="47bab-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="47bab-112">Requirements</span></span>

| <span data-ttu-id="47bab-113">需求</span><span class="sxs-lookup"><span data-stu-id="47bab-113">Requirement</span></span> | <span data-ttu-id="47bab-114">值</span><span class="sxs-lookup"><span data-stu-id="47bab-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="47bab-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="47bab-115">Minimum supported client</span></span>| <span data-ttu-id="47bab-116">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="47bab-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="47bab-117">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="47bab-117">Type library</span></span>            | <span data-ttu-id="47bab-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="47bab-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="47bab-119">DLL</span><span class="sxs-lookup"><span data-stu-id="47bab-119">DLL</span></span>                  | <span data-ttu-id="47bab-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="47bab-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="47bab-121">IID</span><span class="sxs-lookup"><span data-stu-id="47bab-121">IID</span></span>                      | <span data-ttu-id="47bab-122">IID \_ IMsRdpCameraRedirConfig 定義為 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="47bab-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="47bab-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47bab-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47bab-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="47bab-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>