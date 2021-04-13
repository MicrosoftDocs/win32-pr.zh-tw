---
title: IMsRdpCameraRedirConfig 介面
description: 表示可用來重新導向的相機設定。
ms.tgt_platform: multiple
keywords:
- IMsRdpCameraRedirConfig 介面遠端桌面服務
- IMsRdpCameraRedirConfig 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: fbb0f3344e0653ea4a87c876bb8ca7b8a67e7d21
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104509738"
---
# <a name="imsrdpcameraredirconfig-interface"></a><span data-ttu-id="bbe3d-105">IMsRdpCameraRedirConfig 介面</span><span class="sxs-lookup"><span data-stu-id="bbe3d-105">IMsRdpCameraRedirConfig interface</span></span>

<span data-ttu-id="bbe3d-106">表示可用來重新導向的相機設定。</span><span class="sxs-lookup"><span data-stu-id="bbe3d-106">Represents the configurations for a camera that is available for redirection.</span></span>

## <a name="members"></a><span data-ttu-id="bbe3d-107">成員</span><span class="sxs-lookup"><span data-stu-id="bbe3d-107">Members</span></span>

<span data-ttu-id="bbe3d-108">**IMsRdpCameraRedirConfig** 介面繼承自 **IUnknown**。</span><span class="sxs-lookup"><span data-stu-id="bbe3d-108">The **IMsRdpCameraRedirConfig** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="bbe3d-109">**IMsRdpCameraRedirConfig** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="bbe3d-109">**IMsRdpCameraRedirConfig** also has these types of members:</span></span>

- [<span data-ttu-id="bbe3d-110">屬性</span><span class="sxs-lookup"><span data-stu-id="bbe3d-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="bbe3d-111">屬性</span><span class="sxs-lookup"><span data-stu-id="bbe3d-111">Properties</span></span>

<span data-ttu-id="bbe3d-112">**IMsRdpCameraRedirConfig** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="bbe3d-112">The **IMsRdpCameraRedirConfig** interface has these properties.</span></span>

| <span data-ttu-id="bbe3d-113">屬性</span><span class="sxs-lookup"><span data-stu-id="bbe3d-113">Property</span></span>         | <span data-ttu-id="bbe3d-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="bbe3d-114">Access type</span></span>           | <span data-ttu-id="bbe3d-115">Description</span><span class="sxs-lookup"><span data-stu-id="bbe3d-115">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="bbe3d-116">**DeviceExists**</span><span class="sxs-lookup"><span data-stu-id="bbe3d-116">**DeviceExists**</span></span>](imsrdpcameraredirconfig-deviceexists.md)      | <span data-ttu-id="bbe3d-117">唯讀</span><span class="sxs-lookup"><span data-stu-id="bbe3d-117">Read-only</span></span> | <span data-ttu-id="bbe3d-118">指定相機裝置目前是否存在 (也就是相機連線) 。</span><span class="sxs-lookup"><span data-stu-id="bbe3d-118">Specifies whether or not the camera device currently exists (that is, the camera is connected).</span></span>   |
| [<span data-ttu-id="bbe3d-119">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="bbe3d-119">**FriendlyName**</span></span>](imsrdpcameraredirconfig-friendlyname.md)                       | <span data-ttu-id="bbe3d-120">唯讀</span><span class="sxs-lookup"><span data-stu-id="bbe3d-120">Read-only</span></span> |    <span data-ttu-id="bbe3d-121">取得相機的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="bbe3d-121">Gets the camera’s friendly name.</span></span>    |
| [<span data-ttu-id="bbe3d-122">**Id**</span><span class="sxs-lookup"><span data-stu-id="bbe3d-122">**InstanceId**</span></span>](imsrdpcameraredirconfig-instanceid.md)      | <span data-ttu-id="bbe3d-123">唯讀</span><span class="sxs-lookup"><span data-stu-id="bbe3d-123">Read-only</span></span> |  <span data-ttu-id="bbe3d-124">取得相機的實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbe3d-124">Gets the instance ID of the camera.</span></span>  |
| [<span data-ttu-id="bbe3d-125">**ParentInstanceId**</span><span class="sxs-lookup"><span data-stu-id="bbe3d-125">**ParentInstanceId**</span></span>](imsrdpcameraredirconfig-parentinstanceid.md)                       | <span data-ttu-id="bbe3d-126">唯讀</span><span class="sxs-lookup"><span data-stu-id="bbe3d-126">Read-only</span></span> |    <span data-ttu-id="bbe3d-127">取得相機的父裝置實例識別碼。</span><span class="sxs-lookup"><span data-stu-id="bbe3d-127">Gets the parent device instance ID of the camera.</span></span>   |
| [<span data-ttu-id="bbe3d-128">**已重新導向**</span><span class="sxs-lookup"><span data-stu-id="bbe3d-128">**Redirected**</span></span>](imsrdpcameraredirconfig-redirected.md)      | <span data-ttu-id="bbe3d-129">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="bbe3d-129">Read/Write</span></span> |  <span data-ttu-id="bbe3d-130">指定是否將相機重新導向。</span><span class="sxs-lookup"><span data-stu-id="bbe3d-130">Specifies whether or not the camera is redirected.</span></span>  |
| [<span data-ttu-id="bbe3d-131">**>symboliclink**</span><span class="sxs-lookup"><span data-stu-id="bbe3d-131">**SymbolicLink**</span></span>](imsrdpcameraredirconfig-symboliclink.md)                       | <span data-ttu-id="bbe3d-132">唯讀</span><span class="sxs-lookup"><span data-stu-id="bbe3d-132">Read-only</span></span> |   <span data-ttu-id="bbe3d-133">取得相機之 **KSCATEGORY_VIDEO_CAMERA** 介面的符號連結。</span><span class="sxs-lookup"><span data-stu-id="bbe3d-133">Gets the symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>   |

## <a name="requirements"></a><span data-ttu-id="bbe3d-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbe3d-134">Requirements</span></span>

| <span data-ttu-id="bbe3d-135">需求</span><span class="sxs-lookup"><span data-stu-id="bbe3d-135">Requirement</span></span> | <span data-ttu-id="bbe3d-136">值</span><span class="sxs-lookup"><span data-stu-id="bbe3d-136">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="bbe3d-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bbe3d-137">Minimum supported client</span></span>| <span data-ttu-id="bbe3d-138">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="bbe3d-138">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="bbe3d-139">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bbe3d-139">Type library</span></span>            | <span data-ttu-id="bbe3d-140">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="bbe3d-140">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="bbe3d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bbe3d-141">DLL</span></span>                  | <span data-ttu-id="bbe3d-142">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="bbe3d-142">MsTscAx.dll</span></span>     |
| <span data-ttu-id="bbe3d-143">IID</span><span class="sxs-lookup"><span data-stu-id="bbe3d-143">IID</span></span>                      | <span data-ttu-id="bbe3d-144">IID \_ IMsRdpCameraRedirConfig 定義為 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="bbe3d-144">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="bbe3d-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbe3d-145">See also</span></span>

- [<span data-ttu-id="bbe3d-146">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="bbe3d-146">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
- [<span data-ttu-id="bbe3d-147">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="bbe3d-147">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)