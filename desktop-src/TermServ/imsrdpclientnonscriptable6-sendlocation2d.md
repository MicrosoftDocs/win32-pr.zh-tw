---
title: IMsRdpClientNonScriptable6 SendLocation2D 方法
description: 將緯度和經度值傳送至伺服器，讓用戶端的地理位置可以反映在遠端會話中。
ms.tgt_platform: multiple
keywords:
- SendLocation2D 方法遠端桌面服務
- SendLocation2D 方法遠端桌面服務，IMsRdpClientNonScriptable6 介面
- IMsRdpClientNonScriptable6 介面遠端桌面服務，SendLocation2D 方法
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation2D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: b706fdb35ba8360b294d25021c0c1a18bbe90188
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "103687348"
---
# <a name="imsrdpclientnonscriptable6sendlocation2d-method"></a><span data-ttu-id="c55ee-106">IMsRdpClientNonScriptable6：： SendLocation2D 方法</span><span class="sxs-lookup"><span data-stu-id="c55ee-106">IMsRdpClientNonScriptable6::SendLocation2D method</span></span>

<span data-ttu-id="c55ee-107">將緯度和經度值傳送至伺服器，讓用戶端的地理位置可以反映在遠端會話中。</span><span class="sxs-lookup"><span data-stu-id="c55ee-107">Sends a latitude and longitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="c55ee-108">語法</span><span class="sxs-lookup"><span data-stu-id="c55ee-108">Syntax</span></span>

```C++
HRESULT SendLocation2D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude
);
```

## <a name="parameters"></a><span data-ttu-id="c55ee-109">參數</span><span class="sxs-lookup"><span data-stu-id="c55ee-109">Parameters</span></span>

<span data-ttu-id="c55ee-110">*緯度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c55ee-110">*latitude* \[in\]</span></span>

<span data-ttu-id="c55ee-111">地理位置的緯度。</span><span class="sxs-lookup"><span data-stu-id="c55ee-111">The latitude of a geographic location.</span></span> <span data-ttu-id="c55ee-112">緯度值的有效範圍是從-90.0 到90.0 度。</span><span class="sxs-lookup"><span data-stu-id="c55ee-112">The valid range of latitude values is from -90.0 to 90.0 degrees.</span></span>

<span data-ttu-id="c55ee-113">*經度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c55ee-113">*longitude* \[in\]</span></span>

<span data-ttu-id="c55ee-114">地理位置的經度。</span><span class="sxs-lookup"><span data-stu-id="c55ee-114">The longitude of a geographic location.</span></span> <span data-ttu-id="c55ee-115">緯度值的有效範圍是從-180.0 到180.0 度。</span><span class="sxs-lookup"><span data-stu-id="c55ee-115">The valid range of latitude values is from -180.0 to 180.0 degrees.</span></span>

## <a name="return-value"></a><span data-ttu-id="c55ee-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="c55ee-116">Return value</span></span>

<span data-ttu-id="c55ee-117">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="c55ee-117">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="c55ee-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c55ee-118">Requirements</span></span>

| <span data-ttu-id="c55ee-119">需求</span><span class="sxs-lookup"><span data-stu-id="c55ee-119">Requirement</span></span> | <span data-ttu-id="c55ee-120">值</span><span class="sxs-lookup"><span data-stu-id="c55ee-120">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="c55ee-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c55ee-121">Minimum supported client</span></span>| <span data-ttu-id="c55ee-122">Windows 10 1709 版 (組建 16299)</span><span class="sxs-lookup"><span data-stu-id="c55ee-122">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="c55ee-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c55ee-123">Type library</span></span>            | <span data-ttu-id="c55ee-124">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="c55ee-124">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="c55ee-125">DLL</span><span class="sxs-lookup"><span data-stu-id="c55ee-125">DLL</span></span>                  | <span data-ttu-id="c55ee-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="c55ee-126">MsTscAx.dll</span></span>     |
| <span data-ttu-id="c55ee-127">IID</span><span class="sxs-lookup"><span data-stu-id="c55ee-127">IID</span></span>                      | <span data-ttu-id="c55ee-128">IID \_ IMsRdpClientNonScriptable6 定義為 05293249-B28B-4DB8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="c55ee-128">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="c55ee-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c55ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c55ee-130">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="c55ee-130">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
