---
title: 陣列和 Sized-Pointer 屬性
description: MIDL 提供一組豐富的功能，可傳遞資料的陣列和指向資料的指標。 您可以使用這些屬性來指定陣列的特性以及多個指標層級。
ms.assetid: 482be83f-eb09-40a0-8dd6-a0cbf5dc4485
keywords:
- IDL MIDL、屬性、陣列和大小指標
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0f9ba435d5c413ea152c2bc9b492486ccc1be94
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842191"
---
# <a name="array-and-sized-pointer-attributes"></a>陣列和 Sized-Pointer 屬性

MIDL 提供一組豐富的功能，可傳遞資料的陣列和指向資料的指標。 您可以使用這些屬性來指定陣列的特性以及多個指標層級。



| 屬性                       | 使用方式                                                                                                                                                                                                |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**大小 \_ 為**](size-is.md)     | 指定要配置給大小指標的記憶體數量、調整大小指標大小的指標，以及單一或多維度陣列。                                                         |
| [**最大值 \_ 為**](max-is.md)       | 陣列索引的最大值。                                                                                                                                                                |
| [**長度 \_ 為**](length-is.md) | 要傳送的陣列元素數目。                                                                                                                                                      |
| [**第一個 \_ 是**](first-is.md)   | 要傳送之第一個陣列元素的索引。                                                                                                                                              |
| [**last \_**](last-is.md)     | 提供要傳送之最後一個陣列元素的索引。                                                                                                                                         |
| [**字串**](string.md)        | 指出一維 [**char**](char-idl.md)、 [**wchar \_ t**](wchar-t.md)、 [**byte**](byte.md) (或對等的) 陣列，或是這類陣列的指標，會以字串的形式處理。 |
| [**範圍**](range.md)          | 指定引數或欄位的允許值範圍，其值會在執行時間設定。                                                                                                       |



 

MIDL 支援三種指標：參考指標、唯一指標和完整指標。 這些指標是由指標屬性 [**ref**](ref.md)、 [**unique**](unique.md)和 [**ptr**](ptr.md)所指定。

指標屬性可以套用為型別屬性;作為套用至結構成員、等位成員或參數的欄位屬性;或作為套用至函式傳回型別的函式屬性。 指標屬性也可以與 [**指標 \_ default**](pointer-default.md) 關鍵字一起出現。

若要允許指標參數在遠端函式期間變更值，您必須提供多個指標宣告子，以提供另一個間接取值層級。 套用至參數的明確指標屬性只會影響參數最右邊的指標宣告子。 如果在參數宣告中有多個指標宣告子，則其他宣告子會預設為 [**指標 \_ 預設**](pointer-default.md) 屬性所指定的指標屬性。 若要將不同的指標屬性套用至多個指標宣告子，您必須定義指定明確指標屬性的中繼類型。

## <a name="default-pointer-attribute-values"></a>預設 Pointer-Attribute 值

當沒有指標屬性與參數的指標相關聯時，會假設指標是 [**ref**](ref.md) 指標。

當沒有指標屬性與結構或等位成員的指標相關聯時，MIDL 編譯器會使用下列優先順序規則指派指標屬性 (1 為最高) ：

1.  明確套用至指標類型的屬性
2.  明確套用至指標參數或成員的屬性
3.  IDL 檔案中定義類型的 [**指標 \_ default**](pointer-default.md) 屬性
4.  匯入類型之 IDL 檔案中的 [**指標 \_ 預設**](pointer-default.md) 屬性
5.  [**ptr**](ptr.md) (憑證模式) ; [**唯一**](unique.md) (Microsoft RPC 預設模式) 

在預設模式下編譯 IDL 檔案時，匯入的檔案可以從匯入檔案繼承指標屬性。 當您使用/[**憑證**](-osf.md) 參數進行編譯時，無法使用這項功能。 如需詳細資訊，請參閱匯 [**入**](import.md)。

## <a name="function-return-types"></a>函數傳回類型

函數所傳回的指標必須是 [**唯一**](unique.md) 指標或完整指標。 如果函式結果是參考指標（明確地或預設值），MIDL 編譯器會回報錯誤。 傳回的指標一律表示新的儲存體。

傳回指標值的函式可以將指標屬性指定為函數屬性。 如果指標屬性不存在，則函式結果指標會使用提供的值做為 [**指標 \_ 預設**](pointer-default.md) 屬性。

## <a name="pointer-attributes-in-type-definitions"></a>類型定義中的指標屬性

當您在 [**typedef**](typedef.md) 語句的最上層指定指標屬性時，會如預期般將指定的屬性套用至指標宣告子。 如果未指定指標屬性，在使用時，typedef 語句最上層的指標宣告子會繼承指標屬性型別。

DCE IDL 不允許明確地套用相同的指標屬性，例如在 [**typedef**](typedef.md) 宣告和參數屬性清單中都有兩次。 當您使用 MIDL 編譯器的預設 (Microsoft 擴充功能) 模式時，會放寬此條件約束。

如需在遠端程序呼叫中使用 MIDL 陣列和指標的討論，請參閱 [陣列和指標](/windows/desktop/Rpc/arrays-and-pointers)。

 

 