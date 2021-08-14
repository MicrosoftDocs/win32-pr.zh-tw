---
title: Active Directory Domain Services 中的使用者
description: Active Directory Domain Services 包含儲存網域、使用者、使用者群組和安全性資料的目錄服務。
ms.assetid: 7630fde1-14c0-4518-bb77-813f6913503e
ms.tgt_platform: multiple
keywords:
- Active Directory Domain Services Active Directory 中的使用者
- 使用者、active directory 網域服務
- active directory 網域服務，使用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8eab1633577906557639a65bc0f24e3bcfc0221f4fdf19602bfa7807a352a61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182532"
---
# <a name="users-in-active-directory-domain-services"></a>Active Directory Domain Services 中的使用者

Active Directory Domain Services 包含儲存網域、使用者、使用者群組和安全性資料的目錄服務。

在 Windows NT 4.0 及更早版本上，您可以使用 [**NetUserAdd**](/windows/desktop/api/lmaccess/nf-lmaccess-netuseradd)、 [**NetUserEnum**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum)、 [**NetUserDel**](/windows/desktop/api/lmaccess/nf-lmaccess-netuserdel)等函數來管理使用者、使用者群組和其他網路專案。 在 Windows 2000 和更新版本的 Windows 中，ADSI 會提供這些專案及其屬性的統一且安全的存取。 請注意，adsi 提供了 Windows NT 4.0 提供者，可讓您使用 adsi 來管理 Windows NT 4.0 系統上的使用者、使用者群組和電腦。 另外還有 Windows server 2008 Enterprise (server Core 安裝) 、microsoft Exchange 5.5、microsoft Internet information Server (IIS) 、Novell NetWare 目錄服務 (NDS) 和 novell NetWare 3 的提供者。 也就是一組用來管理 Windows NT、NDS 和 NetWare 3 使用者和使用者群組的標準化方法。

此外，Windows 2000 是多重主目錄。 也就是說，您可以在任何網域控制站上，對使用者、使用者群組和其他儲存在目錄中的資料進行變更。 在 Windows 2000 中，您不需要找出網域主控站 (pdc) ，並在 pdc 上進行使用者和使用者群組的變更。

Windows 2000 也會在名為組織單位 (OU) 的網域內引進新的階層命名空間。 OU 可包含電腦、使用者、使用者群組和其他網路物件。 通常會基於管理目的而使用 OU 來將專案分組，例如委派系統管理許可權，並將原則指派給群組作為單一單位。

網域、Ou、使用者、使用者群組、電腦和其他網路專案會儲存為 Active Directory Domain Services 中的物件。 在 Windows 2000 和更新版本的 Windows 中，您仍然會將使用者、使用者群組和電腦新增至網域。 不過，您現在可以選擇將這些物件加入 OU 容器，或您想要新增的物件在其 **classSchema** 物件的 **possSuperiors** 屬性中定義的任何其他容器類型;這是物件的 **classSchema** 物件上的屬性，而這個屬性會限制可包含該物件的物件類型。

 

 