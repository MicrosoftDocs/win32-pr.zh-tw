---
description: 因為在許多情況下，您將只能在 Microsoft Visual Basic 環境中，針對部分元件功能進行偵錯工具，所以在某些情況下，您將需要在編譯之後，對以 Visual Basic 建立的元件進行 debug。 由於 Visual Basic 環境並不會啟用這種情況，因此您必須改為使用 Microsoft Visual C++ 環境。
ms.assetid: a58c5884-3c2d-4699-8b19-277003912dfd
title: 已編譯的 Visual Basic 元件的調試
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2eac784808602d3554e4610e70a8d8a22ef2ca1594062599ec6acd43db68b98a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128780"
---
# <a name="debugging-compiled-visual-basic-components"></a>已編譯的 Visual Basic 元件的調試

假設在許多情況下，您只能夠在 Microsoft Visual Basic 環境內進行部分元件功能的偵錯工具，在某些情況下，您將需要在編譯之後，對以 Visual Basic 建立的元件進行處理。 由於 Visual Basic 環境並不會啟用這種情況，因此您必須改為使用 Microsoft Visual C++ 環境。

**若要在 Visual C++ 環境中進行 Visual Basic 元件的調試**

1.  在 Visual Basic 6.0 中，開啟您要進行偵錯工具的 Visual Basic 專案。

2.  **在 [檔案**] 功能表上，按一下 [**進行 YourProject.dll**]。

3.  在 [**製作 Project** ] 對話方塊中，按一下 [**選項**]。

4.  在 [ **Project 屬性**] 對話方塊的 [**編譯**] 索引標籤上，按一下 [**編譯成機器碼** 而 **不優化**]，然後選取 [**建立符號偵錯工具資訊**] 核取方塊。

5.  按一下 **[確定]**，然後再按一次 **[確定]** ，以編譯您的專案。

6.  將已編譯的 DLL 移至通常已安裝 COM + 應用程式的位置。

    > [!Note]  
    > 如果您未移動 DLL，可能會收到錯誤訊息，告知您找不到 DLL 的符號調試資訊。 如果您無法讓偵錯工具在元件的中斷點上停止，請確認 DLL 位於標準封裝目錄中，從封裝中刪除該元件，然後重新加入元件。

     

7.  開始 Visual C++。

8.  **在 [檔案**] 功能表上，按一下 [**開啟工作區**]。

9.  在 [ **開啟工作區** ] 對話方塊中，將 [ **檔案類型** ] 設定為 [所有檔案] **(\* 。 \*)**，選取已編譯的元件，然後按一下 [ **開啟**]。

10. **在 [檔案**] 功能表中，按一下 [**開啟** (未 **開啟工作區**]) ，然後開啟您想要進行偵錯工具的 Visual Basic 模組 (. bas) 、表單 (. keyfromnode.frm) 或類別 (。

11. 在 [ **Project** ] 功能表上，按一下 [**設定**]。

12. 在 [ **Project 設定**] 對話方塊的 [**調試**] 索引標籤上，選取 [**類別目錄**] 方塊中的 **[一般**]。

13. 在 [ **用於偵錯工具的可執行檔** ] 方塊中，輸入 Dllhost.exe 的完整路徑，後面接著一個引數，指定包含元件的 com + 應用程式的處理序識別碼。 您會在 [COM + 應用程式的 **屬性**] 對話方塊的 [**一般**] 索引標籤上找到處理序識別碼。 以下是範例： C： \\ Winnt \\ System32 \\Dllhost.exe/ProcessID： { <processID> }。

14. 按一下 [確定]。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[com + Visual Basic 支援與 MTS 對比](com--visual-basic-debugging-support-contrasted-with-mts.md)
</dt> <dt>

[Visual Basic IDE 中的調試](debugging-in-the-visual-basic-ide.md)
</dt> </dl>

 

 



