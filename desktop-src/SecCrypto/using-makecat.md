---
description: 製作未簽署的類別目錄檔案，其中包含一組檔案的雜湊，以及集合中每個檔案的相關聯屬性。 類別目錄檔案可讓使用者 (目錄簽署一個檔案) ，而不是簽署許多個別的檔案。
ms.assetid: 0a6ce2cd-db1f-4b47-990c-36fa87c28a60
title: 使用 MakeCat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e36c83531df38b95bde03edd719d98be325dbeac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974958"
---
# <a name="using-makecat"></a>使用 MakeCat

[MakeCat](makecat.md)工具會建立未簽署的類別目錄檔案，其中包含一組檔案的 [*雜湊*](../secgloss/h-gly.md)，以及集合中每個檔案的相關聯屬性。 類別目錄檔案可讓使用者 (目錄簽署一個檔案) ，而不是簽署許多個別的檔案。

簽署並傳輸未簽署的類別目錄檔案之後，接收者可以比較原始檔案的雜湊與目錄檔案中包含的雜湊，並確認檔案不會受到篡改。

在使用 [MakeCat](makecat.md) 工具之前，使用者必須使用任何文字編輯器來準備目錄定義檔 ( 的 cdf) 。 此 cdf 檔案包含檔案清單以及要編目之檔案的屬性 (下列) 所列的規格。 MakeCat 工具會掃描 cdf 檔案、確認每個所列出檔案的屬性清單、將列出的屬性新增至目錄本身、將每個列出的檔案雜湊，然後將每個檔案的雜湊儲存至類別目錄檔案。 每個檔案的雜湊和屬性分別儲存在目錄內。 然後可以簽署和傳送此類別目錄檔案。 接收者接著可以將目錄中每個檔案的雜湊與原始檔案的雜湊進行比較，以證明原始內容完全不會受到篡改。 MakeCat 不會修改 cdf 檔。

下列範例會使用 [MakeCat](makecat.md) 命令。

-   從檔案的副檔名產生類別目錄檔案。

    **MakeCat-v 不錯的 cdf**

檔案（cdf）會剖析 UnsignedPE.exe、UnsignedDOS.exe、Unsigned.cab、不帶 SignedPE.exe 正負號的檔案，藉以產生類別目錄檔案 Good.cat。 經過剖析的檔案以及良好的 cdf 和新產生的 Good.cat，全都在相同的目錄中。

``` syntax
[CatalogHeader]
Name=Good.cat
ResultDir=.\
PublicVersion=0x00000001
EncodingType=
CATATTR1=0x10010001:Movie1:FirstMovie
CATATTR2=0x10010001:Movie2:SecondMovie
CATATTR3=0x10010001:Movie3:ThirdMovie

[CatalogFiles]
UnsignedPE=.\UnsignedPE.EXE
UnsignedDOS=.\UnsignedDOS.EXE
<HASH>UnsignedCAB=.\Unsigned.CAB
UnsignedClass=.\Unsigned.Class
SignedPE=.\SignedPE.EXE
```

> [!Note]  
> 專案中的最後一個專案必須在行尾必須有明確的分行符號。

 

 

 
