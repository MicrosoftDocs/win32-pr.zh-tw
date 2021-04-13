---
title: 修改 Echo 對話資源
description: 修改 Echo 對話資源
ms.assetid: 2a371004-82a5-42fb-b19c-ea1928a122a1
keywords:
- Windows Media Player 外掛程式，Echo 範例屬性頁
- 外掛程式，Echo 範例屬性頁
- 數位信號處理外掛程式，Echo 範例屬性頁
- DSP 外掛程式，Echo 範例屬性頁
- Echo DSP 外掛程式範例，屬性頁
- Echo DSP 外掛程式範例，對話方塊資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09caa800376a7962a11912bc582a091f0de52c16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301483"
---
# <a name="modifying-the-echo-dialog-resource"></a>修改 Echo 對話資源

您需要變更對話方塊資源，也就是屬性頁物件的使用者介面。 您可以先變更現有的編輯方塊和標籤，使其適用于 [延遲時間] 屬性，然後為 [潮濕混合] 屬性新增第二個編輯方塊和標籤。

若要在 Visual C++ 中編輯對話方塊資源：

1.  按一下 [專案] 工作區中的 [ **ResourceView** ] 索引標籤。
2.  開啟最上層資料夾，展開 [資源] 樹狀目錄。
3.  開啟 **對話方塊** 資料夾。
4.  按兩下對話方塊資源名稱 [IDD \_ ECHOPROPPAGE]。 資源編輯器會出現在右窗格中。

## <a name="changing-the-existing-resources"></a>變更現有的資源

若要變更延遲時間屬性的現有屬性頁資源：

1.  首先，變更現有靜態文字控制項中的文字。 以滑鼠右鍵按一下控制項，然後選擇 [ **屬性**]。 在 [ **標題** ] 欄位中，輸入新的標題：
    ```C++
    Delay time (0 to 2000):
    
    ```

    

2.  關閉 [文字屬性] 對話方塊。
3.  現在，變更編輯方塊控制項的名稱。 若要這樣做，請以滑鼠右鍵按一下控制項，然後選擇 [ **屬性**]。 在 [ **識別碼** ] 欄位中，輸入控制項的新名稱：
    ```C++
    IDC_DELAYTIME
    
    ```

    

4.  關閉 [編輯屬性] 對話方塊。
5.  儲存資源。
6.  如果系統提示您重載檔案資源 .h，請回答 **[是]** 。
7.  按一下 [專案] 工作區中的 [ **FileView** ] 索引標籤。 開啟資源。h
8.  找出 \# (IDC SCALEFACTOR) 的 [縮放比例] 編輯方塊資源的定義 \_ ，並將其刪除。 它應該具有與 IDC DELAYTIME 相同的識別碼號碼 \_ 。

## <a name="adding-the-new-resources"></a>加入新的資源

若要加入新的 [潮濕混合] 屬性的屬性頁資源：

1.  按一下 [專案] 工作區中的 [ **ResourceView** ] 索引標籤，即可選取它。
2.  按兩下 [屬性頁] 對話方塊的 [名稱]，然後按一下 [IDD \_ ECHOPROPPAGE]。 資源編輯器會出現在右窗格中。
3.  使用 [工具箱] 將靜態文字控制項和編輯方塊加入至屬性頁。
4.  以滑鼠右鍵按一下靜態文字控制項，然後選擇 [ **屬性**]。
5.  在 [ **識別碼** ] 欄位中輸入靜態文字控制項的新名稱：
    ```C++
    IDC_MIXLABEL
    
    ```

    

6.  輸入標籤的標題：
    ```C++
    Effect level (%):
    
    ```

    

7.  關閉 [文字屬性] 對話方塊。
8.  以滑鼠右鍵按一下編輯方塊，然後選擇 [ **屬性**]。
9.  在 [ **識別碼** ] 欄位中輸入編輯方塊的新名稱：
    ```C++
    IDC_WETMIX
    
    ```

    

10. 關閉 [編輯屬性] 對話方塊。

當您儲存專案時，系統可能會提示您重載資源 .h。 如果發生這種情況，請按一下 **[是]** 。 對話方塊資源編輯器應該針對您新增的專案，將資源名稱和識別碼加入至 .h。 如果基於某些原因而不會發生這種情況，您必須開啟 []，並輸入標籤和編輯方塊控制項的新專案，並指派每個唯一的識別碼。

## <a name="modifying-and-adding-the-string-resources"></a>修改和新增字串資源

外掛程式 wizard 範例程式碼會指定名為 ID SCALERANGEERROR 的字串資源 \_ ，其中包含當使用者輸入超出範圍時要顯示的訊息。 您可以依照 Visual C++ 中的下列步驟，修改此資源以符合您的延遲時間值需求：

1.  按一下 [ **ResourceView** ] 索引標籤。
2.  開啟 [ **字串資料表** ] 資料夾。
3.  按兩下 [ **字串資料表** ] 圖示以開啟 [資源編輯器]。
4.  按兩下您想要編輯的資源名稱，在此案例中為 [識別碼] \_ SCALERANGEERROR。 [字串屬性] 對話方塊隨即出現。
5.  將 [ **識別碼** ] 欄位中的名稱變更為 [識別碼] \_ DELAYRANGEERROR。
6.  變更 [ **標題** ] 欄位中的文字：
    ```C++
    You must enter a delay time between 0 and 2000 milliseconds.
    
    ```

    

7.  關閉 [字串屬性] 對話方塊。

接下來，為潮濕混合屬性錯誤訊息新增字串資源。

1.  按兩下資源編輯器底部的空白行。
2.  將 [ **識別碼** ] 欄位中的名稱變更為 [識別碼] \_ MIXRANGEERROR。
3.  在 [ **標題** ] 欄位中加入下列文字：
    ```C++
    You must enter an effect level between 0 and 100 percent.
    
    ```

    

4.  關閉 [字串屬性] 對話方塊。

您會想要在字串資料表中變更其他兩個值。 識別碼 \_ FRIENDLYNAME 是 Windows Media Player 使用者介面中顯示的名稱，用來識別外掛程式。 識別碼 \_ 描述可讓您告訴使用者您的外掛程式。 這兩個字串都會以參數形式傳遞至 **IWMPMediaPluginRegistrar：： WMPRegisterPlayerPlugin** 函式，該函式是在 Echodll 的 DllRegisterServer 方法中呼叫。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**修改 Echo 範例屬性頁**](modifying-the-echo-sample-property-page.md)
</dt> </dl>

 

 




