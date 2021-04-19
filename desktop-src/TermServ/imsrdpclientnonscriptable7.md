---
title: IMsRdpClientNonScriptable7 介面
description: 提供存取遠端桌面 ActiveX 控制項上用戶端遠端會話的 nonscriptable 屬性。 衍生自 IMsRdpClientNonScriptable6 介面。
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable7 介面遠端桌面服務
- IMsRdpClientNonScriptable7 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 8becf3bbf66ea18b2df87069ba38bab44c56db70
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "106998421"
---
# <a name="imsrdpclientnonscriptable7-interface"></a><span data-ttu-id="77808-106">IMsRdpClientNonScriptable7 介面</span><span class="sxs-lookup"><span data-stu-id="77808-106">IMsRdpClientNonScriptable7 interface</span></span>

<span data-ttu-id="77808-107">提供存取遠端桌面 ActiveX 控制項上用戶端遠端會話的 nonscriptable 屬性。</span><span class="sxs-lookup"><span data-stu-id="77808-107">Provides access to the nonscriptable properties of a client's remote session on the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="77808-108">衍生自 [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="77808-108">Derives from the [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable6.md) interface.</span></span> <span data-ttu-id="77808-109">這個介面的方法只能透過 vtable 存取;它們無法用於可編寫腳本的用戶端。</span><span class="sxs-lookup"><span data-stu-id="77808-109">Methods of this interface can only be accessed through the vtable; they are not available for use to scriptable clients.</span></span>

<span data-ttu-id="77808-110">藉由呼叫 [**IMsTscAx**](imstscax-interface.md)物件上的 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))來取得這個介面的實例，並傳遞 **IID \_ IMsRdpClientNonScriptable7**。</span><span class="sxs-lookup"><span data-stu-id="77808-110">An instance of this interface is obtained by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IMsTscAx**](imstscax-interface.md) object, passing **IID\_IMsRdpClientNonScriptable7**.</span></span>

## <a name="members"></a><span data-ttu-id="77808-111">成員</span><span class="sxs-lookup"><span data-stu-id="77808-111">Members</span></span>

<span data-ttu-id="77808-112">**IMsRdpClientNonScriptable7** 介面繼承自 [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md)。</span><span class="sxs-lookup"><span data-stu-id="77808-112">The **IMsRdpClientNonScriptable7** interface inherits from [**IMsRdpClientNonScriptable6**](imsrdpclientnonscriptable5.md).</span></span> <span data-ttu-id="77808-113">**IMsRdpClientNonScriptable7** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="77808-113">**IMsRdpClientNonScriptable7** also has these types of members:</span></span>

