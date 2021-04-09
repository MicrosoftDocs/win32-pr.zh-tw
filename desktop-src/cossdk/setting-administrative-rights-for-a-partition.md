---
description: 設定資料分割的系統管理許可權
ms.assetid: d38e4a63-9ff9-4acb-bb7e-d6c96644bd32
title: 設定資料分割的系統管理許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c421b37dd50fa21ee9cf146749ec00b0c91d98c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688816"
---
# <a name="setting-administrative-rights-for-a-partition"></a><span data-ttu-id="96d5a-103">設定資料分割的系統管理許可權</span><span class="sxs-lookup"><span data-stu-id="96d5a-103">Setting Administrative Rights for a Partition</span></span>

<span data-ttu-id="96d5a-104">已獲指派 COM + 系統應用程式系統管理員角色的使用者，可以建立、修改和刪除 COM + 分割。</span><span class="sxs-lookup"><span data-stu-id="96d5a-104">Users assigned the Administrator role of the COM+ System Application are allowed to create, modify, and delete COM+ partitions.</span></span> <span data-ttu-id="96d5a-105">在 [元件服務] 系統管理工具中，您可以藉由展開 COM + 系統應用程式的 [ **角色** ] 資料夾，將系統管理角色指派給使用者。</span><span class="sxs-lookup"><span data-stu-id="96d5a-105">Within the Component Services administrative tool, administrative roles can be assigned to users by expanding the **Roles** folder of the COM+ System Application.</span></span>

<span data-ttu-id="96d5a-106">從 Windows Server 2003，COM + 系統應用程式的驗證功能包含 EOAC \_ DISABLE AAA 的值 \_ 。</span><span class="sxs-lookup"><span data-stu-id="96d5a-106">As of Windows Server 2003, the authentication capability for the COM+ System Application includes the value EOAC\_DISABLE\_AAA.</span></span> <span data-ttu-id="96d5a-107">此值會在啟動系統應用程式時，在 [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) 呼叫中使用停用的 (AAA) 啟用。</span><span class="sxs-lookup"><span data-stu-id="96d5a-107">This value, which disables activate-as-activator (AAA) activations, is used in the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) call when launching the System Application.</span></span> <span data-ttu-id="96d5a-108">將驗證功能設定為 EOAC \_ DISABLE \_ AAA，可讓在特殊許可權帳戶下執行的應用程式 (例如 LocalSystem) ，以協助防止其身分識別用來啟動未受信任的元件。</span><span class="sxs-lookup"><span data-stu-id="96d5a-108">Setting the authentication capability to EOAC\_DISABLE\_AAA allows an application that runs under a privileged account (such as LocalSystem) to help prevent its identity from being used to launch untrusted components.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96d5a-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="96d5a-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96d5a-110">收集分割區計量</span><span class="sxs-lookup"><span data-stu-id="96d5a-110">Collecting Partition Metrics</span></span>](collecting-partition-metrics.md)
</dt> <dt>

[<span data-ttu-id="96d5a-111">設定資料分割快取</span><span class="sxs-lookup"><span data-stu-id="96d5a-111">Configuring the Partition Cache</span></span>](configuring-the-partition-cache.md)
</dt> <dt>

[<span data-ttu-id="96d5a-112">將應用程式群組至資料分割</span><span class="sxs-lookup"><span data-stu-id="96d5a-112">Grouping Applications into Partitions</span></span>](grouping-applications-into-partitions.md)
</dt> <dt>

[<span data-ttu-id="96d5a-113">管理本機磁碟分割</span><span class="sxs-lookup"><span data-stu-id="96d5a-113">Managing Local Partitions</span></span>](managing-local-partitions.md)
</dt> <dt>

[<span data-ttu-id="96d5a-114">管理 Active Directory 內的磁碟分割</span><span class="sxs-lookup"><span data-stu-id="96d5a-114">Managing Partitions Within Active Directory</span></span>](managing-partitions-within-active-directory.md)
</dt> </dl>

 

 
