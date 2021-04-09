---
title: RPC) 的結構 (
description: 遠端程序呼叫中的各種結構類型的描述， (RPC) 。
ms.assetid: edaf547d-d3d1-443c-93dd-8e036bc42944
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4ccae91f703badd2e0153dfc3d8acff1ace562f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023821"
---
# <a name="structures-rpc"></a>RPC) 的結構 (

結構有數種類別，在封送處理所需的動作方面逐漸複雜。 它們的開頭是可以全部封鎖複製的簡單結構，然後繼續進行必須依欄位提供服務欄位的複雜結構。

-   [簡單結構](#simple-structure)
-   [具有指標的簡單結構](#simple-structure-with-pointers)
-   [符合標準的結構](#conformant-structure)
-   [具有指標的一致結構](#conformant-structure-with-pointers)
-   [具有或不具有指標的一致結構 () ](#conformant-varying-structure-with-or-without-pointers)
-   [硬結構](#hard-structure)
-   [複雜結構](#complex-structure)
-   [結構成員版面配置描述](#structure-member-layout-description)

> [!Note]  
> 相較于陣列類別目錄，它會清楚地描述最高可達64k 大小的結構， (大小適用于結構) 的平面部分，也就是沒有適用于 SM 和 LG 陣列的專案。

 

**結構通用的成員**

-   **對準**

    封送結構之前的緩衝區所需的對齊方式。 有效的值為0、1、3和 7 (實際對齊減 1) 。

-   **記憶體 \_ 大小**

    結構在記憶體中的大小，以位元組為單位;針對符合標準的結構，這個大小不包含陣列的大小。

-   **\_ \_ 陣列描述的 \_ 位移**

    從目前的格式字串指標位移到結構中所包含之符合的陣列描述。

-   **成員 \_ 版面配置**

    結構中每個元素的描述。 如果需要 endian 轉換，或者型別是複雜結構，則 NDR 常式只需要檢查類型之格式字串的這個部分。

-   **指標 \_ 版面配置**

    請參閱 [指標版面](pointer-layout-tfs.md) 配置區段。

## <a name="simple-structure"></a>簡單結構

簡單結構只包含基底類型、固定陣列和其他簡單結構。 簡單結構的主要功能是可以全部區塊複製。

``` syntax
FC_STRUCT alignment<1> 
memory_size<2> 
member_layout<> 
FC_END
```

## <a name="simple-structure-with-pointers"></a>具有指標的簡單結構

具有指標的簡單結構只包含基底類型、指標、固定陣列、簡單結構和其他具有指標的簡單結構。 因為版面配置<> 只需要在進行 endianess 轉換時流覽，所以會置於描述的結尾。

``` syntax
FC_PSTRUCT alignment<1> 
memory_size<2> 
pointer_layout<> 
member_layout<> 
FC_END
```

## <a name="conformant-structure"></a>符合標準的結構

符合標準的結構只包含基底類型、固定陣列和簡單結構，而且必須包含符合標準的字串或符合標準的陣列。 這個陣列實際上可以包含在另一個符合標準的結構中，或是具有內嵌在此結構中之指標的一致結構。

``` syntax
FC_CSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
member_layout<> 
FC_END
```

## <a name="conformant-structure-with-pointers"></a>具有指標的一致結構

具有指標的一致結構只包含基底類型、指標、固定陣列、簡單結構，以及具有指標的簡單結構;符合標準的結構必須包含符合標準的陣列。 這個陣列實際上可以包含在另一個符合標準的結構中，或是具有內嵌在此結構中的指標。

``` syntax
FC_CPSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
pointer_layout<> 
member_layout<> FC_END
```

## <a name="conformant-varying-structure-with-or-without-pointers"></a>具有或不具有指標的一致結構 () 

一致的不同結構只包含簡單類型、指標、固定陣列、簡單結構，以及具有指標的簡單結構;一致的不同結構必須包含符合標準的字串或一致的陣列。 符合標準的字串或陣列實際上可以包含在另一個符合標準的結構中，也可以包含內嵌在此結構中的指標。

``` syntax
FC_CVSTRUCT alignment<1> 
memory_size<2> 
offset_to_array_description<2> 
[pointer_layout<>] 
layout<> 
FC_END
```

## <a name="hard-structure"></a>硬結構

硬結構是一種概念，目的是要消除與處理複雜結構相關的嚴厲處罰。 它衍生自觀察：複雜結構通常只有一或兩個條件會防止封鎖複製，因此否則沒有其效能與簡單結構相比。 原因通常是等位或列舉欄位。

「硬式結構」（hard structure）是在記憶體中有 enum16、結束填補或聯集做為最後一個成員的結構。 這三個元素可防止結構進入先前的其中一個結構類別，這可享有小型的解讀負荷和最大的優化潛力，但不會將它強制進入成本極高的複雜結構類別。

Enum16 不能讓結構的記憶體和線大小有所差異。 結構不能有任何符合標準的陣列，也不能 (任何指標，除非 union) 的一部分;唯一允許的其他成員為基底類型、固定陣列和簡單結構。

``` syntax
FC_HARD_STRUCTURE alignment<1> 
memory_size<2> 
reserved<4> 
enum_offset<2> 
copy_size<2> 
mem_copy_incr<2> 
union_description_offset<2>
member_layout<> 
FC_END
```

列舉 \_ offset<2> 欄位提供從記憶體中的結構開始到其中包含 enum16 的位移，否則列舉 \_ 位移<2> 欄位為–1。

[複製 \_ 大小<2]> 欄位提供結構中的位元組總數，可能會區塊複製到緩衝區或從中複製。 此總計不包含任何尾端的聯集，也不包含記憶體中的任何結束填補。 此值也是緩衝區指標在複製之後的遞增量。

\_ \_ 記憶體複製增量<2> 欄位是記憶體指標在處理任何尾端等位之前，應該在區塊複製之後遞增的位元組數目。 依此數量遞增 (不是依複製 \_ 大小<2> 位元組) 產生適當的記憶體指標給任何尾端聯集。

## <a name="complex-structure"></a>複雜結構

複雜結構是包含一或多個欄位的任何結構，這些欄位會防止禁止複製結構，或必須在封送處理或封送處理期間執行額外的檢查 (例如，列舉) 的系結檢查。 下列 NDR 類型落在此類別中：

-   [簡單類型](simple-types-tfs.md)： \_ \_ 在64位平臺上的 ENUM16、INT3264 (只能) 、具有 \[ [**範圍** 的整數](/windows/desktop/Midl/range)\]
-   結構結尾的對齊填補
-   介面指標 (使用內嵌複雜) 
-   略過的指標 (與 \[ [**ignore**](/windows/desktop/Midl/ignore) \] 屬性和 FC \_ ignore token 相關) 
-   複雜陣列、不同陣列、字串陣列
-   具有至少一個 nonfixed 維度的多維度一致陣列
-   等位
-   以 \[ [**傳輸 \_ 為**](/windows/desktop/Midl/transmit-as)的方式定義的元素 \] ， \[ [**表示 \_ 為**](/windows/desktop/Midl/represent-as) \] 、 \[ [**電匯 \_**](/windows/desktop/Midl/wire-marshal)、 \] \[ [**使用者 \_ 封送**](/windows/desktop/Midl/user-marshal)處理\]
-   內嵌複雜結構
-   在結構結尾處填補

複雜結構具有下列格式描述：

``` syntax
FC_BOGUS_STRUCT alignment<1> 
memory_size<2> 
offset_to_conformant_array_description<2> 
offset_to_pointer_layout<2> 
member_layout<> 
FC_END 
[pointer_layout<>]
```

記憶體 \_ 大小<2> 欄位是記憶體中的結構大小（以位元組為單位）。

如果結構包含符合標準的陣列，則 \_ 符合標準 \_ 的 \_ 陣列 \_ 描述<2> 欄位會提供相符的陣列描述的位移，否則為零。

如果結構具有指標，指標配置的 \_ 位移 \_ \_<2> 欄位會提供超過結構的版面配置到指標配置的位移，否則此欄位為零。

\_複雜結構的指標版面配置<> 欄位的處理方式，與其他結構的處理方式稍有不同。 複雜結構的 [指標配置] \_<> 欄位只包含結構本身中實際指標欄位的描述。 任何內嵌陣列、等位或結構內包含的任何指標，都不會在複雜結構的指標 \_ 版面配置<> 欄位中描述。

> [!Note]  
> 這與其他結構相反，後者會將內嵌陣列或結構中所包含之任何指標的描述複製到它們自己的指標配置 \_<> 欄位中。

 

複雜結構指標配置的格式也有截然不同的差異。 因為它只包含實際指標成員的描述，而且因為複雜結構會一次封送處理和取消封送處理一個欄位，所以指標 \_ 版面配置<> 欄位只包含所有指標成員的指標描述。 沒有開始 FC \_ PP，也沒有任何一般指標 \_ 版面配置<> 資訊。

## <a name="structure-member-layout-description"></a>結構成員版面配置描述

結構的版面配置描述包含下列一或多個格式字元：

-   任何基底類型字元，例如 FC \_ 字元等等
-   對齊指示詞。 有三個格式字元指定記憶體指標的對齊： FC \_ ALIGNM2、fc \_ ALIGNM4 和 fc \_ ALIGNM8。
    > [!Note]  
    > 另外還有緩衝區對齊權杖，FC \_ ALIGNB2 透過 fc \_ ALIGNM8; 這些都不會使用。

     

-   記憶體填補。 這些只會發生在結構描述的結尾，並表示結構中符合標準的陣列之前的記憶體填補位元組數： FC \_ STRUCTPADn，其中 n 是填補的位元組數目。
-   任何內嵌的 nonbase 類型 (注意，標準的陣列永遠不會出現在結構配置) 中。 這有4個位元組的描述：

    ``` syntax
    FC_EMBEDDED_COMPLEX memory_pad<1> 
    offset_to_description<2>,
    ```

    其中的位移不保證會對齊2個位元組。

    memory \_ pad<1> 是在複雜欄位之前的記憶體中所需的填補。

    \_ \_ 描述的位移<2> 是內嵌型別的相對型別位移。

如有需要，可能也會在 \_ 終止 fc 結束之前有 FC PAD， \_ 以確保格式字串會在 FC 端之後的雙位元組界限上對齊 \_ 。

 

 