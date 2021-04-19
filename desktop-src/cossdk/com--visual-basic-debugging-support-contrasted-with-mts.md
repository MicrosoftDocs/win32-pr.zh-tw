---
description: COM + Visual Basic 支援與 MTS 對比
ms.assetid: aa012f88-1f88-4c7f-b774-82b9e29da5e9
title: COM + Visual Basic 支援與 MTS 對比
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 038b29bbc6fbe5c8375f91f0006b85940f00b944
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971139"
---
# <a name="com-visual-basic-debugging-support-contrasted-with-mts"></a>COM + Visual Basic 支援與 MTS 對比

COM + 移除或減少使用 Microsoft Visual Basic 6.0 和 MTS 進行偵錯工具的幾項限制。 下列清單摘要說明 COM + 所能預期的變更：

-   多個元件的偵錯工具：在 COM + 中，您可以在其中一個 IDE 實例中執行的用戶端呼叫任何數目的 Dll，以做為專案群組。 群組 DLL 專案中的物件可以任意地呼叫彼此，並視需要將內容流動。 當然，這也適用于當 Dll 和用戶端位於相同的 IDE 實例中的相同專案群組時。

-   \_使用 com + 來偵測類別 initialize 和 class \_ terminate 事件的限制：您可以使用 com + 將程式碼放在 \_ \_ com + 應用程式元件的類別 initialize 和 class terminate 事件中，即使該程式碼嘗試存取物件或其對應的內容物件。 您可以在該處設定中斷點，並使用監看式。 您也可以在類別終止事件中設定中斷點 \_ 。

    雖然不再需要作為因應措施，但如果您需要在啟動和關閉元件期間執行程式碼，您仍然可以執行 [**IObjectControl**](/windows/desktop/api/ComSvcs/nn-comsvcs-iobjectcontrol) 介面並 [**使用其啟動**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-activate) 和 [**停用**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-deactivate) 方法。 您現在也可以在程式碼中，將中斷點放在 **停用** 或 [**CanBePooled**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontrol-canbepooled) 方法的程式碼中。

-   監看 MTS 物件：使用 COM +，您可以為 COM + 所傳回的物件變數加入監看式，包括 [**SafeRef**](/windows/desktop/api/ComSvcs/nf-comsvcs-saferef)、 [**GetObjectCoNtext**](/windows/desktop/api/ComSvcs/nf-comsvcs-getobjectcontext)和 [**IObjectCoNtext：： CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-createinstance) 方法的傳回值。

-   當元件失敗時，系統會增加穩定性-在 COM + 中，元件失敗不會再停止 Visual Basic (，這會在與所) 的調試元件相同的進程中執行。 例如，支援即時 (JIT) 重新開機失敗現在可讓您在進行偵錯工具時查看物件內容。

-   偵錯工具可能會重新啟用 COM + 所發行的物件—如同使用 MTS 一樣，Visual Basic 6.0 可能會在您透過用戶端進行單一步驟的偵錯工具時，重新啟用 COM + 物件。 基於 Visual Basic 6.0 探索物件相關資訊的方式，這是預期的行為。 例如，請參考下列程式碼：

    ``` syntax
    Dim obj As Object
    Set obj = CreateObject("MyApp.MyClass")
    obj.Test  'Call the user-defined subroutine named Test.
    Set obj = Nothing
    ```

    如果為 obj。測試方法呼叫 [**IObjectCoNtext：： SetComplete**](/windows/desktop/api/ComSvcs/nf-comsvcs-iobjectcontext-setcomplete)，com + 立即釋出記憶體中的 obj，但是 obj 尚未設定為 Nothing。 當是 obj 時。測試會傳回，Visual Basic 偵錯工具會針對 [**IProvideClassInfo**](/windows/desktop/api/ocidl/nn-ocidl-iprovideclassinfo)介面呼叫 obj 上的 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) 。 與 obj 相關聯的內容包裝函式會建立新的 MyApp 實例，以服務 **QueryInterface** 呼叫。 如此一來，您就會在偵錯工具中的 obj 之後看到未初始化的物件。已傳回測試。 此物件只會出現在偵錯工具中，並由後續指令移除，以將 obj 設為 Nothing。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[已編譯的 Visual Basic 元件的調試](debugging-compiled-visual-basic-components.md)
</dt> <dt>

[Visual Basic IDE 中的調試](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 
