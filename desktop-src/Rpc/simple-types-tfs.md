---
title: 簡單型別
description: 所有的簡單類型都會以單一格式字元表示，並以其名稱表示類型。
ms.assetid: 77c293a1-70c4-4825-bb2e-de36e01d3abb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afe123ca7c06a0522a139dc0cca8a9e24d1d585d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674696"
---
# <a name="simple-types"></a>簡單型別

所有的簡單類型都會以單一格式字元表示，並以其名稱表示類型。 這包括所有數數值型別和一些其他特殊的 IDL 類型。 清單如下所示：

``` syntax
FC_BYTE,                    // 0x01
FC_CHAR,                    // 0x02
FC_SMALL,                   // 0x03
FC_USMALL,                  // 0x04
FC_WCHAR,                   // 0x05
FC_SHORT,                   // 0x06
FC_USHORT,                  // 0x07
FC_LONG,                    // 0x08
FC_ULONG,                   // 0x09
FC_FLOAT,                   // 0x0a
FC_HYPER,                   // 0x0b
FC_DOUBLE,                  // 0x0c
FC_ENUM16,                  // 0x0d
FC_ENUM32,                  // 0x0e
FC_ERROR_STATUS_T,          // 0x10
FC_INT3264,                 // 0xb8
FC_UINT3264,                // 0xb9
```

SMALL、WCHAR、HYPER-V、ERROR \_ STATUS \_ T、 \_ \_ INT3264 類型是具有特殊 RPC 解讀的 MIDL 內建函式。 INT 和 INT32 型別會對應至 fc 的 \_ \_ \_ LONG、不帶正負號 INT 和不帶正負號的 \_ \_ int32 對應至 fc \_ ULONG、INT64 和不帶正負號的 \_ \_ \_ \_ INT64 對應至 fc \_ 超

\_ \_ 不支援 INT128、FLOAT128 和 FLOAT80 類型。

 

 




