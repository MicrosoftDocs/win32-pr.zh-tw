---
title: 群組物件
description: 群組會以 Active Directory Domain Services 中的群組物件來表示。
ms.assetid: 2dd5a293-047a-4639-9c95-7074578952be
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a935d2a44d3350d8c24ca3bdb388f0a4bd8f16ee
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933065"
---
# <a name="group-objects"></a>群組物件

群組會以 Active Directory Domain Services 中的 [**群組**](/windows/desktop/ADSchema/c-group) 物件來表示。 下表列出 **群組** 物件的重要屬性。



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
<td><strong>cn</strong></td>
<td><strong>Cn</strong> (或一般名稱) 是單一值屬性，也就是物件的相對辨別名稱。 <strong>Cn</strong>是 Active Directory Domain Services 中的組名。 和所有其他物件一樣，群組的 <strong>cn</strong> 在包含群組的容器中的同級物件之間必須是唯一的。<br/></td>
</tr>
<tr class="even">
<td><strong>成員</strong></td>
<td><strong>成員</strong>屬性是多重值屬性，其中包含屬於群組成員之使用者、群組和連絡人物件的辨別名稱清單。 清單中的每個專案都是代表該成員之物件的連結參考;因此，當成員物件移動或重新命名時，Active Directory 伺服器會自動更新成員屬性中的辨別名稱。<br/></td>
</tr>
<tr class="odd">
<td><strong>groupType</strong></td>
<td><strong>GroupType</strong>屬性是單一值屬性，它是使用下列位旗標指定群組類型和範圍的整數：
<ul>
<li><strong>ADS_GROUP_TYPE_DOMAIN_LOCAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_GLOBAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_UNIVERSAL_GROUP</strong></li>
<li><strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong></li>
</ul>
<br/> 前三個旗標指定群組範圍。 <strong>ADS_GROUP_TYPE_SECURITY_ENABLED</strong>旗標會指出群組類型。 如果設定此旗標，群組就是安全性群組。 如果未設定此旗標，則群組為通訊群組。 如需詳細資訊，請參閱 <a href="#group-types">群組類型</a>。<br/></td>
</tr>
<tr class="even">
<td><strong>memberOf</strong></td>
<td><strong>MemberOf</strong>屬性是多重值屬性，其中包含將群組包含為成員之群組的辨別名稱清單。 這個屬性會列出群組直接嵌套的群組，不包含嵌套前置項的遞迴清單。 例如，如果群組 D 是嵌套在群組 C 和群組 B 中，而群組 B 是嵌套在群組 A 中，則群組 D 的 <strong>memberOf</strong> 屬性會列出群組 C 和群組 b，但不會列出群組 a。<br/></td>
</tr>
<tr class="odd">
<td><strong>objectGUID</strong></td>
<td><strong>ObjectGUID</strong>屬性是單一值屬性，它是物件的唯一識別碼。 這個屬性是 (GUID) 的全域唯一識別碼。 在目錄中建立物件時，Active Directory 伺服器會產生 GUID，並將其指派給物件的 <strong>objectGUID</strong> 屬性。 GUID 在企業和其他任何地方都是唯一的。<br/> <strong>ObjectGUID</strong>是儲存為 OctetString 的128位 GUID 結構。<br/></td>
</tr>
<tr class="even">
<td><strong>objectSid</strong></td>
<td><strong>ObjectSid</strong>屬性是單一值屬性，可指定群組 (SID) 的安全識別碼。 SID 是用來將群組識別為安全性主體的唯一值。 它是系統在建立群組時所設定的二進位值。<br/> 每個群組都有唯一的 SID，也就是儲存在目錄中群組物件的 <strong>objectSid</strong> 屬性中的 Windows NT/Windows 2000 伺服器網域問題。 每次使用者登入時，系統都會抓取使用者所屬群組的 SID，並將其放在使用者的存取權杖中。 系統會使用使用者存取權杖中的 Sid 來識別使用者及其群組成員資格，在後續與 Windows NT/Windows 2000 安全性的互動中。<br/> 使用 SID 做為使用者或群組的唯一識別碼時，不能再次用來識別另一個使用者或群組。<br/></td>
</tr>
<tr class="odd">
<td><strong>sAMAccountName</strong></td>
<td><strong>SAMAccountName</strong>屬性是單一值屬性，也就是用來支援舊版的用戶端和伺服器的登入名稱 (Windows 95、windows 98 和 LAN Manager) 。 <strong>SAMAccountName</strong>應小於20個字元，以支援舊版的用戶端和伺服器。<br/> <strong>SAMAccountName</strong>在網域內的所有安全性主體物件之間必須是唯一的。<br/></td>
</tr>
</tbody>
</table>



 

