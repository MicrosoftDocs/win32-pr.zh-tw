---
title: COM (COM) 中的錯誤處理
description: COM 中的錯誤處理
ms.assetid: 15f3ae3e-1794-4948-a7aa-6309a703364b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7953a970e470f5ae2c04b6a22c07f1de4fe663b100485732050b13c12a00b559
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119381908"
---
# <a name="error-handling-in-com-com"></a>COM (COM) 中的錯誤處理

幾乎所有的 COM 函數和介面方法都會傳回類型 **HRESULT** 的值。 *結果控制碼* 的 **HRESULT** (，) 是傳回成功、警告和錯誤值的方法。 **HRESULT** 其實不會處理任何事項;它們只是值中有數個欄位編碼的值。 根據 COM 規格，零的結果表示成功，而非零的結果表示失敗。

在原始程式碼層級，所有錯誤值都包含三個部分，以底線分隔。 第一個部分是識別與錯誤相關聯之設備的前置詞，第二個部分是 E 表示錯誤，而第三個部分是描述實際條件的字串。 例如，當硬碟上沒有剩餘空間時，就會傳回 **Stg. \_ E \_ MEDIUMFULL** 。 **Stg.** 前置詞表示儲存設備， **E** 表示狀態碼代表錯誤，而 **MEDIUMFULL** 則會提供有關錯誤的特定資訊。 您可能想要從介面方法或函式傳回的許多值都是在 Winerror.h 中定義。

如需有關錯誤處理的詳細資訊，請參閱下列各節：

-   [COM 錯誤碼的結構](structure-of-com-error-codes.md)
-   [設備 ITF 中的代碼 \_](codes-in-facility-itf.md)
-   [使用宏進行錯誤處理](using-macros-for-error-handling.md)
-   [JAVA 和 Visual Basic 中的 COM 錯誤處理](com-error-handling-in-java-and-visual-basic.md)
-   [錯誤處理策略](error-handling-strategies.md)
-   [處理未知的錯誤](handling-unknown-errors.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 錯誤碼](com-error-codes.md)
</dt> </dl>

 

 




