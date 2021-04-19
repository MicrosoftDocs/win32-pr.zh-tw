---
title: IMsRdpClientAdvancedSettings6 介面
description: 公開管理 advanced ActiveX control 設定的屬性。
ms.assetid: 45b48cdf-3860-4359-99b2-8d2598146d1d
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e61d3358f1af228dcd1b5a7431ee759b486df7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966936"
---
# <a name="imsrdpclientadvancedsettings6-interface"></a><span data-ttu-id="e186b-105">IMsRdpClientAdvancedSettings6 介面</span><span class="sxs-lookup"><span data-stu-id="e186b-105">IMsRdpClientAdvancedSettings6 interface</span></span>

<span data-ttu-id="e186b-106">公開管理 advanced ActiveX control 設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="e186b-106">Exposes properties that manage advanced ActiveX control settings.</span></span> <span data-ttu-id="e186b-107">**IMsRdpClientAdvancedSettings6** 介面衍生自 [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)介面。</span><span class="sxs-lookup"><span data-stu-id="e186b-107">The **IMsRdpClientAdvancedSettings6** interface is derived from the [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="e186b-108">若要取得這個介面的實例，請使用 [**IMsTscAx：： AdvancedSettings**](imstscax-advancedsettings.md) 屬性來取得 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="e186b-108">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="e186b-109">然後呼叫 **IMsTscAdvancedSettings** 指標上的 [**queryinterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，然後將 **IID \_ IMsRdpClientAdvancedSettings6** 傳遞給 **QueryInterface**。</span><span class="sxs-lookup"><span data-stu-id="e186b-109">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings6** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="e186b-110">成員</span><span class="sxs-lookup"><span data-stu-id="e186b-110">Members</span></span>

<span data-ttu-id="e186b-111">**IMsRdpClientAdvancedSettings6** 介面繼承自 [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md)。</span><span class="sxs-lookup"><span data-stu-id="e186b-111">The **IMsRdpClientAdvancedSettings6** interface inherits from [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md).</span></span> <span data-ttu-id="e186b-112">**IMsRdpClientAdvancedSettings6** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e186b-112">**IMsRdpClientAdvancedSettings6** also has these types of members:</span></span>

-   [<span data-ttu-id="e186b-113">屬性</span><span class="sxs-lookup"><span data-stu-id="e186b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e186b-114">屬性</span><span class="sxs-lookup"><span data-stu-id="e186b-114">Properties</span></span>

<span data-ttu-id="e186b-115">**IMsRdpClientAdvancedSettings6** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="e186b-115">The **IMsRdpClientAdvancedSettings6** interface has these properties.</span></span>



| <span data-ttu-id="e186b-116">屬性</span><span class="sxs-lookup"><span data-stu-id="e186b-116">Property</span></span>                                                                                                  | <span data-ttu-id="e186b-117">存取類型</span><span class="sxs-lookup"><span data-stu-id="e186b-117">Access type</span></span>           | <span data-ttu-id="e186b-118">Description</span><span class="sxs-lookup"><span data-stu-id="e186b-118">Description</span></span>                                                                                                                        |
|:----------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e186b-119">**AuthenticationServiceClass**</span><span class="sxs-lookup"><span data-stu-id="e186b-119">**AuthenticationServiceClass**</span></span>](imsrdpclientadvancedsettings6-authenticationserviceclass.md)<br/> | <span data-ttu-id="e186b-120">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e186b-120">Read/write</span></span><br/> | <span data-ttu-id="e186b-121">指定服務主體名稱 (SPN) 用來向伺服器進行驗證。</span><span class="sxs-lookup"><span data-stu-id="e186b-121">Specifies the service principal name (SPN) to use for authentication to the server.</span></span><br/>                                     |
| [<span data-ttu-id="e186b-122">**AuthenticationType**</span><span class="sxs-lookup"><span data-stu-id="e186b-122">**AuthenticationType**</span></span>](imsrdpclientadvancedsettings6-authenticationtype.md)<br/>                 | <span data-ttu-id="e186b-123">唯讀</span><span class="sxs-lookup"><span data-stu-id="e186b-123">Read-only</span></span><br/>  | <span data-ttu-id="e186b-124">指定用於此連接的驗證類型。</span><span class="sxs-lookup"><span data-stu-id="e186b-124">Specifies the type of authentication used for this connection.</span></span><br/>                                                          |
| [<span data-ttu-id="e186b-125">**ConnectToAdministerServer**</span><span class="sxs-lookup"><span data-stu-id="e186b-125">**ConnectToAdministerServer**</span></span>](imsrdpclientadvancedsettings6-connecttoadministerserver.md)<br/>   | <span data-ttu-id="e186b-126">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e186b-126">Read/write</span></span><br/> | <span data-ttu-id="e186b-127">取得或指定 ActiveX 控制項是否應該基於系統管理目的嘗試連接至伺服器。</span><span class="sxs-lookup"><span data-stu-id="e186b-127">Retrieves or specifies whether the ActiveX control should attempt to connect to the server for administrative purposes.</span></span><br/> |
| [<span data-ttu-id="e186b-128">**EnableCredSspSupport**</span><span class="sxs-lookup"><span data-stu-id="e186b-128">**EnableCredSspSupport**</span></span>](imsrdpclientadvancedsettings6-enablecredsspsupport.md)<br/>             | <span data-ttu-id="e186b-129">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e186b-129">Read/write</span></span><br/> | <span data-ttu-id="e186b-130">指定是否為此連線啟用 (CredSSP) 的認證安全性服務提供者。</span><span class="sxs-lookup"><span data-stu-id="e186b-130">Specifies whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span><br/>                    |
| [<span data-ttu-id="e186b-131">**HotKeyFocusReleaseLeft**</span><span class="sxs-lookup"><span data-stu-id="e186b-131">**HotKeyFocusReleaseLeft**</span></span>](imsrdpclientadvancedsettings6-hotkeyfocusreleaseleft.md)<br/>         | <span data-ttu-id="e186b-132">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e186b-132">Read/write</span></span><br/> | <span data-ttu-id="e186b-133">指定要新增至 CTRL + ALT 的虛擬按鍵程式碼，以決定 CTRL + ALT + 向左鍵的替換熱鍵。</span><span class="sxs-lookup"><span data-stu-id="e186b-133">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+LEFT ARROW.</span></span><br/>          |
| [<span data-ttu-id="e186b-134">**HotKeyFocusReleaseRight**</span><span class="sxs-lookup"><span data-stu-id="e186b-134">**HotKeyFocusReleaseRight**</span></span>](imsrdpclientadvancedsettings6-hotkeyfocusreleaseright.md)<br/>       | <span data-ttu-id="e186b-135">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e186b-135">Read/write</span></span><br/> | <span data-ttu-id="e186b-136">指定要新增至 CTRL + ALT 的虛擬按鍵程式碼，以決定 CTRL + ALT + 向右鍵的熱鍵取代。</span><span class="sxs-lookup"><span data-stu-id="e186b-136">Specifies the virtual-key code to add to CTRL+ALT to determine the hotkey replacement for CTRL+ALT+RIGHT ARROW.</span></span><br/>         |
| [<span data-ttu-id="e186b-137">**Pcb**</span><span class="sxs-lookup"><span data-stu-id="e186b-137">**PCB**</span></span>](imsrdpclientadvancedsettings6-pcb.md)<br/>                                               | <span data-ttu-id="e186b-138">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e186b-138">Read/write</span></span><br/> | <span data-ttu-id="e186b-139">指定 preconnection BLOB (PCB) 設定，以在連接到伺服器之前使用。</span><span class="sxs-lookup"><span data-stu-id="e186b-139">Specifies the preconnection BLOB (PCB) setting to use prior to connecting for transmission to the server.</span></span><br/>               |
| [<span data-ttu-id="e186b-140">**RelativeMouseMode**</span><span class="sxs-lookup"><span data-stu-id="e186b-140">**RelativeMouseMode**</span></span>](imsrdpclientadvancedsettings6-relativemousemode.md)<br/>                   | <span data-ttu-id="e186b-141">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="e186b-141">Read/write</span></span><br/> | <span data-ttu-id="e186b-142">指定滑鼠是否應使用相對模式。</span><span class="sxs-lookup"><span data-stu-id="e186b-142">Specifies whether the mouse should use relative mode.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="e186b-143">備註</span><span class="sxs-lookup"><span data-stu-id="e186b-143">Remarks</span></span>

<span data-ttu-id="e186b-144">[**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md)介面已擴充這個介面，繼承了先前介面的所有方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="e186b-144">This interface has been extended by the [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface, inheriting all the methods and properties of the previous interfaces.</span></span>

## <a name="requirements"></a><span data-ttu-id="e186b-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="e186b-145">Requirements</span></span>



| <span data-ttu-id="e186b-146">需求</span><span class="sxs-lookup"><span data-stu-id="e186b-146">Requirement</span></span> | <span data-ttu-id="e186b-147">值</span><span class="sxs-lookup"><span data-stu-id="e186b-147">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e186b-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e186b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="e186b-149">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e186b-149">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="e186b-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e186b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="e186b-151">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e186b-151">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="e186b-152">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e186b-152">Type library</span></span><br/>             | <dl> <span data-ttu-id="e186b-153"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e186b-153"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e186b-154">DLL</span><span class="sxs-lookup"><span data-stu-id="e186b-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e186b-155"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e186b-155"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="e186b-156">IID</span><span class="sxs-lookup"><span data-stu-id="e186b-156">IID</span></span><br/>                      | <span data-ttu-id="e186b-157">IID \_ IMsRdpClientAdvancedSettings6 定義為222c4b5d-45d9-4df0-a7c6-60cf9089d285</span><span class="sxs-lookup"><span data-stu-id="e186b-157">IID\_IMsRdpClientAdvancedSettings6 is defined as 222c4b5d-45d9-4df0-a7c6-60cf9089d285</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e186b-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e186b-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e186b-159">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e186b-159">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e186b-160">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e186b-160">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e186b-161">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e186b-161">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="e186b-162">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e186b-162">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="e186b-163">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e186b-163">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e186b-164">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e186b-164">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

