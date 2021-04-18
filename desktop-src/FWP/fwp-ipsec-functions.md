---
title: IPsec 功能
description: IPsec 功能
ms.assetid: db656c58-7776-44c4-a7ce-c38e59b37c74
keywords:
- Windows 篩選平台 API IPsec 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261e767888b4581587ee550bf240c929f6db4531
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "106965235"
---
# <a name="ipsec-functions"></a><span data-ttu-id="b1ed7-104">IPsec 功能</span><span class="sxs-lookup"><span data-stu-id="b1ed7-104">IPsec Functions</span></span>

<span data-ttu-id="b1ed7-105">Windows 篩選平台 (WFP) 功能與網際網路通訊協定安全性 (IPsec) 如下所示。</span><span class="sxs-lookup"><span data-stu-id="b1ed7-105">The Windows Filtering Platform (WFP) functions that interact with Internet Protocol Security (IPsec) are as follows.</span></span>

-   <span data-ttu-id="b1ed7-106">FwpmIPsecTunnelAdd:</span><span class="sxs-lookup"><span data-stu-id="b1ed7-106">FwpmIPsecTunnelAdd:</span></span>
    -   <span data-ttu-id="b1ed7-107">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) (Windows Vista) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-107">[**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) (Windows Vista)</span></span>
    -   <span data-ttu-id="b1ed7-108">[**FwpmIPsecTunnelAdd1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd1) (Windows 7) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-108">[**FwpmIPsecTunnelAdd1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd1) (Windows 7)</span></span>
    -   <span data-ttu-id="b1ed7-109">[**FwpmIPsecTunnelAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2) (Windows 8) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-109">[**FwpmIPsecTunnelAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2) (Windows 8)</span></span>
