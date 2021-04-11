---
title: 應用程式目錄分割
description: 在 Windows Server 2003 中，Active Directory Domain Services 支援應用程式目錄磁碟分割。
ms.assetid: 55c47803-c1ee-4888-bb19-103374ec9719
ms.tgt_platform: multiple
keywords:
- 應用程式目錄分割廣告
- 應用程式目錄分割 AD，使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63a8e035231aa24569b6fad6d5a7e0e62eaa5a30
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023291"
---
# <a name="application-directory-partitions"></a>應用程式目錄分割

在 Windows Server 2003 中，Active Directory Domain Services 支援應用程式目錄磁碟分割。 應用程式目錄分割可以包含任何類型物件的階層，但安全性主體除外，而且可以設定為複寫到樹系中的任何一組網域控制站。 與網域分割不同的是，應用程式目錄分割不需要複寫到網域中的所有網域控制站，而且資料分割可以複寫到樹系中不同網域的網域控制站。 如需應用程式目錄分割的詳細資訊，請參閱 [關於應用程式目錄](about-application-directory-partitions.md)分割。

您可以建立應用程式目錄分割。 使用標準的 ADSI、LDAP 和 [DirectoryServices](/dotnet/api/system.directoryservices) 作業來修改和刪除。 建立和修改應用程式目錄分割所需的安全性內容，與建立網域分割的方式相同。

下列主題描述如何使用應用程式目錄分割：

-   [應用程式目錄分割複寫](application-directory-partition-replication.md)
-   [應用程式目錄分割安全性](application-directory-partition-security.md)
-   [建立應用程式目錄分割](creating-an-application-directory-partition.md)
-   [刪除應用程式目錄分割](deleting-an-application-directory-partition.md)
-   [列舉樹系中的應用程式目錄分割](enumerating-application-directory-partitions-in-a-forest.md)
-   [尋找應用程式目錄分割主機伺服器](locating-an-application-directory-partition-host-server.md)
-   [新增或刪除應用程式目錄分割複本](adding-or-deleting-an-application-directory-partition-replica.md)
-   [列舉應用程式目錄分割的複本](enumerating-replicas-of-an-application-directory-partition.md)
-   [修改應用程式目錄分割設定](modifying-application-directory-partition-configuration.md)

 

 