---
title: 命名空間
description: 位於指定命名空間內的物件是由唯一名稱所識別。
ms.assetid: d42b4b18-d38f-4071-8e3e-9b9b71d46d4b
ms.tgt_platform: multiple
keywords:
- 命名空間 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d416782f2a96ca716f6e803ad9d0b4200c82cff6ad0ad033751a89a5d2c8af1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117839377"
---
# <a name="namespaces"></a>命名空間

位於指定命名空間內的物件是由唯一名稱所識別。 例如，儲存在電腦磁片磁碟機上的檔案位於檔案系統命名空間中。 檔案的唯一名稱是以檔案系統命名空間中儲存的位置為基礎。 例如：


```C++
C:\public\documents\adsi\adsi_spec.doc
```



目錄服務命名空間也會以唯一的名稱來識別它們所包含的物件，這些物件通常是以可找到物件的目錄中的位置為基礎。 例如，在 X-y 目錄中，指定的物件可能會有如下的名稱：


```C++
CN=John,OU=Marketing,O=Fabrikam
```



不同的目錄服務會使用不同的格式來命名其所包含的物件。 這會處理不同的命名空間，特別是針對開發人員，考慮程式碼可能正在執行的所有不同環境。

Active Directory 服務介面 (ADSI) 的目標是要提供命名架構，以允許存取不同目錄服務提供者的命名空間。

ADSI 定義可以在異類環境中唯一識別物件的命名慣例。 這些名稱稱為 ADsPath 字串。 ADsPath 字串採用數種形式：


```C++
"ADs://"
 
"LDAP://"
 
"WinNT://"
```



其他的 ADsPath 格式可由不同的 adsi 提供者引進 (例如 Internet Information Services server 的 ADSI 提供者，它支援 "IIS://" ADsPaths) 。

 

 




