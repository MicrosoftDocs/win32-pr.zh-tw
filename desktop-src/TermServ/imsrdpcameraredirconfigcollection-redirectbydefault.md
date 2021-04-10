---
title: IMsRdpCameraRedirConfigCollection RedirectByDefault 屬性
description: 指定是否根據預設，將任何新的相機重新導向。
ms.tgt_platform: multiple
keywords:
- RedirectByDefault 屬性遠端桌面服務
- RedirectByDefault 屬性遠端桌面服務，IMsRdpCameraRedirConfigCollection 介面
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務，RedirectByDefault 屬性
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.RedirectByDefault
- IMsRdpCameraRedirConfigCollection.put_RedirectByDefault
- IMsRdpCameraRedirConfigCollection.get_RedirectByDefault
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 810af200eefee0008aea21af684c02b6d31325eb
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104108357"
---
# <a name="imsrdpcameraredirconfigcollectionredirectbydefault-property"></a><span data-ttu-id="665b3-106">IMsRdpCameraRedirConfigCollection：： RedirectByDefault 屬性</span><span class="sxs-lookup"><span data-stu-id="665b3-106">IMsRdpCameraRedirConfigCollection::RedirectByDefault property</span></span>

<span data-ttu-id="665b3-107">指定是否根據預設，將任何新的相機重新導向。</span><span class="sxs-lookup"><span data-stu-id="665b3-107">Specifies whether or not any new camera gets redirected by default.</span></span>

<span data-ttu-id="665b3-108">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="665b3-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="665b3-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="665b3-109">Syntax</span></span>

```C++
HRESULT put_RedirectByDefault(
    [in] VARIANT_BOOL fRedirect
);

HRESULT get_RedirectByDefault(
    [out, retval] VARIANT_BOOL* pfRedirect
);
```

## <a name="property-value"></a><span data-ttu-id="665b3-110">屬性值</span><span class="sxs-lookup"><span data-stu-id="665b3-110">Property value</span></span>

<span data-ttu-id="665b3-111">值，指出是否根據預設，將任何新的相機重新導向。</span><span class="sxs-lookup"><span data-stu-id="665b3-111">A value that indicates whether or not any new camera gets redirected by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="665b3-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="665b3-112">Requirements</span></span>

| <span data-ttu-id="665b3-113">需求</span><span class="sxs-lookup"><span data-stu-id="665b3-113">Requirement</span></span> | <span data-ttu-id="665b3-114">值</span><span class="sxs-lookup"><span data-stu-id="665b3-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="665b3-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="665b3-115">Minimum supported client</span></span>| <span data-ttu-id="665b3-116">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="665b3-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="665b3-117">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="665b3-117">Type library</span></span>            | <span data-ttu-id="665b3-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="665b3-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="665b3-119">DLL</span><span class="sxs-lookup"><span data-stu-id="665b3-119">DLL</span></span>                  | <span data-ttu-id="665b3-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="665b3-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="665b3-121">IID</span><span class="sxs-lookup"><span data-stu-id="665b3-121">IID</span></span>                      | <span data-ttu-id="665b3-122">IID \_ IMsRdpCameraRedirConfigCollection 定義為 AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="665b3-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="665b3-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="665b3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="665b3-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="665b3-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>