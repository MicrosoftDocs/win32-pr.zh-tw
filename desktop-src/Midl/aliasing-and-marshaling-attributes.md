---
title: 別名和封送處理屬性
description: 分散式應用程式在呼叫介面程式時，幾乎一律會在用戶端和伺服器程式之間傳遞資料。
ms.assetid: 64895c64-f16b-47c4-928d-5149808b0476
keywords:
- IDL MIDL、屬性 MIDL、別名和封送處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68ac66aa04210a878c67ee6bcf1a50ff21fa1d1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022029"
---
# <a name="aliasing-and-marshaling-attributes"></a>別名和封送處理屬性

分散式應用程式在呼叫介面程式時，幾乎一律會在用戶端和伺服器程式之間傳遞資料。 開發人員會使用 MIDL 來描述用戶端和伺服器程式以標準方式傳遞的資料。 MIDL 編譯器會針對用戶端和伺服器建立應用程式 stub 或 proxy，以將資料轉換成可透過網路傳送的標準化格式。 這種格式（ (NDR) 格式的網路資料表示）通常稱為資料的電傳格式。 存根必須將其原生格式的資料從程式的記憶體空間轉換成 NDR。 這項轉換稱為封送處理資料。 當用戶端或伺服器程式接收資料時，它必須將該程式的資料從 NDR 轉換成原生格式。 這稱為將資料解除封送。

使用別名和封送處理屬性來控制如何將資料封裝成 NDR 格式，並透過網路傳輸。



| 屬性                             | 使用方式                                                                                                                         |
|---------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [**呼叫 \_ as**](call-as.md)           | 將不可遠端處理函數對應至遠端程序呼叫。                                                                      |
| [**iid \_ 為**](iid-is.md)             | 提供 COM 介面的介面識別碼，該介面是指標的物件。                                     |
| [**傳輸 \_ 為**](transmit-as.md)   | 將資料類型轉換成更簡單的類型，以便透過網路傳輸。                                                       |
| [**網路 \_ 封送處理**](wire-marshal.md) | 類似于 [**傳送 \_ as**](transmit-as.md) ，但您會執行常式來調整大小、封送處理、unmarshal 和釋放資料。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[類型轉換和封送處理 ACF 屬性](type-conversion-and-marshaling-acf-attributes.md)
</dt> </dl>

 

 




