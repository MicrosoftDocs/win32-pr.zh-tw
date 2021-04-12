---
title: IMsRdpClientAdvancedSettings2 介面
description: 管理 advanced client 設定。 衍生自 IMsRdpClientAdvancedSettings 介面。
ms.assetid: 78cffdf5-bd99-4140-80b6-aa8632894487
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 70d7f9ad9b93c0f3cd1d62fdbbaddf4faa55ad9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317327"
---
# <a name="imsrdpclientadvancedsettings2-interface"></a><span data-ttu-id="509c8-106">IMsRdpClientAdvancedSettings2 介面</span><span class="sxs-lookup"><span data-stu-id="509c8-106">IMsRdpClientAdvancedSettings2 interface</span></span>

<span data-ttu-id="509c8-107">管理 advanced client 設定。</span><span class="sxs-lookup"><span data-stu-id="509c8-107">Manages advanced client settings.</span></span> <span data-ttu-id="509c8-108">衍生自 [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="509c8-108">Derives from the [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md) interface.</span></span> <span data-ttu-id="509c8-109">此介面包含方法，可取得和設定遠端桌面 ActiveX 控制項的 advanced (選擇性) 屬性。</span><span class="sxs-lookup"><span data-stu-id="509c8-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="509c8-110">若要取得這個介面的實例，請使用 [**IMsTscAx：： AdvancedSettings**](imstscax-advancedsettings.md) 屬性來取得 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="509c8-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="509c8-111">然後呼叫 **IMsTscAdvancedSettings** 指標上的 [**queryinterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，然後將 **IID \_ IMsRdpClientAdvancedSettings2** 傳遞給 **QueryInterface**。</span><span class="sxs-lookup"><span data-stu-id="509c8-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings2** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="509c8-112">成員</span><span class="sxs-lookup"><span data-stu-id="509c8-112">Members</span></span>

<span data-ttu-id="509c8-113">**IMsRdpClientAdvancedSettings2** 介面繼承自 [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="509c8-113">The **IMsRdpClientAdvancedSettings2** interface inherits from [**IMsRdpClientAdvancedSettings**](imsrdpclientadvancedsettings-interface.md).</span></span> <span data-ttu-id="509c8-114">**IMsRdpClientAdvancedSettings2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="509c8-114">**IMsRdpClientAdvancedSettings2** also has these types of members:</span></span>

-   [<span data-ttu-id="509c8-115">屬性</span><span class="sxs-lookup"><span data-stu-id="509c8-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="509c8-116">屬性</span><span class="sxs-lookup"><span data-stu-id="509c8-116">Properties</span></span>

<span data-ttu-id="509c8-117">**IMsRdpClientAdvancedSettings2** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="509c8-117">The **IMsRdpClientAdvancedSettings2** interface has these properties.</span></span>



| <span data-ttu-id="509c8-118">屬性</span><span class="sxs-lookup"><span data-stu-id="509c8-118">Property</span></span>                                                                                      | <span data-ttu-id="509c8-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="509c8-119">Access type</span></span>           | <span data-ttu-id="509c8-120">Description</span><span class="sxs-lookup"><span data-stu-id="509c8-120">Description</span></span>                                                                                                                                           |
|:----------------------------------------------------------------------------------------------|:----------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="509c8-121">**CanAutoReconnect**</span><span class="sxs-lookup"><span data-stu-id="509c8-121">**CanAutoReconnect**</span></span>](imsrdpclientadvancedsettings2-canautoreconnect.md)<br/>         | <span data-ttu-id="509c8-122">唯讀</span><span class="sxs-lookup"><span data-stu-id="509c8-122">Read-only</span></span><br/>  | <span data-ttu-id="509c8-123">指定當網路連線中斷時，用戶端控制項是否能夠自動重新連接到目前的會話。</span><span class="sxs-lookup"><span data-stu-id="509c8-123">Specifies whether the client control is able to reconnect automatically to the current session in the event of a network disconnection.</span></span><br/>    |
| [<span data-ttu-id="509c8-124">**EnableAutoReconnect**</span><span class="sxs-lookup"><span data-stu-id="509c8-124">**EnableAutoReconnect**</span></span>](imsrdpclientadvancedsettings2-enableautoreconnect.md)<br/>   | <span data-ttu-id="509c8-125">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="509c8-125">Read/write</span></span><br/> | <span data-ttu-id="509c8-126">指定當網路連線中斷時，是否要讓用戶端控制項自動重新連線到會話。</span><span class="sxs-lookup"><span data-stu-id="509c8-126">Specifies whether to enable the client control to reconnect automatically to a session in the event of a network disconnection.</span></span><br/>            |
| [<span data-ttu-id="509c8-127">**MaxReconnectAttempts**</span><span class="sxs-lookup"><span data-stu-id="509c8-127">**MaxReconnectAttempts**</span></span>](imsrdpclientadvancedsettings2-maxreconnectattempts.md)<br/> | <span data-ttu-id="509c8-128">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="509c8-128">Read/write</span></span><br/> | <span data-ttu-id="509c8-129">指定在自動重新連接期間嘗試重新連接的次數。</span><span class="sxs-lookup"><span data-stu-id="509c8-129">Specifies the number of times to try to reconnect during automatic reconnection.</span></span> <span data-ttu-id="509c8-130">這個屬性的有效值為0到200（含）。</span><span class="sxs-lookup"><span data-stu-id="509c8-130">The valid values of this property are 0 to 200 inclusive.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="509c8-131">備註</span><span class="sxs-lookup"><span data-stu-id="509c8-131">Remarks</span></span>

<span data-ttu-id="509c8-132">此介面已由下列介面延伸，每個新介面都會繼承先前介面的所有方法和屬性：</span><span class="sxs-lookup"><span data-stu-id="509c8-132">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="509c8-133">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="509c8-133">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
-   [<span data-ttu-id="509c8-134">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="509c8-134">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="509c8-135">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="509c8-135">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="509c8-136">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="509c8-136">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="509c8-137">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="509c8-137">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="509c8-138">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="509c8-138">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="509c8-139">規格需求</span><span class="sxs-lookup"><span data-stu-id="509c8-139">Requirements</span></span>



| <span data-ttu-id="509c8-140">需求</span><span class="sxs-lookup"><span data-stu-id="509c8-140">Requirement</span></span> | <span data-ttu-id="509c8-141">值</span><span class="sxs-lookup"><span data-stu-id="509c8-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="509c8-142">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="509c8-142">Minimum supported client</span></span><br/> | <span data-ttu-id="509c8-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="509c8-143">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="509c8-144">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="509c8-144">Minimum supported server</span></span><br/> | <span data-ttu-id="509c8-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="509c8-145">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="509c8-146">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="509c8-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="509c8-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="509c8-147"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="509c8-148">DLL</span><span class="sxs-lookup"><span data-stu-id="509c8-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="509c8-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="509c8-149"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="509c8-150">IID</span><span class="sxs-lookup"><span data-stu-id="509c8-150">IID</span></span><br/>                      | <span data-ttu-id="509c8-151">IID \_ IMsRdpClientAdvancedSettings2 定義為9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="509c8-151">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="509c8-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="509c8-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="509c8-153">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="509c8-153">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="509c8-154">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="509c8-154">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="509c8-155">遠端桌面網頁連線參考</span><span class="sxs-lookup"><span data-stu-id="509c8-155">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

