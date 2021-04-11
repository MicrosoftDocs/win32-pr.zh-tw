---
title: IMsRdpWorkspace 介面
description: 公開管理 RemoteApp 和桌面連線認證和連接的方法。
ms.assetid: cddcdfc2-b30a-4d00-84c2-ad036ab6288f
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
ms.openlocfilehash: 0ba55a02c5d984bc87aa05caffd42b3a3b965c43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933998"
---
# <a name="imsrdpworkspace-interface"></a><span data-ttu-id="65b6d-105">IMsRdpWorkspace 介面</span><span class="sxs-lookup"><span data-stu-id="65b6d-105">IMsRdpWorkspace interface</span></span>

<span data-ttu-id="65b6d-106">公開管理 RemoteApp 和桌面連線認證和連接的方法。</span><span class="sxs-lookup"><span data-stu-id="65b6d-106">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span> <span data-ttu-id="65b6d-107">這個介面是由遠端桌面服務 Web 存取控制項所執行。</span><span class="sxs-lookup"><span data-stu-id="65b6d-107">This interface is implemented by the Remote Desktop Services Web Access Control.</span></span> <span data-ttu-id="65b6d-108">此控制項是遠端桌面連線用戶端 (MsTscAx.dll) 的包裝函式，以及 RemoteApp 和桌面連線執行時間 proxy (Tswbprxy.exe) 。</span><span class="sxs-lookup"><span data-stu-id="65b6d-108">This control is a wrapper around the Remote Desktop Connection client (MsTscAx.dll) and the RemoteApp and Desktop Connections runtime proxy (Tswbprxy.exe).</span></span>

## <a name="members"></a><span data-ttu-id="65b6d-109">成員</span><span class="sxs-lookup"><span data-stu-id="65b6d-109">Members</span></span>

<span data-ttu-id="65b6d-110">**IMsRdpWorkspace** 介面繼承自 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。</span><span class="sxs-lookup"><span data-stu-id="65b6d-110">The **IMsRdpWorkspace** interface inherits from the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface.</span></span> <span data-ttu-id="65b6d-111">**IMsRdpWorkspace** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="65b6d-111">**IMsRdpWorkspace** also has these types of members:</span></span>

