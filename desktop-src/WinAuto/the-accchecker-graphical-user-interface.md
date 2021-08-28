---
title: AccChecker 圖形消費者介面
description: 本主題說明組成 AccChecker GUI 的元素。
ms.assetid: C8C156F6-AB29-4011-9DCD-74261AC17404
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf645a3afd35bdd906d1ab26453d16672311cb4
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473384"
---
# <a name="the-accchecker-graphical-user-interface"></a>AccChecker 圖形消費者介面

本主題說明組成 AccChecker GUI 的元素。

-   [驗證索引標籤](#verifications-tab)
-   [結果索引標籤](#results-tab)
-   [MSAA 和 UIA 螢幕讀取器索引標籤](#msaa-and-uia-screen-reader-tabs)
-   [MSAA 和 UIA 樹狀索引標籤](#msaa-and-uia-tree-tabs)
-   [檔案功能表](#file-menu)
-   [相關主題](#related-topics)

## <a name="verifications-tab"></a>驗證索引標籤

AccChecker 會從 [ **驗證** ] 索引標籤的預設視圖開始：

![顯示 U I 協助工具檢查程式中 [驗證] 索引標籤的螢幕擷取畫面。](images/accchecker-verifications-tab.png)

[ **驗證** ] 索引標籤包含下列元件。

-   **驗證目標選取器** 提供下列選項來選取目標應用程式或控制項。
    -   從預先填入的下拉式清單中選擇目標。 此清單包含啟動時所識別的所有最上層 Hwnd。
    -   根據滑鼠游標的位置選擇 HWND (可選取的控制項會以紅色矩形) 反白顯示。 此選項可讓您選取具有 HWND 的任何可見物件。
    -   輸入特定 HWND。
-   **驗證常式檢查清單** 提供可選取要針對應用程式或控制項執行之所需驗證常式的能力。 如需詳細資訊，請參閱驗證常式。
-   **錯誤和警告隱藏檔案選取器** [驗證 **結果** ] 索引標籤會產生隱藏專案檔。以滑鼠右鍵按一下錯誤或警告訊息，並從內容功能表中選取 [ **隱藏** ]，就會為該訊息設定旗標。 如果選取 [隱藏隱藏] 核取方塊，清單中就會顯示 **隱藏的專案** 。 您可以使用用來隱藏專案的相同內容功能表來非隱藏隱藏的專案。

    隱藏專案檔會以 XML 格式 **儲存，方法是從 [檔案**] 功能表中選取 [**儲存隱藏** 專案]。 在將隱藏訊息的後續驗證執行上，會使用此檔案。 若要移除隱藏專案檔，請按一下 [ **清除**]。 如需特定訊息的詳細資訊，請參閱驗證記錄檔訊息。 使用 [檔案] 功能表 **中的 [** **儲存記錄** 檔]，將整個清單儲存為 XML 格式的記錄檔，或儲存為格式化的文字檔。

    ![反白顯示隱藏內容專案的 [accchecker 結果] 索引標籤](images/accchecker-results-tab-with-suppress.png)

    下列範例顯示在 Windows 防火牆控制台應用程式上執行 **屬性** 驗證所產生之隱藏專案檔的內容。 為此範例中的隱藏專案選擇了識別碼為 "ElementHasNoName" 的錯誤。

    ```XML
    <?xml version="1.0" encoding="utf-8"?><ArrayOfLogEvent xmlns:xsi="https://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="https://www.w3.org/2001/XMLSchema">
      <LogEvent>
        <EventID>ElementHasNoName</EventID>
        <Text>Element has no name</Text>
        <ParentChain>Windows Firewall.Windows Firewall</ParentChain>
        <VerificationRoutine>VerificationRoutines.CheckName</VerificationRoutine>
        <Classname>ATL:BUTTON</Classname>
        <AccName />
        <AccRole>PushButton</AccRole>
      </LogEvent>
    </ArrayOfLogEvent>
    ```

    

-   **顯示優先順序的結果** 提供下列選項，以依優先順序篩選驗證結果。
    -   **全部** 包含所有的結果（不論優先順序為何）。
    -   **僅 P1** 只包含優先順序0和優先順序1的結果。
    -   **僅 P1 P2** 包含優先順序0到優先順序2結果。
-   **執行選取的驗證** 提供啟動驗證程式的 [ **執行驗證** ] 按鈕。 當驗證正在執行時，按鈕會變更為 [ **取消驗證** ]，並可用來在目前的驗證完成後停止驗證。

## <a name="results-tab"></a>結果索引標籤

[ **結果** ] 索引標籤會在選取的驗證工作完成後填入。 它是由下列元件所組成。

-   此清單會顯示選取的驗證工作所產生的錯誤、警告和資訊訊息。 您可以使用訊息清單上方的核取方塊，依類型篩選顯示的訊息。
-   驗證目標的訊息詳細資料和螢幕擷取畫面。 從郵寄清單中選取訊息會顯示更多詳細資料，並在 [螢幕擷取畫面] 窗格中反白顯示對應的元素。 [ **視覺化** ] 按鈕會將 AccChecker 切換至 [ **MSAA 樹** ] 索引標籤。如果在 [ **結果** ] 索引標籤上反白顯示錯誤，則會在 [ **MSAA 樹** ] 索引標籤上反白顯示對應專案。

以滑鼠右鍵按一下訊息，會顯示具有下列專案的內容功能表。

-   **隱藏** 將訊息新增至隱藏清單。
-   **複製到剪貼** 簿將訊息詳細資料複製到剪貼簿。
-   **視覺化** 將 AccChecker 切換至 [ **MSAA 樹** ] 索引標籤。會反白顯示對應至所選錯誤的專案。
-   說明顯示訊息的其他相關資訊。

## <a name="msaa-and-uia-screen-reader-tabs"></a>MSAA 和 UIA 螢幕讀取器索引標籤

MSAA 螢幕讀取器和 [UIA 螢幕讀取器] 索引標籤很類似。 這兩者都會顯示幕幕讀取器在驗證目標的模擬遍歷中遇到的元素文字記錄，不同之處在于它會顯示 MSAA 的執行，另一個則顯示 UIA 實作此實作。

專案的流覽和記錄方式，就像螢幕讀取器一樣。 此索引標籤上所顯示的資訊，是確認只會宣告有用和相關資訊的必要資訊。 例如，可以接受一般發音的控制項名稱，例如「MenuItem 編輯」或「按鈕關閉」。但是，無法接受沒有意義的控制項名稱，例如 "CPNavPanel22" 或 "DefaultValue1"。 [ **視覺化** ] 按鈕會使 AccChecker 切換至 [ **MSAA 樹狀結構** ] 或 [ **UIA 樹** ] 索引標籤。如果專案在 [ **螢幕閱讀** 程式] 索引標籤上反白顯示，則會在 [ **MSAA 樹狀目錄** ] 或 [ **UIA 樹** ] 索引標籤上反白

您必須在 [**驗證**] 索引標籤中選取 [**一致性**] 下的 [ **ScreenReader** ] 驗證常式，才能顯示 [ **MSAA 螢幕閱讀程式]** 索引標籤 同樣地，您必須選取 [ **UiaScreenReader** ] 驗證常式，才能顯示 [ **UIA 螢幕閱讀** 程式] 索引標籤。

下列螢幕擷取畫面顯示 [UIA 螢幕閱讀程式] 索引標籤，其中包含記事本驗證範例。

![顯示範例驗證結果的 [accchecker 螢幕讀取器] 索引標籤](images/accchecker-screen-reader-tab.png)

## <a name="msaa-and-uia-tree-tabs"></a>MSAA 和 UIA 樹狀索引標籤

執行任何驗證常式都會使 AccChecker 編譯驗證目標中所有可見的元素，並以階層方式顯示在 [ **MSAA 樹**] 索引標籤和 [ **UIA 樹**] 索引標籤上。下列螢幕擷取畫面顯示 [MSAA 樹] 索引標籤，其中包含記事本的元素階層。

![accchecker msaa 樹狀結構索引標籤](images/accchecker-tree-tab.png)

## <a name="file-menu"></a>檔案功能表




| 功能表 | 命令 | 描述 | 
|------|---------|-------------|
| <strong>File</strong>$ {REMOVE} $<br /> | <strong>開啟</strong> | 提供下列選項。<br /><ul><li><strong>驗證 DLL</strong> 開啟驗證 DLL。 原生 AccChecker 驗證會封裝在獨立 DLL (VerificationRoutines.dll) 中。 這項設計可讓測試小組根據所測試的 UI 平臺來建立自己的一組驗證。</li><li><strong>記錄</strong> 檔可讓您選擇要開啟的驗證記錄檔。</li></ul> | 
| <strong>自動載入可用的驗證</strong> | 自動載入所有可用的 AccChecker 驗證。 | 
| <strong>儲存記錄檔</strong> | 將驗證記錄檔儲存為 XML 或純文字。 純文字較容易閱讀。 | 
| <strong>儲存隱藏專案</strong> | 將隱藏專案記錄儲存為 XML。 此檔案會指定要在迴歸測試中忽略的驗證訊息。 | 
| <strong>結束</strong> | 關閉 AccChecker 工具。 | 
| <strong>驗證</strong>$ {REMOVE} $<br /> | <strong>立即執行</strong> | 依所選驗證目標執行指定的驗證常式。 | 
| <strong>全部啟用</strong> | 檢查所有的驗證常式核取方塊。 | 
| <strong>全部停用</strong> | 取消核取 [所有驗證常式] 核取方塊。 | 
| <strong>選項</strong> | <strong>Always On Top</strong> | 讓 AccChecker 成為迭置順序的最上層視窗。 | 
| <strong>Help</strong>$ {REMOVE} $<br /> | <strong>說明</strong> | 顯示說明資訊。 | 
| <strong>關於</strong> | 顯示 AccChecker 版本和電子郵件地址，以便與 Microsoft 聯絡 AccChecker。 | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[UI 協助工具檢查程式](ui-accessibility-checker.md)
</dt> </dl>

 

 





