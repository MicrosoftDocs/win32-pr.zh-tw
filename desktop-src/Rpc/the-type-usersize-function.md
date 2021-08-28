---
title: Type_UserSize 函式
description: 型 \_ 別 UserSize 函式是 \ 網路 \_ 封送處理 \ 和 \ 使用者 \_ 封送處理 \ 屬性的 helper 函數。
ms.assetid: 74a46418-1a02-47ed-a3ab-35f3364cc38f
keywords:
- type_UserSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2f997d12e11f643eb2faf9990454a8508d15636
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886049"
---
# <a name="the-type_usersize-function"></a>型別 \_ UserSize 函式

**&lt; 型別 &gt; \_ UserSize** 函式是適用于 \[ [有線 \_ 封送](/windows/desktop/Midl/wire-marshal)處理 \] 和 \[ [使用者 \_ 封送](/windows/desktop/Midl/user-marshal)處理屬性的 helper 函數 \] 。 在用戶端或伺服器端將資料封送處理之前，存根會呼叫這個函式來調整使用者資料物件的 RPC 資料緩衝區大小。 函式定義如下：

``` syntax
unsigned long __RPC_USER  <type>_UserSize(
    unsigned long __RPC_FAR * pFlags,
    unsigned long StartingSize,
    <type>  __RPC_FAR *pMyObj);
```

函 &lt; &gt; 式名稱中的型別代表 userm 類型，如「 **\[ 有線 \_ 封 \] 送** 處理」或「 **\[ 使用者 \_ 封送 \]** 處理」類型定義中所指定。 這種類型在與 **\[ 使用者 \_ 封送 \]** 處理屬性（attribute）搭配使用時，可能是 UNTRANSMITTABLE 或甚至是： MIDL 編譯器的未知。 網路類型名稱 (在網路) 傳輸的類型名稱，不會用在函式原型中。 不過，請注意，網路類型會定義憑證 DCE 所指定之資料的版面配置。 所有資料都必須轉換成 (NDR) 格式的網路資料標記法。

*PFlags* 參數是不 **帶正負** 號的長旗標欄位的指標。 旗標的上半部包含憑證 DCE 針對浮點數、位元組順序和字元標記法所定義的 NDR 格式旗標。 下方的單字包含由 COM 通道所定義的封送處理內容旗標。 下表會顯示欄位內旗標的確切版面配置。



| Bits  | 旗標                                  | 值                                                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------|
| 31-24 | 浮點數標記法         | 0 = IEEE 1 = VAX 2 = Cray 3 = IBM                                                         |
| 23-20 | 整數和浮點位元組順序 | 0 = 位元組由大到小的 1 = 位元組由小到大                                                          |
| 19-16 | 字元標記法              | 0 = ASCII 1 = EBCDIC                                                                      |
| 15-0  | 封送處理內容旗標               | 0 = MSHCTX \_ LOCAL 1 = MSHCTX \_ NOSHAREDMEM 2 = MSHCTX \_ DIFFERENTMACHINE 3 = MSHCTX \_ INPROC |



 

封送處理內容旗標可讓您根據 RPC 呼叫的內容改變常式的行為。 比方說，如果您有一個控制碼 (**長**) 至資料區塊，您可以傳送同進程呼叫的控制碼，但您會將呼叫的實際資料傳送給不同的電腦。 封送處理內容旗標及其值會定義在平臺軟體發展工具組 (SDK) 的 Wtypes.h .h 和 Wtypes.h .idl 檔案中。

> [!Note]  
> 正確定義網路類型時，您不需要使用 NDR 格式旗標，因為 NDR 引擎會執行必要的轉換。

 

*StartingSize* 參數是目前的緩衝區位移。 起始大小表示使用者物件的緩衝區位移，且可能會正確對齊。 您的常式應考慮需要什麼填補。

*PMyObj* 參數是使用者類型物件的指標。

傳回值是新的位移或緩衝區位置。 函數應該會傳回累計大小，也就是開始大小加上可能的填補加上資料大小。

**&lt; 型別 &gt; \_ UserSize** 函式可以傳回所需大小的高估值。 傳送緩衝區的實際大小是由資料大小所定義，而不是由緩衝區配置大小所定義。

如果可以在編譯時期計算網路大小，則不會呼叫 **&lt; 類型 &gt; \_ UserSize** 函式。 請注意，對於大部分的等位，即使沒有指標，也只能在執行時間決定網路標記法的實際大小。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[封送處理使用者 \_ 封送處理和網路封送處理的規則 \_](marshaling-rules-for-user-marshal-and-wire-marshal.md)
</dt> <dt>

[使用者 \_ 封送處理](/windows/desktop/Midl/user-marshal)
</dt> <dt>

[網路 \_ 封送處理](/windows/desktop/Midl/wire-marshal)
</dt> </dl>

 

 
