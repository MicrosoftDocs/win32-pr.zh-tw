---
description: 許多主控台應用程式會顯示內容內容表，讓使用者能夠查看和修改各種裝置和系統設定。
title: 如何註冊和執行主控台應用程式的屬性工作表處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f7f8fe80bf5c7baceddac64d513d950378bcdf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849190"
---
# <a name="how-to-register-and-implement-a-property-sheet-handler-for-a-control-panel-application"></a>如何註冊和執行主控台應用程式的屬性工作表處理常式

許多主控台應用程式會顯示內容內容表，讓使用者能夠查看和修改各種裝置和系統設定。 這兩個應用程式（滑鼠和顯示器）可以讓屬性工作表處理常式以自訂頁面取代一或多個頁面。 下列螢幕擷取畫面顯示 [ **滑鼠屬性** ] 屬性工作表。

![滑鼠屬性屬性工作表](images/propsheethandler3.jpg)

主控台應用程式的屬性工作表處理常式類似于檔案類型，但有兩個主要例外：

-   它們是由主控台應用程式呼叫，而非 Shell。
-   以不同方式註冊它們。

## <a name="what-you-need-to-know"></a>您必須知道的事項

### <a name="technologies"></a>技術

-   殼層

### <a name="prerequisites"></a>必要條件

-   瞭解主控台
-   對快速鍵功能表的瞭解

## <a name="instructions"></a>指示

### <a name="step-1-registering-a-property-sheet-handler-for-a-control-panel-application"></a>步驟1：註冊主控台應用程式的屬性工作表處理常式

主控台的應用程式屬性工作表處理常式必須在主控台子機碼下註冊。 此索引鍵可以位於兩個位置的其中一個，視處理常式是每個使用者或每部電腦而定。 針對每位使用者註冊，主控台子機碼是 **HKEY \_ CURRENT \_ user** \\ **主控台**。 如 Regstr 中所定義的宏 REGSTR \_ 路徑 \_ 控制台，可以在程式碼中用來取代 "主控台"。 針對每一電腦的註冊，此位置為：

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            Current Version
               Controls Folder
```

您可以在程式碼中將此路徑稱為 HKEY \_ 本機 \_ 電腦 \\ REGSTR \_ 路徑 \_ CONTROLSFOLDER，並使用 \_ CONTROLSFOLDER 中定義的 REGSTR path \_ REGSTR 宏。

允許屬性工作表處理常式取代頁面的主控台應用程式，在主控台的子機碼底下有一個子機碼，名為的應用程式，例如滑鼠和顯示器。 應用程式的子機碼必須具有具有 **PropertySheetHandlers** 子機碼的 **shellex** 子機碼。 若要註冊屬性工作表處理常式，請將其 GUID 新增至與主控台應用程式相關聯的 **PropertySheetHandlers** 子機碼。 若要這樣做，請建立 **PropertySheetHandlers** 子機碼的子機碼，並為屬性工作表處理常式命名，並將其預設值設定為處理常式 GUID 的字串形式。

下列範例會以每部電腦為單位，為滑鼠主控台的應用程式註冊屬性工作表處理常式。 若要以每位使用者為基礎來註冊，請將 **HKEY \_ 本機 \_ 電腦** \\ **REGSTR \_ 路徑 \_ CONTROLSFOLDER** 取代為 **HKEY \_ CURRENT \_ user** \\ **REGSTR \_ path \_ 控制台**。

```
HKEY_LOCAL_MACHINE
   REGSTR_PATH_CONTROLSFOLDER
      Mouse
         shellex
            PropertySheetHandlers
               MyPropHandler
                  (Default) = {MyPropHandler CLSID GUID}
```

### <a name="step-2-implementing-a-property-sheet-handler-for-a-control-panel-application"></a>步驟2：為主控台應用程式執行屬性工作表處理常式

執行主控台屬性工作表處理常式的程式，與 [如何針對檔案類型註冊和執行屬性工作表處理常式](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)中所討論的程式非常類似。 主要差異在於現在 [**IShellPropSheetExt：： ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) 需要 nontoken 的執行，而不是 [**IShellPropSheetExt：： AddPages**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-addpages)。

當主控台應用程式即將顯示其屬性工作表時，它會針對每個可取代的頁面呼叫屬性工作表處理常式的 [**IShellPropSheetExt：： ReplacePage**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellpropsheetext-replacepage) 方法一次。 *UPageID* 參數會設定為頁面的識別碼。 可用頁面的識別碼定義于 Cplext 中。 下表列出目前可用的識別碼。 

| 頁面識別碼                      | Description         | 主控台應用程式 |
|------------------------------|---------------------|---------------------------|
| CPLPAGE \_ 滑鼠 \_ 按鈕      | 按鈕頁面    | 滑鼠                     |
| CPLPAGE \_ 滑鼠 \_ PTRMOTION    | [動作] 頁面     | 滑鼠                     |
| CPLPAGE \_ 滑鼠 \_ 滾輪        | 滾輪頁面      | 滑鼠                     |
| CPLPAGE \_ 鍵盤 \_ 速度     | [速度] 頁面      | 鍵盤                  |
| CPLPAGE \_ 顯示 \_ 背景 | 背景頁面 | 顯示                   |



 

## <a name="remarks"></a>備註

建立和取代頁面的程式與新增頁面的程式相同。 如需詳細資訊，請參閱 [如何註冊和執行檔案類型的屬性工作表處理常式](how-to-register-and-implement-a-property-sheet-handler-for-a-file-type.md)。

 

 



