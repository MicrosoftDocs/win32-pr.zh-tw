---
title: 效能屬性
description: 在 IDL 檔案中使用下列屬性，以減少存根程式碼的大小或改善效能。
ms.assetid: 0f23265e-7f3e-4a15-ac3b-1d852a8110eb
keywords:
- IDL MIDL，屬性，效能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f784bc534fd1dd7f160eaccb87a2853d491237db915245d4f36823e1ceb559ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869458"
---
# <a name="performance-attributes"></a>效能屬性

在 IDL 檔案中使用下列屬性，以減少存根程式碼的大小或改善效能。



| 屬性                             | 使用方式                                                                                                                                                |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**忽略**](ignore.md)              | 指定包含在結構或等位中的指標，以及指標所指出的物件不會傳送。                        |
| [**當地**](local.md)                | 指定應用程式的本機函式，MIDL 不需要產生 stub 程式碼。                                           |
| [**網路 \_ 封送處理**](wire-marshal.md) | 將資料類型定義為透過網路傳輸的較簡單類型，並可讓您針對該類型執行封送處理和封送處理常式。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[記憶體管理 ACF 屬性](memory-management-acf-attributes.md)
</dt> <dt>

[存根優化 ACF 屬性](stub-optimization-acf-attributes.md)
</dt> </dl>

 

 




