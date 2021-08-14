---
description: 以下是兩個範例二進位範本定義和一個二進位資料物件範例。
ms.assetid: vs|directx_sdk|~\examples.htm
title: " (Direct3D 9 圖形) 範例"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f8b8e2a9c500042e9b8d7c7fd911ab74b2f428d1ef814aca9e5fda1be7dcab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523095"
---
# <a name="examples-direct3d-9-graphics"></a> (Direct3D 9 圖形) 範例

以下是兩個範例二進位範本定義和一個二進位資料物件範例。

> [!Note]  
> 資料會以位元組由小到大的格式儲存，但不會顯示在這些範例中。

 

關閉的範本 RGB 是由 UUID {55b6d780-37ec-11d0-ab39-0020af71e433} 識別，且有三個成員-r、g 和 b-每個都是 float 類型。


```
TOKEN_TEMPLATE, TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_OBRACE,
TOKEN_GUID, 55b6d780, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_FLOAT, TOKEN_NAME, 1, 'r', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'g', TOKEN_SEMICOLON,
TOKEN_FLOAT, TOKEN_NAME, 1, 'b', TOKEN_SEMICOLON,
TOKEN_CBRACE
```



封閉式範本 Matrix4x4 是由 UUID {55b6d781-37ec-11d0-ab39-0020af71e433} 識別，且有一個成員-一維陣列，名為 float 類型的矩陣。


```
TOKEN_TEMPLATE, TOKEN_NAME, 9, 'M', 'a', 't', 'r', 'i', 'x', '4', 'x', '4', TOKEN_OBRACE,
TOKEN_GUID, 55b6d781, 37ec, 11d0, ab, 39, 00, 20, af, 71, e4, 33,
TOKEN_ARRAY, TOKEN_FLOAT, TOKEN_NAME, 6, 'm', 'a', 't', 'r', 'i', 'x',
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_OBRACKET, TOKEN_INTEGER, 4, TOKEN_CBRACKET,
TOKEN_CBRACE
```



接下來的二進位資料物件會顯示稍早定義的 RGB 範本實例。 範例物件的名稱是藍色，而它的三個成員（r、g 和 b）分別具有值0.0、0.0 和1.0。


```
TOKEN_NAME, 3, 'R', 'G', 'B', TOKEN_NAME, 4, 'b', 'l', 'u', 'e', TOKEN_OBRACE,
TOKEN_FLOAT_LIST, 3, 0.0, 0.0, 1.0, TOKEN_CBRACE
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[二進位編碼方式](binary-encoding.md)
</dt> </dl>

 

 



