---
title: 使用指標的規則
description: 將您的程式碼移植到適用于32和64位 Microsoft Windows 的程式碼很簡單。 您只需要遵循一些有關轉換指標的簡單規則，並在您的程式碼中使用新的資料類型。 指標操作的規則如下所示。
ms.assetid: 4c38bee2-fa1c-493f-a12d-e673df4d4895
keywords:
- 使用指標64位 Windows 程式設計的規則
- 指標操作 64-位 Windows 程式設計
- 轉換指標64位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 318ff5beed6dc90bd49b6b293131e17db6f92f6b
ms.sourcegitcommit: ae73f4dd3cf5a3c6a1ea7d191ca32a5b01f6686b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/08/2020
ms.locfileid: "103933683"
---
# <a name="rules-for-using-pointers"></a>使用指標的規則

將您的程式碼移植到適用于32和64位 Microsoft Windows 的程式碼很簡單。 您只需要遵循一些有關轉換指標的簡單規則，並在您的程式碼中使用新的資料類型。 指標操作的規則如下所示。

1.  請勿將指標轉換成 **int**、 **long**、 **ULONG** 或 **DWORD**。

    如果您必須轉換指標以測試部分位、設定或清除位，或以其他方式操作其內容，請使用 **UINT \_ PTR** 或 **INT \_ ptr** 類型。 這些型別是一種整數類資料類型，可調整為32和64位 Windows (的指標大小，例如， **ULONG** （32）位 windows，以及 \_ 64 位 windows) 的 int64。 例如，假設您正在移植下列程式碼：

    `ImageBase = (PVOID)((ULONG)ImageBase | 1);`

    作為移植程式的一部分，您可以變更程式碼，如下所示：

    `ImageBase = (PVOID)((ULONG_PTR)ImageBase | 1);`

    如果有適當的 (，請使用 **UINT \_ Ptr** 和 **INT \_ ptr** ，如果您不確定是否需要，則在) 的情況下使用它們就不會有任何傷害。 請勿將指標轉換為 **ULONG**、 **LONG**、 **INT**、 **UINT** 或 **DWORD** 類型。

    請注意，**控制碼** 定義為 **void \***，因此將句 **柄** 值 typecasting 為 **ULONG** 值以測試、設定或清除低序位2位是64位 Windows 上的錯誤。

2.  使用 **PtrToLong** 或 **PtrToUlong** 函式來截斷指標。

    如果您必須截斷32位值的指標，請使用 (在 Basetsd 中定義的 **PtrToLong** 或 **PtrToUlong** 函數) 。 這些函數會在呼叫期間停用指標截斷警告。

    請小心使用這些函數。 當您使用這些函式的其中一個來轉換指標變數之後，請不要再使用它做為指標。 這些函式會截斷位址的前32位，通常是存取指標最初參考的記憶體所需的部分。 使用這些函式而不謹慎考慮將會產生脆弱的程式碼。

3.  \_在程式碼中使用可以編譯為64位程式碼的指標32值時，請務必小心。 當指標指派給64位程式碼中的原生指標，而不是以零擴充指標時，編譯器將會簽署並擴充指標。
4.  \_在程式碼中使用可以編譯為32位程式碼的指標64值時，請務必小心。 編譯器會在32位程式碼中簽署並擴充指標，而不是以零擴充指標。
5.  請小心使用 OUT 參數。

    例如，假設您有定義如下的函數：

    `void func( OUT PULONG *PointerToUlong );`

    請勿呼叫此函數，如下所示。

    ``` syntax
    ULONG ul;
    PULONG lp;
    func((PULONG *)&ul);
    lp = (PULONG)ul;
    ```

    請改用下列呼叫。

    ``` syntax
    PULONG lp;
    func(&lp);
    ```

    Typecasting &ul to **PULONG \*** 可以防止編譯器錯誤，但函式會將64位指標值寫入 &ul 的記憶體中。 這段程式碼適用于32位的 Windows，但會導致64位 Windows 的資料損毀，而這會是很微妙、難以發現的損毀。 最下面的程式程式碼：不使用 C 程式碼玩訣竅，簡單明瞭。

6.  使用多型介面時請小心。

    請勿建立接受多型資料之 **DWORD** 參數的函數。 如果資料可以是指標或整數值，請使用 UINT \_ PTR 或 **PVOID** 類型。

    例如，請勿建立接受型別為 **DWORD** 值之例外狀況參數陣列的函式。 陣列應為 **DWORD \_ PTR** 值的陣列。 因此，陣列元素可以保留位址或32位整數值。  (一般規則是，如果原始型別是 **DWORD** ，而且必須是指標寬度，請將它轉換成 **DWORD \_ 指標** 值。 這就是為什麼有對應的指標精確度型別。 ) 如果您的程式碼使用 **DWORD**、 **ULONG** 或其他32位類型的多型方法， (也就是說，您真的希望參數或結構成員保留位址) ，請使用 **UINT \_ PTR** 來取代目前的型別。

7.  使用新的視窗類別函數。

    如果您有包含指標的視窗或類別私用資料，您的程式碼將需要使用下列新函數：

    -   [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra)
    -   [**GetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-getwindowlongptra)
    -   [**SetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-setclasslongptra)
    -   [**SetWindowLongPtr**](/windows/win32/api/winuser/nf-winuser-setwindowlongptra)

    這些函式可用於 32-和64位的 Windows，但它們在64位的 Windows 上是必要的。 立即使用這些功能來準備轉換。

    此外，您必須使用64位 Windows 上的新函數，來存取類別私用資料中的指標或控制碼。 為了協助您找出這些情況，在64位編譯期間，Winuser 中不會定義下列索引：

    -   GWL \_ WNDPROC
    -   GWL \_ HINSTANCE
    -   GWL \_ HWDPARENT
    -   GWL \_ USERDATA

    相反地，Winuser 會定義下列新的索引：

    -   GWLP \_ WNDPROC
    -   GWLP \_ HINSTANCE
    -   GWLP \_ HWNDPARENT
    -   GWLP \_ USERDATA
    -   GWLP \_ 識別碼

    例如，下列程式碼不會進行編譯：

    `SetWindowLong(hWnd, GWL_WNDPROC, (LONG)MyWndProc);`

    其應如下變更：

    `SetWindowLongPtr(hWnd, GWLP_WNDPROC, (LONG_PTR)MyWndProc);`

    設定 [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)結構的 **cbWndExtra** 成員時，請務必為指標保留足夠的空間。 例如，如果您目前為指標值保留 sizeof (DWORD) 個位元組，請保留 sizeof (DWORD \_ PTR) 位元組。

8.  使用 **欄位 \_ 位移** 存取所有視窗和類別資料。

    使用硬式編碼的位移來存取視窗資料是很常見的。 這項技術無法移植到64位的 Windows。 若要讓您的程式碼可移植，請使用 **欄位 \_ 位移** 宏來存取視窗和類別資料。 請勿假設第二個指標的位移為4。

9.  **LPARAM**、 **WPARAM** 和 **LRESULT** 類型會變更平臺的大小。

    編譯64位程式碼時，這些類型會擴充至64位，因為它們通常會保留指標或整數類型。 請勿將這些值與 **DWORD**、 **ULONG**、 **UINT**、 **int**、 **int** 或 **long** 值混合。 檢查您如何使用這些類型，並確保不會不慎截斷值。

 

 