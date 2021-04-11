---
description: COM + CRM 安全性考慮
ms.assetid: e212c847-b43b-43be-b089-82336551b89a
title: COM + CRM 安全性考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2ababde9f31c0c2655fbf4f0c46b216ca0cbfee
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110405"
---
# <a name="com-crm-security-considerations"></a><span data-ttu-id="9f54e-103">COM + CRM 安全性考慮</span><span class="sxs-lookup"><span data-stu-id="9f54e-103">COM+ CRM Security Considerations</span></span>

<span data-ttu-id="9f54e-104">CRM 記錄檔可能包含必須受到保護的機密資訊。</span><span class="sxs-lookup"><span data-stu-id="9f54e-104">A CRM log file could contain sensitive information that must be secured.</span></span> <span data-ttu-id="9f54e-105">基於這個理由，如果在第一次建立 CRM 記錄檔時，伺服器應用程式是在互動式使用者以外的任何身分識別下執行，則 CRM 記錄檔只會受限於該使用者的安全性。</span><span class="sxs-lookup"><span data-stu-id="9f54e-105">For this reason, if the server application is running under any identity other than Interactive User when the CRM log file is first created, the CRM log file is security protected for that user only.</span></span> <span data-ttu-id="9f54e-106">這項功能僅適用于 NTFS 檔案系統。</span><span class="sxs-lookup"><span data-stu-id="9f54e-106">This feature is available only on the NTFS file system.</span></span> <span data-ttu-id="9f54e-107">如果後續變更伺服器應用程式的身分識別，則不會自動變更 CRM 記錄檔的安全性資訊。</span><span class="sxs-lookup"><span data-stu-id="9f54e-107">If the identity of the server application is subsequently changed, the security information for the CRM log file is not automatically changed.</span></span> <span data-ttu-id="9f54e-108">您可以使用現有的 Windows 系統管理工具，以手動方式進行變更。</span><span class="sxs-lookup"><span data-stu-id="9f54e-108">It can be changed manually by using existing Windows administration tools.</span></span> <span data-ttu-id="9f54e-109">替代方法是在 CRM 記錄檔處於「乾淨」狀態時刪除 CRM 記錄檔， (在伺服器應用程式) 的控制項關機之後，這是預期的情況。</span><span class="sxs-lookup"><span data-stu-id="9f54e-109">The alternative is simply to delete the CRM log file when it is in a clean state (which is expected after a controlled shutdown of the server application).</span></span>

<span data-ttu-id="9f54e-110">在正常操作中，COM + 會建立 CRM 補償器元件，並呼叫 [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) 介面。</span><span class="sxs-lookup"><span data-stu-id="9f54e-110">In normal operation, COM+ creates the CRM compensator component and calls the [**ICrmCompensator**](/windows/desktop/api/ComSvcs/nn-comsvcs-icrmcompensator) interface.</span></span> <span data-ttu-id="9f54e-111">不過，擁有建立 CRM 補償器許可權的使用者可以在不適當的時間呼叫 **ICrmCompensator** 介面，可能會造成系統安全性問題。</span><span class="sxs-lookup"><span data-stu-id="9f54e-111">However, a user having privileges to create the CRM Compensator can call the **ICrmCompensator** interface at inappropriate times, possibly causing system security problems.</span></span> <span data-ttu-id="9f54e-112">為了協助防止這些安全性問題，系統管理員可以使用以角色為基礎的安全性，將 CRM 補償器元件限制為只有執行它的伺服器應用程式的身分識別。</span><span class="sxs-lookup"><span data-stu-id="9f54e-112">To help protect against these security problems, the system administrator can use role-based security to restrict the CRM Compensator component to only those identities of the server applications in which it runs.</span></span> <span data-ttu-id="9f54e-113">如果元件是在程式庫應用程式中執行，則會包含伺服器應用程式的所有身分識別。</span><span class="sxs-lookup"><span data-stu-id="9f54e-113">If the component is running in a library application, this would include all the identities of the server applications.</span></span>

> [!Note]  
> <span data-ttu-id="9f54e-114">從 Windows Server 2003 開始，為了協助防止從伺服器應用程式外部啟用，您可以藉由將 CRM 補償器元件標示為私用，進一步確保系統的安全。</span><span class="sxs-lookup"><span data-stu-id="9f54e-114">Starting with Windows Server 2003, to help prevent activation from outside the server application, it is possible to further ensure a more secure system by marking the CRM Compensator component as private.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9f54e-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="9f54e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9f54e-116">COM + 補償 Resource Manager 概念</span><span class="sxs-lookup"><span data-stu-id="9f54e-116">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



