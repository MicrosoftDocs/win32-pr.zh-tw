---
title: 'RPC (的指標) '
description: 瞭解 RPC 一般指標，其定義為介面指標和位元組計數指標以外的所有專案。
ms.assetid: 9756E637-BCBB-48F1-B962-25AF2C917921
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ade676610a310e230eb6fa89dd666996bb82040f
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119703"
---
# <a name="pointers-rpc"></a>RPC (的指標) 

## <a name="common-pointers"></a>一般指標

一般指標會定義為介面指標和位元組計數指標以外的所有專案。

描述有兩個可能的版面配置：

``` syntax
pointer_type<1> pointer_attributes<1>
simple_type<1> FC_PAD
```

–或–

``` syntax
pointer_type<1> pointer_attributes<1>
offset_to_complex_description<2>
```

如果指標是簡單類型或 nonsized 字串指標的指標，則會使用第一個格式。 第二種格式是用於所有其他類型的指標。 指標屬性會使用 FC \_ 簡單指標旗標來指出描述的版面配置 \_ 。

指標 \_ 類型<1> 是下列其中一項。



| 格式字元 | 說明                              |
|------------------|------------------------------------------|
| FC \_ RP           | 參考指標。                     |
| FC \_ UP           | 唯一指標。                        |
| FC \_ FP           | 完整指標。                          |
| FC \_ OP           | 物件介面中的唯一指標。 |



 

區分 FC OP 的原因 \_ 是語義：在物件介面中，必須 \[ 先釋出 in、out 指標，然後 \] 才能將新的物件封送至新的物件，並指派新的指標值。

指標 \_ 屬性<1> 可以有下表所示的任何旗標。



| 屬性 | 旗標              | 描述                                                                                                                                                                                                                                      |
|------|--------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 01   | FC \_ 配置 \_ 所有 \_ 節點 | 指標是配置 (所有 \_ 節點) 配置配置的一部分。                                                                                                                                                                   |
| 02   | FC \_ \_ 沒有任何可用           | 配置 (不會 \_ 釋放) 指標。                                                                                                                                                                                                      |
| 04   | \_ \_ 堆疊上的 FC ALLOCED \_   | 在存根的堆疊上配置其引用的指標。                                                                                                                                                                            |
| 08   | FC \_ 簡單 \_ 指標      | 簡單類型或 nonsized 符合標準之字串的指標。 設定此旗標表示指標描述的版面配置是上述的簡單指標配置，否則會指出具有位移的描述項格式。 |
| 10   | FC \_ 指標 \_ DEREF       | 必須先取值的指標，才能處理指標的參考。                                                                                                                                                           |



 

具有 () 大小的指標 \_ 、最大值是 \_ () 、 \_ () 長度、最後一個 \_ () ，以及/或第一個 \_ 套用 () 套用至這些指標的格式字串描述與適當類型陣列的指標相同 (例如，如果大小為 () ，則符合標準的陣列 \_ ，如果大小為 () \_ 且長度為) \_ 。

## <a name="interface-pointers"></a>介面指標

物件介面指標格式字串具有兩種格式的其中一種，取決於編譯器是否知道對應的 IID。

具有常數 IID 的介面指標具有下列描述：

``` syntax
FC_IP FC_CONSTANT_IID 
iid<16>
```

Iid<16> 部分是介面指標的實際 IID。 Iid 會以與 GUID 資料結構相同的格式寫入格式字串： long、short、short、char \[ 8 \] 。

具有 iid 之介面指標的描述 \_ () 套用至：

``` syntax
FC_IP FC_PAD 
iid_description<> 
```

Iid \_ 描述<> 是相互關聯描述項，而且有4或6個位元組，視是否使用 [**/robust**](/windows/desktop/Midl/-robust) 而定。 **NdrComputeConformance** 函數所計算的值是 IID 指標。

## <a name="byte-count-pointers"></a>位元組計數指標

Byte count 指標與稱為 \[ **byte \_ count** 的特殊優化屬性相關 \] 。 使用的格式如下：

``` syntax
FC_BYTE_COUNT_POINTER 
simple_type<1>
byte_count_description<> 
```

還

``` syntax
FC_BYTE_COUNT_POINTER 
FC_PAD
byte_count_description<> 
pointee_description<>
```

<> 的位元組 \_ 計數 \_ 描述是相互關聯描述項，而且有4或6個位元組，視是否使用 [**/robust**](/windows/desktop/Midl/-robust) 而定。

Pointee \_ 描述<> 是 pointee 類型的描述。

 

 
