---
title: IMsRdpClientAdvancedSettings3 介面
description: 管理 advanced client 設定。 衍生自 IMsRdpClientAdvancedSettings2 介面。
ms.assetid: bfa9cf74-5943-45ca-9259-3ef0cc9ab2ab
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 760ae7d40742a800556b3d62bc5a1609b89c986b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685869"
---
# <a name="imsrdpclientadvancedsettings3-interface"></a><span data-ttu-id="c408d-106">IMsRdpClientAdvancedSettings3 介面</span><span class="sxs-lookup"><span data-stu-id="c408d-106">IMsRdpClientAdvancedSettings3 interface</span></span>

<span data-ttu-id="c408d-107">管理 advanced client 設定。</span><span class="sxs-lookup"><span data-stu-id="c408d-107">Manages advanced client settings.</span></span> <span data-ttu-id="c408d-108">衍生自 [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="c408d-108">Derives from the [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md) interface.</span></span> <span data-ttu-id="c408d-109">此介面包含方法，可取得和設定遠端桌面 ActiveX 控制項的 advanced (選擇性) 屬性。</span><span class="sxs-lookup"><span data-stu-id="c408d-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="c408d-110">若要取得這個介面的實例，請使用 [**IMsTscAx：： AdvancedSettings**](imstscax-advancedsettings.md) 屬性來取得 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="c408d-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="c408d-111">然後呼叫 **IMsTscAdvancedSettings** 指標上的 [**queryinterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，然後將 **IID \_ IMsRdpClientAdvancedSettings3** 傳遞給 **QueryInterface**。</span><span class="sxs-lookup"><span data-stu-id="c408d-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings3** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="c408d-112">成員</span><span class="sxs-lookup"><span data-stu-id="c408d-112">Members</span></span>

<span data-ttu-id="c408d-113">**IMsRdpClientAdvancedSettings3** 介面繼承自 [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md)。</span><span class="sxs-lookup"><span data-stu-id="c408d-113">The **IMsRdpClientAdvancedSettings3** interface inherits from [**IMsRdpClientAdvancedSettings2**](imsrdpclientadvancedsettings2.md).</span></span> <span data-ttu-id="c408d-114">**IMsRdpClientAdvancedSettings3** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="c408d-114">**IMsRdpClientAdvancedSettings3** also has these types of members:</span></span>

-   [<span data-ttu-id="c408d-115">屬性</span><span class="sxs-lookup"><span data-stu-id="c408d-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c408d-116">屬性</span><span class="sxs-lookup"><span data-stu-id="c408d-116">Properties</span></span>

<span data-ttu-id="c408d-117">**IMsRdpClientAdvancedSettings3** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="c408d-117">The **IMsRdpClientAdvancedSettings3** interface has these properties.</span></span>



| <span data-ttu-id="c408d-118">屬性</span><span class="sxs-lookup"><span data-stu-id="c408d-118">Property</span></span>                                                                                                            | <span data-ttu-id="c408d-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="c408d-119">Access type</span></span>           | <span data-ttu-id="c408d-120">Description</span><span class="sxs-lookup"><span data-stu-id="c408d-120">Description</span></span>                                                                            |
|:--------------------------------------------------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------|
| [<span data-ttu-id="c408d-121">**ConnectionBarShowMinimizeButton**</span><span class="sxs-lookup"><span data-stu-id="c408d-121">**ConnectionBarShowMinimizeButton**</span></span>](imsrdpclientadvancedsettings3-connectionbarshowminimizebutton.md)<br/> | <span data-ttu-id="c408d-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c408d-122">Read/write</span></span><br/> | <span data-ttu-id="c408d-123">指定是否要在連接列上顯示 [ **最小化** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="c408d-123">Specifies whether to display the **Minimize** button on the connection bar.</span></span><br/> |
| [<span data-ttu-id="c408d-124">**ConnectionBarShowRestoreButton**</span><span class="sxs-lookup"><span data-stu-id="c408d-124">**ConnectionBarShowRestoreButton**</span></span>](imsrdpclientadvancedsettings3-connectionbarshowrestorebutton.md)<br/>   | <span data-ttu-id="c408d-125">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="c408d-125">Read/write</span></span><br/> | <span data-ttu-id="c408d-126">指定是否要在連接列上顯示 [ **還原** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="c408d-126">Specifies whether to display the **Restore** button on the connection bar.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="c408d-127">備註</span><span class="sxs-lookup"><span data-stu-id="c408d-127">Remarks</span></span>

<span data-ttu-id="c408d-128">此介面已由下列介面延伸，每個新介面都會繼承先前介面的所有方法和屬性：</span><span class="sxs-lookup"><span data-stu-id="c408d-128">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="c408d-129">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c408d-129">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
-   [<span data-ttu-id="c408d-130">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c408d-130">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="c408d-131">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c408d-131">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="c408d-132">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c408d-132">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
-   [<span data-ttu-id="c408d-133">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c408d-133">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)

<span data-ttu-id="c408d-134">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="c408d-134">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c408d-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="c408d-135">Requirements</span></span>



| <span data-ttu-id="c408d-136">需求</span><span class="sxs-lookup"><span data-stu-id="c408d-136">Requirement</span></span> | <span data-ttu-id="c408d-137">值</span><span class="sxs-lookup"><span data-stu-id="c408d-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c408d-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c408d-138">Minimum supported client</span></span><br/> | <span data-ttu-id="c408d-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c408d-139">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="c408d-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c408d-140">Minimum supported server</span></span><br/> | <span data-ttu-id="c408d-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c408d-141">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="c408d-142">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c408d-142">Type library</span></span><br/>             | <dl> <span data-ttu-id="c408d-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c408d-143"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c408d-144">DLL</span><span class="sxs-lookup"><span data-stu-id="c408d-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c408d-145"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c408d-145"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c408d-146">IID</span><span class="sxs-lookup"><span data-stu-id="c408d-146">IID</span></span><br/>                      | <span data-ttu-id="c408d-147">IID \_ IMsRdpClientAdvancedSettings3 定義為19cd856b-c542-4c53-acee-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="c408d-147">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c408d-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c408d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c408d-149">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="c408d-149">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="c408d-150">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="c408d-150">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c408d-151">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="c408d-151">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="c408d-152">遠端桌面網頁連線參考</span><span class="sxs-lookup"><span data-stu-id="c408d-152">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

