---
title: 系結至 Active Directory Domain Services
description: 在 Active Directory Domain Services 中，將程式設計物件與特定 Active Directory Domain Services 物件產生關聯的動作稱為「系結」（binding）。
ms.assetid: f48de4d4-c53a-4e40-a34e-4236c3e6cb21
ms.tgt_platform: multiple
keywords:
- 系結至 Active Directory Domain Services Active Directory
- Active Directory Domain Services Active Directory，系結至
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f57aef2b2a3c21ac860d05dd1b7a1e1079d1720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936119"
---
# <a name="binding-to-active-directory-domain-services"></a>系結至 Active Directory Domain Services

在 Active Directory Domain Services 中，將程式設計物件與特定 Active Directory Domain Services 物件產生關聯的動作稱為「系結」（ *binding*）。 當程式設計物件（例如 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 或 [DirectoryEntry](/dotnet/api/system.directoryservices.directoryentry?view=dotnet-plat-ext-3.1&preserve-view=true) 物件）與特定目錄物件相關聯時，程式設計物件會被視為系結 *至* 目錄物件。

## <a name="binding-functions-and-methods"></a>系結函式和方法

以程式設計方式系結至 Active Directory 物件的方法將取決於所使用的程式設計技術。 如需有關使用特定程式設計技術系結至 Active Directory Domain Services 中物件的詳細資訊，請參閱下表所列的主題。



| 程式設計技術                                                                       | 取得詳細資訊                                                           |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [Active Directory 服務介面](/windows/desktop/ADSI/active-directory-service-interfaces-adsi)         | [系結至 ADSI 物件](/windows/desktop/ADSI/binding-to-an-adsi-object)                    |
| [輕量型目錄存取協定](/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api) | [建立 LDAP 會話](/previous-versions/windows/desktop/ldap/establishing-an-ldap-session)              |
| [System.DirectoryServices](/dotnet/api/system.directoryservices)                 | [系結至目錄物件](/previous-versions/ms180840(v=vs.90)) |



 

## <a name="binding-strings"></a>系結字串

所有系結函數和方法都需要系結字串。 系結字串的形式視提供者而定。 有兩個提供者（LDAP 和 WinNT）支援 Active Directory Domain Services。

從 Windows 2000 開始，LDAP 提供者會用來存取 Active Directory Domain Services。 LDAP 系結字串可採用下列其中一種形式：

-   "LDAP:// <host name> / <object name> "
-   "GC:// <host name> / <object name> "

在上述範例中，"LDAP：" 會指定 LDAP 提供者。 "GC：" 使用 LDAP 提供者系結至通用類別目錄服務，以執行快速查詢。

「 &lt; 主機名稱」 &gt; 會指定要系結的伺服器，而且是選擇性的。 可能的話，請不要指定伺服器。 也可以系結至不同網域中的物件。 若要這樣做，請將網域命名系統 (DNS) 目標網域的名稱做為「 &lt; 主機名稱」 &gt; 。 例如，若要系結至 fabrikam.com 之 >domain2.contoso.com 網域中的 Users 容器，系結字串會是 "LDAP://domain2.fabrikam.com/CN=Users,DC=domain2,DC=fabrikam,DC=com"。

「 &lt; 物件名稱」 &gt; 代表 Active Directory Domain Services 中的特定物件。 物件名稱可以是辨別名稱或物件 GUID。

如需 LDAP 系結字串的詳細資訊，請參閱 [Ldap ADsPath](/windows/desktop/ADSI/ldap-adspath)。

針對 Windows NT 4.0，會使用 WinNT 提供者來存取目錄資料，例如使用者、使用者群組、電腦、服務，以及 Windows 2000 中的其他網路物件。 相較于 LDAP 提供者，Windows 2000 和更新版本系統上的 WinNT 提供者具有有限的功能。 如需 WinNT 系結字串的詳細資訊，請參閱 [Winnt ADsPath](/windows/desktop/ADSI/winnt-adspath)。

"LDAP://" 或 "GC://" 的 ADsPath 可以用來系結至命名空間的根目錄。 系結至命名空間的根目錄時，所提供的命名空間物件不會包含任何屬性，而且會包含 LDAP 的網域物件和容器物件，其中包含樹系中所有網域的部分複本以進行 GC。

如需 Active Directory Domain Services 中系結的詳細資訊，請參閱：

-   [無伺服器系結和 RootDSE](serverless-binding-and-rootdse.md)
-   [系結至通用類別目錄](binding-to-the-global-catalog.md)
-   [使用 objectGUID 系結至物件](using-objectguid-to-bind-to-an-object.md)
-   [使用 WKGUID 系結至 Well-Known 物件](binding-to-well-known-objects-using-wkguid.md)
-   [使用 SID 系結至物件](binding-to-an-object-using-a-sid.md)
-   [使用 otherWellKnownObjects 屬性啟用 Rename-Safe 系結](enabling-rename-safe-binding-with-the-otherwellknownobjects-property.md)
-   [驗證](authentication.md)

 

 