## <a name="group-types"></a>群組類型

有兩種類型的群組，由 Active Directory Domain Services、 *安全性群組* 和 *通訊群組* 定義。

安全性群組會提供物件的邏輯群組，而群組本身可用來作為存取控制清單中的安全性主體 (ACL) 。 當安全性群組獲得物件的存取權時，安全性群組的所有成員都會自動收到相同的物件存取權。 具有通用領域的安全性群組也可用來做為電子郵件實體。 傳送電子郵件訊息給通用安全性群組，會將訊息傳送給群組的所有成員。

通訊群組也會提供物件的邏輯群組，但無法提供任何存取權限。 通訊群組未啟用安全性，而且無法當做 ACL 中的安全性主體使用。 通訊群組只用于群組用途。 例如，通訊群組清單可以搭配電子郵件應用程式（例如 Exchange）使用，以傳送電子郵件給使用者集合。

如需 Active Directory Domain Services 中群組類型的詳細資訊，請參閱[Microsoft TechNet](https://technet.microsoft.com/default.aspx)上的[群組類型](/previous-versions/windows/it-pro/windows-server-2003/cc781446(v=ws.10))主題。

## <a name="group-scope"></a>群組領域

有三個群組範圍是由 Active Directory Domain Services、 *通用*、 *全域* 和 *網域本機* 所定義。 群組的範圍定義可以屬於群組的物件類型、群組可以隸屬的群組類型，以及安全性群組可獲得存取權的物件範圍。 當網域功能等級設定為 [Windows 2000 混合模式] 時，就無法建立具有通用領域的安全性群組。

下表列出三個群組範圍，以及安全性群組每個範圍的詳細資訊。

| 影響範圍                   | 可能的成員                                                                                                                                                                                                                                      | 範圍轉換                                                                                                                                                 | 可以授與許可權                                                       | 的可能成員                                                                                                                                                                                                  |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 通用<br/>    | 相同樹系中任何網域的帳戶。<br/> 相同樹系中任何網域的全域群組。<br/> 相同樹系中任何網域的其他萬用群組。<br/>                                                            | 可以轉換成網域區域範圍。<br/> 只要群組不包含任何其他萬用群組，就可以轉換成全域領域。<br/> | 位於相同樹系或信任樹系中的任何網域。<br/>            | 相同樹系中的其他萬用群組。<br/> 相同樹系或信任樹系中的網域本機群組。<br/> 位於相同樹系或信任樹系中的電腦上的本機群組。<br/>            |
| 全球<br/>       | 來自相同網域的帳戶。<br/> 相同網域中的其他全域群組。<br/>                                                                                                                                                        | 只要群組不是任何其他全域群組的成員，就可以轉換成通用範圍。<br/>                                                   | 位於相同樹系中的任何網域，或信任網域或樹系。<br/> | 相同樹系中任何網域的萬用群組。<br/> 相同網域中的其他全域群組。<br/> 來自相同樹系中任何網域或來自任何信任網域的網域本機群組。<br/> |
| 網域本機<br/> | 來自任何網域或任何信任網域的帳戶。<br/> 來自任何網域或任何受信任網域的全域群組。<br/> 相同樹系中任何網域的萬用群組。<br/> 來自相同網域的其他網域本機群組。<br/> | 只要群組不包含任何其他網域本機群組，就可以轉換成通用範圍。<br/>                                              | 在相同的網域中。<br/>                                          | 來自相同網域的其他網域本機群組。<br/> 位於相同網域之電腦上的本機群組，但不包括具有已知 Sid 的內建組。<br/>                                             |



 

 

