---
title: Transmit_as 和 Represent_as
description: 傳送 \_ as 和表示為共用相同的版面配置，但不含 \_ 前置的權杖; 權杖 \_ \_ 會以或 fc 表示的 fc 傳輸 \_ \_ ，但基礎程式碼很常見。
ms.assetid: 70fbb4bf-0892-4c26-9790-9fc21ff8c0dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69267741536314c3e30e2270e7be61edfdb5caff
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933280"
---
# <a name="transmit_as-and-represent_as"></a>傳送 \_ as 和表示 \_ 為

傳送 \_ as 和表示為共用相同的版面配置，但不含 \_ 前置的權杖; 權杖 \_ \_ 會以或 fc 表示的 fc 傳輸 \_ \_ ，但基礎程式碼很常見。

描述具有下列版面配置：

``` syntax
FC_TRANSMIT_AS | FC_REPRESENT_AS
flags<1>
quintuple_index<2>
presented_type_memory_size<2>
transmitted_type_buffer_size<2>
transmitted_type_offset<2>
```

旗標<1> 位元組包含上方旗標半形和較低的對齊半形。

對齊的半項會保持傳輸類型的連線對齊。 當緩衝區調整大小，並使用來自格式代碼的傳輸類型時，就需要這項功能。

旗標半位元組可以有下列旗標：

``` syntax
#define PRESENTED_TYPE_IS_ARRAY     0x10
#define PRESENTED_TYPE_ALIGN_4      0x20
#define PRESENTED_TYPE_ALIGN_8      0x40
```

顯示的 \_ 類型 \_ 是 \_ 陣列旗標，會將頂層傳輸標示為 (，或表示為) 引數，其為某個事物的陣列並以傳值方式傳遞。 [**– Oi**](/windows/desktop/Midl/-oi)解譯器會使用此旗標來跳過這類引數 (這實際上是堆疊上的指標，而不是陣列) 。 另外兩個旗標也只能用在先前的解譯器中，以正確地在堆疊上的呈現型別上執行。

Quintuple \_ 索引<2> 是回呼常式 quintuple 的索引 (這實際上是四個函式) 。 此資料表通用於傳送 as 和表示為，而且會有明顯的對應來表示常式的位置，因為相同的進入點服務會以和表示為程式碼的方式傳輸。 對應是從 \_ local => 到 \_ xmit、 \_ local => from \_ xmit、free \_ inst => free \_ xmit、free \_ local => free \_ inst。

顯示的 \_ 類型 \_ 記憶體 \_ 大小<2> 一律會提供顯示/區欄位型別的大小，包括未知的表示為類型。

傳輸的 \_ 類型 \_ 緩衝區 \_ 大小<2> 為零、大小變化或實際固定大小。 這是可在調整緩衝區大小時略過某些回呼的優化。

傳輸的 \_ 類型 \_ 位移<2> 是傳輸類型格式字串的一般相對類型位移。

 

 