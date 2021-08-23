---
title: IPsec 功能
description: IPsec 功能
ms.assetid: db656c58-7776-44c4-a7ce-c38e59b37c74
keywords:
- Windows篩選平臺 API IPsec 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70ccd557011547a06ce0ad232fa84341f56a1b7f7ebdf4281e04bcf715f19922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069218"
---
# <a name="ipsec-functions"></a>IPsec 功能

Windows 篩選平台 (WFP) 函式，與網際網路通訊協定安全性 (IPsec) 互動，如下所示。

-   FwpmIPsecTunnelAdd:
    -   [**FwpmIPsecTunnelAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) (Windows Vista) 
    -   [**FwpmIPsecTunnelAdd1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd1) (Windows 7) 
    -   [**FwpmIPsecTunnelAdd2**](/windows/desktop/api/fwpmu/nf-fwpmu-fwpmipsectunneladd2) (Windows 8) 
-   [**FwpmIPsecTunnelDeleteByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneldeletebykey0)
-   [**IPSEC \_ 金鑰 \_ 管理員 \_ 按鍵 \_ 聽寫 \_ CHECK0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_key_dictation_check0)
-   [**IPSEC \_ 金鑰 \_ 管理員會 \_ 聽寫 \_ KEY0**](/windows/desktop/api/Fwpmu/nc-fwpmu-ipsec_key_manager_dictate_key0)
-   [**IPSEC \_ 金鑰 \_ 管理員 \_ 通知 \_ KEY0**](/windows/desktop/api/fwpmu/nc-fwpmu-ipsec_key_manager_notify_key0)
-   [**IPSEC \_ SA \_ 內容 \_ CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-ipsec_sa_context_callback0)
-   [**IPsecDospGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospgetsecurityinfo0)
-   [**IPsecDospGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospgetstatistics0)
-   [**IPsecDospSetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospsetsecurityinfo0)
-   [**IPsecDospStateCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstatecreateenumhandle0)
-   [**IPsecDospStateDestroyEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstatedestroyenumhandle0)
-   [**IPsecDospStateEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecdospstateenum0)
-   IPsecGetStatistics:
    -   [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) (Windows Vista) 
    -   [**IPsecGetStatistics1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics1) (Windows 7 和更新版本) 
-   [**IPsecKeyManagerAddAndRegister0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanageraddandregister0)
-   [**IPsecKeyManagersGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersget0)
-   [**IPsecKeyManagerGetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagergetsecurityinfobykey0)
-   [**IPsecKeyManagerSetSecurityInfoByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagersetsecurityinfobykey0)
-   [**IPsecKeyManagerUnregisterAndDelete0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipseckeymanagerunregisteranddelete0)
-   IPsecSaCoNtextAddInbound:
    -   [**IPsecSaCoNtextAddInbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound0) (Windows Vista) 
    -   [**IPsecSaCoNtextAddInbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddinbound1) (Windows 7 和更新版本) 
-   IPsecSaCoNtextAddOutbound:
    -   [**IPsecSaCoNtextAddOutbound0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound0) (Windows Vista) 
    -   [**IPsecSaCoNtextAddOutbound1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextaddoutbound1) (Windows 7 和更新版本) 
-   IPsecSaCoNtextCreate:
    -   [**IPsecSaCoNtextCreate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate0) (Windows Vista) 
    -   [**IPsecSaCoNtextCreate1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreate1) (Windows 7 和更新版本) 
-   [**IPsecSaCoNtextCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextcreateenumhandle0)
-   [**IPsecSaCoNtextDeleteById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdeletebyid0)
-   [**IPsecSaCoNtextDestroyEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextdestroyenumhandle0)
-   IPsecSaCoNtextEnum:
    -   [**IPsecSaCoNtextEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum0) (Windows Vista) 
    -   [**IPsecSaCoNtextEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextenum1) (Windows 7 和更新版本) 
-   [**IPsecSaCoNtextExpire0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextexpire0)
-   IPsecSaCoNtextGetById:
    -   [**IPsecSaCoNtextGetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid0) (Windows Vista) 
    -   [**IPsecSaCoNtextGetById1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetbyid1) (Windows 7 和更新版本) 
-   IPsecSaCoNtextGetSpi:
    -   [**IPsecSaCoNtextGetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi0) (Windows Vista) 
    -   [**IPsecSaCoNtextGetSpi1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextgetspi1) (Windows 7 和更新版本) 
-   [**IPsecSaCoNtextSetSpi0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsetspi0)
-   [**IPsecSaCoNtextSubscribe0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscribe0)
-   [**IPsecSaCoNtextSubscriptionsGet0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextsubscriptionsget0)
-   [**IPsecSaCoNtextUpdate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextupdate0)
-   [**IPsecSaCoNtextUpdate0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacontextupdate0)
-   [**IPsecSaCreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsacreateenumhandle0)
-   [**IPsecSaDbGetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadbgetsecurityinfo0)
-   [**IPsecSaDbSetSecurityInfo0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadbsetsecurityinfo0)
-   [**IPsecSaDestroyEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsadestroyenumhandle0)
-   IPsecSaEnum:
    -   [**IPsecSaEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum0) (Windows Vista) 
    -   [**IPsecSaEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecsaenum1) (Windows 7 和更新版本) 

 

 