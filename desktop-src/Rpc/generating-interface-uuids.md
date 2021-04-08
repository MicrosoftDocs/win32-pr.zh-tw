---
title: 產生介面 Uuid
description: " (Uuid) 和使用 Uuidgen.exe 產生介面通用唯一識別碼。"
ms.assetid: a973b7f9-71c5-46a0-aa0c-51f150560dbc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68c5f727ed3e37139d4da50f84c3929bff333156
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673003"
---
# <a name="generating-interface-uuids"></a>產生介面 Uuid

本節提供 (Uuid) 的通用唯一識別碼的相關資訊，以及下列主題中的 Uuidgen.exe 公用程式：

-   [什麼是 UUID？](#what-is-a-uuid)
-   [使用 Uuidgen.exe](#using-uuidgen)

## <a name="what-is-a-uuid"></a>什麼是 UUID？

所有介面都必須在網路上唯一識別，讓用戶端可以找到它們。 在小型網路中，介面的名稱單獨可能就足以識別它。 不過，這在大型網路上通常不可行。 因此，開發人員通常會將通用唯一識別碼指派 (UUID、與詞彙 GUID 交換，或在每個介面) 全域唯一識別碼。 UUID 是包含一組十六進位數位的字串。 每個介面都有不同的 UUID。 如需詳細資訊，請參閱 [字串 UUID](string-uuid.md)。

UUID 的文字標記法是由8個十六進位數位後面接著連字號的字串所組成，後面接著三個以連字號分隔的4個十六進位數位，後面接著連字號和12個十六進位數位。 下列範例是有效的 UUID 字串：

ba209999-0c6c-11d2-97cf-00c04f8eea45

空白 Uuid 稱為「nil Uuid」，而不是 **Null** uuid。 Nil 一詞表示任何零、空白、空白或未初始化的值。 空字串、空的資料庫記錄或未初始化的 UUID 都是 nil 值的範例。

> [!Note]  
> **Null** 值是特定的值零。 它通常用於 C 和 c + + 程式設計中搭配指標。 Nil 是比 **Null** 更常見的詞彙。 未初始化的物件介面 Uuid 應一律稱為「nil Uuid」（而非 **Null** uuid）。

 

## <a name="using-uuidgen"></a>使用 Uuidgen.exe

Microsoft 提供一個稱為 Uuidgen.exe 的公用程式來產生您的 Uuid。 Uuidgen.exe 公用程式會以 IDL 檔案格式或 C 語言格式產生 UUID。

當您從命令列執行 Uuidgen.exe 公用程式時，您可以使用下列命令參數。



| Uuidgen.exe 參數           | Description                                                                |
|--------------------------|----------------------------------------------------------------------------|
| **/I**                   | 將 UUID 輸出至 IDL 介面範本。                                 |
| **/s**                   | 將 UUID 輸出為初始化的 C 結構。                                |
| **/o** <*檔案名*> | 將輸出重新導向至檔案;在 **/o** 參數之後立即指定。 |
| **/n** <*數位*>   | 指定要產生的 Uuid 數目。                                 |
| **/v**                   | 顯示有關 Uuidgen.exe 的版本資訊。                                |
| **/h** 或 **？**          | 顯示命令選項摘要。                                           |



 

一般而言，您會使用 Uuidgen.exe 公用程式，如下列範例所示。

**uuidgen.exe-i-oMyApp .idl**

此命令會產生 UUID，並將其儲存在可作為範本的 MIDL 檔案中。 執行上述命令時，MyApp 的內容如下所示：

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface INTERFACENAME
{

}
```

下一步是使用您介面的實際名稱來取代預留位置名稱介面名稱。

 

 




