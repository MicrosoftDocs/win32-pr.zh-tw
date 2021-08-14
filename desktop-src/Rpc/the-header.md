---
title: 標頭
description: 下列標頭代表可由最新版本的 MIDL 產生的其中一個標頭樣式。 為了方便起見，這裡提供標頭欄位的完整清單。
ms.assetid: 2078d2d9-1757-4449-9cc1-a21804654722
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b27ee00425f3611234b0cd001f254b1499a0d4873d05846c65a2828c3eeffe57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924537"
---
# <a name="the-header"></a>標頭

下列標頭代表可由最新版本的 MIDL 產生的其中一個標頭樣式。 為了方便起見，這裡提供標頭欄位的完整清單。

 ([**– Oif**](/windows/desktop/Midl/-oi) 標頭) 

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

從 Windows 2000 開始的延伸模組： <8> 32 位，<12> 64 位) 

``` syntax
extension_version<1>
INTERPRETER_OPT_FLAGS2<1>
ClientCorrHint<2>
ServerCorrHint<2>
NotifyIndex<2>
[ FloatDoubleMask<2> ]
```

擴充功能 \_ 版本<1> 提供延伸模組區段的大小（以位元組為單位）。 這麼做可讓目前的 NDR 引擎正確地進入擴充區段，即使該區段的編譯器版本比目前引擎所瞭解的還多。

解譯器 \_ 選擇 \_ FLAGS2 的定義如下：

``` syntax
typedef struct
  {
  unsigned char   HasNewCorrDesc      : 1;    // 0x01
  unsigned char   ClientCorrCheck     : 1;    // 0x02
  unsigned char   ServerCorrCheck     : 1;    // 0x04
  unsigned char   HasNotify           : 1;    // 0x08
  unsigned char   HasNotify2          : 1;    // 0x10
  unsigned char   Unused              : 3;
  } INTERPRETER_OPT_FLAGS2, *PINTERPRETER_OPT_FLAGS2;
```

**HasNewCorrDesc** 成員會指出是否要在編譯器所產生的格式字串中使用新的相互關聯描述項。 新的相互關聯描述項與拒絕攻擊的功能有關。 當常式需要指定端的相互關聯檢查時，會設定 **ClientCorrCheck** 和 **ServerCorrCheck** 成員。

**HasNotify** 和 **HasNotify2** 旗標表示常式會分別使用 **[通知] 和 [ \[ \]** 通知] **\[ \_ 旗 \]** 標屬性所定義的通知功能。

**ClientCorrCheck** 成員是用戶端上的快取大小提示，而 **ServerCorrCheck** 是伺服器端的提示。 當大小以零形式出現時，應使用預設大小。

**NotifyIndex** 元素是通知常式的索引（如果使用的話）。

**FloatDoubleMask** 元素可解決64位 Windows 的浮點引數問題。 只有64位的存根才會產生此欄位。 從虛擬堆疊下載/上傳登錄的元件常式需要遮罩，以處理浮點引數並正確註冊。 遮罩包含每個引數2位，或，而不是每個浮點暫存器。 編碼方式如下：最不重要的位會對應至第一個 FP 暫存器，接下來的2個位對應至第二個暫存器，依此類推。

> [!Note]  
> 針對物件常式，第一個引數會在第二個登錄中結束，因為這個指標是第一個。 針對每個註冊，bits 的意義如下表所示。

 



| Bits | 意義                                          |
|------|--------------------------------------------------|
| 01   | 必須將 float 值載入暫存器。  |
| 10   | 雙精度浮點數應該載入暫存器。 |



 

00和11是不正確位值。

Intel 架構64位處理器目前有八個 FP 暫存器，因此遮罩只能設定16b 最低的位。 遮罩大小已根據未變更的 C 編譯器遮罩，設定為總共16個位。

## <a name="header-streamlining-for-performance"></a>針對效能簡化的標頭

為了簡化程式碼並改善效能，編譯器會嘗試盡可能產生固定大小標頭。 尤其是，非同步 DCOM 會使用下列標頭：

``` syntax
typedef struct _NDR_DCOM_OI2_PROC_HEADER
  {
  unsigned char               HandleType;        // The Oi header
  INTERPRETER_FLAGS           OldOiFlags;        //
  unsigned short              RpcFlagsLow;       //
  unsigned short              RpcFlagsHi;        //
  unsigned short              ProcNum;           //
  unsigned short              StackSize;         //
  // expl handle descr is never generated        //
  unsigned short              ClientBufferSize;  // The Oi2 header
  unsigned short              ServerBufferSize;  //
  INTERPRETER_OPT_FLAGS       Oi2Flags;          //
  unsigned char               NumberParams;      //
  } NDR_DCOM_OI2_PROC_HEADER, *PNDR_DCOM_OI2_PROC_HEADER;
```

 

 