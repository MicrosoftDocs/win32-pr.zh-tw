---
title: RPC 等位
description: 封裝和 nonencapsulated 等位及其格式搭配遠端程序呼叫， (RPC) 。
ms.assetid: de13151a-f4a4-4440-b287-454df4a1e3e1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e5948a0557ea968a385324244d569d3578ec5d6c0dec4af5261866ed3ba2dc8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011016"
---
# <a name="rpc-unions"></a>RPC 等位

封裝和 nonencapsulated 等位都會共用通用聯集 \_ arm \_ 選取器<> 格式：

``` syntax
union_arms<2>
arm1_case_value<4> offset_to_arm_description<2>
..
armN_case_value<4> offset_to_arm_description<2>
default_arm_description<2>
```

Union \_ arm<2> 欄位包含兩個部分。 如果等位是 MIDL 1.0 樣式聯集，則上層4位會包含與最大對齊 arm) 的聯集 arm (對齊。 否則，上層4位為零。 較低的12個位包含聯集內的 arm 數目。 換句話說：

``` syntax
alignment<highest nibble> arm_counter<three lower nibbles>
```

\_ \_ Arm \_ 描述<2> 欄位包含 arm 型別描述的相對帶正負號位移。 不過，此欄位會使用簡單類型的優化進行多載。 在這些情況下，此位移欄位的上層位元組是 FC \_ 魔術 \_ UNION \_ byte (0x80) ，而 short 的下限是 arm 的實際格式字元類型。 因此，位移值有兩個範圍：「80 *xx*」表示 *xx* 是一種類型格式字串;以及範圍內的其他內容 (80 FF。 7f FF) 表示實際的位移。 這會從範圍 <80 00 進行位移。 80 FF > 無法作為位移。 編譯器會檢查是否有 MIDL 版本5.1.164。

預設 arm \_ \_ 描述<2> 欄位表示預設 arm 的聯集 arm 類型（如果有的話）。 如果沒有為聯集指定預設 arm，則預設 \_ arm \_ 描述<2> 欄位為0xffff，如果參數的 \_ 值與任何 arm 案例值不符，則會引發例外狀況。 如果指定了預設 arm，但卻是空的，則預設的 \_ arm \_ 描述<2> 欄位為零。 否則，預設的 \_ arm \_ 描述<2> 欄位與 \_ arm 描述的位移 \_ \_<2> 欄位具有相同的語義。

以下是摘要：

-   0-空的預設值
-   FFFF-沒有預設值
-   80xx-簡單類型
-   其他相對位移

## <a name="encapsulated-unions"></a>封裝聯集

封裝聯集是來自 IDL 中的特殊聯集語法。 實際上，封裝的等位是一種組合結構，其中的判別欄位位於結構的開頭，而聯集則是唯一的另一個成員。

``` syntax
FC_ENCAPSULATED_UNION switch_type<1> 
memory_size<2>
union_arm_selector<>
```

封裝聯集的參數 \_ 類型<1> 欄位有兩個部分。 較低的半值會提供實際的 switch 型別，而上半個位元組會提供不進入的記憶體增量，也就是記憶體指標必須遞增以跳過 switch \_ 為欄位的數量，其中包含切換 \_ 為存根架構結構的 () 欄位和實際聯集欄位之間的任何填補。

記憶體 \_ 大小<2> 欄位為聯集的大小，與 nonencapsulated 聯集相同。 若要取得包含聯集之結構的總大小，請將記憶體 \_ 大小<2> 增加至記憶體增量，也就是切換類型<1> 欄位的上半部半形， \_ 然後對齊相對於增量的對齊方式。

## <a name="nonencapsulated-unions"></a>Nonencapsulated 聯集

Nonencapsulated 聯集是一般情況，其中 union 是一個引數或欄位，而參數分別是另一個引數或欄位。

``` syntax
FC_NON_ENCAPSULATED_UNION switch_type<1> 
switch_is_description<>
offset_to_size_and_arm_description<2>
```

其中：

參數 \_ 類型<1> 欄位是判別的格式字元。

參數 \_ 是 \_ 描述項<> 欄位是相互關聯描述項，而且有4或6個位元組，視是否使用 [**/robust**](/windows/desktop/Midl/-robust) 而定。 不過，針對參數的 \_ \_ 描述<>，如果等位內嵌在結構中，參數的位移欄位 \_ 就是 \_ 描述<> 是 \_ 從結構中聯集位置的欄位 (而不是從結構) 的開頭。

[大小] 和 [arm 描述] 的 [位移] \_ \_ \_ \_ \_<2> 欄位提供聯集大小和 arm 描述的位移，這與封裝聯集的大小和 arm 描述完全相同，而且會由相同類型的所有 nonencapsulated 聯集共用：

``` syntax
memory_size<2> 
union_arm_selector<>
```

 

 