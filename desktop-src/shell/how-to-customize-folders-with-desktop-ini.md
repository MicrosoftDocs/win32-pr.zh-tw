---
description: 使用 Desktop.ini 自訂個別資料夾的外觀和行為。
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: 如何使用 Desktop.ini 自訂資料夾
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a671b169c4b025683cdd220ee3a920b4d592488
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581746"
---
# <a name="how-to-customize-folders-with-desktopini"></a>如何使用 Desktop.ini 自訂資料夾

檔系統資料夾通常會以標準圖示和一組屬性來顯示，以指定是否共用資料夾。 您可以建立該資料夾的 Desktop.ini 檔案，以自訂個別資料夾的外觀和行為。

## <a name="instructions"></a>指示

### <a name="using-desktopini-files"></a>使用 Desktop.ini 檔案

資料夾通常會顯示標準資料夾圖示。 Desktop.ini 檔案的常見用法是將自訂圖示或縮圖影像指派給資料夾。 您也可以使用 Desktop.ini 來建立資訊 *提示，以* 顯示資料夾的相關資訊，並控制資料夾行為的某些層面，例如指定資料夾或資料夾中專案的當地語系化名稱。

**您可以使用下列程式，利用 Desktop.ini 自訂資料夾的樣式：**

1.  使用 [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) 將資料夾設為系統資料夾。 這會將資料夾的唯讀位設定為，以指出應啟用針對 Desktop.ini 保留的特殊行為。 您也可以使用 **attrib + s** *資料夾資料夾*，從命令列將資料夾設為系統資料夾。
2.  建立資料夾的 Desktop.ini 檔案。 您應該將它標示為 *隱藏* 和 *系統* ，以確保它會從一般使用者中隱藏起來。
3.  請確定您建立的 Desktop.ini 檔案是 Unicode 格式。 這是儲存可顯示給使用者之當地語系化字串的必要動作。

### <a name="creating-a-desktopini-file"></a>建立 Desktop.ini 檔案

Desktop.ini 檔案是一個文字檔，可讓您指定如何查看檔系統資料夾。 \[。ShellClassInfo \] 區段可讓您將值指派給數個專案，以自訂資料夾的視圖：

| 值             | 描述                                                                                                                                                                                                                                                                                                                                                                    |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **ConfirmFileOp** | 將此專案設定為0，以避免在刪除或移動資料夾時出現「您正在刪除系統資料夾」警告。                                                                                                                                                                                                                                                                  |
| **NoSharing**     | Windows Vista 或更新版本下不支援。 將此專案設定為1，以防止資料夾共用。                                                                                                                                                                                                                                                                       |
| **IconFile**      | 如果您想要指定資料夾的自訂圖示，請將此專案設定為圖示的檔案名。 .Ico 副檔名是慣用的，但您也可以指定 .bmp 檔案，或 .exe 和 .dll 包含圖示的檔案。 如果您使用相對路徑，則圖示可供透過網路觀看資料夾的人員使用。 您也必須設定 **>iconindex** 專案。 |
| **>iconindex**     | 設定此專案可指定自訂圖示的索引。 如果指派給 **IconFile** 的檔案只包含單一圖示，請將 **>iconindex** 設定為0。                                                                                                                                                                                                                               |
| **InfoTip**       | 將此專案設定為資訊文字字串。 當游標停留在資料夾上時，它會顯示為提示。 如果使用者按一下資料夾，資訊文字會顯示在資料夾的 [資訊] 區塊中，位於標準資訊下方。                                                                                                                      |



 

下圖是含有自訂 Desktop.ini 檔案的 [音樂] 資料夾。 資料夾現在：

-   具有自訂圖示。
-   如果資料夾已移動或刪除，則不會顯示「您正在刪除系統資料夾」警告。
-   無法共用。
-   當游標停留在資料夾上時，顯示資訊文字。

下圖中的資料夾選項設定為顯示隱藏的檔案，以便顯示 Desktop.ini。 資料夾看起來像這樣：

![具有自訂圖示之資料夾的螢幕擷取畫面](images/webview4.jpg)

當游標停留在資料夾上時，就會顯示提示。

![具有提示的資料夾螢幕擷取畫面](images/webview6.jpg)

自訂圖示會取代資料夾名稱出現位置的資料夾圖示。

![取代資料夾圖示的自訂圖示螢幕擷取畫面](images/webview5.jpg)

下列 desktop.ini 檔案是用來自訂 [音樂] 資料夾，如先前的圖例所示。


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



