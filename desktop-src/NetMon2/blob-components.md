---
description: BLOB 元件
ms.assetid: 757cd311-f834-4017-a0da-ff3f4bc49e7e
title: BLOB 元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bfdb9c1f336ad0cddc1798cc98083890096dd39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193918"
---
# <a name="blob-components"></a>BLOB 元件

二進位大型物件 (BLOB) 包含下列階層式元件：

-   擁有者
-   類別
-   標籤
-   值

## <a name="textual-representation"></a>文字標記法

為了方便起見，Blob 會在儲存至檔案時出現在「擁有者：類別：標記：值」格式中。 BLOB 的內部結構是不透明的，因為它代表指標和資料表。 例如，以下是可用於設定 NPP 的 BLOB 專案：

``` syntax
NPP:Configure:BufferSize=32768
```

擁有者為 NPP。 此類別為 [設定]，標記為 [BufferSize]，而值為32768。

 

 



