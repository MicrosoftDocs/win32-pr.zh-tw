---
title: 伺服器和工作站上網路管理功能的需求
description: 如果您在伺服器或工作站上呼叫本主題所列的其中一個網路管理功能，則會將不同的存取需求套用至資訊查詢和資訊更新。
ms.assetid: 05ff1771-8058-4c86-8f45-735bf41dc128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b06e516aa06465c67966cc076a0ca524d4ae4003
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842640"
---
# <a name="requirements-for-network-management-functions-on-servers-and-workstations"></a>伺服器和工作站上網路管理功能的需求

如果您在伺服器或工作站上呼叫本主題所列的其中一個網路管理功能，則會將不同的存取需求套用至資訊查詢和資訊更新。

## <a name="queries"></a>查詢

如果您呼叫下列其中一項功能，在伺服器或工作站上執行查詢，則所有已驗證的使用者預設都可以讀取和列舉資訊。

-   [**NetGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupenum)、 [**NetGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetinfo)、 [**NetGroupGetUsers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netgroupgetusers)
-   [**NetLocalGroupEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupenum)、 [**NetLocalGroupGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetinfo)、 [**NetLocalGroupGetMembers**](/windows/desktop/api/Lmaccess/nf-lmaccess-netlocalgroupgetmembers)
-   [**NetQueryDisplayInformation**](/windows/desktop/api/Lmaccess/nf-lmaccess-netquerydisplayinformation)
-   [**NetSessionGetInfo**](/windows/desktop/api/lmshare/nf-lmshare-netsessiongetinfo) (層級1和2僅) 
-   [**NetShareEnum**](/windows/desktop/api/lmshare/nf-lmshare-netshareenum) (層級2和502僅) 
-   [**NetUserEnum**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuserenum)、 [**NetUserGetGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetgroups)、 [**NetUserGetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetinfo)、 [**NetUserGetLocalGroups**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusergetlocalgroups)、 [**NetUserModalsGet**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusermodalsget)
-   [**NetWkstaGetInfo**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstagetinfo)、 [ **NetWkstaUserEnum**](/windows/desktop/api/Lmwksta/nf-lmwksta-netwkstauserenum)

以下是讀取和列舉資訊時，匿名存取的其他相關資訊。

**Windows Server 2003 和 WINDOWS XP：** 如果 EveryoneIncludesAnonymous 原則設定允許匿名存取，就可以匿名存取訊號。

**Windows 2000：** 如果機原則設定允許匿名存取，則可以匿名存取安全物件。 您可以將登錄中的下列機碼設定為值1，以限制匿名存取。

**HKEY \_LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ Lsa** \\ **機**= 1

如需詳細資訊，請參閱 Microsoft 知識庫中的下列文章：

文章識別碼： [Q246261](https://support.microsoft.com/kb/246261)

標題：如何使用機登錄值。

## <a name="updates"></a>更新

依預設，只有系統管理員和 Power Users 可以寫入資訊。

如需控制安全物件之存取的詳細資訊，請參閱 [存取控制](/windows/desktop/SecAuthZ/access-control)、 [許可權](/windows/desktop/SecAuthZ/privileges)和 [安全物件](/windows/desktop/SecAuthZ/securable-objects)。 如需呼叫需要系統管理員許可權之函式的詳細資訊，請參閱 [以特殊許可權](/windows/desktop/SecBP/running-with-special-privileges)執行。

 

 