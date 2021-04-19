---
description: 本主題指出當您開發 COM + 元件時，要牢記在心的幾個錯誤處理策略。
ms.assetid: 1ae5875b-8085-44f2-9071-c2a5d7543ac1
title: 在 COM + 中處理錯誤的策略
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91ca64546683fa45ac8df3bcb47534d8de482798
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970914"
---
# <a name="strategies-for-handling-errors-in-com"></a>在 COM + 中處理錯誤的策略

本主題指出當您開發 COM + 元件時，要牢記在心的幾個錯誤處理策略。

-   **針對所有元件介面中的所有方法，傳回 HRESULT 值。**  COM + 會使用 **HRESULT** 值來報告任何在進行函式呼叫或介面方法呼叫時的錯誤。 **HRESULT** 指出方法是否成功或失敗，並識別與錯誤相關聯的設備，例如 RPC、WIN32 或 ITF，以取得介面特定的錯誤。 此外，系統 Api 也提供從 **HRESULT** 查閱到描述錯誤狀況的字串。 使用傳回 **HRESULT** 值的方法是妥善撰寫元件的基礎，而且對偵錯工具而言很重要。 Microsoft Visual Basic 會自動以 **HRESULT** 作為傳回來定義每個方法。 在 Microsoft Visual C++ 中，您必須明確傳回 **HRESULT**。 如需 Hresult 的詳細資訊，請參閱 [COM 錯誤碼的結構](/windows/desktop/com/structure-of-com-error-codes)。
-   **依您的開發工具提供的任何方式起始 ErrorInfo 集合物件。** [**ErrorInfo**](errorinfo.md) 集合物件通常稱為 COM 例外狀況，因為它們允許物件傳遞 (或擲回) 豐富的錯誤資訊給其呼叫者，甚至是跨多個範圍的界限。 此泛型錯誤物件的值是它會補充 HRESULT，並擴充您可以傳回給呼叫者的錯誤資訊類型。 每個 **ErrorInfo** 集合物件會傳回內容描述、錯誤的來源，以及產生錯誤之方法的介面識別碼。 您也可以在說明檔中包含專案的指標。 Automation 提供三個介面來管理 error 物件。 您的元件必須執行 **ISupportErrorInfo** 自動化介面，以通告其對 **ErrorInfo** 集合的支援。 當發生錯誤時，元件會使用 **ICreateErrorInfo** Automation 介面初始化 error 物件。 當呼叫端檢查 HRESULT 並探索方法呼叫失敗時，它會查詢物件以查看它是否支援 **ErrorInfo** 集合。 如果有的話，呼叫端會使用 **IErrorInfo** Automation 介面來取得錯誤資訊。 Visual Basic 程式設計人員可以輕鬆地存取 **ErrorInfo** 集合物件，此物件是透過 Err 物件公開。 您可以使用錯誤引發函數引發錯誤，並使用 **On Error** 語句攔截錯誤。 Visual Basic 執行時間層會為您處理對應。 如果您使用 Visual C++ COM 編譯器支援，您可以使用 \_ com \_ 引發 \_ 錯誤類別來報告錯誤，並使用 \_ com \_ 錯誤類別來取得錯誤資訊。 COM + 不會將傳統 c + + 例外狀況傳播為擴充的 **IErrorInfo** 資訊。 如需有關 **ErrorInfo** 集合物件的詳細資訊，請參閱自動化指南中的「錯誤處理」。
    > [!Note]  
    > COM 要求所有的 [**ErrorInfo**](errorinfo.md) 集合物件以傳值方式封送處理，表示執行 **IErrorInfo** Automation 介面的元件也必須執行和支援 [**IMarshal**](/windows/desktop/api/objidl/nn-objidl-imarshal) 介面。 **IMarshal** 介面執行必須支援元件的傳值封送處理。

     

-   **使用交易來管理共用資源失敗。** 當您使用狀態管理的資源管理員時，自動交易可大幅減少您必須撰寫的錯誤處理常式代碼數量。 不過，交易並不會完全免除錯誤處理的需求。 您仍然需要從介面方法傳回錯誤碼，並檢查呼叫者內的錯誤碼，以避免對註定失敗交易執行不必要的工作。 如需結合錯誤處理與交易處理的詳細資訊，請參閱藉 [由通知根物件來加速交易](speeding-transactions-by-notifying-the-root-object.md)。
-   **明確引發錯誤。** 除非物件明確引發錯誤，否則請避免讓錯誤資訊離開物件。 攔截所有工具產生的錯誤，並在您的元件程式碼中處理這些錯誤。 至少要包含標準處理常式，以一致的方式報告未預期的錯誤。
-   **使用設備 \_ ITF 的錯誤範圍來報告介面特定的錯誤。** 介面特定的錯誤應該在 \_ 0x0200 與0xffff 之間的設備 ITF 範圍內。 您可以在 Visual Basic 中將自訂錯誤碼定義為 vbObjectError 的位移。 使用 \_ c + + 中的「建立 HRESULT」宏來引入介面特定的錯誤碼，如下列範例所示：

    ``` syntax
    const HRESULT ERROR_NUMBER = MAKE_HRESULT (SEVERITY_ERROR, FACILITY_ITF, 10);
    ```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[錯誤隔離和 Failfast 原則](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[找出錯誤的來源](finding-the-source-of-an-error.md)
</dt> <dt>

[COM + 如何修改傳回值](how-com--modifies-return-values.md)
</dt> <dt>

[解讀錯誤碼](interpreting-error-codes.md)
</dt> <dt>

[疑難排解](troubleshooting.md)
</dt> </dl>

 

 
