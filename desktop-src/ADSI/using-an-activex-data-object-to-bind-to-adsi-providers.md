---
title: 使用 ActiveX 資料物件系結至 ADSI 提供者
description: 因為 ADSI 也是 OLE DB 的提供者，所以您可以使用 ActiveX Data 物件 (ADO) 來連接至 ADSI 提供者。
ms.assetid: b42d804b-f1eb-4085-88aa-015a92309ee8
ms.tgt_platform: multiple
keywords:
- ActiveX 資料物件 ADSI
- ActiveX data object ADSI，使用 ADO 系結至 ADSI 提供者
- 服務提供者 ADSI，使用 ActiveX 資料物件系結至
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4efb64da28d5c4c2596fcf889e3b3db88b77205c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020781"
---
# <a name="using-an-activex-data-object-to-bind-to-adsi-providers"></a>使用 ActiveX 資料物件系結至 ADSI 提供者

因為 ADSI 也是 OLE DB 的提供者，所以您可以使用 ActiveX Data 物件 (ADO) 來連接至 ADSI 提供者。 與其他 ADO 提供者一樣，若要連接到 OLE DB 提供者，您必須建立新的連線物件，並選擇性地指定認證。 ADSI OLE DB 提供者的名稱是 **ADsDSOObject**。

例如：


```VB
Dim con As New Connection 
'VBScript use: con = CreateObject("ADODB.Connection")
con.Provider = "ADsDSOObject"
con.Open "YourDescriptionHere"
```



在先前的範例中，您會代表目前的使用者進行連接。 若要指定不同的認證，請使用連接屬性：


```VB
con.Provider = "ADsDSOObject"
con.Properties("User ID") = "jeffsmith"
con.Properties("Password") = "guesswhat?"
con.Properties("Encrypt Password") = True
con.Open "YourDescriptionHere"
```



ADSI OLE DB 定義下列連接屬性。



| 屬性           | 資料類型   | 預設   |
|--------------------|-------------|-----------|
| 「使用者識別碼」          | **BSTR**    | **NULL**  |
| "Password"         | **BSTR**    | **NULL**  |
| 「加密密碼」 | **布林** | **FALSE** |
| "ADSI 旗標"        | **Long**    | 0         |



 

使用 OLE DB ADO 時，您無法系結至特定的物件。 不過，您可以查詢特定物件並取回結果集。 只有支援 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch) 的 ADSI 提供者才能讓 ADO 成為程式設計模型。

ADSI 旗標屬性是用來指定系結驗證選項。 這個屬性可以是來自 [**ADS \_ 驗證 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_authentication_enum) 列舉的旗標組合。

 

 




