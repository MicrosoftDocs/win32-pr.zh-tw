---
title: 建立使用者
description: 若要在 Active Directory Domain Services 中建立使用者，請在您要放置使用者之網域的網域容器中建立使用者物件。
ms.assetid: fb51895f-71e1-45b6-b8bc-ed674e822734
ms.tgt_platform: multiple
keywords:
- Active Directory 範例 Active Directory，建立使用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3422d269351ae29fd15d12585ca02b91a4b9c23
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469225"
---
# <a name="creating-a-user"></a>建立使用者

若要在 Active Directory Domain Services 中建立使用者，請在您要放置使用者之網域的網域容器中建立使用者物件。 您可以在網域的根目錄、組織單位內或在容器內建立使用者。

當您建立使用者物件時，您也必須設定下表所列的屬性，將物件設定為 Active Directory Domain Services 和 Windows 安全性系統所能辨識的合法使用者。



| 屬性                                       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**快遞 之 家**](/windows/desktop/ADSchema/a-cn)                         | 指定目錄中使用者物件的名稱。 這會是物件的相對辨別名稱 (RDN) 。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) | 指定一個字串，此字串是用來支援舊版 Windows 的用戶端和伺服器的名稱。 [**SAMAccountName**](/windows/desktop/ADSchema/a-samaccountname)應小於20個字元，以支援舊版 Windows 的用戶端。<br/> [**SAMAccountName**](/windows/desktop/ADSchema/a-samaccountname)在網域內的所有安全性主體物件之間必須是唯一的。 您應該對網域執行查詢，以確認 **sAMAccountName** 在網域內是唯一的。<br/> [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) 是選擇性屬性。 如果未指定任何值，伺服器將會建立隨機的 **sAMAccountName** 值。<br/> |



 

您也可以設定其他屬性。 如果您未在建立時明確設定，則會使用預設值來設定下列使用者屬性。




| 屬性 | 描述 | 
|-----------|-------------|
| <a href="/windows/desktop/ADSchema/a-accountexpires"><strong>accountExpires</strong></a> | 指定帳戶將到期的時間。 預設值為 <strong>TIMEQ_FOREVER</strong>，表示帳戶永遠不會過期。<br /> | 
| <a href="/windows/desktop/ADSchema/a-ntsecuritydescriptor"><strong>nTSecurityDescriptor</strong></a> | 根據特定規則建立安全描述項。 如需詳細資訊，請參閱 <a href="how-security-descriptors-are-set-on-new-directory-objects.md">如何在新的目錄物件上設定安全描述項</a>。<br /> | 
| <a href="/windows/desktop/ADSchema/a-objectcategory"><strong>objectCategory</strong></a> | 指定使用者類別。 預設值為「Person」。<br /> | 
| <a href="/windows/desktop/ADSchema/a-name"><strong>名字</strong></a> | 指定使用者名稱。 預設值為 <a href="/windows/desktop/ADSchema/a-cn"><strong>cn</strong></a>的設定值。<br /> | 
| <a href="/windows/desktop/ADSchema/a-pwdlastset"><strong>pwdLastSet</strong></a> | 指定使用者上次設定密碼的時間。 預設值為零，表示使用者必須在下次登入時變更密碼。<br /> | 
| <a href="/windows/desktop/ADSchema/a-useraccountcontrol"><strong>userAccountControl</strong></a> | 包含值，這些值會決定使用者的數個登入和帳戶功能。<br /> 預設會設定下列旗標：<br /><ul><li><strong>UF_ACCOUNTDISABLE</strong> -帳戶已停用。</li><li><strong>UF_PASSWD_NOTREQD</strong> -不需要密碼。</li><li><strong>UF_NORMAL_ACCOUNT</strong> -代表一般使用者的預設帳戶類型。</li></ul> | 
| <a href="/windows/desktop/ADSchema/a-memberof"><strong>memberOf</strong></a> | 指定使用者為其直接成員的群組或群組。 預設值為「網域使用者」。<br /> | 




 

