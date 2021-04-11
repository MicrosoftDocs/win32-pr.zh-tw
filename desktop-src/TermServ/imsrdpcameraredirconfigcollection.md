---
title: IMsRdpCameraRedirConfigCollection 介面
description: 代表 (的相機集合，以及可用於重新導向的相關聯設定) 。
ms.tgt_platform: multiple
keywords:
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務
- IMsRdpCameraRedirConfigCollection 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 3d97249a7485ec024ee3611809c87c5b6ed41143
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104108356"
---
# <a name="imsrdpcameraredirconfigcollection-interface"></a><span data-ttu-id="0a569-105">IMsRdpCameraRedirConfigCollection 介面</span><span class="sxs-lookup"><span data-stu-id="0a569-105">IMsRdpCameraRedirConfigCollection interface</span></span>

 <span data-ttu-id="0a569-106">代表 (的相機集合，以及可用於重新導向的相關聯設定) 。</span><span class="sxs-lookup"><span data-stu-id="0a569-106">Represents the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

## <a name="members"></a><span data-ttu-id="0a569-107">成員</span><span class="sxs-lookup"><span data-stu-id="0a569-107">Members</span></span>

<span data-ttu-id="0a569-108">**IMsRdpCameraRedirConfigCollection** 介面繼承自 **IUnknown**。</span><span class="sxs-lookup"><span data-stu-id="0a569-108">The **IMsRdpCameraRedirConfigCollection** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="0a569-109">**IMsRdpCameraRedirConfigCollection** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="0a569-109">**IMsRdpCameraRedirConfigCollection** also has these types of members:</span></span>

