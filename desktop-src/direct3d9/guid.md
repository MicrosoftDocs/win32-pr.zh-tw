---
description: 定義可以在其他範本中使用的 GUID。
ms.assetid: dbfdd307-310f-4c80-b4aa-f16a81a9a372
title: " (DirectX 9) 的 Guid"
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e83e45d6e993153cf293a2ad55080c74f2e6049d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510019"
---
# <a name="guid-directx-9"></a> (DirectX 9) 的 Guid

定義可以在其他範本中使用的 GUID。

``` syntax
template Guid
{
    < a42790e0-7810-11cf-8f52-0040333594a3 >
    DWORD data1;
    WORD data2;
    WORD data3;
    array UCHAR data4[8];
} 
```

這些參數會形成 GUID 的二進位儲存格式：

-   data1-32-位不帶正負號整數資料值
-   data2-16 位不帶正負號整數資料值
-   data3-16 位不帶正負號整數資料值
-   data4-不帶正負號字元的陣列

## <a name="see-also"></a>另請參閱

<dl> <dt>

[範本](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



