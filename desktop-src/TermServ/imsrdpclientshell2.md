---
title: IMsRdpClientShell2 介面
description: 公開從遠端桌面 Web 存取 (RD Web 存取) 或從其他入口網站啟動遠端桌面連線用戶端的屬性。
ms.assetid: cc8ef78f-b7d6-42cd-bb67-8a8e1f33be08
ms.tgt_platform: multiple
keywords:
- IMsRdpClientShell2 介面遠端桌面服務
- IMsRdpClientShell2 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpClientShell2
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb93fd938602b195f60877be884dbe0bd458a598
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685670"
---
# <a name="imsrdpclientshell2-interface"></a><span data-ttu-id="10fd6-105">IMsRdpClientShell2 介面</span><span class="sxs-lookup"><span data-stu-id="10fd6-105">IMsRdpClientShell2 interface</span></span>

<span data-ttu-id="10fd6-106">公開從遠端桌面 Web 存取 (RD Web 存取) 或從其他入口網站啟動遠端桌面連線用戶端的屬性。</span><span class="sxs-lookup"><span data-stu-id="10fd6-106">Exposes properties that launch the Remote Desktop Connection client from Remote Desktop Web Access (RD Web Access) or from other web portals.</span></span>

<span data-ttu-id="10fd6-107">此介面是由遠端桌面服務 Web 存取控制項所執行，這是遠端桌面連線用戶端 (MsTscAx.dll) 和 RemoteApp 和桌面連線執行時間 proxy (Tswbprxy.exe) 周圍的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="10fd6-107">This interface is implemented by the Remote Desktop Services Web Access Control, which is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="10fd6-108">成員</span><span class="sxs-lookup"><span data-stu-id="10fd6-108">Members</span></span>

<span data-ttu-id="10fd6-109">**IMsRdpClientShell2** 介面繼承自 **IMsRdpClientShell**。</span><span class="sxs-lookup"><span data-stu-id="10fd6-109">The **IMsRdpClientShell2** interface inherits from **IMsRdpClientShell**.</span></span> <span data-ttu-id="10fd6-110">**IMsRdpClientShell2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="10fd6-110">**IMsRdpClientShell2** also has these types of members:</span></span>

-   [<span data-ttu-id="10fd6-111">屬性</span><span class="sxs-lookup"><span data-stu-id="10fd6-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="10fd6-112">屬性</span><span class="sxs-lookup"><span data-stu-id="10fd6-112">Properties</span></span>

<span data-ttu-id="10fd6-113">**IMsRdpClientShell2** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="10fd6-113">The **IMsRdpClientShell2** interface has these properties.</span></span>



| <span data-ttu-id="10fd6-114">屬性</span><span class="sxs-lookup"><span data-stu-id="10fd6-114">Property</span></span>                                                                               | <span data-ttu-id="10fd6-115">存取類型</span><span class="sxs-lookup"><span data-stu-id="10fd6-115">Access type</span></span>          | <span data-ttu-id="10fd6-116">Description</span><span class="sxs-lookup"><span data-stu-id="10fd6-116">Description</span></span>                                                                                                                                                                       |
|:---------------------------------------------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="10fd6-117">**MsRdpWorkspace**</span><span class="sxs-lookup"><span data-stu-id="10fd6-117">**MsRdpWorkspace**</span></span>](imsrdpclientshell2-msrdpworkspace.md)<br/>                 | <span data-ttu-id="10fd6-118">唯讀</span><span class="sxs-lookup"><span data-stu-id="10fd6-118">Read-only</span></span><br/> | <span data-ttu-id="10fd6-119">抓取 [**IMsRdpWorkspace**](imsrdpworkspace.md) 介面的指標，該介面可用來管理 RemoteApp 和桌面連線的認證和連接。</span><span class="sxs-lookup"><span data-stu-id="10fd6-119">Retrieves a pointer to the [**IMsRdpWorkspace**](imsrdpworkspace.md) interface, which is used to manage RemoteApp and Desktop Connection credentials and connections.</span></span><br/> |
| [<span data-ttu-id="10fd6-120">**SecuredSettingsEnabled**</span><span class="sxs-lookup"><span data-stu-id="10fd6-120">**SecuredSettingsEnabled**</span></span>](imsrdpclientshell2-securedsettingsenabled.md)<br/> | <span data-ttu-id="10fd6-121">唯讀</span><span class="sxs-lookup"><span data-stu-id="10fd6-121">Read-only</span></span><br/> | <span data-ttu-id="10fd6-122">抓取值，指出目前的網頁是否位於信任的 Internet Explorer URL 安全性區域中。</span><span class="sxs-lookup"><span data-stu-id="10fd6-122">Retrieves a value that indicates whether the current webpage is in a trusted Internet Explorer URL security zone.</span></span><br/>                                                      |



 

## <a name="requirements"></a><span data-ttu-id="10fd6-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="10fd6-123">Requirements</span></span>



| <span data-ttu-id="10fd6-124">需求</span><span class="sxs-lookup"><span data-stu-id="10fd6-124">Requirement</span></span> | <span data-ttu-id="10fd6-125">值</span><span class="sxs-lookup"><span data-stu-id="10fd6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="10fd6-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10fd6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="10fd6-127">Windows 7</span><span class="sxs-lookup"><span data-stu-id="10fd6-127">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="10fd6-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10fd6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="10fd6-129">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="10fd6-129">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="10fd6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="10fd6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10fd6-131"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10fd6-131"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10fd6-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10fd6-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10fd6-133">**IMsRdpWorkspace**</span><span class="sxs-lookup"><span data-stu-id="10fd6-133">**IMsRdpWorkspace**</span></span>](imsrdpworkspace.md)
</dt> </dl>

 

 