- [<span data-ttu-id="77808-114">方法</span><span class="sxs-lookup"><span data-stu-id="77808-114">Methods</span></span>](#methods)
- [<span data-ttu-id="77808-115">屬性</span><span class="sxs-lookup"><span data-stu-id="77808-115">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="77808-116">方法</span><span class="sxs-lookup"><span data-stu-id="77808-116">Methods</span></span>

<span data-ttu-id="77808-117">**IMsRdpClientNonScriptable7** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="77808-117">The **IMsRdpClientNonScriptable7** interface has these methods.</span></span>


| <span data-ttu-id="77808-118">方法</span><span class="sxs-lookup"><span data-stu-id="77808-118">Method</span></span>            | <span data-ttu-id="77808-119">描述</span><span class="sxs-lookup"><span data-stu-id="77808-119">Description</span></span>              |
|:------------------|:-------------------------|
| [<span data-ttu-id="77808-120">**DisableDpiCursorScalingForProcess**</span><span class="sxs-lookup"><span data-stu-id="77808-120">**DisableDpiCursorScalingForProcess**</span></span>](imsrdpclientnonscriptable7-disabledpicursorscalingforprocess.md)       |  <span data-ttu-id="77808-121">停用從伺服器收到的滑鼠游標區域調整，以確保正確轉譯資料指標圖形，而不進行修改。</span><span class="sxs-lookup"><span data-stu-id="77808-121">Disables local scaling of the mouse cursor received from the server, ensuring that the cursor shape is rendered correctly without modification.</span></span>                   |

### <a name="properties"></a><span data-ttu-id="77808-122">屬性</span><span class="sxs-lookup"><span data-stu-id="77808-122">Properties</span></span>

<span data-ttu-id="77808-123">**IMsRdpClientNonScriptable7** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="77808-123">The **IMsRdpClientNonScriptable7** interface has these properties.</span></span>

| <span data-ttu-id="77808-124">屬性</span><span class="sxs-lookup"><span data-stu-id="77808-124">Property</span></span>         | <span data-ttu-id="77808-125">存取類型</span><span class="sxs-lookup"><span data-stu-id="77808-125">Access type</span></span>           | <span data-ttu-id="77808-126">Description</span><span class="sxs-lookup"><span data-stu-id="77808-126">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="77808-127">**CameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="77808-127">**CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)      | <span data-ttu-id="77808-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="77808-128">Read-only</span></span> |  <span data-ttu-id="77808-129">取得 (的攝影機集合，以及可用於重新導向的相關聯設定) 。</span><span class="sxs-lookup"><span data-stu-id="77808-129">Gets the collection of cameras (and the associated configurations) that are available for redirection.</span></span>   |
| [<span data-ttu-id="77808-130">**剪貼簿**</span><span class="sxs-lookup"><span data-stu-id="77808-130">**Clipboard**</span></span>](imsrdpclientnonscriptable7-clipboard.md)                       | <span data-ttu-id="77808-131">唯讀</span><span class="sxs-lookup"><span data-stu-id="77808-131">Read-only</span></span> |    <span data-ttu-id="77808-132">如果啟用手動剪貼簿同步，則取得用來同步處理本機和遠端寫字板的剪貼簿控制器。</span><span class="sxs-lookup"><span data-stu-id="77808-132">Gets the Clipboard controller used to synchronize the local and remote clipboards if manual clipboard sync is enabled.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="77808-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="77808-133">Requirements</span></span>

| <span data-ttu-id="77808-134">需求</span><span class="sxs-lookup"><span data-stu-id="77808-134">Requirement</span></span> | <span data-ttu-id="77808-135">值</span><span class="sxs-lookup"><span data-stu-id="77808-135">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="77808-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77808-136">Minimum supported client</span></span>| <span data-ttu-id="77808-137">Windows 10 1803 版 (組建 17134)</span><span class="sxs-lookup"><span data-stu-id="77808-137">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="77808-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="77808-138">Type library</span></span>            | <span data-ttu-id="77808-139">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="77808-139">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="77808-140">DLL</span><span class="sxs-lookup"><span data-stu-id="77808-140">DLL</span></span>                  | <span data-ttu-id="77808-141">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="77808-141">MsTscAx.dll</span></span>     |
| <span data-ttu-id="77808-142">CLSID</span><span class="sxs-lookup"><span data-stu-id="77808-142">CLSID</span></span>                    | <span data-ttu-id="77808-143">CLSID \_ MsRdpClient12 定義為0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span><span class="sxs-lookup"><span data-stu-id="77808-143">CLSID\_MsRdpClient12 is defined as 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span></span><br/> <span data-ttu-id="77808-144">CLSID \_ MsRdpClient12NotSafeForScripting 定義為3BB805C2-D9E2-4174-8A1E-C87D69563662</span><span class="sxs-lookup"><span data-stu-id="77808-144">CLSID\_MsRdpClient12NotSafeForScripting is defined as 3BB805C2-D9E2-4174-8A1E-C87D69563662</span></span><br/> <span data-ttu-id="77808-145">CLSID \_ MsRdpClient11 定義為22A7E88C-5BF5-4DE6-B687-60F7331DF190</span><span class="sxs-lookup"><span data-stu-id="77808-145">CLSID\_MsRdpClient11 is defined as 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span></span><br/> <span data-ttu-id="77808-146">CLSID \_ MsRdpClient11NotSafeForScripting 定義為1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span><span class="sxs-lookup"><span data-stu-id="77808-146">CLSID\_MsRdpClient11NotSafeForScripting is defined as 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span></span><br/>  |
| <span data-ttu-id="77808-147">IID</span><span class="sxs-lookup"><span data-stu-id="77808-147">IID</span></span>                      | <span data-ttu-id="77808-148">IID \_ IMsRdpClientNonScriptable7 定義為71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span><span class="sxs-lookup"><span data-stu-id="77808-148">IID\_IMsRdpClientNonScriptable7 is defined as 71B4A60A-FE21-46D8-A39B-8E32BA0C5ECC</span></span>            |

## <a name="see-also"></a><span data-ttu-id="77808-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77808-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77808-150">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="77808-150">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
