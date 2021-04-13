---
title: IMsRdpClientShell 介面
description: 遠端桌面連線 (RDC) 用戶端設定，這些設定是用來從遠端桌面啟動用戶端 Web 存取 (RD Web 存取) 或從其他入口網站。
ms.assetid: 05ca2e90-656a-40a3-a438-29d7985e9feb
ms.tgt_platform: multiple
keywords:
- IMsRdpClientShell 介面遠端桌面服務
- IMsRdpClientShell 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b529ed1819864e5fc6106472b33ddd00312560c1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466001"
---
# <a name="imsrdpclientshell-interface"></a><span data-ttu-id="9c754-105">IMsRdpClientShell 介面</span><span class="sxs-lookup"><span data-stu-id="9c754-105">IMsRdpClientShell interface</span></span>

<span data-ttu-id="9c754-106">遠端桌面連線 (RDC) 用戶端設定，這些設定是用來從遠端桌面啟動用戶端 Web 存取 (RD Web 存取) 或從其他入口網站。</span><span class="sxs-lookup"><span data-stu-id="9c754-106">Remote Desktop Connection (RDC) client settings that are used to launch the client from Remote Desktop Web Access (RD Web Access) or from other web portals.</span></span>

## <a name="members"></a><span data-ttu-id="9c754-107">成員</span><span class="sxs-lookup"><span data-stu-id="9c754-107">Members</span></span>

<span data-ttu-id="9c754-108">**IMsRdpClientShell** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="9c754-108">The **IMsRdpClientShell** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="9c754-109">**IMsRdpClientShell** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="9c754-109">**IMsRdpClientShell** also has these types of members:</span></span>

