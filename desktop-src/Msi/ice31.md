---
description: ICE31 會驗證顯示文字之控制項中所使用的任何預先定義字型樣式。 它也會驗證 DefaultUIFont 屬性是否參考有效的字型樣式。
ms.assetid: 07e60774-0e26-4a50-b818-a8f074512e3e
title: ICE31
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 783c8b842f80707bbd1ca833fbc7ad1f154a47a0d3aa24377ee58a1c6549bf7b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528668"
---
# <a name="ice31"></a>ICE31

ICE31 會驗證顯示文字之 [控制項](controls.md) 中所使用的任何預先定義字型樣式。 它也會驗證 [**DefaultUIFont**](defaultuifont.md) 屬性是否參考有效的字型樣式。

控制項可以有預先定義的字型樣式，如 [新增控制項和文字](adding-controls-and-text.md)中所述。 若要設定文字字串的字型與字型樣式，請在顯示的字元字串前面加上 { \\ style} 或 {&*style*}。 其中 style 是在 [資料行] 資料表的 [樣式 [表單](textstyle-table.md)] 資料行中所列的識別碼。 如果這兩個都不存在，但 [**DefaultUIFont**](defaultuifont.md) 屬性定義為有效的文字樣式，則會使用該字型。

ICE31 會檢查 [控制項資料表](control-table.md) 中每個控制項的文字資料行，以確認文字文字 [資料表](textstyle-table.md)中有有效的專案。

ICE31 會忽略 [ScrollableText 控制項](scrollabletext-control.md)。

## <a name="results"></a>結果

ICE31 會針對未定義的樣式、太長的樣式名稱、遺漏的樣式表單，以及沒有右大括弧的樣式標記張貼錯誤訊息。

如果 style 標記不在行首，或控制項有多個樣式標記時，ICE31 會張貼警告。

## <a name="example"></a>範例

ICE31 會針對所顯示的範例張貼下列錯誤：

-   控制項 DialogB. Control1 使用未定義的文本樣式 BadStyle。
-   控制項 DialogB. Control2 使用未定義的文本樣式 BadStyle。
-   控制項 DialogB. Control6 缺少文字樣式的右大括弧。
-   控制項 DialogB。 Control3 指定的文字樣式太長，無法有效。

ICE31 會針對所顯示的範例張貼下列警告：

-   DialogB. Control4 中的文字樣式標記沒有任何作用。 您真的想要讓它顯示為文字嗎？

[控制資料表](control-table.md) (部分) 



| 對話  | 控制  | Text                                                                                                                                                                |
|---------|----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| DialogA | Control0 | { \\ OKStyle} 這是要顯示的文字。                                                                                                                             |
| DialogA | Control1 | {&OKStyle}這是要顯示的文字。                                                                                                                              |
| DialogB | Control1 | {&BadStyle}這是要顯示的文字。                                                                                                                             |
| DialogB | Control2 | { \\ BadStyle} 這是要顯示的文字。                                                                                                                            |
| DialogB | Control3 | {&樣式的長度超過72個字元，因此也不能是樣式，即使您在樣式表單中進行管理，也不能是一樣的樣式}這是要顯示的文字。 |
| DialogB | Control4 | 警告 { \\ OKStyle} 這是要顯示的文字。                                                                                                                     |
| DialogB | Control5 | { \\ OKStyle} {&OKStyle} 這是要顯示的文字。                                                                                                                   |
| DialogB | Control6 | { \\ OKStyle 這是要顯示的文字。                                                                                                                             |



 

 (部分) 的[樣式表單](textstyle-table.md)



| 文本 |
|-----------|
| OkStyle   |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



