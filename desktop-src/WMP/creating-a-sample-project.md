---
title: 建立範例專案
description: 建立範例專案
ms.assetid: 9cbbd1a7-88e7-4947-8dca-e06e364102f7
keywords:
- Windows Media Player 線上商店，建立範例專案
- 線上商店，建立範例專案
- 輸入2個線上商店，建立範例專案
- Windows Media Player 線上商店、範例專案
- 線上商店、範例專案
- 類型2線上商店、範例專案
- 專案嚮導 Windows Media Player 線上商店
- project wizard、線上商店
- 輸入2線上商店、專案嚮導
- 外掛程式，專案嚮導
- 專案嚮導 Windows Media Player 外掛程式
- 建立範例專案
- 範例，請輸入2個線上商店
- 專案嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4756cc7ae8d27c2a790a7ac96af638eea72d861
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "104092574"
---
# <a name="creating-a-sample-project"></a>建立範例專案

若要使用專案嚮導建立新的專案，請遵循下列步驟：

1.  開啟 Microsoft Visual Studio。
2.  從 [檔案] 功能表，指向 [新增]，然後按一下 [專案]。
3.  在 [ **專案類型** ] 清單方塊中，選擇 [ **Visual C++ 專案**]。
4.  在 [ **範本** ] 清單方塊中，選擇 Windows Media Player 的 [ **線上商店] Wizard**。
5.  輸入專案的名稱和位置。
6.  按一下 **[確定** ] 以啟動專案嚮導。
7.  選取 [ **類型 2] (基本整合)**，然後按 **[下一步]**。
8.  輸入服務的易記名稱和內容散發者識別碼。 輸入從使用者電腦移除服務之網頁的 URL。
    > [!Note]  
    > 您為內容散發者識別碼提供的值不能包含空格。 Wizard 會從您提供的字串中移除任何空格。

     

9.  按一下 [完成] 以建立專案。

Wizard 會自動產生新的 c + + 專案，以建立可執行 **IWMPSubscriptionService** 和 **IWMPSubscriptionService2** 介面的 type 2 online store 外掛程式。 您每次執行嚮導時，都會建立相同的專案，但當您編譯專案時所建立的元件會有唯一的類別識別碼。 根據您在執行嚮導時所提供的值，專案名稱、易記名稱和內容散發者識別碼也可能不同。 範例專案會使用符合您為易記名稱提供之值的索引鍵名稱來註冊元件。

此範例會使用 Active Template Library (ATL) 程式碼來提供 COM 執行。

嚮導會為您建立下列檔案：

-   *專案名稱* dll .cpp。 將動態連結程式庫 (DLL) 匯出，例如主要 DLL 進入點函數。 也包含 ATL 物件對應和模組宣告。
-   *專案名稱*.cpp。 包含 IWMPSubscriptionService 和 IWMPSubscriptionService2 介面之方法的預設實值。 也包含程式碼，用來定義當 Windows Media Player 呼叫方法時，範例會開啟的對話方塊。
-   *專案名稱*.def。宣告 DLL 匯出。
-   Stdafx.h .cpp。 包含標準標頭。
-   wmp. h。 Windows Media Player 標頭檔。
-   wmpplug。 Windows Media Player 外掛程式標頭檔。
-   subscriptionservices。 Windows Media Player online 會儲存標頭檔。
-   資源 .h。 包含資源定義。
-   **專案名稱**.h。 包含線上商店物件和對話方塊的類別定義。 定義物件的類別識別碼和內容散發者識別碼常數。
-   Stdafx.h。 包含標準系統包含。
-   *專案名稱*。 資源腳本檔。 這包含對話方塊資源和控制項的定義。 這也是字串資料表的儲存位置。 字串資料表包含您的專案名稱和易記名稱的字串常數。 通常您會使用 Visual Studio 資源編輯器中的這個檔案，而不是純文字。
-   *專案名稱*.rgs。 登入指令檔檔。 此檔案包含用來將您的元件類別新增至登錄的資訊，讓 Windows Media Player 可以找到它。 您可以在此檔案中變更服務的索引鍵名稱。

> [!Note]  
> 您應該將 DLL 的基底位址設定為0x0F100000，以避免與 Windows Media Player 衝突。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Type 2 線上商店的外掛程式**](building-the-plug-in-for-a-type-2-online-store.md)
</dt> <dt>

[**IWMPSubscriptionService 介面**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice)
</dt> <dt>

[**IWMPSubscriptionService2 介面**](/previous-versions/windows/desktop/api/subscriptionservices/nn-subscriptionservices-iwmpsubscriptionservice2)
</dt> </dl>

 

 




