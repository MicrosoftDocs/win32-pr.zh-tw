---
description: 如何從沒有關聯的檔案類型的 [開啟檔案] 對話方塊中排除應用程式。
title: 如何從非關聯檔案類型的 [開啟檔案] 對話方塊中排除應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d90ae5ab49128df1eedd9b760286ce54f6b6498cbe00d4a945145a80f956cde
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350909"
---
# <a name="how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types"></a>如何從非關聯檔案類型的 [開啟檔案] 對話方塊中排除應用程式

當使用者嘗試開啟的檔案不是任何已註冊檔案類型的成員時 (也就是) 未知的檔案類型，或是當使用者從檔案的快捷方式功能表中選取 [ **開啟檔案** ] 或 **[開啟檔案-> 選擇預設程式** ] 時，命令介面會顯示一個子功能表或對話方塊，讓使用者能夠指定用來開啟檔案的程式。

根據預設，任何註冊為 **HKEY \_ 類別 \_ 根** 應用程式子機碼的應用程式， \\ 都會顯示在 [**開啟檔案**] 對話方塊中。 無論應用程式是否已註冊來處理檔案類型，這些應用程式都會在 **開啟檔案** 中顯示。

若要防止應用程式在應用程式不應該或無法用來開啟特定檔案類型時出現在 [ **開啟檔案** ] 對話方塊中，請使用本主題中所述的兩種技術之一。

## <a name="instructions"></a>指示

### <a name="step-1"></a>步驟 1:

將 NoOpenWith 專案新增至應用程式的子機碼。 當應用程式使用檔案類型時，Windows 會記錄該資訊來建立 **建議的程式** 清單。 這份清單會顯示在 **開啟檔案** 子功能表中，如下列螢幕擷取畫面所示。

![顯示快捷方式功能表的螢幕擷取畫面，其中顯示 [開啟方式] 子功能表](images/file-assoc/openwithsubmenu.png)

這些建議的應用程式也會顯示在 [**開啟檔案**] 對話方塊的 [**建議的程式**] 部分中，如下列螢幕擷取畫面所示。

![具有建議程式之 [開啟方式] 對話方塊的螢幕擷取畫面](images/file-assoc/openwithdialog.png)

> [!Note]  
> 如果應用程式已在檔案類型的 [OpenWithList](fa-file-types.md) 或 OpenWithProgIDs 中註冊本身，即使已設定 NoOpenWith 專案，也會出現在 [ **建議的程式** ] 清單中。 此外，請記住，不論是否在建議的程式清單中提供應用程式，使用者都可以手動流覽至任何可執行檔。

 

應用程式可以在應用程式的子機碼底下指定 NoOpenWith 值，以停用此追蹤。

NoOpenWith 專案是空的 **REG \_ SZ** 值，如下列範例所示。

```
HKEY_CLASSES_ROOT
   Applications
      MyProgram.exe
         NoOpenWith
```

設定 NoOpenWith 專案也會有下列影響：

-   防止將檔案釘選到應用程式的捷徑清單透過拖放，除非應用程式是特別註冊來處理該檔案類型。
-   防止 [一般檔案] 對話方塊和 [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) 函式的任何呼叫將任何檔案新增至應用程式的捷徑清單，除非應用程式已特別註冊來處理該檔案類型。

### <a name="step-2"></a>步驟 2:

避免應用程式出現在 [ **開啟檔案** ] 對話方塊中的第二種方式，是使用 **SupportedTypes** 子機碼來明確列出應用程式可以開啟的檔案類型延伸模組。 這可防止應用程式在無法開啟的檔案類型的 [ **開啟檔案** ] 對話方塊中出現。 它也會讓應用程式出現在 **建議的程式** 清單中，如先前所述。

如果應用程式可以將檔案儲存為特定檔案類型，但無法開啟該檔案類型，這個方法特別有用。 應用程式也應該 \_ 在呼叫 [**儲存**] 對話方塊時，透過 [**IFileDialog：： >setoptions**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ifiledialog-setoptions)設定 FOS DONTADDTORECENT 旗標。 這會讓專案不會加入至捷徑清單的 **最新** 或 **經常** 的部分。 它也會封鎖在 [OpenWithList](fa-file-types.md)下追蹤應用程式。

每個支援的延伸模組都會新增為 **SupportedTypes** 子機碼底下的專案，如下列範例所示。 專案的類型為 **REG \_ SZ** 或 **reg \_ Null**，沒有相關聯的值。

```
HKEY_CLASSES_ROOT
   Applications
      ApplicationName
         SupportedTypes
            .ext1
            .ext2
            .ext3
```

如果提供 **SupportedTypes** 子機碼，則只有具有這些副檔名的檔案才有資格釘選到應用程式的捷徑清單，或在應用程式 **最近** 或 **經常** 的目的地清單中進行追蹤。

NoOpenWith 專案會覆寫 **SupportedTypes** 子機碼，並在 [ **開啟檔案** ] 對話方塊中隱藏應用程式。

 

 
