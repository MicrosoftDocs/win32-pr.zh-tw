---
title: " (RPC) 的陣列 (TFS) "
description: 遠端程序呼叫 (RPC) 陣列類別包含固定大小、符合標準、一致、變化、複雜。
ms.assetid: 7144ec87-90f2-463a-80e4-28cb4771325f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6271f6a459ebfb96cc5c4d55153bb4c77b013a50925d9c3a4ba9dd81b0f6fbdf
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073488"
---
# <a name="arrays-rpc"></a> (RPC) 的陣列

已根據其效能特性定義了數個數組類別，主要是是否可以封鎖複製陣列。

某些類別（例如固定大小的陣列）有兩種類型的陣列描述元：它們是由前置 FC 權杖的名稱中的修正所表示。



| 格式字元 | 說明                                                           |
|------------------|-----------------------------------------------------------------------|
| SM               | 類型的總大小可以用16位不帶正負號的整數表示。    |
| LG               | 類型的總大小需要以32位不帶正負號的長度來表示。 |



 

陣列通用的欄位：

-   總 \_ 大小

    記憶體中的陣列大小總計（以位元組為單位）。 這與調整後的網路大小相同。 針對填補問題不存在且大小為實際陣列大小的類別，會計算總大小。

-   元素 \_ 大小

    陣列單一元素的記憶體大小總計，包括填補 (只有) 複雜的陣列時，才會發生這種情況。

-   元素 \_ 描述

    陣列元素類型的描述。

-   指標 \_ 版面配置

    如需詳細資訊，請參閱 [指標版面](pointer-layout-tfs.md) 配置主題。

## <a name="fixed-sized-arrays"></a>固定大小的陣列

針對具有已知大小的陣列產生固定大小的陣列格式字串，因此可能會被區塊複製到封送處理緩衝區。 這兩個固定的陣列描述元格式如下所示。

``` syntax
FC_SMFARRAY alignment<1> 
total_size<2> 
[pointer_layout<>]  
element_description<> 
FC_END
```

及

``` syntax
FC_LGFARRAY alignment<1> 
total_size<4> 
[pointer_layout<>] 
element_description<> 
FC_END
```

## <a name="conformant-array"></a>符合標準的陣列

一旦知道陣列的大小，就可以封鎖複製符合標準的陣列。

``` syntax
FC_CARRAY alignment<1>
element_size<2> 
conformance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END
```

一致性 \_ 描述<> 是相互關聯描述項，而且有4或6個位元組，視是否使用 [**/robust**](/windows/desktop/Midl/-robust) 而定。

## <a name="conformant-varying-array"></a>一致的不同陣列

也可以封鎖複製一致的不同陣列。

``` syntax
FC_CVARRAY alignment<1> 
element_size<2> 
conformance_description<> 
variance_description<>  
[pointer_layout<>] 
element_description<> 
FC_END
```

一致性 \_ 描述<> 和差異 \_ 描述<> 是相互關聯描述項，而且有4或6個位元組，視是否使用 [**/robust**](/windows/desktop/Midl/-robust) 而定。

## <a name="varying-array"></a>不同陣列

不同的陣列有兩種可能性，視陣列的大小而定。

``` syntax
FC_SMVARRAY alignment<1>
total_size<2>  
number_elements<2> 
element_size<2> 
variance_description<> 
[pointer_layout<>] 
element_description<> 
FC_END

FC_LGVARRAY alignment<1>
total_size<4>  
number_elements<4> 
element_size<2> 
variance_description<4>
[pointer_layout<>] 
element_description<> 
FC_END
```

差異 \_ 描述<> 是相互關聯描述項，而且有4或6個位元組，視所使用的 [**/robust**](/windows/desktop/Midl/-robust) 而定。

針對內嵌于結構內的不同陣列，差異描述<2> 欄位的位移 \_<> 是從結構中不同陣列的位置到差異描述欄位的相對位移。 位移通常相對於結構的開頭。

## <a name="complex-arrays"></a>複雜陣列

複雜陣列是具有專案的任何陣列，可防止它被封鎖複製，因此需要採取其他動作。 這些元素會讓陣列變得複雜：

-   簡單類型： \_ \_ 在64位平臺上的 ENUM16、INT3264 (只能) 、具有 \[ [**範圍** 的整數](/windows/desktop/Midl/range)\]
-   參考和介面指標 (64 位平臺上的所有指標) 
-   等位
-   複雜結構 (如需結構複雜的原因清單，請參閱複雜結構描述主題) 
-   以 \[ [**傳輸 \_ 為**](/windows/desktop/Midl/transmit-as) \] 、 \[ [**使用者 \_ 封送**](/windows/desktop/Midl/user-marshal)處理定義的元素\]
-   無論基礎專案類型為何，所有具有至少一個符合和/或不同維度的多維陣列都是複雜的。

複雜的陣列描述如下所示：

``` syntax
FC_BOGUS_ARRAY alignment<1> 
number_of_elements<2> 
conformance_description<> 
variance_description<> 
element_description<> 
FC_END
```

\_ \_ 如果陣列一致，<2> 欄位的元素數目為零。

一致性 \_ 描述<> 和差異 \_ 描述<> 是相互關聯描述項，而且有4或6個位元組，視是否使用 [**/robust**](/windows/desktop/Midl/-robust) 而定。 如果陣列具有一致性和/或變異數，則一致性 \_ 描述<> 和/或變異 \_ 數描述<> 欄位 (s) 有有效的描述，否則，相互關聯描述項的前4個位元組會設定為0xffffffff。 旗標（如果有的話）會設定為零。

 

 
