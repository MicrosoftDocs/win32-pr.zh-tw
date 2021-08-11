---
description: 本主題說明如何使用 Windows 7 SDK 中所提供的檔案類型驗證器。
ms.assetid: 96FCA74B-DEB2-49D1-B670-EBD8BE0783F1
title: 如何使用檔案類型驗證器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65af06de30d4fca2a9f5209d20e200153c061248576e7e94c8342cf9ae60e4f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118223370"
---
# <a name="how-to-use-the-file-type-verifier"></a>如何使用檔案類型驗證器

本主題說明如何使用[Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)中所提供的檔案類型驗證器。 如果您的程式會從 Windows Shell 建立要與使用者互動的檔案類型 (通常儲存在使用者的已知資料夾（例如 **我的檔**) ）中，請務必測試您的應用程式，並確認它所建立的檔案已正確註冊，並在流覽和搜尋檔案時提供高品質的使用者體驗。 如果您希望使用者在 Windows 7 上執行您的應用程式，這項功能特別重要，因為許多 Shell 功能都依賴高品質的檔案類型處理常式。

若要使用檔案類型驗證器驗證您的檔案類型，請遵循下列步驟。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

在您的測試環境上安裝應用程式，並將檔案類型驗證器複製到該環境。 檔案類型驗證器可在[Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)中取得。

### <a name="step-2"></a>步驟 2:

使用您的應用程式建立要測試的檔案。

### <a name="step-3"></a>步驟 3：

開機檔案類型驗證器。

### <a name="step-4"></a>步驟 4：

選取檔案類型的類別，如下列螢幕擷取畫面所示。

![顯示拖放功能的螢幕擷取畫面。](images/file-assoc/filetypeverifier1.png)

類別選取專案會決定要由工具執行的一組測試。 如果您的型別可能落在多個類別之下 (例如，.TIF 檔案可能是圖片或檔，視內容而定) ，請使用每個適當的類別再次執行工具。

### <a name="step-5"></a>步驟 5：

使用 Windows 檔案總管，找出要測試的檔案，並使用滑鼠將它拖曳至檔案類型驗證器中的目標，如下列螢幕擷取畫面所示。

![顯示拖放功能的螢幕擷取畫面](images/file-assoc/filetypeverifier2.png)

### <a name="step-6"></a>步驟 6：

等候檔案類型驗證器工具繼續進行一系列的測試。 進度列會顯示測試的進度，如下列螢幕擷取畫面所示。

![顯示進度列的螢幕擷取畫面](images/file-assoc/filetypeverifier3.png)

### <a name="step-7"></a>步驟 7：

檢查檔案類型測試的結果摘要，如下列螢幕擷取畫面所示。

![顯示結果摘要的螢幕擷取畫面](images/file-assoc/filetypeverifier4.png)

### <a name="step-8"></a>步驟 8：

按一下 [摘要] 頁面上的任何結果，以查看詳細記錄。 預覽處理常式的範例記錄檔會顯示在下列螢幕擷取畫面中。

![顯示預覽處理常式記錄檔的螢幕擷取畫面](images/file-assoc/filetypeverifier5.png)

### <a name="step-9"></a>步驟 9：

若要儲存記錄檔的複本，請按一下記錄檔顯示底部的 [ **儲存記錄** 檔]，然後選擇適當的位置以將它儲存在您的電腦上。

### <a name="step-10"></a>步驟 10：

如果回報失敗，請在您的應用程式中進行適當的變更，然後再次執行工具，以確認測試中不再顯示失敗。 如果回報警告，請評估這些警告，並決定它們是否與您的特定檔案類型相關，並視需要對您的應用程式進行適當的變更。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows 7 SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)
</dt> </dl>

 

 



