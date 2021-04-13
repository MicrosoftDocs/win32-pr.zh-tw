---
title: 多播群組管理員函數
description: 以下是用來向多播群組管理員註冊的功能
ms.assetid: d4374ced-06ea-49dd-8f52-0d06612aa4c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbc3dbcfe24e63283907e5e68f211fd1f4cb6e3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311121"
---
# <a name="multicast-group-manager-functions"></a>多播群組管理員函數

以下是用來向多播群組管理員註冊的函數：

[**MgmRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmregistermprotocol)

[**MgmDeRegisterMProtocol**](/windows/desktop/api/Mgm/nf-mgm-mgmderegistermprotocol)

以下是用來管理介面擁有權的函式：

[**MgmGetProtocolOnInterface**](/windows/desktop/api/Mgm/nf-mgm-mgmgetprotocoloninterface)

[**MgmTakeInterfaceOwnership**](/windows/desktop/api/Mgm/nf-mgm-mgmtakeinterfaceownership)

[**MgmReleaseInterfaceOwnership**](/windows/desktop/api/Mgm/nf-mgm-mgmreleaseinterfaceownership)

以下是用來管理群組成員資格的函數：

[**MgmAddGroupMembershipEntry**](/windows/desktop/api/Mgm/nf-mgm-mgmaddgroupmembershipentry)

[**MgmDeleteGroupMembershipEntry**](/windows/desktop/api/Mgm/nf-mgm-mgmdeletegroupmembershipentry)

下列函式可用來取得多播轉送專案 (MFEs) 和 MFE 統計資料：

[**MgmGetFirstMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfe)

[**MgmGetNextMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfe)

[**MgmGetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfe)

[**MgmGetFirstMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetfirstmfestats)

[**MgmGetNextMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetnextmfestats)

[**MgmGetMfeStats**](/windows/desktop/api/Mgm/nf-mgm-mgmgetmfestats)

下列函式是用來修改 MFEs：

[**MgmSetMfe**](/windows/desktop/api/Mgm/nf-mgm-mgmsetmfe)

下列函式會用來取得已加入的群組清單：

[**MgmGroupEnumerationStart**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationstart)

[**MgmGroupEnumerationGetNext**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationgetnext)

[**MgmGroupEnumerationEnd**](/windows/desktop/api/Mgm/nf-mgm-mgmgroupenumerationend)

 

 




