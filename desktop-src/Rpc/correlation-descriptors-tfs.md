---
title: 相互關聯描述元
description: 相互關聯描述元是一個格式字串，它會根據與另一個引數相關的一個引數來描述運算式。
ms.assetid: 9f5f5077-d6a9-4253-bddf-b8cd0c868973
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35f13f0793b99b80b7abb0b493c249b30ad53d76
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842667"
---
# <a name="correlation-descriptors"></a>相互關聯描述元

相互關聯描述元是一個格式字串，它會根據與另一個引數相關的一個引數來描述運算式。 需要相互關聯描述項，才能處理與屬性相關的語法 \[ ，例如，**大小 \_ 為 ()** \] 、 \[ **長度 \_ 為 ()** \] 、 \[ **參數 \_ ()** \] 且 \[ **iid \_ 為 ()** \] 。 相互關聯描述項會搭配陣列、大小的指標、等位和介面指標使用。 最終運算式值可以是大小、長度、聯集判別或 IID 的指標。 就格式字串而言，相互關聯描述項會搭配陣列、等位和介面指標使用。 格式字串中會將大小的指標描述為數組的指標。

有兩個執行基本運算式計算的常式： NdrpComputeConformance 用於大小、參數和 IID， \* 而 NdrpComputeVariance 則用於長度。 另外也有一個常式可以針對阻絕攻擊功能執行相互關聯值驗證。

相互關聯描述項的設計僅支援非常有限的運算式。 在複雜的情況下，編譯器會在需要時產生引擎所要呼叫的運算式評估常式。

相互關聯描述項的格式如下：

``` syntax
correlation_type<1>
correlation_operator<1>
offset<2>
[robust_flags<2>]
```

相互關聯描述項相互關聯 \_ 類型<1> 包含兩個 nibbles：上面的4個位描述可找到運算式的位置，而較低的4個位則描述運算式值的類型。

上半個位元組可以有下列五個值的其中一個：

``` syntax
00  FC_NORMAL_CONFORMANCE
10  FC_POINTER_CONFORMANCE
20  FC_TOP_LEVEL_CONFORMANCE
80  FC_TOP_LEVEL_MULTID_CONFORMANCE
40  FC_CONSTANT_CONFORMANCE
```

<dl> <dt>

<span id="FC_NORMAL_CONFORMANCE"></span><span id="fc_normal_conformance"></span>FC \_ 正常 \_ 一致性
</dt> <dd>

符合標準的標準案例，例如在結構的欄位中所述。

</dd> <dt>

<span id="FC_POINTER_CONFORMANCE"></span><span id="fc_pointer_conformance"></span>FC \_ 指標 \_ 一致性
</dt> <dd>

若為屬性化指標 (**\_ () 的大小**，則 **長度 \_ 會 ()** 為結構中欄位的) 。 這會影響基底記憶體指標的設定方式。

</dd> <dt>

<span id="FC_TOP_LEVEL_CONFORMANCE"></span><span id="fc_top_level_conformance"></span>FC \_ 最 \_ 上層 \_ 一致性
</dt> <dd>

適用于其他參數所描述的最上層一致性。

</dd> <dt>

<span id="FC_TOP_LEVEL_MULTID_CONFORMANCE"></span><span id="fc_top_level_multid_conformance"></span>FC \_ 最 \_ 上層 \_ MULTID \_ 一致性
</dt> <dd>

針對其他參數所描述之多維度陣列的最高層級一致性。

> [!Note]  
> 多維度大小的陣列和指標會觸發切換至 [**– Oicf**](/windows/desktop/Midl/-oi)。

 

</dd> <dt>

<span id="FC_CONSTANT_CONFORMANCE"></span><span id="fc_constant_conformance"></span>FC \_ 常數 \_ 一致性
</dt> <dd>

若為常數值。 編譯器會從使用者提供的常數運算式之該層值。 當發生這種情況時，一致性描述中的後續3個位元組會包含較長的3個位元組，以描述一致性大小。 不需要進一步的計算。

</dd> </dl>

較低的半值會提供需要從記憶體解壓縮的數值型別：

``` syntax
FC_LONG | FC_ULONG | 
FC_SHORT | FC_USHORT | 
FC_SMALL | FC_USMALL | 
FC_HYPER
```

