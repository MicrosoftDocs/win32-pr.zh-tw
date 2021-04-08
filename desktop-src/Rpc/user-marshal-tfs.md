---
title: 使用者封送處理
description: 遠端程序呼叫中的使用者封送處理 (RPC) 。
ms.assetid: 5119e959-d8b8-4fca-8910-568bb9063a9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c901fd8c75137b4657322a89692ff8a3afb5408
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840024"
---
# <a name="user-marshal"></a>使用者封送處理

使用者封送處理的格式字串類似于傳輸 \_ 方式：

``` syntax
FC_USER_MARSHAL
flags<1>
quadruple_index<2>
user_type_memory_size<2>
transmitted_type_buffer size<2>
offset_to_the_transmitted_type<2>
```

旗標<1> 位元組包含上方旗標半形和較低的對齊半形。

旗標半形的上方2位可用來描述網路類型是否定義為唯一指標、參考指標或沒有指標 (不能是 ptr) 。 下列資訊清單已定義為可設定/取得旗標：

``` syntax
#define USER_MARSHAL_UNIQUE         0x80
#define USER_MARSHAL_REF            0x40
#define USER_MARSHAL_POINTER        0xc0  /* unique or ref */
#define USER_MARSHAL_IID            0x20  /* JIT compiler only */
```

旗標字組的對齊半位，可保持傳輸類型的對齊。

四 \_ 個索引<2> 是使用者封送處理函式的回呼常式最四個索引。 常式位置如下：調整、封送處理、封送處理和釋放常式。

使用者 \_ 類型 \_ 記憶體 \_ 大小<2> 提供使用者特定類型的大小，包括未知的類型。

\_ \_ \_ 當大小變化或實際的固定大小時，傳輸的類型緩衝區大小<2> 為零。 這是一項優化，可讓 MIDL 在調整緩衝區大小時略過回呼，也可在釋放時略過回呼。

## <a name="range"></a>範圍

\[範圍 \] 檢查可提供其他方法來驗證 NDR 層的引數。 \[範圍描述項的 \] 格式如下：

``` syntax
FC_RANGE,   flags_type <1>
low value<4>
high value<4>
```

旗標採用上半個位元組，而類型為第二個位元組的下半部半形。 低和高值取決於要檢查的變數類型。

旗標旨在作為擴充車輛;編譯器已將半值設定為零。

 

 




