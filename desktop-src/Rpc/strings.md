---
title: " (RPC) 的字串屬性"
description: '\ 字串 \ 屬性和遠端程序呼叫 (RPC) 。'
ms.assetid: 794e03f2-b1e9-42dc-8536-9ced5c0e3dad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e413c0b3b8f5a379dc3448f07aed4a5a7a6aba07
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933515"
---
# <a name="string-attribute-rpc"></a> (RPC) 的字串屬性

\[[字串](/windows/desktop/Midl/string) \] 屬性指出參數是 [char](/windows/desktop/Midl/char-idl)、 [byte](/windows/desktop/Midl/byte)或 **w \_ 字元** 類型陣列的指標。 如同符合標準的陣列，會在執行時間決定 **\[ 字串 \]** 參數的大小。 與符合標準的陣列不同的是，開發人員不需要提供與陣列相關聯的長度，而 **\[ \] 字串** 屬性會藉由呼叫 **strlen**，告訴存根判斷陣列的大小。 當 **\[ \]** \[ [長度 \_ 為](/windows/desktop/Midl/length-is) \] 或 \[ [最後一個 \_ 是](/windows/desktop/Midl/last-is)屬性時，不能同時使用字串屬性 \] 。

**\[ 在中，字串 \]** 屬性組合會指示存根只將字串從用戶端傳遞至伺服器。 伺服器上配置的記憶體數量與傳送的字串大小加1。

\[ [Out](/windows/desktop/Midl/out-idl)、 **string** \] 屬性會導向存根，只將字串從伺服器傳遞至用戶端。 C 語言堅持的呼叫方式設計，所有 **\[ out \]** 參數都必須是指標。

**\[ Out \]** 參數必須是指標，且根據預設，所有指標參數都是參考指標。 參考指標在呼叫期間不會變更，它會指向與呼叫之前相同的記憶體。 針對字串指標，參考指標的其他條件約束表示用戶端必須在進行遠端程序呼叫之前配置足夠的有效記憶體。 存根會將 **\[ out、string \]** 屬性指出的字串傳送至已在用戶端上配置的記憶體中。

下列主題描述字串的遠端過程參數原型：

-   [\[in、out、string \] 原型](-in-out-string-prototype.md)
-   [\[在、字串 \] 和 \[ 輸出中，字串 \] 原型](-in-string-and-out-string-prototype.md)

 

 