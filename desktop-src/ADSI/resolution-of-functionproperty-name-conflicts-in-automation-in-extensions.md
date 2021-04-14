---
title: 函數/屬性名稱在延伸模組中的自動化衝突
description: 在本主題中，\ 0034; object \ 0034;表示以 ADSI 用戶端為物件進行流覽的整個物件。 也就是 ADSI 及其所有副檔名。
ms.assetid: 76207326-879e-408b-8004-06d940401a41
ms.tgt_platform: multiple
keywords:
- 函數和屬性名稱在延伸模組中的自動化衝突
- 擴充功能 ADSI，解決函式和屬性名稱在自動化中的衝突
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9a7ac99b99ecdf0ee1b940f066d9e8166a15542
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104382849"
---
# <a name="resolution-of-functionproperty-name-conflicts-in-automation-in-extensions"></a>函數/屬性名稱在延伸模組中的自動化衝突

在本主題中，「物件」會以 ADSI 用戶端的形式來表示整個物件。 也就是 ADSI 及其所有副檔名。

## <a name="same-function-name-with-the-same-parameters"></a>具有相同參數的相同函式名稱

如果物件中有兩個以上的雙重 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面支援相同名稱的屬性或方法（例如， **Func1**），則會使用下列準則來判斷調用。 如果用戶端有一個可支援稱為 **Func1** 之方法的雙重介面指標，而且如果 Automation 環境支援 vtable 存取，則會直接透過 ADSI vtable 存取來叫用 **Func1** 。

如果上述任一條件為 false，則會呼叫 [**IDispatch：： GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) 和 [**Idispatch：： invoke**](/windows/win32/api/oaidl/nf-oaidl-idispatch-invoke) 來叫用 **Func1**。

如需有關用戶端如何新增雙重介面指標的詳細資訊，以及有關支援 vtable 存取之環境類型的說明，請參閱 [ADSI 擴充模型中的晚期繫結與 Vtable 存取](late-binding-vs--vtable-access-in-the-adsi-extension-model.md)。

由於所有的擴充物件都會將 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 函式重新導向至匯總工具，因此匯總工具會控制要叫用的 **Func1** 。 這些規則包括：

-   如果有任何介面，且匯總工具 (ADSI) 中只有一個介面，則會支援稱為 **Func1** 的函式，而匯總工具會叫用它自己的 **Func1**。
-   否則，匯總工具會依登錄中列出的順序，逐一查看其每個擴充功能，並尋找第一個執行名為 **Func1** 函式的擴充功能。 此第一個延伸模組中的多個雙重 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面可能會有一個稱為 **Func1** 的函式，但可能不太可能。 延伸模組必須決定要在自動化中叫用的 **Func1** 。

## <a name="same-function-name-with-different-parameters"></a>具有不同參數的相同函式名稱

上一節討論了如何解決函式名稱衝突，也就是在自動化中發生的函式名稱與相同參數清單的函式名稱，例如 number、type 和 order。 如果兩個函式的名稱相同但參數不同，該怎麼辦？ 如果 ADSI 用戶端使用 [**IDispatch：： GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) 叫用函式，而不使用多個名稱來指定參數，adsi 擴充功能模型就無法區分這些函式。 根據上面討論的解決方式，登錄中透過其中一個介面支援此函式的第一個擴充功能，會叫用此函式的版本，而呼叫可能會失敗或產生不正確的結果。

例如：

-   Extn1 (在 [類別 CA] 下的登錄中優先-優先順序較高) 支援 **IInterface1**。
-   Extn2 類別下登錄中的第三個 (第三個-低優先順序) 支援 **IInterface2**。
-   **IInterface1** 支援 **Method1 (int param1，int param2)**。
-   **IInterface2** 支援 **Method1 (int param1)**。

ADSI 用戶端具有類別 CA 物件的 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) 介面指標。 它想要叫用 **IInterface2：： Method1**。 如果用戶端呼叫「pDispatch->GetIDsOfNames (IID \_ Null、rgszNames、1、MY \_ LCID、rgDispId) 」，只要在 *Method1 \[ 0 \]* 中儲存函式名稱 "rgszNames"，就會叫用 **IInterface1：： Method1** ，而不是使用所需的 **IInterface2：： Method1** ，而且此函式會失敗，因為參數數目不同。

為了將這個問題降至最低，延伸模組開發人員可以在其函式名稱前面加上其專屬的識別碼，並避免使用相同名稱但不同參數之函式的介面設計。

如果發生名稱衝突，即使介面是雙重介面，ADSI 用戶端仍可直接進行 vtable 存取，以避免此問題。 如果無法進行直接 vtable 存取，ADSI 用戶端應該使用多個名稱來呼叫 [**IDispatch：： GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) ，並指定函式名稱，以及先前所述的陣列 *rgszNames* 中的參數。

Visual Basic 5 不會使用多個名稱來呼叫 [**IDispatch：： GetIDsOfNames**](/windows/win32/api/oaidl/nf-oaidl-idispatch-getidsofnames) 函數。 也就是說，它只會將函式名稱傳遞給 **GetIDsOfNames**，而不會傳遞引數。 不過，Visual Basic 5 可讓使用者藉由直接 vtable 存取來叫用函式，而不是叫用 **IDispatch：： GetIDsOfNames** 函數（如果介面是雙重介面）。 開發人員應該盡可能使用直接 vtable 存取。

如需名稱衝突解決方式的詳細資訊，請參閱 [解析函數名稱衝突的範例](example-for-resolving-function-name-conflicts.md)。

 

 