---
title: IMsRdpCameraRedirConfig DeviceExists 屬性
description: 指定相機裝置目前是否存在 (也就是相機連線) 。
ms.tgt_platform: multiple
keywords:
- DeviceExists 屬性遠端桌面服務
- DeviceExists 屬性遠端桌面服務，IMsRdpCameraRedirConfig 介面
- IMsRdpCameraRedirConfig 介面遠端桌面服務，DeviceExists 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig.DeviceExists
- IMsRdpCameraRedirConfig.get_DeviceExists
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 368b2d46e6dfc2c32c0bb294edceda31f8a58f4e
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104467402"
---
# <a name="imsrdpcameraredirconfigdeviceexists-property"></a><span data-ttu-id="5f8bc-106">IMsRdpCameraRedirConfig：:D eviceExists 屬性</span><span class="sxs-lookup"><span data-stu-id="5f8bc-106">IMsRdpCameraRedirConfig::DeviceExists property</span></span>

<span data-ttu-id="5f8bc-107">指定相機裝置目前是否存在 (也就是相機連線) 。</span><span class="sxs-lookup"><span data-stu-id="5f8bc-107">Specifies whether or not the camera device currently exists (that is, the camera is connected).</span></span>

<span data-ttu-id="5f8bc-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="5f8bc-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f8bc-109">語法</span><span class="sxs-lookup"><span data-stu-id="5f8bc-109">Syntax</span></span>

```C++
HRESULT get_DeviceExists(
    [out, retval] VARIANT_BOOL* pfExists
);
```

## <a name="property-value"></a><span data-ttu-id="5f8bc-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="5f8bc-110">Property value</span></span>

<span data-ttu-id="5f8bc-111">值，指出攝影機裝置目前是否存在 (也就是相機連線) 。</span><span class="sxs-lookup"><span data-stu-id="5f8bc-111">A value that indicates whether or not the camera device currently exists (that is, the camera is connected).</span></span>

## <a name="requirements"></a><span data-ttu-id="5f8bc-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="5f8bc-112">Requirements</span></span>

| <span data-ttu-id="5f8bc-113">需求</span><span class="sxs-lookup"><span data-stu-id="5f8bc-113">Requirement</span></span> | <span data-ttu-id="5f8bc-114">值</span><span class="sxs-lookup"><span data-stu-id="5f8bc-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="5f8bc-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5f8bc-115">Minimum supported client</span></span>| <span data-ttu-id="5f8bc-116">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="5f8bc-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="5f8bc-117">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5f8bc-117">Type library</span></span>            | <span data-ttu-id="5f8bc-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="5f8bc-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="5f8bc-119">DLL</span><span class="sxs-lookup"><span data-stu-id="5f8bc-119">DLL</span></span>                  | <span data-ttu-id="5f8bc-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="5f8bc-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="5f8bc-121">IID</span><span class="sxs-lookup"><span data-stu-id="5f8bc-121">IID</span></span>                      | <span data-ttu-id="5f8bc-122">IID \_ IMsRdpCameraRedirConfig 定義為 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="5f8bc-122">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="5f8bc-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5f8bc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f8bc-124">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="5f8bc-124">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
</dt> </dl>