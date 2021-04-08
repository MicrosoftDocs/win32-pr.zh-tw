---
title: 目錄服務代理程式
description: 目錄服務代理程式 (DSA) 是在每個網域控制站上執行的服務和進程集合，並提供資料存放區的存取權。
ms.assetid: a921a822-6b2e-4a84-8112-0ae516443667
ms.tgt_platform: multiple
keywords:
- 目錄服務代理程式 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df39d1670f6668f933c20bcd2b9a8771ce83ec56
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842095"
---
# <a name="directory-system-agent"></a>目錄服務代理程式

[*目錄服務代理程式*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) (DSA) 是在每個網域控制站上執行的服務和進程集合，並提供資料存放區的存取權。 資料存放區是位於硬碟的目錄資料的實體存放區。 在 Active Directory Domain Services 中，DSA 是本機系統授權單位的一部分 (LSA) 子系統。 用戶端會使用 DSA 所支援的下列其中一種機制來存取目錄：

-   LDAP 用戶端會使用輕量型目錄存取協定 (LDAP) 來連線至 DSA。 Active Directory Domain Services 支援 rfc 3377 定義的 LDAP 3.0，以及由 RFC 1777 定義的 LDAP 2.0。 Windows 用戶端會使用 LDAP 3.0 來連接到 DSA。
-   MAPI 用戶端（例如 Microsoft Exchange Server）會使用 MAPI 遠端程序呼叫介面連接到 DSA。
-   Active Directory Domain Services 的 Dsa 會彼此連接，以使用專屬的遠端程序呼叫介面來執行複寫。

 

 