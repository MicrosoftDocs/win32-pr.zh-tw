---
title: 系結字串
description: 由於可從目錄服務存取的物件數目，因此可能會發生命名衝突。
ms.assetid: b4c44b19-d7b6-4dde-b44c-4a49cecbacf2
ms.tgt_platform: multiple
keywords:
- 系結字串 ADSI
- ADsPath ADSI、描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b13d2d8b58dd01713fa6382f27714b72651ad6f8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103933604"
---
# <a name="binding-string"></a>系結字串

由於可從目錄服務存取的物件數目，因此可能會發生命名衝突。 系結字串（通常稱為 ADsPath）可讓您指定特定物件，而不會造成命名衝突。 這可套用至單一目錄服務提供者，或跨多個目錄服務提供者。

ADsPath 是可唯一識別目錄服務上 ADSI 物件的字串。 由於 ADSI 物件存在於基礎目錄服務的命名空間內容中，因此 ADsPath 名稱語法的一部分是提供者特定的。

下表列出預設提供的 ADSI 提供者。



| 提供者         | 描述                                                                                                                                                     |
|------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WinNT<br/> | 用來與 Windows 網域控制站通訊。 如需 WinNT ADsPath 的詳細資訊，請參閱 [Winnt adspath](winnt-adspath.md)。<br/>           |
| LDAP<br/>  | 用來與 LDAP 伺服器通訊，例如 Active Directory。 如需有關 LDAP ADsPath 的詳細資訊，請參閱 [Ldap adspath](ldap-adspath.md)。<br/>  |
| 廣告<br/>   | 提供可用於列舉用戶端上安裝之所有 ADSI 提供者的 [**IADsNamespaces**](/windows/desktop/api/Iads/nn-iads-iadsnamespaces) 執行。<br/> |



 

使用這些提供者名稱來存取預設的提供者命名空間。 例如，如果您系結至 LDAP，ADSI 會系結至包含目前登入之網域物件的容器。 如果您系結至 WinNT，ADSI 會系結至保存與網路上所有網域相互關聯之物件的容器。

ADsPath 字串的初始元素是 ADSI 提供者 (progID) 的程式設計識別碼，後面接著 "：//"，後面接著提供者命名空間所指示的語法。 ProgID 字串可能會區分大小寫，視提供者而定。 上列提供者的 progID 字串會區分大小寫。

視提供者而定，路徑字串可能會區分大小寫。 上述提供者的路徑字串不區分大小寫。

以下是 ADsPaths 的範例。

``` syntax
LDAP://CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
LDAP://server01/CN=Jeff Smith,CN=users,DC=fabrikam,DC=com
 
WinNT://MyDomain/ComputerName,Computer
WinNT://MyDomain/UserAccount
```

若要尋找電腦上安裝的所有提供者，請系結至 ADs 提供者，如下列程式碼範例所示。


```VB
Set x = GetObject("ADs:")
For Each provider In x
    provider.Name
Next
```



使用 LDAP 提供者時，您可以在 (DN) 表單的 x.500 辨別名稱中指定 ADsPath，從 CN 標記開始，或者可以指定其階層式反向，從 O 標記開始。 您在初始 ADsPath 中使用的表單決定了標記的順序。

下表列出 ADsPath 特殊字元。



| Name                      | 字元           | 描述                                                                                                                                                                                           |
|---------------------------|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 雙引號<br/>   | "<br/>        | 用來括住 ADsPath 的任何部分，其可能包含特殊字元，因此字串會以字面方式解讀。 例如，"CN = Name/Prefix"。<br/>                                     |
| 反斜線<br/>      | \\<br/>       | 用在特殊字元之前，表示它們應該當做常值使用。 如需詳細資訊和特殊字元清單，請參閱 [分辨名稱](/previous-versions/windows/desktop/ldap/distinguished-names)。<br/> |
| 斜線<br/>          | /<br/>        | 元件分隔符號。<br/>                                                                                                                                                                       |
| 角括號<br/> | <><br/> | 在另一個命名慣例中分隔 ADsPath。<br/>                                                                                                                                       |



 

若要在搜尋規格中分隔 ADsPath 或作為 URL 的一部分，請使用左和右角括弧 (< >) 。 例如，" &lt; WinNT://MyDomain/UserAccount &gt; "。

由於命名空間需求，某些 ADSI 提供者可能已新增語法限制。

## <a name="active-directory-binding-options"></a>Active Directory 系結選項

Active Directory 可讓您使用數種其他類型的系結字串系結至物件，例如 COM 全域唯一識別碼 (GUID) 或 (SID) 的安全識別碼。 如需詳細資訊，請參閱系結 [至 Active Directory](/windows/desktop/AD/binding-to-active-directory-domain-services)。

 