藉由系結至所需的容器，然後使用下列其中一種方法來建立使用者。 必須先設定 [**cn**](/windows/desktop/ADSchema/a-cn) 和 [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) 屬性，才能將使用者認可至伺服器。



| 方法                                                                       | 描述                                                                                                                                                                                                                                                                                                                                                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IADsContainer 建立**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)                        | [**Cn**](/windows/desktop/ADSchema/a-cn)屬性是取自 *bstrRelativeName* 參數。 必須藉由呼叫 [**IADs SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 來認可新的使用者，否則將不會建立該物件。 如需詳細資訊，請參閱 [建立使用者的範例程式碼](example-code-for-creating-a-user.md)。<br/>                                                                                            |
| [**IDirectoryObject::CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) | [**Cn**](/windows/desktop/ADSchema/a-cn)屬性是取自 *pszRDNName* 參數。 呼叫 [**CreateDSObject**](/windows/desktop/api/iads/nf-iads-idirectoryobject-createdsobject) 時，會認可新的使用者。 如需詳細資訊，請參閱 [建立使用者的範例程式碼](example-code-for-creating-a-user.md)。<br/>                                                                                                                |
| [DirectoryEntries 新增](/dotnet/api/system.directoryservices.directoryentries.add?view=dotnet-plat-ext-3.1)       | [**Cn**](/windows/desktop/ADSchema/a-cn)屬性是取自 *name* 參數。 您必須藉由呼叫 [DirectoryEntry. CommitChanges](/dotnet/api/system.directoryservices.directoryentry.commitchanges#System_DirectoryServices_DirectoryEntry_CommitChanges) 來認可新的使用者物件，否則不會建立該物件。 如需詳細資訊，請參閱 [新增目錄物件](/previous-versions/ms180851(v=vs.90))。<br/> |



 

必須先將新的使用者認可到伺服器，才能修改 [**cn**](/windows/desktop/ADSchema/a-cn) 和 [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname) 以外的任何屬性。 這是因為使用者帳戶在使用者認可之前，不會實際存在。 如果針對不存在於伺服器上的物件抓取或修改某個屬性，將會發生錯誤。 這包括呼叫 [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword) 方法。 例如，使用 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-create)建立使用者時，會遵循下列順序：

1.  呼叫 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) ，以使用指定的 [**cn**](/windows/desktop/ADSchema/a-cn)在本機快取中建立使用者。
2.  使用 [**IADs**](/windows/desktop/api/iads/nf-iads-iads-put)方法，將 [**sAMAccountName**](/windows/desktop/ADSchema/a-samaccountname)屬性設定為所需的值。
3.  現在修改其他屬性（例如 [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)）。 這種限制也適用于 ADSI 屬性，例如 [**IADsUser. AccountDisabled**](/windows/desktop/ADSI/iadsuser-property-methods)和 [**IADsUser. SetPassword**](/windows/desktop/api/iads/nf-iads-iadsuser-setpassword)之類的方法。
4.  呼叫 [**IADs SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) ，以將新的使用者認可至伺服器。

建立新的使用者帳戶時，預設會予以停用。 帳戶必須以手動方式或以程式設計方式啟用。 若要以程式設計方式啟用使用者帳戶，請從 [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol)屬性中移除 **ADS 的 \_ UF \_ ACCOUNTDISABLE** 旗標。

建立新的使用者帳戶時，帳戶的 [**userAccountControl**](/windows/desktop/ADSchema/a-useraccountcontrol) 屬性會自動設定 [ **UF PASSWD] \_ \_ NOTREQD** 旗標，這表示帳戶不需要任何密碼。 如果在中建立帳戶的網域安全性原則需要所有使用者帳戶的密碼，則必須從帳戶的 **userAccountControl** 屬性中移除 [ **UF \_ PASSWD \_ NOTREQD** ] 旗標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立使用者的範例程式碼](example-code-for-creating-a-user.md)
</dt> </dl>
