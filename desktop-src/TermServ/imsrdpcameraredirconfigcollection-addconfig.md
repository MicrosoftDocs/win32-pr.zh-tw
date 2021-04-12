---
title: IMsRdpCameraRedirConfigCollection AddConfig 方法
description: 將 IMsRdpCameraRedirConfig 物件新增至集合 (對應的相機不需要連線) 。
ms.tgt_platform: multiple
keywords:
- AddConfig 方法遠端桌面服務
- AddConfig 方法遠端桌面服務，IMsRdpCameraRedirConfigCollection 介面
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務，AddConfig 方法
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.AddConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e8c954b710c3f35bca9685d461e478104dac9039
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104509737"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a><span data-ttu-id="d911b-106">IMsRdpCameraRedirConfigCollection：： AddConfig 方法</span><span class="sxs-lookup"><span data-stu-id="d911b-106">IMsRdpCameraRedirConfigCollection::AddConfig method</span></span>

<span data-ttu-id="d911b-107">將 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件新增至集合 (對應的相機不需要連線) 。</span><span class="sxs-lookup"><span data-stu-id="d911b-107">Adds an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object to the collection (the corresponding camera does not have to be connected).</span></span>

## <a name="syntax"></a><span data-ttu-id="d911b-108">語法</span><span class="sxs-lookup"><span data-stu-id="d911b-108">Syntax</span></span>

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a><span data-ttu-id="d911b-109">參數</span><span class="sxs-lookup"><span data-stu-id="d911b-109">Parameters</span></span>

<span data-ttu-id="d911b-110">*>symboliclink* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d911b-110">*symbolicLink* \[in\]</span></span>

<span data-ttu-id="d911b-111">新 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件的符號連結。</span><span class="sxs-lookup"><span data-stu-id="d911b-111">The symbolic link for the new [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object.</span></span>

<span data-ttu-id="d911b-112">*fRedirected* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d911b-112">*fRedirected* \[in\]</span></span>

<span data-ttu-id="d911b-113">指定是否預設會重新導向新的相機。</span><span class="sxs-lookup"><span data-stu-id="d911b-113">Specifies whether or not the new camera gets redirected by default.</span></span>

## <a name="return-value"></a><span data-ttu-id="d911b-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="d911b-114">Return value</span></span>

<span data-ttu-id="d911b-115">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="d911b-115">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="d911b-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="d911b-116">Requirements</span></span>

| <span data-ttu-id="d911b-117">需求</span><span class="sxs-lookup"><span data-stu-id="d911b-117">Requirement</span></span> | <span data-ttu-id="d911b-118">值</span><span class="sxs-lookup"><span data-stu-id="d911b-118">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="d911b-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d911b-119">Minimum supported client</span></span>| <span data-ttu-id="d911b-120">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="d911b-120">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="d911b-121">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d911b-121">Type library</span></span>            | <span data-ttu-id="d911b-122">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="d911b-122">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="d911b-123">DLL</span><span class="sxs-lookup"><span data-stu-id="d911b-123">DLL</span></span>                  | <span data-ttu-id="d911b-124">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="d911b-124">MsTscAx.dll</span></span>     |
| <span data-ttu-id="d911b-125">IID</span><span class="sxs-lookup"><span data-stu-id="d911b-125">IID</span></span>                      | <span data-ttu-id="d911b-126">IID \_ IMsRdpCameraRedirConfigCollection 定義為 AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="d911b-126">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="d911b-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d911b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d911b-128">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="d911b-128">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>