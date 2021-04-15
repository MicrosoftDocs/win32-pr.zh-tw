---
title: IMsRdpClientAdvancedSettings4 介面
description: 管理 advanced client 設定。 衍生自 IMsRdpClientAdvancedSettings3 介面。
ms.assetid: cb1785d6-1f94-4423-bdda-0e3e4e9b8641
ms.tgt_platform: multiple
keywords:
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c7d840206a139e3c3272551eab6a187a7b18416e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384589"
---
# <a name="imsrdpclientadvancedsettings4-interface"></a><span data-ttu-id="93617-106">IMsRdpClientAdvancedSettings4 介面</span><span class="sxs-lookup"><span data-stu-id="93617-106">IMsRdpClientAdvancedSettings4 interface</span></span>

<span data-ttu-id="93617-107">管理 advanced client 設定。</span><span class="sxs-lookup"><span data-stu-id="93617-107">Manages advanced client settings.</span></span> <span data-ttu-id="93617-108">衍生自 [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="93617-108">Derives from the [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md) interface.</span></span> <span data-ttu-id="93617-109">此介面包含方法，可取得和設定遠端桌面 ActiveX 控制項的 advanced (選擇性) 屬性。</span><span class="sxs-lookup"><span data-stu-id="93617-109">This interface includes methods to retrieve and set advanced (optional) properties for the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="93617-110">若要取得這個介面的實例，請使用 [**IMsTscAx：： AdvancedSettings**](imstscax-advancedsettings.md) 屬性來取得 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) 介面指標。</span><span class="sxs-lookup"><span data-stu-id="93617-110">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="93617-111">然後呼叫 **IMsTscAdvancedSettings** 指標上的 [**queryinterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) ，然後將 **IID \_ IMsRdpClientAdvancedSettings4** 傳遞給 **QueryInterface**。</span><span class="sxs-lookup"><span data-stu-id="93617-111">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings4** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="93617-112">成員</span><span class="sxs-lookup"><span data-stu-id="93617-112">Members</span></span>

<span data-ttu-id="93617-113">**IMsRdpClientAdvancedSettings4** 介面繼承自 [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md)。</span><span class="sxs-lookup"><span data-stu-id="93617-113">The **IMsRdpClientAdvancedSettings4** interface inherits from [**IMsRdpClientAdvancedSettings3**](imsrdpclientadvancedsettings3.md).</span></span> <span data-ttu-id="93617-114">**IMsRdpClientAdvancedSettings4** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="93617-114">**IMsRdpClientAdvancedSettings4** also has these types of members:</span></span>

-   [<span data-ttu-id="93617-115">屬性</span><span class="sxs-lookup"><span data-stu-id="93617-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="93617-116">屬性</span><span class="sxs-lookup"><span data-stu-id="93617-116">Properties</span></span>

<span data-ttu-id="93617-117">**IMsRdpClientAdvancedSettings4** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="93617-117">The **IMsRdpClientAdvancedSettings4** interface has these properties.</span></span>



| <span data-ttu-id="93617-118">屬性</span><span class="sxs-lookup"><span data-stu-id="93617-118">Property</span></span>                                                                                    | <span data-ttu-id="93617-119">存取類型</span><span class="sxs-lookup"><span data-stu-id="93617-119">Access type</span></span>           | <span data-ttu-id="93617-120">Description</span><span class="sxs-lookup"><span data-stu-id="93617-120">Description</span></span>                                                              |
|:--------------------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------|
| [<span data-ttu-id="93617-121">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="93617-121">**AuthenticationLevel**</span></span>](imsrdpclientadvancedsettings4-authenticationlevel.md)<br/> | <span data-ttu-id="93617-122">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="93617-122">Read/write</span></span><br/> | <span data-ttu-id="93617-123">指定要用於連接的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="93617-123">Specifies the authentication level to use for the connection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="93617-124">備註</span><span class="sxs-lookup"><span data-stu-id="93617-124">Remarks</span></span>

<span data-ttu-id="93617-125">此介面已由下列介面延伸，每個新介面都會繼承先前介面的所有方法和屬性：</span><span class="sxs-lookup"><span data-stu-id="93617-125">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="93617-126">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="93617-126">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
-   [<span data-ttu-id="93617-127">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="93617-127">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="93617-128">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="93617-128">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)

<span data-ttu-id="93617-129">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="93617-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93617-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="93617-130">Requirements</span></span>



| <span data-ttu-id="93617-131">需求</span><span class="sxs-lookup"><span data-stu-id="93617-131">Requirement</span></span> | <span data-ttu-id="93617-132">值</span><span class="sxs-lookup"><span data-stu-id="93617-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="93617-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93617-133">Minimum supported client</span></span><br/> | <span data-ttu-id="93617-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="93617-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="93617-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93617-135">Minimum supported server</span></span><br/> | <span data-ttu-id="93617-136">Windows Server 2008、Windows Server 2008 SP1</span><span class="sxs-lookup"><span data-stu-id="93617-136">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                     |
| <span data-ttu-id="93617-137">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="93617-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="93617-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93617-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="93617-139">DLL</span><span class="sxs-lookup"><span data-stu-id="93617-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93617-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93617-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="93617-141">IID</span><span class="sxs-lookup"><span data-stu-id="93617-141">IID</span></span><br/>                      | <span data-ttu-id="93617-142">IID \_ IMsRdpClientAdvancedSettings4 定義為 FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span><span class="sxs-lookup"><span data-stu-id="93617-142">IID\_IMsRdpClientAdvancedSettings4 is defined as FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="93617-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93617-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93617-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="93617-144">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="93617-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="93617-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="93617-146">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="93617-146">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="93617-147">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="93617-147">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="93617-148">遠端桌面網頁連線參考</span><span class="sxs-lookup"><span data-stu-id="93617-148">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

