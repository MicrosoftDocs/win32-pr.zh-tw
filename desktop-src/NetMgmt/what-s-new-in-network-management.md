---
title: 網路管理的新功能
description: 網路管理的新功能
ms.assetid: f805b662-1807-4703-b27e-4721895fe450
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e857ae495491fb35cdd396f227034540ad8f208510b678c9a93eaa7d212230b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983075"
---
# <a name="whats-new-in-network-management"></a>網路管理的新功能

## <a name="windows-8-and-windows-server-2012"></a>Windows 8 與 Windows Server 2012

Microsoft Windows 8 引進了新的網路管理程式設計功能。 這些新的元素擴充了網路管理的功能，可在布建具有 Windows 8 的電腦時，建立離線網域加入作業的布建套件。

以下是新的網路管理功能：

-   [**NetCreateProvisioningPackage**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [**NetRequestProvisioningPackageInstall**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestprovisioningpackageinstall)

以下是新的網路管理結構：

-   [**NETSETUP 布建 \_ \_ 參數**](/windows/desktop/api/Lmjoin/ns-lmjoin-netsetup_provisioning_params)
-   [**使用者 \_ 資訊 \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24)

[**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)函式已在 Windows 8 上增強，以支援新的資訊層級，並傳回 [**使用者 \_ 資訊 \_ 24**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_24)結構，其中包含連線到網際網路身分識別之帳戶的使用者帳戶資訊。

## <a name="windows-7-and-windows-server-2008-r2"></a>Windows 7 與 Windows Server 2008 R2

Microsoft Windows 7 引進了新的網路管理程式設計功能。 這些元素會擴充網路管理的功能，以在布建 Windows 7 的電腦時允許離線網域加入作業。

以下是新的網路管理功能：

-   [**NetProvisionComputerAccount**](/windows/desktop/api/Lmjoin/nf-lmjoin-netprovisioncomputeraccount)
-   [**NetRequestOfflineDomainJoin**](/windows/desktop/api/Lmjoin/nf-lmjoin-netrequestofflinedomainjoin)

下列現有的網路管理功能已增強，可支援其他選項：

-   [**NetJoinDomain**](/windows/desktop/api/Lmjoin/nf-lmjoin-netjoindomain)

## <a name="windows-server-2003"></a>Windows Server 2003

Microsoft Windows Server 2003 引進了新的網路管理程式設計功能。 這些元素擴充了 Windows Server 2003 和更新版本上網路管理作業的功能。

## <a name="windows-xp"></a>Windows XP

Microsoft Windows XP 引進了新的網路管理程式設計功能。 這些元素會在 Windows XP 和更新版本上擴充網路管理作業的功能。

以下是新的網路管理功能：

-   [**NetAddAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netaddalternatecomputername)
-   [**NetEnumerateComputerNames**](/windows/desktop/api/Lmjoin/nf-lmjoin-netenumeratecomputernames)
-   [**NetRemoveAlternateComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netremovealternatecomputername)
-   [**NetSetPrimaryComputerName**](/windows/desktop/api/Lmjoin/nf-lmjoin-netsetprimarycomputername)
-   [**SetNetScheduleAccountInformation**](/windows/desktop/api/AtAcct/nf-atacct-setnetscheduleaccountinformation)

 

 




