---
title: 關於 Active Directory Domain Services
description: 本指南提供在針對支援 Active Directory 的作業系統設計的分散式應用程式中整合 Microsoft Active Directory 的基本資訊。
ms.assetid: cc6c63dd-ae22-40a7-8312-0a4648bb92bd
ms.tgt_platform: multiple
keywords:
- Active Directory Active Directory，關於
- Active Directory Domain Services Active Directory，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e4ef886409b435e1687d8ca6cf530b940852f3569818bb3afab69f57ab6b97c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117841072"
---
# <a name="about-active-directory-domain-services"></a>關於 Active Directory Domain Services

## <a name="writing-powerful-applications-that-use-active-directory-domain-services"></a>撰寫使用 Active Directory Domain Services 的強大應用程式

本指南提供在針對支援 Active Directory Domain Services 的作業系統設計的分散式應用程式中整合 Active Directory Domain Services 的基本資訊，包括：

-   Windows Server 2008
-   Windows Server 2008 R2
-   Windows Server 2012
-   Windows Server 2012 R2
-   Windows Server 2016

> [!Note]  
> 這些主題適用于軟體發展人員。 如需支援問題，請參閱 [Microsoft 支援服務](https://windows.microsoft.com/windows/support#1tc)。 如需管理 Active Directory 的詳細資訊，請參閱 TechNet 上的 [Active Directory Domain Services](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc770946(v=ws.10)) 。

 

## <a name="fundamental-directory-features"></a>基本目錄功能

目錄服務是分散式應用程式的基礎服務。 目錄服務必須提供下表所列的功能。



| 功能               | 描述                                                                                         |
|-----------------------|-----------------------------------------------------------------------------------------------------|
| 位置透明度 | 能夠在沒有物件位址的情況下尋找使用者、群組、網路服務或資源的資料           |
| 物件資料           | 能夠在階層式樹狀結構中儲存使用者、群組、組織和服務資料                    |
| 豐富查詢            | 藉由查詢物件屬性來尋找物件                                          |
| 高可用性     | 能夠在可有效率地讀取/寫入作業的位置找出目錄的複本 |



 

## <a name="advanced-features-of-active-directory-domain-services"></a>Active Directory Domain Services 的 Advanced 功能

Active Directory Domain Services 提供下表所列的功能。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>功能</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>網際網路標準的支援</td>
<td>Active Directory Domain Services 會根據已發佈的網際網路標準（例如 LDAP 和 DNS）來實行其功能。</td>
</tr>
<tr class="even">
<td>緊密整合且彈性的安全性</td>
<td>優點包括︰<br/>
<ul>
<li>選擇驗證套件。 Kerberos、安全通訊端層 (SSL) 或組合;例如，建立用於加密的 SSL 通道，然後使用 Kerberos 進行驗證。</li>
<li>使用 Active Directory Domain Services 中的使用者和群組，集中管理服務和資源存取。</li>
<li>管理委派，讓中央系統管理員可以委派系統管理工作，例如密碼變更或特定物件的建立和刪除。</li>
<li>Active Directory 伺服器使用 Windows 作業系統中檔案系統所使用的相同存取控制機制。 因此，在檔案系統上管理存取控制的相同工具也適用于 Active Directory Domain Services。</li>
<li>全方位的公開金鑰基礎結構。 Microsoft 憑證伺服器和智慧卡支援已與 Active Directory Domain Services 整合，以提供智慧卡登入和憑證管理。</li>
</ul></td>
</tr>
<tr class="odd">
<td>容易程式化</td>
<td>您可以使用 <a href="/windows/desktop/ADSI/active-directory-service-interfaces-adsi">Active Directory 服務介面</a> Api、 <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">輕量型目錄存取協定</a> api 或 <a href="/dotnet/api/system.directoryservices">DirectoryServices</a> 命名空間，以程式設計方式存取和管理 Active Directory 伺服器。</td>
</tr>
<tr class="even">
<td>啟用目錄的系統服務</td>
<td>您可以藉由建立 Windows Installer 套件，並使用 Windows 作業系統中提供的應用程式部署功能，輕鬆地將您的用戶端應用程式部署到分散式桌面。</td>
</tr>
<tr class="odd">
<td>主要應用程式整合</td>
<td>重要的分散式應用程式（例如 Exchange）會與 Active Directory Domain Services 整合。 因此，公司可以減少要管理的目錄服務數目。</td>
</tr>
<tr class="even">
<td>豐富且可擴充的架構</td>
<td>架構會定義可寫入和讀取目錄服務的物件和屬性。 Active Directory 的架構很豐富。 服務需要的大部分物件和屬性都可以使用。 如果沒有，分散式應用程式可以擴充架構以支援應用程式需求。</td>
</tr>
</tbody>
</table>



 

如需 Active Directory Domain Services 的詳細資訊，請參閱：

-   [Active Directory Domain Services 的核心概念](core-concepts-of-active-directory-domain-services.md)
-   [Active Directory 架構](active-directory-domain-services-architecture.md)
-   [Active Directory 架構](active-directory-schema.md)