-   [<span data-ttu-id="65b6d-112">方法</span><span class="sxs-lookup"><span data-stu-id="65b6d-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="65b6d-113">方法</span><span class="sxs-lookup"><span data-stu-id="65b6d-113">Methods</span></span>

<span data-ttu-id="65b6d-114">**IMsRdpWorkspace** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="65b6d-114">The **IMsRdpWorkspace** interface has these methods.</span></span>



| <span data-ttu-id="65b6d-115">方法</span><span class="sxs-lookup"><span data-stu-id="65b6d-115">Method</span></span>                                                                                   | <span data-ttu-id="65b6d-116">描述</span><span class="sxs-lookup"><span data-stu-id="65b6d-116">Description</span></span>                                                                                                                                                           |
|:-----------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65b6d-117">[**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="65b6d-117">[**ClearWorkspaceCredential**](/previous-versions/windows/desktop/legacy/ee351596(v=vs.85))</span></span>             | <span data-ttu-id="65b6d-118">刪除與指定之連接識別碼相關聯的使用者認證。</span><span class="sxs-lookup"><span data-stu-id="65b6d-118">Deletes the user credentials associated with the specified connection ID.</span></span><br/>                                                                                  |
| <span data-ttu-id="65b6d-119">[**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="65b6d-119">[**DisconnectWorkspace**](/previous-versions/windows/desktop/legacy/ee351597(v=vs.85))</span></span>                       | <span data-ttu-id="65b6d-120">中斷與指定之連接識別碼相關聯的所有現有連接，並從認證存放區刪除對應的使用者認證。</span><span class="sxs-lookup"><span data-stu-id="65b6d-120">Disconnects all existing connections associated with the specified connection ID and deletes the corresponding user credentials from the credential store.</span></span><br/> |
| <span data-ttu-id="65b6d-121">[**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="65b6d-121">[**IsWorkspaceCredentialSpecified**](/previous-versions/windows/desktop/legacy/ee351598(v=vs.85))</span></span> | <span data-ttu-id="65b6d-122">判斷指定之連接識別碼的使用者認證是否存在。</span><span class="sxs-lookup"><span data-stu-id="65b6d-122">Determines whether user credentials exist for the specified connection ID.</span></span><br/>                                                                                 |
| <span data-ttu-id="65b6d-123">[**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="65b6d-123">[**IsWorkspaceSSOEnabled**](/previous-versions/windows/desktop/legacy/ee351599(v=vs.85))</span></span>                   | <span data-ttu-id="65b6d-124">判斷是否已啟用 RemoteApp 和桌面連線的單一登入 (SSO) 。</span><span class="sxs-lookup"><span data-stu-id="65b6d-124">Determines whether single sign on (SSO) is enabled for RemoteApp and Desktop Connection.</span></span><br/>                                                                   |
| <span data-ttu-id="65b6d-125">[**OnAuthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="65b6d-125">[**OnAuthenticated**](/previous-versions/windows/desktop/legacy/ee351600(v=vs.85))</span></span>                               | <span data-ttu-id="65b6d-126">標示連接識別碼的使用者認證驗證，接著在工作列通知區域中顯示 connect 通知。</span><span class="sxs-lookup"><span data-stu-id="65b6d-126">Marks the authentication of user credentials for the connection ID, and subsequently shows the connect notification in the taskbar notification area.</span></span> <br/>     |
| <span data-ttu-id="65b6d-127">[**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="65b6d-127">[**StartWorkspace**](/previous-versions/windows/desktop/legacy/ee351601(v=vs.85))</span></span>                                 | <span data-ttu-id="65b6d-128">將使用者認證和憑證與連接識別碼產生關聯。</span><span class="sxs-lookup"><span data-stu-id="65b6d-128">Associates user credentials and certificates with a connection ID.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="65b6d-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="65b6d-129">Requirements</span></span>



| <span data-ttu-id="65b6d-130">需求</span><span class="sxs-lookup"><span data-stu-id="65b6d-130">Requirement</span></span> | <span data-ttu-id="65b6d-131">值</span><span class="sxs-lookup"><span data-stu-id="65b6d-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="65b6d-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65b6d-132">Minimum supported client</span></span><br/> | <span data-ttu-id="65b6d-133">Windows 7</span><span class="sxs-lookup"><span data-stu-id="65b6d-133">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="65b6d-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65b6d-134">Minimum supported server</span></span><br/> | <span data-ttu-id="65b6d-135">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="65b6d-135">Windows Server 2008 R2</span></span><br/>                                                             |
| <span data-ttu-id="65b6d-136">DLL</span><span class="sxs-lookup"><span data-stu-id="65b6d-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65b6d-137"><dt>MsRdpWebAccess.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65b6d-137"><dt>MsRdpWebAccess.dll</dt></span></span> </dl> |
| <span data-ttu-id="65b6d-138">IID</span><span class="sxs-lookup"><span data-stu-id="65b6d-138">IID</span></span><br/>                      | <span data-ttu-id="65b6d-139">IID \_ IMsRdpWorkspace 定義為145D0621-04CF-4FC2-A766-A81A9069CDF8</span><span class="sxs-lookup"><span data-stu-id="65b6d-139">IID\_IMsRdpWorkspace is defined as 145D0621-04CF-4FC2-A766-A81A9069CDF8</span></span><br/>            |



## <a name="see-also"></a><span data-ttu-id="65b6d-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65b6d-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65b6d-141">**IMsRdpClientShell2**</span><span class="sxs-lookup"><span data-stu-id="65b6d-141">**IMsRdpClientShell2**</span></span>](imsrdpclientshell2.md)
</dt> </dl>

 

