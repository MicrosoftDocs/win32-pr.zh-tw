---
title: 管理參考計數的規則
description: 使用參考計數來管理物件的存留期，可讓多個用戶端取得和釋放單一物件的存取權，而不需要在管理物件的存留期時彼此協調。
ms.assetid: bbe7d16c-fcb7-474d-a22d-5a3b33dd800e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9520cbbc88cb73c6e2abbd7908bed3754bb3945
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382922"
---
# <a name="rules-for-managing-reference-counts"></a>管理參考計數的規則

使用參考計數來管理物件的存留期，可讓多個用戶端取得和釋放單一物件的存取權，而不需要在管理物件的存留期時彼此協調。 只要用戶端物件符合特定的使用規則，物件實際上就會提供這項管理。 這些規則會指定如何管理物件間的參考。  (COM 不會指定物件的內部執行，不過這些規則是物件內原則的合理起點。 ) 

就概念而言，介面指標可視為位於指標變數內，這些變數包含所有保留介面指標的內部計算狀態。 這會包含記憶體位置、內部處理器暫存器中的變數，以及程式設計人員產生和編譯器產生的變數。 指派給指標變數或將其初始化，需要建立已存在之指標的新複本。 其中某個變數中有一個指標複本 (指派/初始化) 中所使用的值，現在有兩個。 指標變數的指派會終結目前變數中的指標複製，如同變數本身的終結。  (也就是已終結變數的範圍，例如堆疊框架。 ) 

從 COM 用戶端的觀點來看，一律會針對每個介面進行參考計數。 用戶端絕對不應假設物件對所有介面都使用相同的計數器。

預設的情況是必須針對每個介面指標的新複本呼叫 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) ，而且必須針對介面指標的每個終結來呼叫 [**版本**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) ，除非下列規則允許的情況：

-   **函數的 out 參數。** 呼叫端必須在參數上呼叫 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) ，因為當 out 值儲存在其上方時，將會在執行程式碼中釋放 (的 [**發行**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)) 呼叫。
-   **提取全域變數。** 從全域變數中現有的指標複本建立介面指標的本機複本時，您必須在本機複本上呼叫 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) ，因為當本機複本仍然有效時，另一個函數可能會損毀全域變數中的複本。
-   **新的指標，合成「超薄空氣」。** 使用特殊內部知識會合成介面指標的函式，而不是從其他來源取得介面指標，必須一開始就在新合成的指標上呼叫 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 。 這類常式的重要範例包括實例建立常式、 [**QueryInterface**](/windows/desktop/api/Unknwn/nf-unknwn-iunknown-queryinterface(q))的執行等等。
-   **正在抓取內部儲存指標的複本。** 當函式抓取由呼叫的物件在內部儲存的指標複本時，該物件的程式碼必須在函式傳回之前呼叫指標上的 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 。 一旦已抓取指標，原始物件就沒有其他方法可判斷其存留期與內部儲存之指標複本的相關程度。

預設情況的唯一例外狀況是，管理程式碼必須知道物件的兩個或多個複本之存留期的關聯性，並藉由允許其參考計數移至零來確定物件未終結。 通常有兩種情況，如下所示：

-   當指標的其中一個複本已存在，且後續建立第二個複本，然後在第一個複本仍然存在時終結，則可以省略第二個複本的 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 和 [**Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)呼叫。
-   當有一份指標存在並建立第二個複本，然後在第二個複本上被終結時，就會省略第二個複本的 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref)呼叫，並在第二個複本 [**釋放**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 。

以下是這些情況的特定範例，前兩個特別常見：

-   **函數中的參數。** 當做參數傳遞至函式之介面指標的複本存留期，會以用來初始化值之指標的形式進行嵌套，因此，不需要在參數上有個別的參考計數。
-   **函數中的 Out 參數，包括傳回值。** 若要設定 out 參數，函式必須有介面指標的穩定複本。 傳回時，呼叫端會負責釋放指標。 因此，out 參數不需要個別的參考計數。
-   **區域變數。** 方法執行可控制堆疊框架上所配置之每個指標變數的存留期，並且可以用來判斷如何省略多餘的 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) / [**發行**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release)組。
-   **Backpointers.** 某些資料結構包含兩個物件，每個物件都有指向另一個的指標。 如果已知第一個物件的存留期包含第二個物件的存留期，則在第一個物件的第二個物件指標上不需要有參考計數。 通常，避免這個迴圈對於維護適當的解除配置行為相當重要。 不過，微調指標應謹慎使用，因為處理遠端處理的作業系統部分無法得知此關聯性。 因此，在幾乎所有情況下，讓 backpointer 看到第一個指標的第二個 "friend" 物件 (因此避免迴圈) 是慣用的解決方案。 例如，COM 的可連線物件架構會使用這種方法。

當您在執行或使用參考計數的物件時，套用 *人工參考計數* 可能會很有用，這可保證處理函式期間的物件穩定性。 在執行介面的方法時，您可能會呼叫有機會將您的參考計數遞減至物件的函式，而導致物件過早釋放和執行失敗。 若要避免這種情況，最好的方法是在方法執行的開頭插入 [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 的呼叫，並將它與在方法傳回之前的 [**版本**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 呼叫配對。

在某些情況下， [**AddRef**](/windows/win32/api/unknwn/nf-unknwn-iunknown-addref) 和 [**發行**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) 的傳回值可能不穩定，因此不應該依賴;它們只能用於偵測或診斷用途。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[透過參考計數來管理物件存留期](managing-object-lifetimes-through-reference-counting.md)
</dt> </dl>

 

 