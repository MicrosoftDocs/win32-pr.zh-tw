---
title: IMsRdpCameraRedirConfigCollection BySymbolicLink 屬性
description: 從集合中傳回 IMsRdpCameraRedirConfig 物件，這個集合會對應至相機的 **KSCATEGORY_VIDEO_CAMERA** 介面之指定符號連結。
ms.tgt_platform: multiple
keywords:
- BySymbolicLink 屬性遠端桌面服務
- BySymbolicLink 屬性遠端桌面服務，IMsRdpCameraRedirConfigCollection 介面
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務，BySymbolicLink 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.BySymbolicLink
- IMsRdpCameraRedirConfigCollection.get_BySymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d4888c7e468e0522240d8ef922563ab28eb33e77
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "106996595"
---
# <a name="imsrdpcameraredirconfigcollectionbysymboliclink-property"></a><span data-ttu-id="939dd-106">IMsRdpCameraRedirConfigCollection::.BySymbolicLink 屬性</span><span class="sxs-lookup"><span data-stu-id="939dd-106">IMsRdpCameraRedirConfigCollection::.BySymbolicLink property</span></span>

<span data-ttu-id="939dd-107">從集合中傳回 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件，這個集合會對應至相機的 **KSCATEGORY_VIDEO_CAMERA** 介面之指定符號連結。</span><span class="sxs-lookup"><span data-stu-id="939dd-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the given symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

<span data-ttu-id="939dd-108">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="939dd-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="939dd-109">語法</span><span class="sxs-lookup"><span data-stu-id="939dd-109">Syntax</span></span>

```C++
HRESULT get_BySymbolicLink(
    [in]          BSTR symbolicLink,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="939dd-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="939dd-110">Property value</span></span>

<span data-ttu-id="939dd-111">對應到指定符號連結的 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="939dd-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified symbolic link.</span></span>

## <a name="requirements"></a><span data-ttu-id="939dd-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="939dd-112">Requirements</span></span>

| <span data-ttu-id="939dd-113">需求</span><span class="sxs-lookup"><span data-stu-id="939dd-113">Requirement</span></span> | <span data-ttu-id="939dd-114">值</span><span class="sxs-lookup"><span data-stu-id="939dd-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="939dd-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="939dd-115">Minimum supported client</span></span>| <span data-ttu-id="939dd-116">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="939dd-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="939dd-117">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="939dd-117">Type library</span></span>            | <span data-ttu-id="939dd-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="939dd-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="939dd-119">DLL</span><span class="sxs-lookup"><span data-stu-id="939dd-119">DLL</span></span>                  | <span data-ttu-id="939dd-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="939dd-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="939dd-121">IID</span><span class="sxs-lookup"><span data-stu-id="939dd-121">IID</span></span>                      | <span data-ttu-id="939dd-122">IID \_ IMsRdpCameraRedirConfigCollection 定義為 AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="939dd-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="939dd-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="939dd-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="939dd-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="939dd-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>