-   [<span data-ttu-id="b1ed7-110">**FwpmIPsecTunnelDeleteByKey0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-110">**FwpmIPsecTunnelDeleteByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)
-   [<span data-ttu-id="b1ed7-111">**IPSEC \_ 金鑰 \_ 管理員 \_ 按鍵 \_ 聽寫 \_ CHECK0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-111">**IPSEC\_KEY\_MANAGER\_KEY\_DICTATION\_CHECK0**</span></span>](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [<span data-ttu-id="b1ed7-112">**IPSEC \_ 金鑰 \_ 管理員會 \_ 聽寫 \_ KEY0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-112">**IPSEC\_KEY\_MANAGER\_DICTATE\_KEY0**</span></span>](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [<span data-ttu-id="b1ed7-113">**IPSEC \_ 金鑰 \_ 管理員 \_ 通知 \_ KEY0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-113">**IPSEC\_KEY\_MANAGER\_NOTIFY\_KEY0**</span></span>](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [<span data-ttu-id="b1ed7-114">**IPSEC \_ SA \_ 內容 \_ CALLBACK0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-114">**IPSEC\_SA\_CONTEXT\_CALLBACK0**</span></span>](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [<span data-ttu-id="b1ed7-115">**IPsecDospGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-115">**IPsecDospGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospgetsecurityinfo0)
-   [<span data-ttu-id="b1ed7-116">**IPsecDospGetStatistics0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-116">**IPsecDospGetStatistics0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospgetstatistics0)
-   [<span data-ttu-id="b1ed7-117">**IPsecDospSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-117">**IPsecDospSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospsetsecurityinfo0)
-   [<span data-ttu-id="b1ed7-118">**IPsecDospStateCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-118">**IPsecDospStateCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstatecreateenumhandle0)
-   [<span data-ttu-id="b1ed7-119">**IPsecDospStateDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-119">**IPsecDospStateDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstatedestroyenumhandle0)
-   [<span data-ttu-id="b1ed7-120">**IPsecDospStateEnum0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-120">**IPsecDospStateEnum0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstateenum0)
-   <span data-ttu-id="b1ed7-121">IPsecGetStatistics:</span><span class="sxs-lookup"><span data-stu-id="b1ed7-121">IPsecGetStatistics:</span></span>
    -   <span data-ttu-id="b1ed7-122">[**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) (Windows Vista) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-122">[**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) (Windows Vista)</span></span>
    -   <span data-ttu-id="b1ed7-123">[**IPsecGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics1) (Windows 7 及更新版本) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-123">[**IPsecGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="b1ed7-124">**IPsecKeyManagerAddAndRegister0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-124">**IPsecKeyManagerAddAndRegister0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [<span data-ttu-id="b1ed7-125">**IPsecKeyManagersGet0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-125">**IPsecKeyManagersGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [<span data-ttu-id="b1ed7-126">**IPsecKeyManagerGetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-126">**IPsecKeyManagerGetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [<span data-ttu-id="b1ed7-127">**IPsecKeyManagerSetSecurityInfoByKey0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-127">**IPsecKeyManagerSetSecurityInfoByKey0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [<span data-ttu-id="b1ed7-128">**IPsecKeyManagerUnregisterAndDelete0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-128">**IPsecKeyManagerUnregisterAndDelete0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   <span data-ttu-id="b1ed7-129">IPsecSaCoNtextAddInbound:</span><span class="sxs-lookup"><span data-stu-id="b1ed7-129">IPsecSaContextAddInbound:</span></span>
    -   <span data-ttu-id="b1ed7-130">[**IPsecSaCoNtextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0) (Windows Vista) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-130">[**IPsecSaContextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0) (Windows Vista)</span></span>
    -   <span data-ttu-id="b1ed7-131">[**IPsecSaCoNtextAddInbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound1) (Windows 7 及更新版本) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-131">[**IPsecSaContextAddInbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound1) (Windows 7 and later)</span></span>
-   <span data-ttu-id="b1ed7-132">IPsecSaCoNtextAddOutbound:</span><span class="sxs-lookup"><span data-stu-id="b1ed7-132">IPsecSaContextAddOutbound:</span></span>
    -   <span data-ttu-id="b1ed7-133">[**IPsecSaCoNtextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0) (Windows Vista) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-133">[**IPsecSaContextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0) (Windows Vista)</span></span>
    -   <span data-ttu-id="b1ed7-134">[**IPsecSaCoNtextAddOutbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound1) (Windows 7 及更新版本) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-134">[**IPsecSaContextAddOutbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound1) (Windows 7 and later)</span></span>
-   <span data-ttu-id="b1ed7-135">IPsecSaCoNtextCreate:</span><span class="sxs-lookup"><span data-stu-id="b1ed7-135">IPsecSaContextCreate:</span></span>
    -   <span data-ttu-id="b1ed7-136">[**IPsecSaCoNtextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0) (Windows Vista) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-136">[**IPsecSaContextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0) (Windows Vista)</span></span>
    -   <span data-ttu-id="b1ed7-137">[**IPsecSaCoNtextCreate1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate1) (Windows 7 及更新版本) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-137">[**IPsecSaContextCreate1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="b1ed7-138">**IPsecSaCoNtextCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-138">**IPsecSaContextCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)
-   [<span data-ttu-id="b1ed7-139">**IPsecSaCoNtextDeleteById0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-139">**IPsecSaContextDeleteById0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)
-   [<span data-ttu-id="b1ed7-140">**IPsecSaCoNtextDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-140">**IPsecSaContextDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdestroyenumhandle0)
-   <span data-ttu-id="b1ed7-141">IPsecSaCoNtextEnum:</span><span class="sxs-lookup"><span data-stu-id="b1ed7-141">IPsecSaContextEnum:</span></span>
    -   <span data-ttu-id="b1ed7-142">[**IPsecSaCoNtextEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum0) (Windows Vista) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-142">[**IPsecSaContextEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum0) (Windows Vista)</span></span>
    -   <span data-ttu-id="b1ed7-143">[**IPsecSaCoNtextEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum1) (Windows 7 及更新版本) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-143">[**IPsecSaContextEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="b1ed7-144">**IPsecSaCoNtextExpire0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-144">**IPsecSaContextExpire0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)
-   <span data-ttu-id="b1ed7-145">IPsecSaCoNtextGetById:</span><span class="sxs-lookup"><span data-stu-id="b1ed7-145">IPsecSaContextGetById:</span></span>
    -   <span data-ttu-id="b1ed7-146">[**IPsecSaCoNtextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0) (Windows Vista) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-146">[**IPsecSaContextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0) (Windows Vista)</span></span>
    -   <span data-ttu-id="b1ed7-147">[**IPsecSaCoNtextGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid1) (Windows 7 及更新版本) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-147">[**IPsecSaContextGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid1) (Windows 7 and later)</span></span>
-   <span data-ttu-id="b1ed7-148">IPsecSaCoNtextGetSpi:</span><span class="sxs-lookup"><span data-stu-id="b1ed7-148">IPsecSaContextGetSpi:</span></span>
    -   <span data-ttu-id="b1ed7-149">[**IPsecSaCoNtextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) (Windows Vista) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-149">[**IPsecSaContextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) (Windows Vista)</span></span>
    -   <span data-ttu-id="b1ed7-150">[**IPsecSaCoNtextGetSpi1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi1) (Windows 7 及更新版本) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-150">[**IPsecSaContextGetSpi1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi1) (Windows 7 and later)</span></span>
-   [<span data-ttu-id="b1ed7-151">**IPsecSaCoNtextSetSpi0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-151">**IPsecSaContextSetSpi0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsetspi0)
-   [<span data-ttu-id="b1ed7-152">**IPsecSaCoNtextSubscribe0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-152">**IPsecSaContextSubscribe0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [<span data-ttu-id="b1ed7-153">**IPsecSaCoNtextSubscriptionsGet0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-153">**IPsecSaContextSubscriptionsGet0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [<span data-ttu-id="b1ed7-154">**IPsecSaCoNtextUpdate0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-154">**IPsecSaContextUpdate0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextupdate0)
-   [<span data-ttu-id="b1ed7-155">**IPsecSaCoNtextUpdate0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-155">**IPsecSaContextUpdate0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextupdate0)
-   [<span data-ttu-id="b1ed7-156">**IPsecSaCreateEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-156">**IPsecSaCreateEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)
-   [<span data-ttu-id="b1ed7-157">**IPsecSaDbGetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-157">**IPsecSaDbGetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadbgetsecurityinfo0)
-   [<span data-ttu-id="b1ed7-158">**IPsecSaDbSetSecurityInfo0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-158">**IPsecSaDbSetSecurityInfo0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadbsetsecurityinfo0)
-   [<span data-ttu-id="b1ed7-159">**IPsecSaDestroyEnumHandle0**</span><span class="sxs-lookup"><span data-stu-id="b1ed7-159">**IPsecSaDestroyEnumHandle0**</span></span>](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadestroyenumhandle0)
-   <span data-ttu-id="b1ed7-160">IPsecSaEnum:</span><span class="sxs-lookup"><span data-stu-id="b1ed7-160">IPsecSaEnum:</span></span>
    -   <span data-ttu-id="b1ed7-161">[**IPsecSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum0) (Windows Vista) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-161">[**IPsecSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum0) (Windows Vista)</span></span>
    -   <span data-ttu-id="b1ed7-162">[**IPsecSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum1) (Windows 7 及更新版本) </span><span class="sxs-lookup"><span data-stu-id="b1ed7-162">[**IPsecSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum1) (Windows 7 and later)</span></span>

 

 