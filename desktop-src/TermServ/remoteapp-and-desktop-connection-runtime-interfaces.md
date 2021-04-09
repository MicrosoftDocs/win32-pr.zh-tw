---
title: RemoteApp 和桌面連線執行時間介面
description: 支援允許在 RemoteApp 和桌面連線中開發自訂用戶端的介面。
ms.assetid: 4580df05-5e44-40d0-8765-5d9b4e1d339e
ms.tgt_platform: multiple
keywords:
- 遠端桌面服務遠端桌面服務 RemoteApp 和桌面連線執行時間 API 參考
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6b7c3c2fd3841cfe797fc559ba1aa30d3479436
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104092383"
---
# <a name="remoteapp-and-desktop-connection-runtime-interfaces"></a><span data-ttu-id="6e7e4-104">RemoteApp 和桌面連線執行時間介面</span><span class="sxs-lookup"><span data-stu-id="6e7e4-104">RemoteApp and Desktop Connection Runtime interfaces</span></span>

<span data-ttu-id="6e7e4-105">RemoteApp 和桌面連線執行時間 API 支援可讓您在 RemoteApp 和桌面連線中開發自訂用戶端的介面。</span><span class="sxs-lookup"><span data-stu-id="6e7e4-105">The RemoteApp and Desktop Connection Runtime API supports interfaces that allow the development of custom clients in RemoteApp and Desktop Connection.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6e7e4-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="6e7e4-106">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="6e7e4-107">**IWorkspace**</span><span class="sxs-lookup"><span data-stu-id="6e7e4-107">**IWorkspace**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace)
</dt> <dd>

<span data-ttu-id="6e7e4-108">公開方法，以提供 RemoteApp 和桌面連線中連接的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="6e7e4-108">Exposes methods that provide information about a connection in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="6e7e4-109">**IWorkspace2**</span><span class="sxs-lookup"><span data-stu-id="6e7e4-109">**IWorkspace2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace2)
</dt> <dd>

<span data-ttu-id="6e7e4-110">公開可在 RemoteApp 和桌面連線中提供連接相關資訊的其他方法。</span><span class="sxs-lookup"><span data-stu-id="6e7e4-110">Exposes additional methods that provide information about a connection in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="6e7e4-111">**IWorkspace3**</span><span class="sxs-lookup"><span data-stu-id="6e7e4-111">**IWorkspace3**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspace3)
</dt> <dd>

<span data-ttu-id="6e7e4-112">公開方法，以提供 RemoteApp 和桌面連線中連接的相關資訊，並新增取得或設定宣告權杖的能力。</span><span class="sxs-lookup"><span data-stu-id="6e7e4-112">Exposes methods that provide information about a connection in RemoteApp and Desktop Connection, and adds the ability to retrieve or set a claims token.</span></span>

</dd> <dt>

[<span data-ttu-id="6e7e4-113">**IWorkspaceClientExt**</span><span class="sxs-lookup"><span data-stu-id="6e7e4-113">**IWorkspaceClientExt**</span></span>](/windows/desktop/api/Workspaceruntimeclientext/nn-workspaceruntimeclientext-iworkspaceclientext)
</dt> <dd>

<span data-ttu-id="6e7e4-114">公開方法，以允許執行時間中斷 RemoteApp 和桌面連線中的自訂用戶端連線。</span><span class="sxs-lookup"><span data-stu-id="6e7e4-114">Exposes methods that allow the runtime to disconnect a custom client in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="6e7e4-115">**IWorkspaceRegistration**</span><span class="sxs-lookup"><span data-stu-id="6e7e4-115">**IWorkspaceRegistration**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration)
</dt> <dd>

<span data-ttu-id="6e7e4-116">公開在 RemoteApp 和桌面連線中加入和移除自訂用戶端參考的方法。</span><span class="sxs-lookup"><span data-stu-id="6e7e4-116">Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="6e7e4-117">**IWorkspaceRegistration2**</span><span class="sxs-lookup"><span data-stu-id="6e7e4-117">**IWorkspaceRegistration2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspaceregistration2)
</dt> <dd>

<span data-ttu-id="6e7e4-118">公開在 RemoteApp 和桌面連線中加入和移除自訂用戶端參考的方法。</span><span class="sxs-lookup"><span data-stu-id="6e7e4-118">Exposes methods that add and remove references to custom clients in RemoteApp and Desktop Connection.</span></span>

</dd> <dt>

[<span data-ttu-id="6e7e4-119">**IWorkspaceReportMessage**</span><span class="sxs-lookup"><span data-stu-id="6e7e4-119">**IWorkspaceReportMessage**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacereportmessage)
</dt> <dd>

<span data-ttu-id="6e7e4-120">公開支援遠端工作區之錯誤訊息處理的方法。</span><span class="sxs-lookup"><span data-stu-id="6e7e4-120">Exposes methods that support error message handling for remote workspaces.</span></span>

</dd> <dt>

[<span data-ttu-id="6e7e4-121">**IWorkspaceResTypeRegistry**</span><span class="sxs-lookup"><span data-stu-id="6e7e4-121">**IWorkspaceResTypeRegistry**</span></span>](/windows/desktop/api/Workspaceax/nn-workspaceax-iworkspacerestyperegistry)
</dt> <dd>

<span data-ttu-id="6e7e4-122">公開允許外掛程式在 RemoteApp 和桌面連線執行時間中管理協力廠商副檔名的方法。</span><span class="sxs-lookup"><span data-stu-id="6e7e4-122">Exposes methods that allow a plug-in to manage third-party file name extensions in RemoteApp and Desktop Connection runtime.</span></span>

</dd> <dt>

[<span data-ttu-id="6e7e4-123">**IWorkspaceScriptable**</span><span class="sxs-lookup"><span data-stu-id="6e7e4-123">**IWorkspaceScriptable**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable)
</dt> <dd>

<span data-ttu-id="6e7e4-124">公開管理 RemoteApp 和桌面連線認證和連接的方法。</span><span class="sxs-lookup"><span data-stu-id="6e7e4-124">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> <dt>

[<span data-ttu-id="6e7e4-125">**IWorkspaceScriptable2**</span><span class="sxs-lookup"><span data-stu-id="6e7e4-125">**IWorkspaceScriptable2**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable2)
</dt> <dd>

<span data-ttu-id="6e7e4-126">公開管理 RemoteApp 和桌面連線認證和連接的方法。</span><span class="sxs-lookup"><span data-stu-id="6e7e4-126">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> <dt>

[<span data-ttu-id="6e7e4-127">**IWorkspaceScriptable3**</span><span class="sxs-lookup"><span data-stu-id="6e7e4-127">**IWorkspaceScriptable3**</span></span>](/windows/desktop/api/workspaceruntime/nn-workspaceruntime-iworkspacescriptable3)
</dt> <dd>

<span data-ttu-id="6e7e4-128">公開管理 RemoteApp 和桌面連線認證和連接的方法。</span><span class="sxs-lookup"><span data-stu-id="6e7e4-128">Exposes methods that manage RemoteApp and Desktop Connection credentials and connections.</span></span>

</dd> </dl>

 

 




