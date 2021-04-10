---
title: IMsRdpCameraRedirConfigCollection EncodeVideo 屬性
description: 指定影片資料流程是否為 h.264 編碼。
ms.tgt_platform: multiple
keywords:
- EncodeVideo 屬性遠端桌面服務
- EncodeVideo 屬性遠端桌面服務，IMsRdpCameraRedirConfigCollection 介面
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務，EncodeVideo 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.EncodeVideo
- IMsRdpCameraRedirConfigCollection.put_EncodeVideo
- IMsRdpCameraRedirConfigCollection.get_EncodeVideo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 6b2994f4db3de04f339bb242120b6c63cd2e0c7b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104108360"
---
# <a name="imsrdpcameraredirconfigcollectionencodevideo-property"></a><span data-ttu-id="d5cee-106">IMsRdpCameraRedirConfigCollection：： EncodeVideo 屬性</span><span class="sxs-lookup"><span data-stu-id="d5cee-106">IMsRdpCameraRedirConfigCollection::EncodeVideo property</span></span>

<span data-ttu-id="d5cee-107">指定影片資料流程是否為 h.264 編碼。</span><span class="sxs-lookup"><span data-stu-id="d5cee-107">Specifies whether or not the video stream is H.264 encoded.</span></span>

<span data-ttu-id="d5cee-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d5cee-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5cee-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5cee-109">Syntax</span></span>

```C++
HRESULT put_EncodeVideo(
    [in] VARIANT_BOOL fEncode
);

HRESULT get_EncodeVideo(
    [out, retval] VARIANT_BOOL* pfEncode
);
```

## <a name="property-value"></a><span data-ttu-id="d5cee-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="d5cee-110">Property value</span></span>

<span data-ttu-id="d5cee-111">值，指出影片資料流程是否為 h.264 編碼。</span><span class="sxs-lookup"><span data-stu-id="d5cee-111">A value that indicates whether or not the video stream is H.264 encoded.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5cee-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5cee-112">Requirements</span></span>

| <span data-ttu-id="d5cee-113">需求</span><span class="sxs-lookup"><span data-stu-id="d5cee-113">Requirement</span></span> | <span data-ttu-id="d5cee-114">值</span><span class="sxs-lookup"><span data-stu-id="d5cee-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="d5cee-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5cee-115">Minimum supported client</span></span>| <span data-ttu-id="d5cee-116">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="d5cee-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="d5cee-117">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d5cee-117">Type library</span></span>            | <span data-ttu-id="d5cee-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="d5cee-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="d5cee-119">DLL</span><span class="sxs-lookup"><span data-stu-id="d5cee-119">DLL</span></span>                  | <span data-ttu-id="d5cee-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="d5cee-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="d5cee-121">IID</span><span class="sxs-lookup"><span data-stu-id="d5cee-121">IID</span></span>                      | <span data-ttu-id="d5cee-122">IID \_ IMsRdpCameraRedirConfigCollection 定義為 AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="d5cee-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="d5cee-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5cee-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5cee-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="d5cee-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>