---
description: 您可以使用 IX500DistinguishedName 介面，從辨別名稱字串建立主體名稱。
ms.assetid: 78fbf15a-678f-4d87-a309-e70374e3ecee
title: 建立主體名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00a7350268c4b7fe5f0d6bde0630bfa7556bc8dd6085e11261456299b725dd57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119670208"
---
# <a name="creating-a-subject-name"></a>建立主體名稱

您可以使用 [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) 介面，從辨別名稱字串建立主體名稱。 字串是由 (RDNs) 的串連相對辨別名稱所組成。 憑證註冊 API 支援下列 RDN 金鑰。

| 答案                               | OID                                             | 描述                                                                                        |
|-----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------|
| C<br/>                      | XCN \_ OID \_ 國家/地區 \_ 名稱<br/>              | 包含兩個字母的 ISO 3166 國家或地區碼。<br/>                                  |
| CN<br/>                     | XCN \_ OID \_ 一般 \_ 名稱<br/>               | 包含一般名稱。<br/>                                                                 |
| E<br/> 電子郵件<br/>     | XCN \_ OID \_ RSA \_ emailAddr<br/>             | 包含電子郵件地址。<br/>                                                              |
| DC<br/>                     | XCN \_ OID \_ 網域 \_ 元件<br/>          | 包含網域名稱系統 (DNS) 名稱的其中一個部分。<br/>                                   |
| G<br/> GivenName<br/> | XCN \_ \_ 指定 \_ 名稱的 OID<br/>                | 包含個人名稱中不是姓氏的部分。<br/>                             |
| I<br/>                      | XCN \_ OID \_ 縮寫<br/>                   | 包含人員的縮寫。<br/>                                                           |
| L<br/>                      | XCN \_ OID \_ 位置 \_ 名稱<br/>             | 包含識別城市、國家/地區或其他地理區域的位置名稱。<br/> |
| O<br/>                      | XCN \_ OID \_ 組織 \_ 名稱<br/>         | 包含組織的名稱。<br/>                                                   |
| OU<br/>                     | XCN \_ OID \_ 組織 \_ 單位 \_ 名稱<br/> | 包含組織內單位細分的名稱。<br/>                         |
| S<br/> ST<br/>        | XCN \_ OID \_ 州名 \_ 或 \_ 省份 \_ 名稱<br/>  | 包含州或省的完整名稱。<br/>                                          |
| STREET<br/>                 | XCN \_ OID \_ 街道 \_ 位址<br/>            | 包含實體位址。<br/>                                                          |
| SN<br/>                     | XCN \_ OID \_ SUR \_ 名稱<br/>                  | 包含人員的系列名稱。<br/>                                                   |
| T<br/> TITLE<br/>     | XCN \_ OID \_ 標題<br/>                      | 包含組織中人員的標題。<br/>                                     |



 

當您初始化 [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) 物件時，您可以藉由指定 [**X500NameFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) 列舉型別中的值，來識別辨別名稱的格式。 例如，假設主體辨別名稱是由下列 RDNs 所組成：<dl> CN = 系統管理員  
CN = Users  
DC = jdomcsc  
DC = nttest  
DC = microsoft  
DC = com  
</dl>

如果您將這些 RDNs 串連成下列以逗號分隔的辨別名稱字串，您可以在初始化 [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname)物件時，指定 **XCN \_ CERT \_ name \_ STR \_ 逗點 \_ 旗** 標值。

``` syntax
CN=Administrator,CN=Users,DC=jdomcsc,DC=nttest,DC=microsoft,DC=com
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[編碼主體名稱](encoding-a-subject-name.md)
</dt> <dt>

[主體名稱](subject-names.md)
</dt> </dl>

 

 




