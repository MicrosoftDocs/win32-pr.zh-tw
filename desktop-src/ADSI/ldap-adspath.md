---
title: LDAP ADsPath
description: 本主題說明您應該針對 LDAP ADsPath 使用的語法。
ms.assetid: adacf6af-8683-4c3c-91bf-9489f2d5d817
ms.tgt_platform: multiple
keywords:
- LDAP ADsPath
- ADsPath、LDAP、描述
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1850c30ff8a5a086fbd697080ac32b5e55549496739d9388a6d5e7ab251403d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839468"
---
# <a name="ldap-adspath"></a>LDAP ADsPath

Microsoft LDAP 提供者 ADsPath 需要下列格式。


```C++
LDAP://HostName[:PortNumber][/DistinguishedName]
```



> [!Note]  
> 左和右方括弧字元 (\[ \]) 表示選擇性參數，而不是系結字串的常值部分。

 

「主機名稱」可以是電腦名稱稱、IP 位址或功能變數名稱。 您也可以在系結字串中指定伺服器名稱。 大部分的 LDAP 提供者都遵循需要指定伺服器名稱的模型。

"PortNumber" 會指定要用於連接的埠。 如果未指定埠號碼，LDAP 提供者會使用預設的埠號碼。 如果使用 ssl 連線，預設的埠號碼為389（如果未使用 SSL 連線）或636（如果使用 SSL 連線）。

"DistinguishedName" 指定特定物件的分辨名稱。 指定之物件的辨別名稱一定是唯一的。

下表列出系結字串的範例。



| LDAP ADsPath 範例                                      | 描述                                                |
|-----------------------------------------------------------|------------------------------------------------------------|
| LDAP：                                                     | 系結至 LDAP 命名空間的根目錄。                    |
| LDAP://server01                                           | 系結至特定的伺服器。                                 |
| LDAP://server01:390                                       | 使用指定的埠號碼系結至特定的伺服器。 |
| LDAP：//CN = Jeff Smith，CN = users，DC = fabrikam，DC = com          | 系結至特定物件。                                 |
| LDAP://server01/CN=Jeff Smith，CN = users，DC = fabrikam，DC = com | 透過特定伺服器系結至特定物件。       |



 

如果成功完成特定目錄要求時需要 Kerberos 驗證，系結字串必須使用無伺服器 ADsPath，例如 LDAP：//CN = Jeff Smith，CN = users，DC = fabrikam，DC = com，或者必須使用具有完整 DNS 伺服器名稱的 ADsPath，例如 LDAP://server01.fabrikam.com/CN=Jeff Smith、CN = users，DC = fabrikam，DC = com。 使用一般 NETBIOS 名稱或簡短 DNS 名稱（例如，使用名稱 server01 而非 server01.fabrikam.com）系結至伺服器，並不保證會產生 Kerberos 驗證。

如需 LDAP 系結字串的詳細資訊和範例，以及可在 LDAP 系結字串中使用之特殊字元的描述，請參閱 LDAP ADsPath。

**Windows 2000 SP1 和更新版本：** 使用 LDAP 提供者時，如果系結字串包含伺服器名稱，您可以使用 **ADS \_ 伺服器 \_** 系結旗標搭配 [**ADsOpenObject**](/windows/desktop/api/Adshlp/nf-adshlp-adsopenobject)函式或 [**IADsOpenDSObject：： objdso.opendsobject**](/windows/desktop/api/Iads/nf-iads-iadsopendsobject-opendsobject)方法來提高效能。 **ADS \_ 伺服器 \_** 系結旗標表示指定了伺服器名稱，可讓 ADSI 避開其他不必要的網路流量。

## <a name="ldap-special-characters"></a>LDAP 特殊字元

LDAP 有數個特殊字元，這些特殊字元已保留供 LDAP API 使用。 您可以在 [辨別名稱](/previous-versions/windows/desktop/ldap/distinguished-names)中找到特殊字元清單。 若要在 ADsPath 中使用其中一個字元，而不產生錯誤，字元前面必須加上反斜線 (\\) 字元。 這就是所謂的 *轉義* 字元。 例如，如果以 "，" 形式提供使用者名稱 <last name> <first name> ，則必須將名稱值中的逗號加上轉義。 產生的字串看起來像這樣：


```C++
LDAP://CN=Smith\,Jeff,CN=users,DC=fabrikam,DC=com
```



您也可以使用其兩位數的十六進位字元碼來指定該逸出字元。 下列範例會顯示這一點。


```C++
LDAP://CN=Smith\2CJeff,CN=users,DC=fabrikam,DC=com
```



不可列印的字元（例如換行字元和換行字元）必須由其兩位數的十六進位字元碼進行轉義和指定。 下列範例會顯示這一點。


```C++
LDAP://CN=Line\0AFeed,CN=users,DC=fabrikam,DC=com
```



## <a name="for-more-information"></a>詳細資訊

如需符合 LDAP 標準之目錄服務所使用之辨別名稱標記法的詳細資訊，請參閱 [https://www.ietf.org/rfc/rfc1779.txt](https://www.ietf.org/rfc/rfc1779.txt) 。

 

 