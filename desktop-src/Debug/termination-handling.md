---
description: 終止處理常式可確保每當控制流程離開特定的受防護程式碼主體時，就會執行特定的程式碼區塊。 終止處理常式是由下列元素所組成。
ms.assetid: 899e2939-e028-4be1-9f08-9a79bf97eb37
title: 終止處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b23e2c81465ab9d469d3d5c503c12f5bf1c7a333507d302f3e5639e0158834e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119292957"
---
# <a name="termination-handling"></a>終止處理

*終止處理常式* 可確保每當控制流程離開特定的受防護程式碼主體時，就會執行特定的程式碼區塊。 終止處理常式是由下列元素所組成。

-   受保護的程式碼主體
-   當控制流程離開受防護主體時要執行的終止程式碼區塊

終止處理常式是以特定語言的語法來宣告。 使用 Microsoft c/c + + 優化編譯器時，它們會使用 **\_ \_ try** 和 **\_ \_ finally** 來執行。 如需詳細資訊，請參閱 [處理常式語法](handler-syntax.md)。

受保護的程式碼主體可以是程式碼區塊、一組嵌套區塊，或整個程式或函式。 每當執行受保護的主體時，就會執行終止程式碼區塊。 唯一的例外是當執行緒在執行受防護主體期間終止時 (例如，如果從受防護主體) 內呼叫 [**ExitThread**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitthread) 或 [**ExitProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-exitprocess) 函數。

當控制權的流程離開受保護的主體時，就會執行終止區塊，不論受防護主體是否正常終止或異常。 當區塊中的最後一個語句執行時，會將受保護的主體視為正常終止，並且控制順序進入終止區塊。 當控制流程因為例外狀況而離開受保護主體，或由於 **return**、 **goto**、 **break** 或 **continue** 等控制語句而離開受保護主體時，就會發生異常終止。 您可以從終止區塊內呼叫 [**AbnormalTermination**](abnormaltermination.md) 函式，以判斷受防護主體是否正常終止。

 

 
