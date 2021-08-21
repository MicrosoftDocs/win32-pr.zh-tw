---
title: 逗點分隔值 (CSV) 腳本
description: Windows 2000 包含命令列公用程式 CSVDE，可使用 .csv 檔案匯入目錄物件，並將目錄物件匯出為 .csv 檔。
ms.assetid: fda242eb-7561-444f-b560-94bd87fe4e39
ms.tgt_platform: multiple
keywords:
- 逗點分隔值腳本廣告
- 腳本，逗點分隔值 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3764593303f7f2a81c524df16665c74afd1c83909e8286511090ee6c84323bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118022444"
---
# <a name="comma-separated-value-csv-scripts"></a>逗點分隔值 (CSV) 腳本

Windows 2000 包含命令列公用程式 CSVDE，可使用 .csv 檔案匯入目錄物件，並將目錄物件匯出為 .csv 檔。 系統會建立 CSV 腳本以方便使用。 腳本中的第一行會識別接下來各行中的屬性。 資料行是以逗號分隔。 檔案格式與 Microsoft Excel 的 .csv 格式相容，因此可以輕鬆地建立檔案。 使用 Excel 或任何其他可讀取和寫入 .csv 檔案的工具。 CSVDE 支援 Unicode。

## <a name="example-csv-file"></a>範例 CSV 檔案

下列程式碼範例是新增輔助類別的 CSV 檔案。

``` syntax
DN,adminDisplayName,cn,defaultHidingValue,defaultObjectCategory,description,governsID,lDAPDisplayName,mayContain,mustContain,distinguishedName,objectCategory,objectClass,objectClassCategory,possSuperiors,name,rDNAttID,schemaIDGUID,subClassOf,auxiliaryClass,defaultSecurityDescriptor
"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",My-Test-Auxiliary-Class1,My-Test-Auxiliary-Class1,FALSE,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=Fabrikam,DC=com",Test class used to show how to add an auxiliary class.,1.2.840.113556.1.4.7000.159.24.10.611.11,myTestAuxiliaryClass1,myTestAttributeDNString,description;myTestAttributeUnicodeString,"CN=My-Test-Auxiliary-Class1,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com","CN=Class-Schema,CN=Schema,CN=Configuration,DC=myorg,DC=mytest,DC=fabrikam,DC=com",classSchema,3,domainDNS;container,My-Test-Auxiliary-Class1,cn,X'9a6b3176c5dbd2118bd00000f875b660',top,,
```

 

 




