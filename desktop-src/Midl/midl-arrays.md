---
title: MIDL 陣列
description: MIDL 陣列。
ms.assetid: dee30788-0575-4b49-a6b8-5208ad295183
keywords:
- 資料類型 MIDL、陣列
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78c5ca08740084783f615d2cd34b46f0de4a4020
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023421"
---
# <a name="midl-arrays"></a>MIDL 陣列

陣列宣告子會在 IDL 檔案的介面主體中顯示為下列其中一項：

-   一般宣告的一部分
-   結構或等位宣告子的成員
-   遠端程序呼叫的參數

陣列中每個維度的界限都會以一組不同的方括弧括住。 評估為 *n* 的運算式表示零的下限和 *n-1* 的上限。 如果方括弧是空的，或包含單一星號 (\*) ，下限為零，而上限是在執行時間決定。

陣列也可以包含兩個值，並以表示陣列的下限和上限的省略號分隔，如下 \[ 所示。*上方* \] 。 Microsoft RPC 需要的下限為零。 MIDL 編譯器無法辨識指定非零下限的結構。

陣列可以與欄位屬性大小相關聯，[**最大值 \_**](max-is.md)為，[**長度 \_ 為**](length-is.md)，[**第一個 \_ 是**](first-is.md)，[**最後 \_ 是**](last-is.md)指定陣列的大小或陣列中包含有效資料的部分。 [**\_**](size-is.md) 這些欄位屬性會識別指定陣列維度或索引的參數、結構欄位或常數。

陣列必須與 field 屬性指定的識別碼相關聯，方法如下：當陣列是參數時，識別碼也必須是相同函式的參數。當陣列是結構欄位時，識別碼必須是相同結構的另一個結構欄位。

如果任何維度的上限都是在執行時間決定的，則陣列稱為「一致」。  (只有上限可在執行時間決定。 ) 若要判斷上限，陣列宣告必須包含 [大小] 或 [**[ \_**](size-is.md) [**最大值 \_**](max-is.md) ] 屬性。

當陣列的界限是在編譯時期決定時，陣列稱為「變動」，但是傳輸的元素範圍是在執行時間決定。 若要判斷已傳送的元素範圍，陣列宣告必須包含 [**長度 \_ 為**](length-is.md)、 [**第一個 \_ 為**](first-is.md)，或 [**最後一個 \_ 是**](last-is.md) 屬性。

一致的不同陣列 (也稱為「開啟」 ) 是一個陣列，其上限和傳送的元素範圍是在執行時間決定。 最多可以在 C 結構中嵌套一個符合或一致的不同陣列，而且必須是結構的最後一個元素。 相反地，nonconformant 變化的陣列可以出現在結構中的任何位置。

## <a name="examples"></a>範例

``` syntax
/* IDL file interface body */ 
#define MAX_INDEX 10 
 
typedef char  ATYPE[MAX_INDEX]; 
typedef short BTYPE[];        // Equivalent to [*]; 
typedef long  CTYPE[*][10];   // [][10] 
typedef float DTYPE[0..10];   // Equivalent to [11] 
typedef float ETYPE[0..(MAX_INDEX)];  
 
typedef struct 
{ 
    unsigned short size; 
    unsigned short length; 
    [size_is(size), length_is(length)] char string[*]; 
} counted_string; 
 
HRESULT MyFunction( 
     [in, out] short * pSize,  
     [in, out, string, size_is(*pSize)] char a[0..*] 
);
```

如需詳細資訊，請參閱 [陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)。

## <a name="multidimensional-arrays"></a>多維陣列

使用者可以宣告類型為數組，然後宣告這類類型的物件陣列。 *N* 維度陣列類型的 *m* 維度陣列的語法與 *m* + *n* 維度陣列的語法相同。

例如，型別 RECT \_ 型別可以定義為二維陣列，而變數 *RECT* 可以定義為 RECT 型別的陣列 \_ 。 這相當於三維陣列的 *相等 \_ 矩形*：

``` syntax
typedef short int RECT_TYPE[10][20]; 
RECT_TYPE rect[15]; 
short int equivalent_rect[15][10][20];  // ~RECT_TYPE rect[15]
```

Microsoft RPC 為 C 導向。 遵循 C 語言慣例，只有多維陣列的第一個維度可以在執行時間決定。 與支援其他語言之 DCE IDL 陣列的互通性限制為：

-   具有常數的多維度陣列 (編譯時間決定的) 界限。
-   具有所有常數界限（第一個維度除外）的多維度陣列。 第一個維度的已傳輸元素上限和範圍取決於執行時間。
-   具有零下限的任何一維陣列。

當 **\[** [**字串**](string.md) **\]** 屬性用於多維度陣列時，屬性會套用至最右邊的陣列。

## <a name="arrays-of-pointers"></a>指標陣列

參考指標必須指向有效的資料。 用戶端應用程式必須為 **\[** [**in**](in.md) **\]** 或 **\[** **in、**[**out**](out-idl.md)參考指標陣列中的所有記憶體配置 **\]** ，尤其是當陣列與 **\[ in \]**、 **\[** **in、 \] out**、 **\[** [**length \_ 為**](length-is.md) **\]** 或 **\[** [**last \_ 為**](last-is.md) **\]** 值時。 用戶端應用程式也必須在呼叫之前初始化所有陣列元素。 回到用戶端之前，伺服器應用程式必須確認傳送的範圍中的所有陣列元素都指向有效的儲存體。

在伺服器端上，存根會為所有陣列元素配置儲存體，而不管在 **\[** 呼叫時，[**長度 \_ 為**](length-is.md) **\]** 或 **\[** [**最後 \_ 一個**](last-is.md) **\]** 值。 這項功能可能會影響應用程式的效能。

唯一指標的陣列沒有任何限制。 在用戶端和伺服器上，儲存體都會配置給 null 指標。 當指標為非 null 時，資料會放在預先配置的儲存體中。

選擇性的指標宣告子可以在陣列宣告子前面。

當內嵌參考指標是 **\[** [](out-idl.md) **\]** 僅限輸出的參數時，伺服器管理員程式碼必須將有效值指派給參考指標的陣列。 例如：

``` syntax
typedef [ref] short * ARefPointer;
typedef ARefPointer ArrayOfRef[10];
HRESULT proc1( [out] ArrayOfRef Parameter );
```

產生的存根會配置陣列，並將 null 值指派給內嵌于陣列中的所有指標。

 

 