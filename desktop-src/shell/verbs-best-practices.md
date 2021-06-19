---
description: 瞭解當您在 Windows Shell 中執行自訂檔案格式時，快速鍵功能表處理常式和多個動詞的最佳作法。
title: 快速鍵功能表處理常式和多個動詞的最佳作法
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4D352ECB-6214-4f6e-A3E5-F79E154D090A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 14ec2e8915aa1df47ca21c6436ec963be3f590f5
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396443"
---
# <a name="best-practices-for-shortcut-menu-handlers-and-multiple-verbs"></a>快速鍵功能表處理常式和多個動詞的最佳作法

本主題的組織方式如下：

-   [最佳作法](#best-practices-for-shortcut-menu-handlers-and-multiple-verbs)
    -   [動詞實行的最佳作法](#best-practices-for-verb-implementations)
-   [多重選取動詞的最佳作法](#best-practices-for-multiple-selection-verbs)
    -   [異類選取專案](#heterogenous-selections)
-   [相關主題](#related-topics)

## <a name="best-practices"></a>最佳做法

靜態動詞命令是要執行的最簡單動詞命令，並提供豐富的功能。 強烈建議您使用其中一個靜態動詞方法來執行動詞。

### <a name="best-practices-for-verb-implementations"></a>動詞實行的最佳作法

下列清單代表動詞實行的最佳作法：

-   請一律選擇符合您需求的最簡單動詞方法。
-   盡可能使用靜態動詞方法。
-   請勿在 UI 執行緒上執行需要大量資源的作業或 i/o。 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)和 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)在執行的工作中必須非常保守。 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand) 必須在另一個進程中執行，或者您必須建立新的執行緒，以避免封鎖呼叫者。
-   與獨立軟體廠商 (ISV) 名稱的前置動詞，如下所示 `ISVName.verb` 。 使用不合格的名稱可能會與多個選擇相同動詞名稱的 Isv 產生衝突。
-   一律使用應用程式特定的 ProgID。 由於某些專案類型不會使用此對應，因此需要廠商唯一的名稱。
-   相對於叫用的方法定位 UI，但不在啟動程式執行緒上執行。
-   針對傳遞給 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)方法的標準動詞，請不要接受傳回值 **S \_ OK** 。 這麼做會導致叫用真正的動詞執行失敗，並傳回標準動詞的失敗碼。 如果您不支援標準動詞，則在遇到非零 HIWORD (lpVerb) 值時，會傳回失敗。
-   請避免使用 **rundll32.exe** 作為動詞的主機。
-   在實 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu) 時，請務必使用 ResultFromShort 宏，透過 **HRESULT** 值傳回已新增至功能表的動詞數。
-   如果您在下列其中一個登錄機碼專案上註冊，請小心並務必在最特定的類型上註冊處理常式，以減少可能的非預期結果：
    -   **HKEY \_ 類別 \_ 根目錄\\\***
    -   **HKEY \_ 類別 \_ 根 \\ AllFileSystemObjects**
    -   **HKEY \_ 類別 \_ 根 \\ 資料夾**
    -   **HKEY \_ 類別 \_ 根目錄 \\**
-   只有在您預期您可能需要變更快速鍵功能表中的預設動詞時，才設定 **MayChangeDefaultMenu** 索引鍵。 如果您的處理常式未變更預設的動詞命令，您就不應該設定此索引鍵，因為這樣做會導致系統不必要地載入您的 DLL。
-   將您在 [**IShellExtInit：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellextinit-initialize)中執行的工作降至最低。 針對快速鍵功能表處理常式，請先捕捉傳遞給 **IShellExtInit：： Initialize** 的資料物件，然後在 [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)或 [**ICoNtextMenu：： InvokeCommand**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-invokecommand)中進行處理。

## <a name="best-practices-for-multiple-selection-verbs"></a>多重選取動詞的最佳作法

因為多重選取動詞案例中的專案數可能很大，所以請務必考慮動詞執行的效能含意。 例如，當使用者在 \* 包含大量專案的範圍上搜尋 ""，然後按一下 [ **全選** ] 和 [按一下滑鼠右鍵] 時，就會顯示該動詞中有上千個專案的選取專案。 因此，動詞應該只考慮選取專案中的第一個專案，以及整體專案計數。 第一個專案定義為視圖頂端的專案，或使用者第一次以滑鼠右鍵按一下的專案。

在 Windows 7 和更新版本中，當查詢快捷方式功能表時，傳遞至動詞命令的專案數目限制為16。 然後會重新建立該動詞命令，並在叫用該動詞時，使用完整的選取專案重新初始化。

在某些情況下，請考慮少量的固定專案。 例如，「差異」動詞適用于只考慮前兩個專案的「差異」動詞。 一般而言，您不需要測試選取專案中的每個專案，以查看它是否為特定類型，或查詢選取專案中的每個專案是否有其屬性。 請查看第一個專案，並決定是否適合加入您的動詞。

### <a name="heterogenous-selections"></a>異類選取專案

在多重選取案例中，會自動加入開放式動詞，假設未檢查項目可以由動詞處理。 相反地，當選取範圍包含未檢查項目時，不會加入封閉式動詞，而且只會在專案數目很小的情況下加入。

播放機樣式動詞應該是開放式的，並且以無訊息方式略過未處理的專案。 如果無法對專案採取動作，可能會導致資料遺失或混淆，則動詞應該警告使用者有關無法處理的專案。 例如，「備份」動詞應該表示某些專案無法備份。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[為快捷方式功能表選擇靜態或動態動詞](shortcut-choose-method.md)
</dt> <dt>

[建立快捷方式功能表處理常式](context-menu-handlers.md)
</dt> <dt>

[使用動態動詞自訂快捷方式功能表](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[快捷方式 (內容) 功能表和快捷方式功能表處理常式](context-menu.md)
</dt> <dt>

[動詞和檔案關聯](fa-verbs.md)
</dt> <dt>

[快速鍵功能表參考](context-menu-reference.md)
</dt> </dl>

 

 



