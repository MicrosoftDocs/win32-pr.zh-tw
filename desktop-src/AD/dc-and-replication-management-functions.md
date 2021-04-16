---
title: 網域控制站和複寫管理功能
description: 本主題包含用於網域控制站和複寫管理的函數清單。
ms.assetid: a92783c2-ffb8-473e-8484-1c05ca5453ff
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00660658874bad4e34a8f6917e08289007cec4d7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023263"
---
# <a name="domain-controller-and-replication-management-functions"></a>網域控制站和複寫管理功能

網域控制站 (DC) 和複寫管理函式提供的工具可用來尋找 DC 的相關資料、轉換不同格式之間網路物件的名稱、操作服務主體名稱 (Spn) 和目錄服務代理程式 (Dsa) ，以及管理伺服器的複寫。 下列功能可讓開發人員使用網域控制站、複寫和目錄服務：

-   [**DsAddSidHistory**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsaddsidhistorya)
-   [**DsBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbinda)
-   [**DsBindingSetTimeout**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindingsettimeout)
-   [**DsBindToISTG**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindtoistga)
-   [**DsBindWithCred**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithcreda)
-   [**DsBindWithSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithspna)
-   [**DsBindWithSpnEx**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithspnexa)
-   [**DsClientMakeSpnForTargetServer**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsclientmakespnfortargetservera)
-   [**DsCrackNames**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dscracknamesa)
-   [**DsCrackSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dscrackspna)
-   [**DsCrackUnquotedMangledRdn**](/windows/desktop/api/Dsparse/nf-dsparse-dscrackunquotedmangledrdna)
-   [**DsFreeDomainControllerInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreedomaincontrollerinfoa)
-   [**DsFreeNameResult**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreenameresulta)
-   [**DsFreePasswordCredentials**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreepasswordcredentials)
-   [**DsFreeSchemaGuidMap**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreeschemaguidmapa)
-   [**DsFreeSpnArray**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsfreespnarraya)
-   [**DsGetDomainControllerInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetdomaincontrollerinfoa)
-   [**DsGetRdnW**](/windows/desktop/api/Dsparse/nf-dsparse-dsgetrdnw)
-   [**DsGetSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsgetspna)
-   [**DsInheritSecurityIdentity**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsinheritsecurityidentitya)
-   [**DsIsMangledDn**](/windows/desktop/api/Dsparse/nf-dsparse-dsismangleddna)
-   [**DsIsMangledRdnValue**](/windows/desktop/api/Dsparse/nf-dsparse-dsismangledrdnvaluea)
-   [**DsListDomainsInSite**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistdomainsinsitea)
-   [**DsListInfoForServer**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistinfoforservera)
-   [**DsListRoles**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistrolesa)
-   [**DsListServersForDomainInSite**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistserversfordomaininsitea)
-   [**DsListServersInSite**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistserversinsitea)
-   [**DsListSites**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dslistsitesa)
-   [**DsMakePasswordCredentials**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsmakepasswordcredentialsa)
-   [**DsMakeSpn**](/windows/desktop/api/Dsparse/nf-dsparse-dsmakespna)
-   [**DsMapSchemaGuids**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsmapschemaguidsa)
-   [**DsQuerySitesByCost**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsquerysitesbycosta)
-   [**DsQuerySitesFree**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsquerysitesfree)
-   [**DsQuoteRdnValue**](/windows/desktop/api/Dsparse/nf-dsparse-dsquoterdnvaluea)
-   [**DsRemoveDsDomain**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsremovedsdomaina)
-   [**DsRemoveDsServer**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsremovedsservera)
-   [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda)
-   [**DsReplicaConsistencyCheck**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaconsistencycheck)
-   [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela)
-   [**DsReplicaFreeInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicafreeinfo)
-   [**DsReplicaGetInfo**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfow)
-   [**DsReplicaGetInfo2**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicagetinfo2w)
-   [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya)
-   [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca)
-   [**DsReplicaSyncAll**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasyncalla)
-   [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa)
-   [**DsReplicaVerifyObjects**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaverifyobjectsa)
-   [**DsServerRegisterSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsserverregisterspna)
-   [**DsUnBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsunbinda)
-   [**DsUnquoteRdnValue**](/windows/desktop/api/Dsparse/nf-dsparse-dsunquoterdnvaluea)
-   [**DsWriteAccountSpn**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dswriteaccountspna)
-   [**SyncUpdateProc**](/previous-versions/windows/desktop/legacy/ms677968(v=vs.85))

這些函數大多需要系結至目錄服務的控制碼。 [**DsBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbinda)和 [**DsBindWithCred**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsbindwithcreda)函式會啟動具有特定網域控制站的 RPC 會話，然後將控制碼系結至目錄服務，並傳回控制碼。 當不再需要控制碼時，請使用 [**DsUnBind**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsunbinda) 函式來結束 RPC 會話，並解除控制碼的系結。

在來源伺服器與目的地伺服器之間進行複寫。 來源伺服器會維護應該複寫的目的地伺服器清單，而目的地伺服器會維護從中接收復寫的來源伺服器清單。 您可以使用 [**DsReplicaAdd**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaadda) 函式，將目的地伺服器上的來源伺服器清單新增到目的地伺服器上的來源伺服器清單中，並使用 [**DsReplicaDel**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicadela) 函數來移除目的地伺服器上來源伺服器清單的參考。 [**DsReplicaModify**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicamodifya)函數可以用來變更目的地伺服器上的現有來源伺服器參考。 若要變更來源伺服器上的目的地伺服器清單，請使用 [**DsReplicaUpdateRefs**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicaupdaterefsa) 函數。

實際的複寫是由 [**DsReplicaSync**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasynca) 和 [**DsReplicaSyncAll**](/windows/desktop/api/Ntdsapi/nf-ntdsapi-dsreplicasyncalla) 函數所執行。 **DsReplicaSync** 函式會將特定目的地伺服器與單一來源伺服器同步。 使用 **DsReplicaSyncAll** 函式，將目的地伺服器與網站中的所有其他伺服器同步。

 

 