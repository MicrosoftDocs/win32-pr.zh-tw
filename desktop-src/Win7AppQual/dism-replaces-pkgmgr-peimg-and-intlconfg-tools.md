---
description: 部署映像服務與管理 (DISM)
ms.assetid: bbfee966-121b-4b53-9e3e-08a747559da0
title: 部署映像服務與管理 (DISM)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 234d16233927dca2d5dba296fd33fb64135f691e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088486"
---
# <a name="deployment-image-servicing-and-management-dism"></a><span data-ttu-id="792c1-103">部署映像服務與管理 (DISM)</span><span class="sxs-lookup"><span data-stu-id="792c1-103">Deployment Image Servicing and Management (DISM)</span></span>

## <a name="affected-platforms"></a><span data-ttu-id="792c1-104">受影響的平臺</span><span class="sxs-lookup"><span data-stu-id="792c1-104">Affected Platforms</span></span>

<span data-ttu-id="792c1-105">**客戶** 端-WINDOWS Vista SP1 和更新版本的 \| windows 7</span><span class="sxs-lookup"><span data-stu-id="792c1-105">**Clients** - Windows Vista SP1 and later \| Windows 7</span></span>  
<span data-ttu-id="792c1-106">**伺服器** -windows SERVER 2008 RTM 和更新版本的 \| Windows server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="792c1-106">**Servers** - Windows Server 2008 RTM and later \| Windows Server 2008 R2</span></span>  


## <a name="description"></a><span data-ttu-id="792c1-107">Description</span><span class="sxs-lookup"><span data-stu-id="792c1-107">Description</span></span>

<span data-ttu-id="792c1-108">部署映射服務與管理 (DISM) 工具取代 Windows 7 中已淘汰的 pkgmgr、PEImg 和 IntlConfg 工具。</span><span class="sxs-lookup"><span data-stu-id="792c1-108">The Deployment Image Servicing and Management (DISM) tool replaces the pkgmgr, PEImg, and IntlConfg tools that are being retired in Windows 7.</span></span> <span data-ttu-id="792c1-109">DISM 提供單一的集中式工具，以更有效率且標準化的方式來執行這三項工具的所有功能，消除這些工具目前使用者所經歷的許多挫折來源。</span><span class="sxs-lookup"><span data-stu-id="792c1-109">DISM provides a single centralized tool for performing all of the functions of these three tools in a more efficient and standardized way, eliminating the source of many of the frustrations experienced by current users of these tools.</span></span>

<span data-ttu-id="792c1-110">DISM 包含適用于 Windows Vista SP1 和更新版本的填充碼，以及 Windows Server 2008 RTM 和更新版本的填充碼，可將 pkgmgr 呼叫從 Windows 7 上執行的繼承應用程式重新導向至 DISM。</span><span class="sxs-lookup"><span data-stu-id="792c1-110">DISM includes a shim for Windows Vista SP1 and later, as well as for Windows Server 2008 RTM and later, that redirects pkgmgr calls from legacy applications running on Windows 7 to DISM.</span></span> <span data-ttu-id="792c1-111">如果應用程式是在其中一個支援的作業系統上執行，填充碼會將呼叫路由傳送至 pkgmgr。</span><span class="sxs-lookup"><span data-stu-id="792c1-111">If the application is running on one of the supported operating systems, the shim routes the call to pkgmgr.</span></span> <span data-ttu-id="792c1-112">呼叫 PEImg 或 IntlConfg 的繼承應用程式不會有填充碼。</span><span class="sxs-lookup"><span data-stu-id="792c1-112">No shims exist for legacy applications that call PEImg or IntlConfg.</span></span>

## <a name="usage"></a><span data-ttu-id="792c1-113">使用方式</span><span class="sxs-lookup"><span data-stu-id="792c1-113">Usage</span></span>

<span data-ttu-id="792c1-114">DISM 在任何支援的平臺上 pkgmgr 終端使用者是透明的。</span><span class="sxs-lookup"><span data-stu-id="792c1-114">DISM is transparent to pkgmgr end users on any of the supported platforms.</span></span> <span data-ttu-id="792c1-115">但是，如果應用程式從 Windows 7 呼叫 PEImg 或 IntlConfg，則呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="792c1-115">However, if an application calls either PEImg or IntlConfg from Windows 7, the call will fail.</span></span>

<span data-ttu-id="792c1-116">更新任何呼叫 pkgmgr、PEImg 或 IntlConfg 的腳本，以改為呼叫 DISM。</span><span class="sxs-lookup"><span data-stu-id="792c1-116">Update any scripts that call pkgmgr, PEImg, or IntlConfg to call DISM instead.</span></span> <span data-ttu-id="792c1-117">請務必包含 pkgmgr 腳本的更新，因為在未來的 Windows 作業系統版本中，將會移除為 pkgmgr 提供回溯相容性的填充碼。</span><span class="sxs-lookup"><span data-stu-id="792c1-117">It is important to include the updating of pkgmgr scripts in this effort, since the shim that provides backward compatibility for pkgmgr will be removed in future versions of the Windows operating systems.</span></span>

<span data-ttu-id="792c1-118">檢查以確定對 DISM 的呼叫已取代任何對 pkgmgr、PEImg 和 IntlConfg 的呼叫，且作業順利執行。</span><span class="sxs-lookup"><span data-stu-id="792c1-118">Check to ensure that calls to DISM have replaced any calls to pkgmgr, PEImg, and IntlConfg, and that the operation executes successfully.</span></span>

## <a name="related-topics"></a><span data-ttu-id="792c1-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="792c1-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="792c1-120">[部署映射服務與管理 (TechNet) ](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span><span class="sxs-lookup"><span data-stu-id="792c1-120">[Deployment Image Servicing and Management (TechNet)](/previous-versions/windows/it-pro/windows-7/dd744256(v=ws.10))</span></span>
</dt> </dl>

 

 
