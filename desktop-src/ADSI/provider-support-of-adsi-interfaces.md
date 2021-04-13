---
title: ADSI 介面的提供者支援
description: 下表列出適用于 Windows 2000 和 DS 用戶端的 ADSI 提供者所支援之介面的簡短描述。
ms.assetid: 8eb9a88c-cf18-4fe4-b256-1d6fcaf96c62
ms.tgt_platform: multiple
keywords:
- Adsi 介面 ADSI 介面的提供者支援
- ADSI ADSI、服務提供者、每個提供者所支援的介面
- IADsUser 的提供者支援
- IADsComputer 的提供者支援
- IADsComputerOperations 的提供者支援
- IADsDomain 的提供者支援
- IADsFileService 的提供者支援
- IADsGroup 的提供者支援
- 得到 iadsclass 的提供者支援
- IADsProperty 的提供者支援
- IADsSyntax 的提供者支援
- IADsContainer 的提供者支援
- IADsNamespaces 的提供者支援
- IADsAccessControlEntry 的提供者支援
- IADsAccessControlList 的提供者支援
- IADsSecurityDescriptor 的提供者支援
- IADsObjectOptions 的提供者支援
- IADsCollection 的提供者支援
- IADsMembers 的提供者支援
- IADsPathname 的提供者支援
- IADsPrintQueue 的提供者支援
- IADsPrintQueueOperations 的提供者支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf12803929d96a61aac6603be2c528084c91693c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300075"
---
# <a name="provider-support-of-adsi-interfaces"></a>ADSI 介面的提供者支援

下表列出適用于 Windows 2000 和 DS 用戶端的 ADSI 提供者所支援之介面的簡短描述。 標示為 "Yes" 的專案表示至少有一個指定提供者的 ADSI 物件支援相關聯的介面。 「否」表示提供者的物件不支援此版本中的介面。 未來，系統提供的提供者可能會支援目前不支援的介面。

如需有關 ADSI 提供者特定的執行詳細資料的詳細資訊，請參閱：

-   [ADSI LDAP 提供者](adsi-ldap-provider.md)
-   [ADSI WinNT 提供者](adsi-winnt-provider.md)
-   [ADSI 路由器](adsi-router.md)

如需每個介面所支援之屬性或方法的詳細資訊，請在資料表的第一個資料行中，按一下適當的介面名稱。