-   [<span data-ttu-id="9c754-110">方法</span><span class="sxs-lookup"><span data-stu-id="9c754-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="9c754-111">屬性</span><span class="sxs-lookup"><span data-stu-id="9c754-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="9c754-112">方法</span><span class="sxs-lookup"><span data-stu-id="9c754-112">Methods</span></span>

<span data-ttu-id="9c754-113">**IMsRdpClientShell** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="9c754-113">The **IMsRdpClientShell** interface has these methods.</span></span>



| <span data-ttu-id="9c754-114">方法</span><span class="sxs-lookup"><span data-stu-id="9c754-114">Method</span></span>                                                     | <span data-ttu-id="9c754-115">描述</span><span class="sxs-lookup"><span data-stu-id="9c754-115">Description</span></span>                                                  |
|:-----------------------------------------------------------|:-------------------------------------------------------------|
| <span data-ttu-id="9c754-116">[**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9c754-116">[**GetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381303(v=vs.85))</span></span> | <span data-ttu-id="9c754-117">捕獲單一 RDP 屬性。</span><span class="sxs-lookup"><span data-stu-id="9c754-117">Retrieves a single RDP property.</span></span><br/>                  |
| [<span data-ttu-id="9c754-118">**啟動**</span><span class="sxs-lookup"><span data-stu-id="9c754-118">**Launch**</span></span>](imsrdpclientshell-launch.md)                 | <span data-ttu-id="9c754-119">從 web 入口網站啟動遠端檔案內容。</span><span class="sxs-lookup"><span data-stu-id="9c754-119">Launches remote file content from the web portal.</span></span><br/> |
| <span data-ttu-id="9c754-120">[**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="9c754-120">[**SetRdpProperty**](/previous-versions/windows/desktop/legacy/aa381312(v=vs.85))</span></span> | <span data-ttu-id="9c754-121">設定單一 RDP 屬性。</span><span class="sxs-lookup"><span data-stu-id="9c754-121">Sets a single RDP property.</span></span><br/>                       |



 

### <a name="properties"></a><span data-ttu-id="9c754-122">屬性</span><span class="sxs-lookup"><span data-stu-id="9c754-122">Properties</span></span>

<span data-ttu-id="9c754-123">**IMsRdpClientShell** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="9c754-123">The **IMsRdpClientShell** interface has these properties.</span></span>



| <span data-ttu-id="9c754-124">屬性</span><span class="sxs-lookup"><span data-stu-id="9c754-124">Property</span></span>                                                                                              | <span data-ttu-id="9c754-125">存取類型</span><span class="sxs-lookup"><span data-stu-id="9c754-125">Access type</span></span>           | <span data-ttu-id="9c754-126">Description</span><span class="sxs-lookup"><span data-stu-id="9c754-126">Description</span></span>                                                                                               |
|:------------------------------------------------------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9c754-127">**IsRemoteProgramClientInstalled**</span><span class="sxs-lookup"><span data-stu-id="9c754-127">**IsRemoteProgramClientInstalled**</span></span>](imsrdpclientshell-isremoteprogramclientinstalled.md)<br/> | <span data-ttu-id="9c754-128">唯讀</span><span class="sxs-lookup"><span data-stu-id="9c754-128">Read-only</span></span><br/>  | <span data-ttu-id="9c754-129">抓取遠端桌面連線 (RDC) 用戶端是否支援 RemoteApp 功能。</span><span class="sxs-lookup"><span data-stu-id="9c754-129">Retrieves whether the Remote Desktop Connection (RDC) client supports RemoteApp functionality.</span></span><br/> |
| [<span data-ttu-id="9c754-130">**PublicMode**</span><span class="sxs-lookup"><span data-stu-id="9c754-130">**PublicMode**</span></span>](imsrdpclientshell-publicmode.md)<br/>                                         | <span data-ttu-id="9c754-131">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9c754-131">Read/write</span></span><br/> | <span data-ttu-id="9c754-132">抓取是否啟用公用模式。</span><span class="sxs-lookup"><span data-stu-id="9c754-132">Retrieves whether public mode is enabled.</span></span><br/>                                                      |
| [<span data-ttu-id="9c754-133">**RdpFileContents**</span><span class="sxs-lookup"><span data-stu-id="9c754-133">**RdpFileContents**</span></span>](imsrdpclientshell-rdpfilecontents.md)<br/>                               | <span data-ttu-id="9c754-134">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="9c754-134">Read/write</span></span><br/> | <span data-ttu-id="9c754-135">RDP 設定檔的串流版本。</span><span class="sxs-lookup"><span data-stu-id="9c754-135">Stream version of the RDP configuration file.</span></span><br/>                                                  |



 

## <a name="requirements"></a><span data-ttu-id="9c754-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c754-136">Requirements</span></span>



| <span data-ttu-id="9c754-137">需求</span><span class="sxs-lookup"><span data-stu-id="9c754-137">Requirement</span></span> | <span data-ttu-id="9c754-138">值</span><span class="sxs-lookup"><span data-stu-id="9c754-138">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9c754-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c754-139">Minimum supported client</span></span><br/> | <span data-ttu-id="9c754-140">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9c754-140">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9c754-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c754-141">Minimum supported server</span></span><br/> | <span data-ttu-id="9c754-142">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9c754-142">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="9c754-143">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9c754-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="9c754-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c754-144"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9c754-145">DLL</span><span class="sxs-lookup"><span data-stu-id="9c754-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c754-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c754-146"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9c754-147">IID</span><span class="sxs-lookup"><span data-stu-id="9c754-147">IID</span></span><br/>                      | <span data-ttu-id="9c754-148">IID \_ IMsRdpClientShell 定義為 d012ae6d-c19a-4bfe-b367-201f8911f134</span><span class="sxs-lookup"><span data-stu-id="9c754-148">IID\_IMsRdpClientShell is defined as d012ae6d-c19a-4bfe-b367-201f8911f134</span></span><br/>   |



## <a name="see-also"></a><span data-ttu-id="9c754-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c754-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c754-150">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="9c754-150">**IDispatch**</span></span>](/windows/win32/api/oaidl/nn-oaidl-idispatch)
</dt> <dt>

[<span data-ttu-id="9c754-151">遠端桌面網頁連線參考</span><span class="sxs-lookup"><span data-stu-id="9c754-151">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

