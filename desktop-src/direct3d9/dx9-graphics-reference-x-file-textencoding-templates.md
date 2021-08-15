---
description: 範本會定義資料串流的轉譯方式-資料是由範本定義來進行。 本節將討論範本的下列各方面，並提供範例範本。
ms.assetid: f84978a8-8315-4626-be68-f00f3a72e5ac
title: '範本 (X 檔案格式，文字編碼) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a719278893c771818df029e13b2d7221c6ca0ccdcb0869b9966a737793981176
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119373508"
---
# <a name="templates-x-file-format-text-encoding"></a>範本 (X 檔案格式，文字編碼) 

範本會定義資料串流的轉譯方式-資料是由範本定義來進行。 本節將討論範本的下列各方面，並提供範例範本。

有一個特殊範本-標頭範本。 建議每個應用程式定義標頭範本，並用它來定義應用程式特定的資訊，例如版本資訊。 如果有此標頭，則會使用. x 檔案格式 API 來讀取此標頭。 如果有旗標成員可用，則會使用它來判斷如何解讀下列資料。 旗標成員（如果已定義）應該是 DWORD。 目前已定義一個位-位0。 如果清除此位，則檔案中的下列資料為二進位。 如果設定，則下列資料是文字。 您可以使用多個標頭資料物件在檔案內的二進位和文字之間切換。

## <a name="template-form-name-and-uuid"></a>範本表單、名稱和 UUID

範本的格式如下。


```
template <template-name> {
<UUID>
    <member 1>;
...
    <member n>;
[restrictions]
}
```



範本名稱是英數位元名稱，可 () 包含底線字元 \_ 。 不得以數位開頭。 UUID 是一種通用的唯一識別碼，格式化為開放式 Software Foundation 的分散式運算環境標準，並以角括弧括住 (< >) 。 例如： <3D82AB43-62DA-11cf-AB39-0020AF71E433>。

## <a name="template-members"></a>範本成員

範本成員包含名為資料類型，後面接著選擇性名稱或命名資料類型的陣列。 有效的基本資料類型定義于下表中。



| 類型    | 大小                               |
|---------|------------------------------------|
| WORD    | 16 位元                            |
| DWORD   | 32 位元                            |
| FLOAT   | IEEE float                         |
| DOUBLE  | 64 位元                            |
| CHAR    | 8 位元                             |
| UCHAR   | 8 位元                             |
| BYTE    | 8 位元                             |
| STRING  | 以 Null 結束的字串             |
| CSTRING |  (不支援格式化的 C 字串)  |
| UNICODE | 不支援 Unicode 字串 ()      |



 

您也可以在範本定義中參考其他先前在資料流程中遇到的範本所定義的資料類型。 不允許向前參考。

任何有效的資料類型都可以表示為範本定義中的陣列。 下列範例顯示基本語法。


```
array <data-type> <name>[<dimension-size>];
```



<維度大小> 可以是整數，也可以是另一個樣板成員的命名參考，而該成員的值會被取代。 陣列可以是 n 維，其中 n 是由結尾的成對方括弧數目所決定，如下列範例所示。


```
array DWORD FixedHerd[24];
array DWORD Herd[nCows];
array FLOAT Matrix4x4[4][4];
```



## <a name="template-restrictions"></a>範本限制

範本可以是開啟、關閉或限制的。 這些限制會決定哪些資料類型可以出現在範本所定義之資料物件的直屬階層中。 開啟的範本沒有任何限制，關閉的範本會拒絕所有的資料類型，且受限制的範本允許資料類型的名稱清單。

指出開啟範本的語法是以方括弧括住的三個句點。


```
[ ... ]
```



以逗號分隔的已命名資料類型清單，並以方括弧括住的 Uuid （以方括弧括住）表示受限的範本。


```
[ { data-type [ UUID ] , } ... ]
```



上述任一項都沒有指出已關閉的範本。

## <a name="template-example"></a>範本範例

以下顯示範例範本。


```
template Mesh {
<3D82AB44-62DA-11cf-AB39-0020AF71E433>
DWORD nVertices;
array Vector vertices[nVertices];
DWORD nFaces;
array MeshFace faces[nFaces];
 [ ... ]                // An open template
}
template Vector {
<3D82AB5E-62DA-11cf-AB39-0020AF71E433>
FLOAT x;
FLOAT y;
FLOAT z;
}                        // A closed template
template FileSystem {
<UUID>
STRING name;
[ Directory <UUID>, File <UUID> ]    // A restricted template
}
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[文字編碼方式](text-encoding.md)
</dt> </dl>

 

 