| 介面名稱                                                 | LDAP | WinNT |
|----------------------------------------------------------------|------|-------|
| [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)                                           | 是  | 是   |
| [**IADsAccessControlEntry**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)       | 是  | 否    |
| [**IADsAccessControlList**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)         | 是  | 否    |
| [**IADsAcl**](/windows/desktop/api/Iads/nn-iads-iadsacl)                                     | 否   | 否    |
| [**IADsBackLink**](/windows/desktop/api/Iads/nn-iads-iadsbacklink)                           | 否   | 否    |
| [**IADsCaseIgnoreList**](/windows/desktop/api/Iads/nn-iads-iadscaseignorelist)               | 否   | 否    |
| [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)                                 | 是  | 是   |
| [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection)                       | 否   | 是   |
| [**IADsComputer**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                           | 否   | 是   |
| [**IADsComputerOperations**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)       | 否   | 是   |
| [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)                         | 是  | 是   |
| [**IADsDeleteOps**](/windows/desktop/api/Iads/nn-iads-iadsdeleteops)                         | 是  | 否    |
| [**IADsDomain**](/windows/desktop/api/Iads/nn-iads-iadsdomain)                               | 否   | 是   |
| [**IADsEmail**](/windows/desktop/api/Iads/nn-iads-iadsemail)                                 | 否   | 否    |
| [**IADsExtension**](/windows/desktop/api/Iads/nn-iads-iadsextension)                         | 是  | 是   |
| [**IADsFaxNumber**](/windows/desktop/api/Iads/nn-iads-iadsfaxnumber)                         | 否   | 否    |
| [**IADsFileService**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)                     | 否   | 是   |
| [**IADsFileServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsfileserviceoperations) | 否   | 是   |
| [**IADsFileShare**](/windows/desktop/api/Iads/nn-iads-iadsfileshare)                         | 否   | 是   |
| [**IADsGroup**](/windows/desktop/api/Iads/nn-iads-iadsgroup)                                 | 是  | 是   |
| [**IADsHold**](/windows/desktop/api/Iads/nn-iads-iadshold)                                   | 否   | 否    |
| [**IADsLargeInteger**](/windows/desktop/api/Iads/nn-iads-iadslargeinteger)                   | 是  | 否    |
| [**IADsLocality**](/windows/desktop/api/Iads/nn-iads-iadslocality)                           | 是  | 否    |
| [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                             | 是  | 是   |
| [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces)                       | 是  | 是   |
| [**IADsNetAddress**](/windows/desktop/api/Iads/nn-iads-iadsnetaddress)                       | 否   | 否    |
| [**IADsO**](/windows/desktop/api/Iads/nn-iads-iadso)                                         | 是  | 否    |
| [**IADsObjectOptions**](/windows/desktop/api/Iads/nn-iads-iadsobjectoptions)                 | 是  | 否    |
| [**IADsOctetList**](/windows/desktop/api/Iads/nn-iads-iadsoctetlist)                         | 否   | 否    |
| [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)                   | 是  | 是   |
| [**IADsOU**](/windows/desktop/api/Iads/nn-iads-iadsou)                                       | 是  | 否    |
| [**IADsPath**](/windows/desktop/api/Iads/nn-iads-iadspath)                                   | 否   | 否    |
| [**IADsPathName**](/windows/desktop/api/Iads/nn-iads-iadspathname)                           | 是  | 是   |
| [**IADsPostalAddress**](/windows/desktop/api/Iads/nn-iads-iadspostaladdress)                 | 否   | 否    |
| [**IADsPrintJob**](/windows/desktop/api/Iads/nn-iads-iadsprintjob)                           | 否   | 是   |
| [**IADsPrintJobOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintjoboperations)       | 否   | 是   |
| [**IADsPrintQueue**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)                       | 是  | 是   |
| [**IADsPrintQueueOperations**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)   | 是  | 是   |
| [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)                           | 是  | 是   |
| [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)                 | 是  | 是   |
| [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)                   | 是  | 是   |
| [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)                 | 是  | 是   |
| [**IADsPropertyValue2**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue2)               | 是  | 是   |
| [**IADsReplicaPointer**](/windows/desktop/api/Iads/nn-iads-iadsreplicapointer)               | 否   | 否    |
| [**IADsResource**](/windows/desktop/api/Iads/nn-iads-iadsresource)                           | 否   | 是   |
| [**IADsSecurityDescriptor**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)       | 是  | 否    |
| [**IADsService**](/windows/desktop/api/Iads/nn-iads-iadsservice)                             | 否   | 是   |
| [**IADsServiceOperations**](/windows/desktop/api/Iads/nn-iads-iadsserviceoperations)         | 否   | 是   |
| [**IADsSession**](/windows/desktop/api/Iads/nn-iads-iadssession)                             | 否   | 是   |
| [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)                               | 是  | 是   |
| [**IADsTimestamp**](/windows/desktop/api/Iads/nn-iads-iadstimestamp)                         | 否   | 否    |
| [**IADsTypedName**](/windows/desktop/api/Iads/nn-iads-iadstypedname)                         | 否   | 否    |
| [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser)                                   | 是  | 是   |
| [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)                   | 是  | 否    |
| [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)                   | 是  | 否    |



 

## <a name="provider-support-for-iadsuser"></a>IADsUser 的提供者支援



| 屬性                                                    | LDAP          | WinNT         |
|-------------------------------------------------------------|---------------|---------------|
| [**AccountDisabled**](iadsuser-property-methods.md)        | 支援     | 支援     |
| [**Iadsuser.accountexpirationdate**](iadsuser-property-methods.md)  | 支援     | 支援     |
| [**BadLoginAddress**](iadsuser-property-methods.md)        | 不支援   | 不支援 |
| [**BadLoginCount**](iadsuser-property-methods.md)          | 支援     | 支援     |
| [**部門**](iadsuser-property-methods.md)             | 支援     | 不支援   |
| [**描述**](iadsuser-property-methods.md)            | 支援     | 支援     |
| [**部門**](iadsuser-property-methods.md)               | 支援     | 不支援   |
| [**EmailAddress**](iadsuser-property-methods.md)           | 支援     | 不支援   |
| [**EmployeeID**](iadsuser-property-methods.md)             | 支援     | 不支援   |
| [**FaxNumber**](iadsuser-property-methods.md)              | 支援     | 不支援   |
| [**名字**](iadsuser-property-methods.md)              | 支援     | 不支援   |
| [**FullName**](iadsuser-property-methods.md)               | 支援     | 支援     |
| [**GraceLoginsAllowed**](iadsuser-property-methods.md)     | 不支援 | 不支援   |
| [**GraceLoginsRemaining**](iadsuser-property-methods.md)   | 不支援 | 不支援   |
| [**HomeDirectory**](iadsuser-property-methods.md)          | 支援     | 支援     |
| [**網頁**](iadsuser-property-methods.md)               | 支援     | 不支援   |
| [**IsAccountLocked**](iadsuser-property-methods.md)        | 支援     | 支援     |
| [**語言**](iadsuser-property-methods.md)              | 不支援 | 不支援   |
| [**LastFailedLogin**](iadsuser-property-methods.md)        | 支援     | 不支援   |
| [**LastLogin**](iadsuser-property-methods.md)              | 支援     | 支援     |
| [**LastLogoff**](iadsuser-property-methods.md)             | 支援     | 支援     |
| [**姓氏**](iadsuser-property-methods.md)               | 支援     | 不支援   |
| [**LoginHours**](iadsuser-property-methods.md)             | 支援     | 支援     |
| [**LoginScript**](iadsuser-property-methods.md)            | 支援     | 支援     |
| [**LoginWorkstations**](iadsuser-property-methods.md)      | 支援     | 支援     |
| [**經理**](iadsuser-property-methods.md)                | 支援     | 不支援   |
| [**MaxLogins**](iadsuser-property-methods.md)              | 不支援   | 不支援   |
| [**MaxStorage**](iadsuser-property-methods.md)             | 支援     | 支援     |
| [**NamePrefix**](iadsuser-property-methods.md)             | 支援     | 不支援   |
| [**>namesuffix**](iadsuser-property-methods.md)             | 支援     | 不支援   |
| [**OfficeLocations**](iadsuser-property-methods.md)        | 支援     | 不支援   |
| [**OtherName**](iadsuser-property-methods.md)              | 支援     | 不支援   |
| [**PasswordExpirationDate**](iadsuser-property-methods.md) | 不支援   | 支援     |
| [**PasswordLastChanged**](iadsuser-property-methods.md)    | 支援     | 不支援   |
| [**PasswordMinimumLength**](iadsuser-property-methods.md)  | 不支援   | 支援     |
| [**PasswordRequired**](iadsuser-property-methods.md)       | 支援     | 支援     |
| [**Picture**](iadsuser-property-methods.md)                | 支援     | 不支援   |
| [**PostalAddresses**](iadsuser-property-methods.md)        | 支援     | 不支援   |
| [**PostalCodes**](iadsuser-property-methods.md)            | 支援     | 不支援   |
| [**設定檔**](iadsuser-property-methods.md)                | 支援     | 支援     |
| [**RequireUniquePassword**](iadsuser-property-methods.md)  | 不支援   | 不支援   |
| [**SeeAlso**](iadsuser-property-methods.md)                | 支援     | 不支援   |
| [**TelephoneHome**](iadsuser-property-methods.md)          | 支援     | 不支援   |
| [**TelephoneMobile**](iadsuser-property-methods.md)        | 支援     | 不支援   |
| [**TelephoneNumber**](iadsuser-property-methods.md)        | 支援     | 不支援   |
| [**TelephonePager**](iadsuser-property-methods.md)         | 支援     | 不支援   |
| [**標題**](iadsuser-property-methods.md)                  | 支援     | 不支援   |



 

## <a name="provider-support-for-iadscomputer"></a>IADsComputer 的提供者支援



| 屬性                                     | LDAP                    | WinNT       |
|------------------------------------------------|-------------------------|-------------|
| [**ComputerID**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | 不支援的介面 | 不支援 |
| [**部門**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | 不支援的介面 | 不支援 |
| [**描述**](/windows/desktop/api/Iads/nn-iads-iadscomputer)            | 不支援的介面 | 不支援 |
| [**部門**](/windows/desktop/api/Iads/nn-iads-iadscomputer)               | 不支援的介面 | 支援   |
| [**Location**](/windows/desktop/api/Iads/nn-iads-iadscomputer)               | 不支援的介面 | 不支援 |
| [**MemorySize**](/windows/desktop/api/Iads/nn-iads-iadscomputer)             | 不支援的介面 | 不支援 |
| [**型號**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                  | 不支援的介面 | 不支援 |
| [**NetAddresses**](/windows/desktop/api/Iads/nn-iads-iadscomputer)           | 不支援的介面 | 不支援 |
| [**OperatingSystem**](/windows/desktop/api/Iads/nn-iads-iadscomputer)        | 不支援的介面 | 支援   |
| [**OperatingSystemVersion**](/windows/desktop/api/Iads/nn-iads-iadscomputer) | 不支援的介面 | 支援   |
| [**擁有者**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                  | 不支援的介面 | 支援   |
| [**PrimaryUser**](/windows/desktop/api/Iads/nn-iads-iadscomputer)            | 不支援的介面 | 不支援 |
| [**處理器**](/windows/desktop/api/Iads/nn-iads-iadscomputer)              | 不支援的介面 | 支援   |
| [**ProcessorCount**](/windows/desktop/api/Iads/nn-iads-iadscomputer)         | 不支援的介面 | 支援   |
| [**角色**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                   | 不支援的介面 | 不支援 |
| [**網站**](/windows/desktop/api/Iads/nn-iads-iadscomputer)                   | 不支援的介面 | 不支援 |
| [**StorageCapacity**](/windows/desktop/api/Iads/nn-iads-iadscomputer)        | 不支援的介面 | 不支援 |



 

## <a name="provider-support-for-iadscomputeroperations"></a>IADsComputerOperations 的提供者支援



| 屬性                                   | LDAP                    | WinNT           |
|--------------------------------------------|-------------------------|-----------------|
| [**關閉**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations) | 不支援的介面 | 未實作 |
| [**狀態**](/windows/desktop/api/Iads/nn-iads-iadscomputeroperations)   | 不支援的介面 | 未實作 |



 

## <a name="provider-support-for-iadsdomain"></a>IADsDomain 的提供者支援



| 屬性                                         | LDAP                    | WinNT           |
|--------------------------------------------------|-------------------------|-----------------|
| [**IsWorkgroup**](/windows/desktop/api/Iads/nn-iads-iadsdomain)                | 不支援的介面 | 未實作 |
| [**MinPasswordLength**](/windows/desktop/api/Iads/nn-iads-iadsdomain)          | 不支援的介面 | 支援       |
| [**MinPasswordAge**](/windows/desktop/api/Iads/nn-iads-iadsdomain)             | 不支援的介面 | 支援       |
| [**MaxpasswordAge**](/windows/desktop/api/Iads/nn-iads-iadsdomain)             | 不支援的介面 | 支援       |
| [**MaxBadPasswordsAllowed**](/windows/desktop/api/Iads/nn-iads-iadsdomain)     | 不支援的介面 | 支援       |
| [**Msds-passwordhistorylength**](/windows/desktop/api/Iads/nn-iads-iadsdomain)      | 不支援的介面 | 支援       |
| [**PasswordAttributes**](/windows/desktop/api/Iads/nn-iads-iadsdomain)         | 不支援的介面 | 不支援     |
| [**AutoUnlockInterval**](/windows/desktop/api/Iads/nn-iads-iadsdomain)         | 不支援的介面 | 支援       |
| [**LockoutObservationInterval**](/windows/desktop/api/Iads/nn-iads-iadsdomain) | 不支援的介面 | 支援       |



 

## <a name="provider-support-for-iadsfileservice"></a>IADsFileService 的提供者支援



| 屬性                                | LDAP                    | WinNT     |
|-----------------------------------------|-------------------------|-----------|
| [**描述**](/windows/desktop/api/Iads/nn-iads-iadsfileservice)  | 不支援的介面 | 支援 |
| [**MaxUserCount**](/windows/desktop/api/Iads/nn-iads-iadsfileservice) | 不支援的介面 | 支援 |



 

## <a name="provider-support-for-iadsgroup"></a>IADsGroup 的提供者支援



| 屬性                         | LDAP      | WinNT     |
|----------------------------------|-----------|-----------|
| [**描述**](/windows/desktop/api/Iads/nn-iads-iadsgroup) | 支援 | 支援 |



 

## <a name="provider-support-for-iadsclass"></a>得到 iadsclass 的提供者支援



| 屬性                                   | LDAP               | WinNT           |
|--------------------------------------------|--------------------|-----------------|
| [**PrimaryInterface**](/windows/desktop/api/Iads/nn-iads-iadsclass)      | 支援          | 支援       |
| [**Clsid**](/windows/desktop/api/Iads/nn-iads-iadsclass)                 | 支援          | 支援       |
| [**老**](/windows/desktop/api/Iads/nn-iads-iadsclass)                   | 支援          | 支援       |
| [**摘要**](/windows/desktop/api/Iads/nn-iads-iadsclass)              | 支援          | 支援       |
| [**輔助**](/windows/desktop/api/Iads/nn-iads-iadsclass)             | 支援          | 支援       |
| [**MandatoryProperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)   | 支援          | 支援       |
| [**OptionalProperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)    | 支援          | 支援       |
| [**NamingProperties**](/windows/desktop/api/Iads/nn-iads-iadsclass)      | 支援          | 未實作 |
| [**DerivedFrom**](/windows/desktop/api/Iads/nn-iads-iadsclass)           | 支援          | 不支援     |
| [**AuxDerivedFrom**](/windows/desktop/api/Iads/nn-iads-iadsclass)        | 支援          | 不支援     |
| [**PossibleSuperiors**](/windows/desktop/api/Iads/nn-iads-iadsclass)     | 支援          | 支援       |
| [**遏制**](/windows/desktop/api/Iads/nn-iads-iadsclass)           | 支援讀取 | 支援       |
| [**容器**](/windows/desktop/api/Iads/nn-iads-iadsclass)             | 支援讀取 | 支援       |
| [**HelpFileName**](/windows/desktop/api/Iads/nn-iads-iadsclass)          | 支援          | 支援       |
| [**HelpFileCoNtext**](/windows/desktop/api/Iads/nn-iads-iadsclass)       | 支援          | 支援       |
| 方法                                     | LDAP               | WinNT           |
| [**限定詞**](/windows/desktop/api/Iads/nf-iads-iadsclass-qualifiers) | 未實作    | 未實作 |



 

## <a name="provider-support-for-iadsproperty"></a>IADsProperty 的提供者支援



| 屬性                            | LDAP      | WinNT     |
|-------------------------------------|-----------|-----------|
| [**老**](/windows/desktop/api/Iads/nn-iads-iadsproperty)         | 支援 | 支援 |
| [**Syntax**](/windows/desktop/api/Iads/nn-iads-iadsproperty)      | 支援 | 支援 |
| [**MaxRange**](/windows/desktop/api/Iads/nn-iads-iadsproperty)    | 支援 | 支援 |
| [**MinRange**](/windows/desktop/api/Iads/nn-iads-iadsproperty)    | 支援 | 支援 |
| [**多**](/windows/desktop/api/Iads/nn-iads-iadsproperty) | 支援 | 支援 |



 

## <a name="provider-support-for-iadssyntax"></a>IADsSyntax 的提供者支援



| 屬性                              | LDAP      | WinNT     |
|---------------------------------------|-----------|-----------|
| [**OleAutoDataType**](/windows/desktop/api/Iads/nn-iads-iadssyntax) | 支援 | 支援 |



 

## <a name="provider-support-for-iadscontainer"></a>IADsContainer 的提供者支援



| 屬性                        | LDAP            | WinNT           |
|---------------------------------|-----------------|-----------------|
| [**計數**](/windows/desktop/api/Iads/nn-iads-iadscontainer)  | 未實作 | 未實作 |
| [**提示**](/windows/desktop/api/Iads/nn-iads-iadscontainer)  | 支援       | 未實作 |
| [**篩選**](/windows/desktop/api/Iads/nn-iads-iadscontainer) | 支援       | 支援       |



 

## <a name="provider-support-for-iadsnamespaces"></a>IADsNamespaces 的提供者支援



| 屬性                                   | LDAP      | WinNT     |
|--------------------------------------------|-----------|-----------|
| [**defaultContainer**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) | 支援 | 支援 |



 

## <a name="provider-support-for-iadsaccesscontrolentry"></a>IADsAccessControlEntry 的提供者支援



| 屬性                                              | LDAP      | WinNT       |
|-------------------------------------------------------|-----------|-------------|
| [**AccessMask**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | 支援 | 不支援 |
| [**AccessType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | 支援 | 不支援 |
| [**AccessFlags**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)         | 支援 | 不支援 |
| [**標誌**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)               | 支援 | 不支援 |
| [**ObjectType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)          | 支援 | 不支援 |
| [**InheritedObjectType**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry) | 支援 | 不支援 |
| [**受託 人**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrolentry)             | 支援 | 不支援 |



 

## <a name="provider-support-for-iadsaccesscontrollist"></a>IADsAccessControlList 的提供者支援



| 屬性                                                       | LDAP      | WinNT       |
|----------------------------------------------------------------|-----------|-------------|
| [**AceCount**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                      | 支援 | 不支援 |
| [**AceRevision**](/windows/desktop/api/Iads/nn-iads-iadsaccesscontrollist)                   | 支援 | 不支援 |
| 方法                                                         | LDAP      | WinNT       |
| [**AddAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-addace)                 | 支援 | 不支援 |
| [**CopyAccessList**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-copyaccesslist) | 支援 | 不支援 |
| [**RemoveAce**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-removeace)           | 支援 | 不支援 |
| [**取得 \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsaccesscontrollist-get__newenum)   | 支援 | 不支援 |



 

## <a name="provider-support-for-iadssecuritydescriptor"></a>IADsSecurityDescriptor 的提供者支援



| 屬性                                                                        | LDAP      | WinNT       |
|---------------------------------------------------------------------------------|-----------|-------------|
| [**控制**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                       | 支援 | 不支援 |
| [**DaclDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                 | 支援 | 不支援 |
| [**Objdescriptor.discretionaryacl**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                              | 支援 | 不支援 |
| [**Group**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                         | 支援 | 不支援 |
| [**GroupDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                | 支援 | 不支援 |
| [**擁有者**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                         | 支援 | 不支援 |
| [**OwnerDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                | 支援 | 不支援 |
| [**SaclDefaulted**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                 | 支援 | 不支援 |
| [**SystemAcl**](/windows/desktop/api/Iads/nn-iads-iadssecuritydescriptor)                                     | 支援 | 不支援 |
| 方法                                                                          | LDAP      | WinNT       |
| [**CopySecurityDescriptor**](/windows/desktop/api/Iads/nf-iads-iadssecuritydescriptor-copysecuritydescriptor) | 支援 | 不支援 |



 

## <a name="provider-support-for-iadsobjectoptions"></a>IADsObjectOptions 的提供者支援



| 方法                                           | LDAP      | WinNT                   |
|--------------------------------------------------|-----------|-------------------------|
| [**GetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-getoption) | 支援 | 不支援的介面 |
| [**SetOption**](/windows/desktop/api/Iads/nf-iads-iadsobjectoptions-setoption) | 支援 | 不支援的介面 |



 

## <a name="provider-support-for-iadscollection"></a>IADsCollection 的提供者支援



| 方法                                                | LDAP                    | WinNT       |
|-------------------------------------------------------|-------------------------|-------------|
| [**加入**](/windows/desktop/api/Iads/nf-iads-iadscollection-add)                     | 不支援的介面 | 不支援 |
| [**取得 \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadscollection-get__newenum) | 不支援的介面 | 支援   |
| [**GetObject**](/windows/desktop/api/Iads/nf-iads-iadscollection-getobject)         | 不支援的介面 | 支援   |
| [**移除**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove)               | 不支援的介面 | 支援   |



 

## <a name="provider-support-for-iadsmembers"></a>IADsMembers 的提供者支援



| 屬性                                           | LDAP                                                      | WinNT       |
|----------------------------------------------------|-----------------------------------------------------------|-------------|
| [**計數**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                       | 支援 GroupCollection，但不適用於 UserCollection | 不支援 |
| [**篩選**](/windows/desktop/api/Iads/nn-iads-iadsmembers)                      | 支援                                                 | 支援   |
| 方法                                             | LDAP                                                      | WinNT       |
| [**取得 \_ \_ NewEnum**](/windows/desktop/api/Iads/nf-iads-iadsmembers-get__newenum) | 支援                                                 | 支援   |



 

## <a name="provider-support-for-iadspathname"></a>IADsPathname 的提供者支援



| 屬性                                                    | LDAP      | WinNT       |
|-------------------------------------------------------------|-----------|-------------|
| [**EscapedMode**](/windows/desktop/api/Iads/nn-iads-iadspathname)                         | 支援 | 支援   |
| 方法                                                      | LDAP      | WinNT       |
| [**設定**](/windows/desktop/api/Iads/nf-iads-iadspathname-set)                             | 支援 | 支援   |
| [**SetDisplayType**](/windows/desktop/api/Iads/nf-iads-iadspathname-setdisplaytype)       | 支援 | 支援   |
| [**擷取**](/windows/desktop/api/Iads/nf-iads-iadspathname-retrieve)                   | 支援 | 支援   |
| [**GetNumElements**](/windows/desktop/api/Iads/nf-iads-iadspathname-getnumelements)       | 支援 | 支援   |
| [**GetElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-getelement)               | 支援 | 支援   |
| [**GetEscapedElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-getescapedelement) | 支援 | 不支援 |
| [**RemoveLeafElement**](/windows/desktop/api/Iads/nf-iads-iadspathname-removeleafelement) | 支援 | 支援   |
| [**CopyPath**](/windows/desktop/api/Iads/nf-iads-iadspathname-copypath)                   | 支援 | 支援   |



 

## <a name="provider-support-for-iadsprintqueue"></a>IADsPrintQueue 的提供者支援



| 屬性                                     | LDAP        | WinNT       |
|----------------------------------------------|-------------|-------------|
| [**PrinterPath**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)        | 支援   | 不支援 |
| [**型號**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)              | 支援   | 支援。  |
| [**資料類型**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | 不支援 | 支援   |
| [**PrintProcessor**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)     | 不支援 | 支援   |
| [**描述**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)        | 支援   | 支援   |
| [**Location**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | 支援   | 支援   |
| [**StartTime**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)          | 支援   | 支援   |
| [**UntilTime**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)          | 支援   | 支援   |
| [**DefaultJobPriority**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue) | 不支援 | 支援   |
| [**優先順序**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)           | 支援   | 支援   |
| [**BannerPage**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)         | 支援   | 支援   |
| [**PrintDevices**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)       | 支援   | 支援   |
| [**NetAddresses**](/windows/desktop/api/Iads/nn-iads-iadsprintqueue)       | 不支援 | 不支援 |



 

## <a name="provider-support-for-iadsprintqueueoperations"></a>IADsPrintQueueOperations 的提供者支援



| 屬性                                                | LDAP      | WinNT      |
|---------------------------------------------------------|-----------|------------|
| [**狀態**](/windows/desktop/api/Iads/nn-iads-iadsprintqueueoperations)              | 支援 | 支援  |
| 方法                                                  | LDAP      | WinNT      |
| [**暫停**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-pause)         | 支援 | 支援。 |
| [**PrintJobs**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-printjobs) | 支援 | 支援  |
| [**清除**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-purge)         | 支援 | 支援  |
| [**繼續**](/windows/desktop/api/Iads/nf-iads-iadsprintqueueoperations-resume)       | 支援 | 支援  |



 

 

 




