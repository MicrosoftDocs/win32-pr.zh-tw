---
title: 欄位屬性
description: 欄位屬性 (屬性（attribute）套用至陣列、結構、等位或字元陣列的欄位，) 和遠端程序呼叫 (RPC) 。
ms.assetid: 4508479d-ff0a-4698-94aa-588837032067
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e6d14bab0cf14710e91fceb466111c4af32d3d2828e4b7bdacc9494fa27b7d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929997"
---
# <a name="field-attributes"></a>欄位屬性

欄位屬性是可以套用至陣列、結構、等位或字元陣列之欄位的屬性：

-   **\[**[**略**](/windows/desktop/Midl/ignore)過 **\]** ， **\[** [**大小 \_ 為**](/windows/desktop/Midl/size-is)**\]**
-   **\[**[**最大值 \_ 為**](/windows/desktop/Midl/max-is)**\]**
-   **\[**[**長度 \_ 為**](/windows/desktop/Midl/length-is)**\]**
-   **\[**[**第一個 \_ 是**](/windows/desktop/Midl/first-is)**\]**
-   **\[**[**last \_**](/windows/desktop/Midl/last-is)**\]**
-   **\[**[**切換 \_ 為**](/windows/desktop/Midl/switch-is)**\]**
-   **\[**[**字串**](/windows/desktop/Midl/string)**\]**
-   [指標屬性](three-pointer-types.md)

例如，欄位屬性會與陣列宣告一起使用，以指定陣列的大小或包含有效資料之陣列的部分。 這是藉由將另一個參數、結構欄位或常數運算式與陣列產生關聯來完成。

**\[** [**Ignore**](/windows/desktop/Midl/ignore) **\]** 屬性會指定在封送處理過程中要忽略的指標欄位。 這種略過的欄位會在接收者端設定為 **Null** 。

MIDL 提供 *一致*、 *變化* 和 *開放式* 的陣列。 如果陣列的界限是在執行時間決定的，則會將其稱為一致。 **\[** [**Size \_ 為 attribute 會**](/windows/desktop/Midl/size-is) **\]** 指定陣列配置大小的上限，而 **\[** [**max \_ 為**](/windows/desktop/Midl/max-is)屬性則會 **\]** 指定有效陣列索引值的上限。 如需詳細資訊，請參閱 **\[** [**陣列**](arrays.md) **\]** 。

如果陣列的界限是在編譯時期決定的，則會將陣列稱為變動，但是會在執行時間決定傳送的元素範圍。 開放式陣列 (也稱為一致的不同陣列) 是在執行時間決定其上限和傳送的元素範圍的陣列。 若要判斷陣列的已傳輸元素範圍，陣列宣告必須包含 **\[** [**長度 \_ 為**](/windows/desktop/Midl/length-is) **\]** 、 **\[** [**第一個 \_ 為**](/windows/desktop/Midl/first-is) **\]** ，或最後一個 **\[** [**\_ 是**](/windows/desktop/Midl/last-is) **\]** 屬性。

[ **\[ 長度 \_ ] \] 是**[屬性] 指定要傳送的陣列元素數目， **\[ 第 \_ 一個 \] 是** 屬性指定要傳送之第一個陣列元素的索引。 **\[ 最後一個 \_ 是 \]** 屬性，它會指定要傳送之最後一個陣列元素的索引。

**\[**[**參數 \_ 是**](/windows/desktop/Midl/switch-is) **\]** 欄位屬性指定了聯集鑒別子。 當 union 是程式參數時，聯集鑒別子必須是相同程式的另一個參數。 當聯集是結構的欄位時，鑒別子必須是結構與聯集欄位相同層級的另一個欄位。 鑒別子必須是 [**布林值**](/windows/desktop/Midl/boolean)、 [**char**](/windows/desktop/Midl/char-idl)、 [**int**](/windows/desktop/Midl/int)或 [**列舉**](/windows/desktop/Midl/enum) 型別，或是解析成其中一種類型的型別。 如需詳細資訊，請參閱 [Nonencapsulated](/windows/desktop/Midl/nonencapsulated-unions)聯集和 **\[ 切換 \_ 為 \]**。

**\[**[**字串**](/windows/desktop/Midl/string) **\]** 欄位屬性會指定一維字元或位元組陣列，或以零終止的字元或位元組資料流程的指標，視為字串。 字串屬性只適用于一維陣列和指標。 元素類型受限於 [**char**](/windows/desktop/Midl/char-idl)、 [**byte**](/windows/desktop/Midl/byte)、 [**wchar \_ t**](/windows/desktop/Midl/wchar-t)或解析成其中一種類型的命名類型。

如需欄位屬性出現所在內容的相關資訊，請參閱 [Midl 陣列](/windows/desktop/Midl/midl-arrays)、 [Midl 結構](/windows/desktop/Midl/midl-structures)和 [midl](/windows/desktop/Midl/midl-unions)等位。

 

 