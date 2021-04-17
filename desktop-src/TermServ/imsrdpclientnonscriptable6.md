---
title: IMsRdpClientNonScriptable6 介面
description: 提供存取遠端桌面 ActiveX 控制項上用戶端遠端會話的 nonscriptable 屬性。 衍生自 IMsRdpClientNonScriptable5 介面。
ms.tgt_platform: multiple
keywords:
- IMsRdpClientNonScriptable6 介面遠端桌面服務
- IMsRdpClientNonScriptable6 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 0d6793452ebf59f1974831aef0fa10f2469d8e92
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/19/2020
ms.locfileid: "104385486"
---
# <a name="imsrdpclientnonscriptable6-interface"></a><span data-ttu-id="b02e2-106">IMsRdpClientNonScriptable6 介面</span><span class="sxs-lookup"><span data-stu-id="b02e2-106">IMsRdpClientNonScriptable6 interface</span></span>

<span data-ttu-id="b02e2-107">提供存取遠端桌面 ActiveX 控制項上用戶端遠端會話的 nonscriptable 屬性。</span><span class="sxs-lookup"><span data-stu-id="b02e2-107">Provides access to the nonscriptable properties of a client's remote session on the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="b02e2-108">衍生自 [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="b02e2-108">Derives from the [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md) interface.</span></span> <span data-ttu-id="b02e2-109">這個介面的方法只能透過 vtable 存取;它們無法用於可編寫腳本的用戶端。</span><span class="sxs-lookup"><span data-stu-id="b02e2-109">Methods of this interface can only be accessed through the vtable; they are not available for use to scriptable clients.</span></span>

<span data-ttu-id="b02e2-110">藉由呼叫 [**IMsTscAx**](imstscax-interface.md)物件上的 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))來取得這個介面的實例，並傳遞 **IID \_ IMsRdpClientNonScriptable6**。</span><span class="sxs-lookup"><span data-stu-id="b02e2-110">An instance of this interface is obtained by calling [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the [**IMsTscAx**](imstscax-interface.md) object, passing **IID\_IMsRdpClientNonScriptable6**.</span></span>

## <a name="members"></a><span data-ttu-id="b02e2-111">成員</span><span class="sxs-lookup"><span data-stu-id="b02e2-111">Members</span></span>

<span data-ttu-id="b02e2-112">**IMsRdpClientNonScriptable6** 介面繼承自 [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)。</span><span class="sxs-lookup"><span data-stu-id="b02e2-112">The **IMsRdpClientNonScriptable6** interface inherits from [**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md).</span></span> <span data-ttu-id="b02e2-113">**IMsRdpClientNonScriptable6** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="b02e2-113">**IMsRdpClientNonScriptable6** also has these types of members:</span></span>

- [<span data-ttu-id="b02e2-114">方法</span><span class="sxs-lookup"><span data-stu-id="b02e2-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="b02e2-115">方法</span><span class="sxs-lookup"><span data-stu-id="b02e2-115">Methods</span></span>

<span data-ttu-id="b02e2-116">**IMsRdpClientNonScriptable6** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="b02e2-116">The **IMsRdpClientNonScriptable6** interface has these methods.</span></span>


| <span data-ttu-id="b02e2-117">方法</span><span class="sxs-lookup"><span data-stu-id="b02e2-117">Method</span></span>            | <span data-ttu-id="b02e2-118">描述</span><span class="sxs-lookup"><span data-stu-id="b02e2-118">Description</span></span>                   |
|:-----------------------------|:-----------------|
| [<span data-ttu-id="b02e2-119">**SendLocation2D**</span><span class="sxs-lookup"><span data-stu-id="b02e2-119">**SendLocation2D**</span></span>](imsrdpclientnonscriptable6-sendlocation2d.md)     |  <span data-ttu-id="b02e2-120">將緯度和經度值傳送至伺服器，讓用戶端的地理位置可以反映在遠端會話中。</span><span class="sxs-lookup"><span data-stu-id="b02e2-120">Sends a latitude and longitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>                   |
| [<span data-ttu-id="b02e2-121">**SendLocation3D**</span><span class="sxs-lookup"><span data-stu-id="b02e2-121">**SendLocation3D**</span></span>](imsrdpclientnonscriptable6-sendlocation3d.md)     | <span data-ttu-id="b02e2-122">將緯度、經度和海拔值傳送至伺服器，讓用戶端的地理位置可以反映在遠端會話中。</span><span class="sxs-lookup"><span data-stu-id="b02e2-122">Sends a latitude, longitude and altitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>                 |

## <a name="requirements"></a><span data-ttu-id="b02e2-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="b02e2-123">Requirements</span></span>

| <span data-ttu-id="b02e2-124">需求</span><span class="sxs-lookup"><span data-stu-id="b02e2-124">Requirement</span></span> | <span data-ttu-id="b02e2-125">值</span><span class="sxs-lookup"><span data-stu-id="b02e2-125">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="b02e2-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b02e2-126">Minimum supported client</span></span>| <span data-ttu-id="b02e2-127">Windows 10 1709 版 (組建 16299)</span><span class="sxs-lookup"><span data-stu-id="b02e2-127">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="b02e2-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="b02e2-128">Type library</span></span>            | <span data-ttu-id="b02e2-129">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="b02e2-129">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="b02e2-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b02e2-130">DLL</span></span>                  | <span data-ttu-id="b02e2-131">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="b02e2-131">MsTscAx.dll</span></span>     |
| <span data-ttu-id="b02e2-132">CLSID</span><span class="sxs-lookup"><span data-stu-id="b02e2-132">CLSID</span></span>                    | <span data-ttu-id="b02e2-133">CLSID \_ MsRdpClient12 定義為0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span><span class="sxs-lookup"><span data-stu-id="b02e2-133">CLSID\_MsRdpClient12 is defined as 0BDA33B8-9AF1-4065-989E-5A7F1ACF09D8</span></span><br/> <span data-ttu-id="b02e2-134">CLSID \_ MsRdpClient12NotSafeForScripting 定義為3BB805C2-D9E2-4174-8A1E-C87D69563662</span><span class="sxs-lookup"><span data-stu-id="b02e2-134">CLSID\_MsRdpClient12NotSafeForScripting is defined as 3BB805C2-D9E2-4174-8A1E-C87D69563662</span></span><br/> <span data-ttu-id="b02e2-135">CLSID \_ MsRdpClient11 定義為22A7E88C-5BF5-4DE6-B687-60F7331DF190</span><span class="sxs-lookup"><span data-stu-id="b02e2-135">CLSID\_MsRdpClient11 is defined as 22A7E88C-5BF5-4DE6-B687-60F7331DF190</span></span><br/> <span data-ttu-id="b02e2-136">CLSID \_ MsRdpClient11NotSafeForScripting 定義為1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span><span class="sxs-lookup"><span data-stu-id="b02e2-136">CLSID\_MsRdpClient11NotSafeForScripting is defined as 1DF7C823-B2D4-4B54-975A-F2AC5D7CF8B8</span></span><br/>  |
| <span data-ttu-id="b02e2-137">IID</span><span class="sxs-lookup"><span data-stu-id="b02e2-137">IID</span></span>                      | <span data-ttu-id="b02e2-138">IID \_ IMsRdpClientNonScriptable6 定義為 05293249-B28B-4DB8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="b02e2-138">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="b02e2-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b02e2-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b02e2-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="b02e2-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>
