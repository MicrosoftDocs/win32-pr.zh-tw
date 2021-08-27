---
title: 類型屬性
description: 遠端程序呼叫 (RPC) ，以及可套用至型別宣告的 MIDL 型別屬性。
ms.assetid: cd7fd582-6162-4154-9dff-6c86c344b9ae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5da8f3beb62f443b95a42283d4625200812436bce1bc667edc07d68f2542544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011166"
---
# <a name="type-attributes"></a>類型屬性

型別屬性是可套用至型別宣告的 MIDL 屬性：

-   **\[**[**處理**](/windows/desktop/Midl/handle)**\]**
-   **\[**[**內容 \_ 控制碼**](/windows/desktop/Midl/context-handle)**\]**
-   **\[**[**切換 \_ 類型**](/windows/desktop/Midl/switch-type)**\]**
-   [指標類型屬性](three-pointer-types.md)

**\[ Switch \_ type \]** 屬性會指定聯集鑒別子的類型。 這個屬性只適用于 nonencapsulated 聯集。

內容控制碼是具有 **\[ 內容 \_ 控制碼 \]** 屬性的指標。 **\[ 內容 \_ 控制碼 \]** 屬性可讓您撰寫程式，以便在遠端程序呼叫之間維護狀態資訊。 具有非 null 值的內容控制碼代表儲存的內容，而且有兩個用途：

-   在用戶端上，它包含 RPC 執行時間程式庫將呼叫導向伺服器所需的資訊。
-   在伺服器端，它會作為作用中內容的控制碼。

**\[** [**Handle**](/windows/desktop/Midl/handle) **\]** 屬性指定型別可以做為使用者定義的 (泛型) 控制碼來進行。 這項功能允許設計對應用程式有意義的控制碼。 使用者必須提供系結和解除系結常式，才能在使用者定義的控制碼類型與 RPC 基本控制碼類型之間轉換， **處理 \_ t**。 基本控制碼包含對 RPC 執行時間程式庫有意義的目的地資訊。 使用者定義控制碼只能在類型宣告中定義，而不能定義在函式宣告中。 具有 **\[ handle \]** 屬性的參數具有雙重用途。 它是用來判斷呼叫的系結，而且會以一般資料參數的形式傳送至呼叫的程式。

 

 