> [!Note]
> 不支援64位運算式。 \_只有在64位平臺上 **\_ () IID** 才能將 iid 的指標值解壓縮時，才會使用 FC hyper-v \* 。
>
> 編譯器會在下列情況下，將類型半值設定為零：上述常數運算式以及需要呼叫評估運算式常式（例如，當 \_ 使用 fc 常數 \_ 一致性和 fc 回呼時） \_ 。

 

大小 \_ 為 \_ op<1> 欄位允許將下列其中一項作業套用至一致性變數：

``` syntax
FC_DEREFERENCE | 
FC_DIV_2 | FC_MULT_2 | FC_SUB_1 | FC_ADD_1 | 
FC_CALLBACK
```

FC 取值 \_ 常數用於相互關聯的 pointee，例如 **\[ 大小 \_ 是 (\* pL) \]**。 算術運算子只會使用指定的常數。 FC \_ 回呼常數表示需要呼叫運算式評估常式。

Offset<2> 欄位通常是運算式引數變數的相對記憶體位移。 它也可以是運算式評估–常式索引。 如本檔先前所述，針對常數運算式，它是實際的最終運算式值的一部分。

位移<2> 欄位為記憶體位移的解讀，取決於運算式的複雜度、運算式變數的位置，以及陣列的大小寫，不論陣列實際上是否為屬性化指標。

如果陣列是屬性化指標，而一致性變數是結構中的欄位，則位移欄位包含從結構開頭到符合性描述欄位的位移。 如果陣列不是屬性化指標，且一致性變數是結構中的欄位，則位移欄位包含從結構的 nonconformant 部分結尾到符合性描述欄位的位移。 一般來說，符合標準的陣列位於結構的結尾。

針對最上層的一致性，offset 欄位包含從存根的第一個參數在堆疊上的位置到描述一致性之參數的位移。 這不會用在 **–作業系統** 模式中。 位移欄位的解釋還有其他例外狀況;這些類型的描述中會說明這類例外狀況。

當 offset<2> 用於 FC 回呼時 \_ ，它會在編譯器所產生的運算式評估常式資料表中包含索引。 存根訊息會傳遞至評估常式，然後計算一致性值，並將它指派給存根訊息的 MaxCount 欄位。

已 \_ 新增 Windows 2000 的健全旗標<2> 欄位以支援 [**/robust**](/windows/desktop/Midl/-robust)，例如拒絕攻擊功能。 第一個位元組定義了下列旗標：

``` syntax
typedef  struct  _NDR_CORRELATION_FLAGS
  {
  unsigned char   Early     : 1;
  unsigned char   Split     : 1;
  unsigned char   IsIidIs   : 1;
  unsigned char   DontCheck : 1;
  unsigned char   Unused    : 4;
  } NDR_CORRELATION_FLAGS;
```

早期旗標表示早期與晚期關聯。 早期關聯性是指運算式引數在所述引數的前面，例如，size 引數是在調整大小的指標引數之前。 當運算式引數位於相關引數之後時，就會使用晚期關聯。 引擎會立即執行早期關聯值的驗證，並儲存延遲的相互關聯值，以便在封送處理完成之後檢查。

分割旗標表示 \[ 在 in \] 和 \[ out \] 引數之間進行非同步分割。 例如，大小的引數可能是 \[ ， \] 而調整大小的指標可能會 \[ 輸出 \] 。 在 DCOM 非同步內容中，這些引數會出現在不同的堆疊上，因此引擎必須知道這一點。

IsIidIs 旗標表示 **iid \_ ()** 相互關聯。 NdrComputeConformance 常式會被欺騙，以運算式值的形式取得 IID 的指標，但驗證常式無法比較這類值 (它們會是指標) ，因此旗標表示需要比較實際的 Iid。

### <a name="variance-description-and-other-array-attributes"></a>差異描述和其他陣列屬性

變異數描述欄位格式與 [一致性描述] 欄位相同。 差別在於，NDR 引擎會使用不同的存根訊息欄位作為暫存變數。 在變異數描述的案例中，這是評估的長度，而且對應的欄位稱為 ActualLength。

使用變異數時，起始位移通常為零，且引擎會據以調整。 如果 **第一個 \_ 是 ()** 屬性套用至一致的不同陣列，則會強制執行運算式評估常式的回呼。

 

 