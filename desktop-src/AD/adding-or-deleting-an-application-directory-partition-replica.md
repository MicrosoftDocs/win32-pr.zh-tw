---
title: 新增或刪除應用程式目錄分割複本
description: 應用程式目錄分割的第一個複本是在建立時系結至該磁碟分割的網域控制站上建立的。
ms.assetid: 2dafc822-d0e8-4960-9a45-cc21d1d2924c
ms.tgt_platform: multiple
keywords:
- 新增或刪除應用程式目錄分割複本 AD
- 應用程式目錄分割 AD、新增或刪除分割區複本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c84b19e64f6abfc5e63d6e0e3d1b3a192da3e38
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104092643"
---
# <a name="adding-or-deleting-an-application-directory-partition-replica"></a>新增或刪除應用程式目錄分割複本

應用程式目錄分割的第一個複本是在建立時系結至該磁碟分割的網域控制站上建立的。 您可以在樹系中的任何網域控制站上建立額外的複本，而不一定要在與初始網域控制站相同的網域中建立。 應用程式目錄分割複本只能存在於執行 Windows Server 2003 或更新版本的網域控制站上。 如需詳細資訊，請參閱這篇有關 [分割區管理](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc730970(v=ws.10))的 TechNet 文章。

**若要新增應用程式目錄分割的複本，請執行下列步驟**

1.  在 [資料分割] 容器中搜尋具有與應用程式目錄分割的辨別名稱相等的 [**nCName**](/windows/desktop/ADSchema/a-ncname)屬性值的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件。
2.  系結至已啟用委派的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref) 物件。 這是必要的，因為只能在 Domain-Naming FSMO 角色持有者上修改 **交叉引用** 物件。 在啟用委派的情況下，網域控制站可以使用相同的認證來與 Domain-Naming FSMO 角色持有者聯繫。
3.  針對將裝載新複本的網域控制站，將 [**nTDSDSA**](/windows/desktop/ADSchema/c-ntdsdsa)物件的辨別名稱加入至 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件的 [自 [**NC-複本位置**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)] 屬性。

當新的「高階 [**NC-複本位置**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) 」屬性值複寫至將裝載應用程式目錄分割複本的新網域控制站時，系統會觸發 KCC 將應用程式目錄分割複寫到目標網域控制站。

若要移除應用程式目錄分割的複本，請執行上述相同步驟，以找出代表應用程式目錄分割的 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件，並從 **交叉引用** 物件的 [使用 [**NC-複本位置**](/windows/desktop/ADSchema/a-msds-nc-replica-locations)] 屬性中移除對應至網域控制站的值。

當新的「高階 [**NC-複本位置**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) 」屬性值複寫到將不再裝載應用程式目錄分割複本的網域控制站時，系統將會觸發 KCC，以移除目標網域控制站上的應用程式目錄分割複本。

如果已移除或降級裝載應用程式目錄分割複本的網域控制站，Active Directory 伺服器將會自動從所有 [**交叉引用**](/windows/desktop/ADSchema/c-crossref)物件的 [使用中- [**-----**](/windows/desktop/ADSchema/a-msds-nc-replica-locations) -----------------------replica-

 

 