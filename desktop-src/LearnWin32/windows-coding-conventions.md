---
title: Windows編碼慣例
description: 如果您不熟悉 Windows 程式設計，當您第一次看到 Windows 程式時，可能會令人不安。
ms.assetid: 466a66db-7681-4fce-9672-07849cd1b096
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b78c24f38f9f2f410c044637ca3aa59d4baa39e9b671b3485c5b85899b69c2fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118387393"
---
# <a name="windows-coding-conventions"></a>Windows編碼慣例

如果您不熟悉 Windows 程式設計，當您第一次看到 Windows 程式時，可能會令人不安。 程式碼會填入奇怪的型別定義，例如 **DWORD \_ PTR** 和 **LPRECT**，而變數的名稱像是 *hWnd* 和 *pwsz* (稱為匈牙利文標記法) 。 值得花一點時間瞭解一些 Windows 程式碼撰寫慣例。

大部分的 Windows api 都是由函數或元件物件模型 (COM) 介面所組成。 許多 Windows api 都是以 c + + 類別的形式提供。  (有個值得注意的例外狀況 GDI+，其中一個是2d 圖形 api。 ) 

## <a name="typedefs"></a>Typedefs

Windows 標頭包含許多 typedef。 其中許多都是在標頭檔 WinDef 中定義。 以下是您經常會遇到的部分。

### <a name="integer-types"></a>整數類型



| 資料類型     | 大小    | 簽署？  |
|---------------|---------|----------|
| **BYTE**      | 8 位元  | 不帶正負號 |
| **Dword**     | 32 位元 | 不帶正負號 |
| **時會**     | 32 位元 | 簽署人   |
| **INT64**     | 64 位元 | 簽署人   |
| **LONG**      | 32 位元 | 簽署人   |
| **LONGLONG**  | 64 位元 | 簽署人   |
| **UINT32**    | 32 位元 | 不帶正負號 |
| **UINT64**    | 64 位元 | 不帶正負號 |
| **ULONG**     | 32 位元 | 不帶正負號 |
| **ULONGLONG** | 64 位元 | 不帶正負號 |
| **WORD**      | 16 位元 | 不帶正負號 |



 

如您所見，這些 typedef 中有一定數量的多餘。 部分重迭只是因為 Windows api 的歷程記錄。 此處所列的類型具有固定的大小，在32位和64應用程式中的大小都相同。 例如， **DWORD** 類型一律為32位寬。

### <a name="boolean-type"></a>布林類型

**BOOL** 是布林值內容中所使用之整數值的 typedef。 標頭檔 WinDef 也會定義兩個搭配 **BOOL** 使用的值。


```C++
#define FALSE    0 
#define TRUE     1
```



不過，儘管這個定義為 **TRUE**，但傳回 **BOOL** 類型的大部分函式都可以傳回任何非零值以表示布林值。 因此，您應該一律撰寫下列內容：


```C++
// Right way.
BOOL result = SomeFunctionThatReturnsBoolean();
if (result) 
{ 
    ...
}
```



而不是：


```C++
// Wrong!
if (result == TRUE) 
{
    ... 
}
```



請注意， **BOOL** 是整數型別，而且無法與 c + + **BOOL** 型別互換。

### <a name="pointer-types"></a>指標類型

Windows 定義許多表單 *指標至 X* 的資料類型。 這些通常會在名稱中使用前置詞 *P* 或 *LP* 。 例如， **LPRECT** [**是矩形的指標，其中**](/previous-versions//dd162897(v=vs.85)) **rect** 是描述矩形的結構。 下列變數宣告是相等的。


```C++
RECT*  rect;  // Pointer to a RECT structure.
LPRECT rect;  // The same
PRECT  rect;  // Also the same.
```



在過去， *P* 代表「指標」，而 *LP* 代表「長指標」。 長指標 (也稱為 *遠指標*) 是從16位 Windows 的 holdover，當它們需要處理目前區段以外的記憶體範圍時。 已保留 *LP* 前置詞，可讓您更輕鬆地將16位程式碼移植到32位的 Windows。 今天沒有任何差別，指標就是指標。

### <a name="pointer-precision-types"></a>指標精確度類型

下列資料類型一律是指標的大小，也就是32位應用程式中的32位寬，以及64位應用程式中的64位寬。 大小是在編譯時期決定。 當32位應用程式在64位 Windows 上執行時，這些資料類型仍然是4個位元組寬。  (64 位應用程式無法在32位 Windows 上執行，因此不會發生反向情況。 ) 

-   **DWORD \_ PTR**
-   **INT \_ PTR**
-   **長 \_ PTR**
-   **ULONG \_ PTR**
-   **UINT \_ PTR**

這些類型會在整數可能轉換成指標的情況下使用。 它們也可用來定義指標算術的變數，以及定義迴圈計數器，以逐一查看記憶體緩衝區中的完整位元組範圍。 更常見的情況是，它們會出現在現有32位值在64位 Windows 上展開至64位的位置。

## <a name="hungarian-notation"></a>匈牙利文標記法

*匈牙利文標記法* 是將前置詞新增至變數名稱的做法，以提供變數的其他相關資訊。  (標記法的發明者（Charles Simonyi）是匈牙利文，因此其名稱) 。

在其原始形式中，匈牙利文標記法會提供變數的相關 *語義* 資訊，告訴您預期的用途。 例如， *i* 表示索引， *cb* 表示以位元組為單位的大小 ( 「位元組計數」 ) ，以及 *rw* 和資料行 *的平均資料* 列和資料行數目。 這些前置詞的設計目的是為了避免在錯誤的內容中意外使用變數。 例如，如果您看到運算式 `rwPosition +  cbTable` ，您會知道將資料列編號加入至大小，這在程式碼中幾乎肯定是錯誤的

比較常見的匈牙利文標記法會使用前置詞來提供 *類型* 資訊，例如 *dw* for **DWORD** 和 *w* for **WORD**。

如果您在網路上搜尋「匈牙利文標記法」，您會發現有關匈牙利文標記法是否正確或不正確的許多意見。 某些程式設計人員對於匈牙利文標記法的不喜歡。 其他人覺得很有用。 無論如何，MSDN 上的許多程式碼範例都使用匈牙利文標記法，但您不需要記住首碼來瞭解程式碼。

## <a name="next"></a>下一個

[使用字串](working-with-strings.md)

 

 