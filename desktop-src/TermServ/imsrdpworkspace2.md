---
title: IMsRdpWorkspace2 介面
description: 公開將 RemoteApp 和桌面連線認證與連接產生關聯的方法。
ms.assetid: 7E09AF14-2D6C-4D6E-8033-C691D9DC8057
ms.tgt_platform: multiple
keywords:
- IMsRdpWorkspace 介面遠端桌面服務
- IMsRdpWorkspace 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IMsRdpWorkspace
api_location:
- MsRdpWebAccess.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d6b5ff193eec393b67029d355a0f0c1bc67c0ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025023"
---
# <a name="imsrdpworkspace2-interface"></a><span data-ttu-id="dd4b9-105">IMsRdpWorkspace2 介面</span><span class="sxs-lookup"><span data-stu-id="dd4b9-105">IMsRdpWorkspace2 interface</span></span>

<span data-ttu-id="dd4b9-106">公開將 RemoteApp 和桌面連線認證與連接產生關聯的方法。</span><span class="sxs-lookup"><span data-stu-id="dd4b9-106">Exposes a method that associates RemoteApp and Desktop Connection credentials with a connection.</span></span> <span data-ttu-id="dd4b9-107">這個介面是由遠端桌面服務 Web 存取控制項所執行。</span><span class="sxs-lookup"><span data-stu-id="dd4b9-107">This interface is implemented by the Remote Desktop Services Web Access Control.</span></span> <span data-ttu-id="dd4b9-108">此控制項是遠端桌面連線用戶端 (MsTscAx.dll) 的包裝函式，以及 RemoteApp 和桌面連線執行時間 proxy (Tswbprxy.exe) 。</span><span class="sxs-lookup"><span data-stu-id="dd4b9-108">This control is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="dd4b9-109">成員</span><span class="sxs-lookup"><span data-stu-id="dd4b9-109">Members</span></span>

<span data-ttu-id="dd4b9-110">**IMsRdpWorkspace** 介面繼承自 [**IMsRdpWorkspace**](imsrdpworkspace.md)。</span><span class="sxs-lookup"><span data-stu-id="dd4b9-110">The **IMsRdpWorkspace** interface inherits from [**IMsRdpWorkspace**](imsrdpworkspace.md).</span></span> <span data-ttu-id="dd4b9-111">**IMsRdpWorkspace2** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="dd4b9-111">**IMsRdpWorkspace2** also has these types of members:</span></span>

-   [<span data-ttu-id="dd4b9-112">方法</span><span class="sxs-lookup"><span data-stu-id="dd4b9-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="dd4b9-113">方法</span><span class="sxs-lookup"><span data-stu-id="dd4b9-113">Methods</span></span>

<span data-ttu-id="dd4b9-114">**IMsRdpWorkspace** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="dd4b9-114">The **IMsRdpWorkspace** interface has these methods.</span></span>



| <span data-ttu-id="dd4b9-115">方法</span><span class="sxs-lookup"><span data-stu-id="dd4b9-115">Method</span></span>                                                        | <span data-ttu-id="dd4b9-116">描述</span><span class="sxs-lookup"><span data-stu-id="dd4b9-116">Description</span></span>                                                                    |
|:--------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="dd4b9-117">[**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="dd4b9-117">[**StartWorkspaceEx**](/previous-versions/windows/desktop/legacy/dn123459(v=vs.85))</span></span> | <span data-ttu-id="dd4b9-118">將使用者認證和憑證與連接識別碼產生關聯。</span><span class="sxs-lookup"><span data-stu-id="dd4b9-118">Associates user credentials and certificates with a connection ID.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="dd4b9-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd4b9-119">Requirements</span></span>



| <span data-ttu-id="dd4b9-120">需求</span><span class="sxs-lookup"><span data-stu-id="dd4b9-120">Requirement</span></span> | <span data-ttu-id="dd4b9-121">值</span><span class="sxs-lookup"><span data-stu-id="dd4b9-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="dd4b9-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dd4b9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="dd4b9-123">Windows 8</span><span class="sxs-lookup"><span data-stu-id="dd4b9-123">Windows 8</span></span><br/>                                                                          |
| <span data-ttu-id="dd4b9-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dd4b9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="dd4b9-125">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="dd4b9-125">Windows Server 2012</span></span><br/>                                                                |
| <span data-ttu-id="dd4b9-126">DLL</span><span class="sxs-lookup"><span data-stu-id="dd4b9-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dd4b9-127"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dd4b9-127"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |
| <span data-ttu-id="dd4b9-128">IID</span><span class="sxs-lookup"><span data-stu-id="dd4b9-128">IID</span></span><br/>                      | <span data-ttu-id="dd4b9-129">IID \_ IMsRdpWorkspace2 定義為145D0622-04CF-4FC3-A776-A82A9169CDF8</span><span class="sxs-lookup"><span data-stu-id="dd4b9-129">IID\_IMsRdpWorkspace2 is defined as 145D0622-04CF-4FC3-A776-A82A9169CDF8</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="dd4b9-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd4b9-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd4b9-131">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="dd4b9-131">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> <dt>

[<span data-ttu-id="dd4b9-132">**IMsRdpWorkspace**</span><span class="sxs-lookup"><span data-stu-id="dd4b9-132">**IMsRdpWorkspace**</span></span>](imsrdpworkspace.md)
</dt> </dl>

 