- [<span data-ttu-id="0a569-110">方法</span><span class="sxs-lookup"><span data-stu-id="0a569-110">Methods</span></span>](#methods)
- [<span data-ttu-id="0a569-111">屬性</span><span class="sxs-lookup"><span data-stu-id="0a569-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="0a569-112">方法</span><span class="sxs-lookup"><span data-stu-id="0a569-112">Methods</span></span>

<span data-ttu-id="0a569-113">**IMsRdpCameraRedirConfigCollection** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="0a569-113">The **IMsRdpCameraRedirConfigCollection** interface has these methods.</span></span>

| <span data-ttu-id="0a569-114">方法</span><span class="sxs-lookup"><span data-stu-id="0a569-114">Method</span></span>            | <span data-ttu-id="0a569-115">描述</span><span class="sxs-lookup"><span data-stu-id="0a569-115">Description</span></span>              |
|:------------------|:-------------------------|
| [<span data-ttu-id="0a569-116">**AddConfig**</span><span class="sxs-lookup"><span data-stu-id="0a569-116">**AddConfig**</span></span>](imsrdpcameraredirconfigcollection-addconfig.md)       |  <span data-ttu-id="0a569-117">將 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件新增至集合 (對應的相機不需要連線) 。</span><span class="sxs-lookup"><span data-stu-id="0a569-117">Adds an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object to the collection (the corresponding camera does not have to be connected).</span></span>                   |
| [<span data-ttu-id="0a569-118">**重新掃描**</span><span class="sxs-lookup"><span data-stu-id="0a569-118">**Rescan**</span></span>](imsrdpcameraredirconfigcollection-rescan.md)       |  <span data-ttu-id="0a569-119">列舉連線的相機裝置。</span><span class="sxs-lookup"><span data-stu-id="0a569-119">Enumerates connected camera devices.</span></span>                   |

### <a name="properties"></a><span data-ttu-id="0a569-120">屬性</span><span class="sxs-lookup"><span data-stu-id="0a569-120">Properties</span></span>

<span data-ttu-id="0a569-121">**IMsRdpCameraRedirConfigCollection** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="0a569-121">The **IMsRdpCameraRedirConfigCollection** interface has these properties.</span></span>

| <span data-ttu-id="0a569-122">屬性</span><span class="sxs-lookup"><span data-stu-id="0a569-122">Property</span></span>         | <span data-ttu-id="0a569-123">存取類型</span><span class="sxs-lookup"><span data-stu-id="0a569-123">Access type</span></span>           | <span data-ttu-id="0a569-124">Description</span><span class="sxs-lookup"><span data-stu-id="0a569-124">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="0a569-125">**ByIndex**</span><span class="sxs-lookup"><span data-stu-id="0a569-125">**ByIndex**</span></span>](imsrdpcameraredirconfigcollection-byindex.md)      | <span data-ttu-id="0a569-126">唯讀</span><span class="sxs-lookup"><span data-stu-id="0a569-126">Read-only</span></span> |  <span data-ttu-id="0a569-127">依物件在集合中的索引傳回 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="0a569-127">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object by its index in the collection.</span></span>   |
| [<span data-ttu-id="0a569-128">**ByInstanceId**</span><span class="sxs-lookup"><span data-stu-id="0a569-128">**ByInstanceId**</span></span>](imsrdpcameraredirconfigcollection-byinstanceid.md)                       | <span data-ttu-id="0a569-129">唯讀</span><span class="sxs-lookup"><span data-stu-id="0a569-129">Read-only</span></span> |    <span data-ttu-id="0a569-130">從集合中傳回對應至指定實例識別碼的 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="0a569-130">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the specified instance ID.</span></span>    |
| [<span data-ttu-id="0a569-131">**BySymbolicLink**</span><span class="sxs-lookup"><span data-stu-id="0a569-131">**BySymbolicLink**</span></span>](imsrdpcameraredirconfigcollection-bysymboliclink.md)      | <span data-ttu-id="0a569-132">唯讀</span><span class="sxs-lookup"><span data-stu-id="0a569-132">Read-only</span></span> |  <span data-ttu-id="0a569-133">從集合中傳回 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件，這個集合會對應至相機的 **KSCATEGORY_VIDEO_CAMERA** 介面之指定符號連結。</span><span class="sxs-lookup"><span data-stu-id="0a569-133">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the given symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>  |
| [<span data-ttu-id="0a569-134">**計數**</span><span class="sxs-lookup"><span data-stu-id="0a569-134">**Count**</span></span>](imsrdpcameraredirconfigcollection-count.md)                       | <span data-ttu-id="0a569-135">唯讀</span><span class="sxs-lookup"><span data-stu-id="0a569-135">Read-only</span></span> |    <span data-ttu-id="0a569-136">傳回集合中的 [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) 物件數目。</span><span class="sxs-lookup"><span data-stu-id="0a569-136">Returns the number of [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) objects in the collection.</span></span>   |
| [<span data-ttu-id="0a569-137">**EncodeVideo**</span><span class="sxs-lookup"><span data-stu-id="0a569-137">**EncodeVideo**</span></span>](imsrdpcameraredirconfigcollection-encodevideo.md)      | <span data-ttu-id="0a569-138">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0a569-138">Read/Write</span></span> |  <span data-ttu-id="0a569-139">指定影片資料流程是否為 h.264 編碼。</span><span class="sxs-lookup"><span data-stu-id="0a569-139">Specifies whether or not the video stream is H.264 encoded.</span></span>  |
| [<span data-ttu-id="0a569-140">**EncodingQuality**</span><span class="sxs-lookup"><span data-stu-id="0a569-140">**EncodingQuality**</span></span>](imsrdpcameraredirconfigcollection-encodingquality.md)                       | <span data-ttu-id="0a569-141">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0a569-141">Read/Write</span></span> |    <span data-ttu-id="0a569-142">指定編碼品質 (位速率) 。</span><span class="sxs-lookup"><span data-stu-id="0a569-142">Specifies the encoding quality (bit rate).</span></span>   |
| [<span data-ttu-id="0a569-143">**RedirectByDefault**</span><span class="sxs-lookup"><span data-stu-id="0a569-143">**RedirectByDefault**</span></span>](imsrdpcameraredirconfigcollection-redirectbydefault.md)                       | <span data-ttu-id="0a569-144">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="0a569-144">Read/Write</span></span> |   <span data-ttu-id="0a569-145">指定是否根據預設，將任何新的相機重新導向。</span><span class="sxs-lookup"><span data-stu-id="0a569-145">Specifies whether or not any new camera gets redirected by default.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="0a569-146">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a569-146">Requirements</span></span>

| <span data-ttu-id="0a569-147">需求</span><span class="sxs-lookup"><span data-stu-id="0a569-147">Requirement</span></span> | <span data-ttu-id="0a569-148">值</span><span class="sxs-lookup"><span data-stu-id="0a569-148">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="0a569-149">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a569-149">Minimum supported client</span></span>| <span data-ttu-id="0a569-150">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="0a569-150">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="0a569-151">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0a569-151">Type library</span></span>            | <span data-ttu-id="0a569-152">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="0a569-152">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="0a569-153">DLL</span><span class="sxs-lookup"><span data-stu-id="0a569-153">DLL</span></span>                  | <span data-ttu-id="0a569-154">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="0a569-154">MsTscAx.dll</span></span>     |
| <span data-ttu-id="0a569-155">IID</span><span class="sxs-lookup"><span data-stu-id="0a569-155">IID</span></span>                      | <span data-ttu-id="0a569-156">IID \_ IMsRdpCameraRedirConfigCollection 定義為 AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="0a569-156">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>            |

## <a name="see-also"></a><span data-ttu-id="0a569-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0a569-157">See also</span></span>

- [<span data-ttu-id="0a569-158">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="0a569-158">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
- [<span data-ttu-id="0a569-159">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="0a569-159">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)
