---
title: 服務連接點屬性
description: ServiceConnectionPoint 類別的屬性足以應付大部分的服務。
ms.assetid: 08888d2c-b46e-4b86-87e4-0c061ea147a0
ms.tgt_platform: multiple
keywords:
- 服務連接點屬性
- 服務連接點 AD，屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511bbba8acf50a185f1bdd8b55d9b7f8ce684817
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104092623"
---
# <a name="service-connection-point-properties"></a>服務連接點屬性

**ServiceConnectionPoint** 類別的屬性足以應付大部分的服務。 Active Directory Domain Services 不會定義使用屬性的方式，因此服務的用戶端必須能夠解讀和使用服務 Scp 中的資料。 必須發行其他相關資料的服務，可以藉由建立 **serviceConnectionPoint** 類別的子類別來延伸 Active Directory 架構，讓子類別成為相異名稱。 如需架構延伸的詳細資訊，請參閱 [擴充架構](extending-the-schema.md)。

SCP 最重要的屬性是 **關鍵字**、 **serviceDNSName**、 **serviceDNSNameType**、 **serviceClassName** 和 **serviceBindingInformation**。 用戶端應用程式會在目錄中搜尋 **關鍵字** 值以找出您的 SCP。 找到您的 SCP 之後，用戶端就可以讀取其他屬性來取得服務資料。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>關鍵 字</strong><br/></td>
<td><strong>關鍵字</strong>屬性可包含多個字串值，以識別您的服務。 此屬性包含在通用類別目錄中，這表示企業樹系的任何網域中的用戶端可以在通用類別目錄中搜尋與您的服務相關聯的關鍵字。 這個屬性也會編制索引，以改善查詢效能。 建立 SCP 的安裝程式會設定 <strong>關鍵字</strong> 屬性的值。 一般而言，使用中的服務不會修改這些值。<br/> 您應該包含在 SCP 中的確切關鍵字，取決於用戶端搜尋服務的方式。 要使用的最佳關鍵字是 GUID 字串，因為 Guid 在樹系中保證是唯一的。 使用 RPC 程式庫中 <a href="/windows/desktop/api/rpcdce/nf-rpcdce-uuidtostring"><strong>UuidToString</strong></a> 函數所傳回的 GUID 字串格式。 如果用戶端可能會使用它們來搜尋您的服務，您也可以包含人們可讀取的名稱。 SCP 中的關鍵字應該包含 GUID 字串及/或名稱，以識別與服務相關的下列資料：
<ul>
<li>您的公司或組織：例如 Fabrikam。</li>
<li>產品或服務：例如 SQL Server。 這可讓用戶端應用程式尋找該類型服務的 Scp。</li>
<li>產品或服務的特定版本，例如7.5。</li>
<li>針對針對某一類型服務發佈一組特定資料或功能的 Scp，請包含可識別特定實例的 GUID 字串或名稱。 例如，資料庫服務可以發行特定資料庫的 SCP。 在此情況下，SCP 會包含用來識別服務的產品 GUID，以及用來識別資料庫的另一個 GUID。</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><strong>serviceDNSName</strong> 和 <strong>serviceDNSNameType</strong><br/></td>
<td>用戶端應用程式會使用 <strong>serviceDNSName</strong> 和 <strong>serviceDNSNameType</strong> 屬性來判斷服務的主機電腦。 <strong>ServiceDNSNameType</strong>值指出<strong>serviceDNSName</strong>所指定的 DNS 名稱類型，通常 &quot; 是 &quot; <strong>serviceDNSName</strong>包含主機名稱， &quot; &quot; 如果<strong>serviceDNSName</strong>包含 srv 記錄名稱，則為 srv。<br/> <strong>ServiceDNSName</strong>值通常是服務主機電腦的 DNS 名稱。 您的服務安裝程式可以呼叫 <a href="/windows/desktop/api/sysinfoapi/nf-sysinfoapi-getcomputernameexa"><strong>GetComputerNameEx</strong></a> 函數來取得本機電腦的 DNS 名稱。<br/> 對於具有 DNS SRV 記錄的服務， <strong>serviceDNSName</strong> 可以是 SRV 記錄的名稱。 用戶端應用程式會使用 DNS Api 來取得所有符合此名稱的 SRV 記錄。 然後，用戶端會從其中一個 SRV 記錄抓取 DNS 主機名稱。 這項技術適用于複寫的服務，因為 SRV 記錄也包含可讓用戶端選取最佳複本的資料。<br/></td>
</tr>
<tr class="odd">
<td><strong>serviceBindingInformation</strong><br/></td>
<td>多值屬性，包含儲存系結至服務所需資料的字串值。 這個屬性會進行索引，並複寫至通用類別目錄。<br/> <strong>ServiceBindingInformation</strong>的內容是發佈 SCP 的服務所特有;用戶端必須解讀系結資料。 在最常見的情況下，系結資料包含在服務主機電腦上的埠號碼。<br/></td>
</tr>
<tr class="even">
<td><strong>serviceClassName</strong><br/></td>
<td>單一值屬性，識別 SCP 所表示的服務類別。 這是發佈 SCP 之服務特定的描述性字串;例如，SqlServer。 針對支援相互驗證的服務，用戶端可以使用此屬性以及服務主機電腦的 DNS 名稱，形成服務主體名稱。 如需詳細資訊，請參閱 <a href="mutual-authentication-using-kerberos.md">使用 Kerberos 進行相互驗證</a>。<br/></td>
</tr>
</tbody>
</table>



 

 

