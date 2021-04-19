---
title: IMsTscSecuredSettings 介面
description: 包含方法，可取得並設定僅限特定 Internet Explorer URL 安全性區域的遠端桌面 ActiveX 控制項屬性。 |IMsTscSecuredSettings 介面
ms.assetid: 1136dbc5-abe6-40e0-b44f-700a1460fbd2
ms.tgt_platform: multiple
keywords:
- IMsTscSecuredSettings 介面遠端桌面服務
- IMsTscSecuredSettings 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsTscSecuredSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2037393147bd5a2e35d6eb803951890c9b5e7de5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106997342"
---
# <a name="imstscsecuredsettings-interface"></a><span data-ttu-id="acec3-106">IMsTscSecuredSettings 介面</span><span class="sxs-lookup"><span data-stu-id="acec3-106">IMsTscSecuredSettings interface</span></span>

<span data-ttu-id="acec3-107">包含方法，可取得並設定僅限特定 Internet Explorer URL 安全性區域的遠端桌面 ActiveX 控制項屬性。</span><span class="sxs-lookup"><span data-stu-id="acec3-107">Includes methods to retrieve and set properties of the Remote Desktop ActiveX control that are restricted to specific Internet Explorer URL security zones.</span></span> <span data-ttu-id="acec3-108">屬性包括指定用戶端控制項模式 (全螢幕模式或視窗模式) ，以及在連接至遠端桌面工作階段主機 (RD 工作階段主機) 伺服器時啟動的程式。</span><span class="sxs-lookup"><span data-stu-id="acec3-108">Properties include those that specify the mode of the client control (full-screen mode or window mode) and the program to start upon connection to the Remote Desktop Session Host (RD Session Host) server.</span></span> <span data-ttu-id="acec3-109">您也可以透過 [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) 介面使用這些方法。</span><span class="sxs-lookup"><span data-stu-id="acec3-109">These methods are also available through the [**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md) interface.</span></span>

## <a name="members"></a><span data-ttu-id="acec3-110">成員</span><span class="sxs-lookup"><span data-stu-id="acec3-110">Members</span></span>

<span data-ttu-id="acec3-111">**IMsTscSecuredSettings** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="acec3-111">The **IMsTscSecuredSettings** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="acec3-112">**IMsTscSecuredSettings** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="acec3-112">**IMsTscSecuredSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="acec3-113">屬性</span><span class="sxs-lookup"><span data-stu-id="acec3-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="acec3-114">屬性</span><span class="sxs-lookup"><span data-stu-id="acec3-114">Properties</span></span>

<span data-ttu-id="acec3-115">**IMsTscSecuredSettings** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="acec3-115">The **IMsTscSecuredSettings** interface has these properties.</span></span>



| <span data-ttu-id="acec3-116">屬性</span><span class="sxs-lookup"><span data-stu-id="acec3-116">Property</span></span>                                                              | <span data-ttu-id="acec3-117">存取類型</span><span class="sxs-lookup"><span data-stu-id="acec3-117">Access type</span></span>           | <span data-ttu-id="acec3-118">Description</span><span class="sxs-lookup"><span data-stu-id="acec3-118">Description</span></span>                                                                |
|:----------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="acec3-119">**FullScreen**</span><span class="sxs-lookup"><span data-stu-id="acec3-119">**FullScreen**</span></span>](imstscsecuredsettings-fullscreen.md)<br/>     | <span data-ttu-id="acec3-120">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="acec3-120">Read/write</span></span><br/> | <span data-ttu-id="acec3-121">用戶端控制項的全螢幕狀態。</span><span class="sxs-lookup"><span data-stu-id="acec3-121">The full-screen state of the client control.</span></span><br/>                    |
| [<span data-ttu-id="acec3-122">**StartProgram**</span><span class="sxs-lookup"><span data-stu-id="acec3-122">**StartProgram**</span></span>](imstscsecuredsettings-startprogram.md)<br/> | <span data-ttu-id="acec3-123">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="acec3-123">Read/write</span></span><br/> | <span data-ttu-id="acec3-124">連接時要在遠端伺服器上啟動的程式。</span><span class="sxs-lookup"><span data-stu-id="acec3-124">The program to be started on the remote server upon connection.</span></span><br/> |
| [<span data-ttu-id="acec3-125">**WorkDir**</span><span class="sxs-lookup"><span data-stu-id="acec3-125">**WorkDir**</span></span>](imstscsecuredsettings-workdir.md)<br/>           | <span data-ttu-id="acec3-126">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="acec3-126">Read/write</span></span><br/> | <span data-ttu-id="acec3-127">啟動程式的工作目錄。</span><span class="sxs-lookup"><span data-stu-id="acec3-127">The working directory of the start program.</span></span><br/>                     |



 

## <a name="remarks"></a><span data-ttu-id="acec3-128">備註</span><span class="sxs-lookup"><span data-stu-id="acec3-128">Remarks</span></span>

<span data-ttu-id="acec3-129">如需此介面之方法的詳細資訊，請參閱 [提供 RDP 用戶端安全性](providing-for-rdp-client-security.md) 。</span><span class="sxs-lookup"><span data-stu-id="acec3-129">Refer to [Providing for RDP Client Security](providing-for-rdp-client-security.md) for more information about the methods of this interface.</span></span>

<span data-ttu-id="acec3-130">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="acec3-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="acec3-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="acec3-131">Requirements</span></span>



| <span data-ttu-id="acec3-132">需求</span><span class="sxs-lookup"><span data-stu-id="acec3-132">Requirement</span></span> | <span data-ttu-id="acec3-133">值</span><span class="sxs-lookup"><span data-stu-id="acec3-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="acec3-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="acec3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="acec3-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="acec3-135">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="acec3-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="acec3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="acec3-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="acec3-137">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="acec3-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="acec3-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="acec3-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acec3-139"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="acec3-140">DLL</span><span class="sxs-lookup"><span data-stu-id="acec3-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="acec3-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="acec3-141"><dt>MsTscAx.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acec3-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="acec3-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acec3-143">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="acec3-143">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="acec3-144">遠端桌面網頁連線參考</span><span class="sxs-lookup"><span data-stu-id="acec3-144">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

