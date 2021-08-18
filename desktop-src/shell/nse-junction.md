---
description: 命名空間延伸的根目錄通常會 Windows 檔案總管顯示為樹狀目錄和資料夾檢視中的資料夾。
title: 指定命名空間延伸模組的位置
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2c1fdd5d-b359-4d5c-a20e-0622f3a1cb1d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: e20b9a1644b2272ee06ff8a792198f79ffebca8b8a971b690c1be1160830aae8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118719884"
---
# <a name="specifying-a-namespace-extensions-location"></a>指定命名空間延伸模組的位置

命名空間延伸的根目錄通常會 Windows 檔案總管顯示為樹狀目錄和資料夾檢視中的資料夾。 若要讓 Windows 檔案總管顯示延伸模組的檔案和子資料夾，您必須指定根資料夾位於 Shell 命名空間階層中的位置。 這個位置稱為「 *連接點*」。

-   [使用虛擬資料夾做為連接點](#using-virtual-folders-as-junction-points)
-   [使用檔系統資料夾做為連接點](#using-file-system-folders-as-junction-points)
-   [開啟命名空間延伸模組的視圖](#opening-a-view-of-a-namespace-extension)

## <a name="using-virtual-folders-as-junction-points"></a>使用虛擬資料夾做為連接點

定義延伸模組連接點最簡單的方式，就是將根資料夾設為系統虛擬資料夾的子資料夾。 這種類型的連接點稱為 *虛擬連接點*。 **桌上型電腦** 和 **我的電腦** 資料夾是虛擬連接點的典型位置，但您也可以在遠端電腦上或在 [**我的網路位置**]、[ **Internet Explorer**] 和 [**主控台**] 資料夾中定義虛擬連接點。

若要定義虛擬連接點，請建立代表適當虛擬資料夾的機碼子機碼，並將它命名為您的延伸模組類別識別碼的字串格式， (CLSID) 。 註冊的 CLSID 會如下所示。

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  Virtual Folder Name
                     NameSpace
                        {Extension CLSID}
                           (Default) = Junction Point Name
```

*虛擬資料夾名稱* 是下表中的其中一個子機碼。



| Location          | 虛擬資料夾名稱                        |
|-------------------|--------------------------------------------|
| 控制台     | **控制台**                           |
| 桌面           | **桌上型電腦**                                |
| 整個網路    | **NetworkNeighborhood** \\**EntireNetwork** |
| 我的電腦       | **MyComputer**                             |
| 網路上的芳鄰 | **NetworkNeighborhood**                    |
| 遠端電腦   | **RemoteComputer**                         |
| 使用者檔案       | **UsersFiles**                             |



 

遠端擴充必須使用 [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer)初始化。

## <a name="using-file-system-folders-as-junction-points"></a>使用檔系統資料夾做為連接點

有兩種方式可將檔系統資料夾定義為連接點。 最簡單的方法是在適當的位置建立資料夾，並將句點附加到資料夾的名稱，後面接著您的延伸模組 CLSID 的字串形式。 Windows 檔案總管中只會顯示資料夾名稱。 下列範例會建立具有 MyFolder 顯示名稱的連接點。


```
MyFolder.{Extension CLSID}
```



或者，您可以透過下列方式，將傳統命名資料夾定義為連接點：

-   將資料夾設為唯讀。
-   藉由呼叫 [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera)，將資料夾設為系統資料夾。
-   將隱藏的 Desktop.ini 檔案放在包含副檔名 CLSID 的資料夾中。

Desktop.ini 是標準文字檔，可新增至任何資料夾，以自訂資料夾行為的特定層面。 如需如何使用此檔案的一般討論，請參閱 [如何使用 Desktop.ini自訂資料夾 ](how-to-customize-folders-with-desktop-ini.md)。 若要將資料夾定義為連接點，則為 \[ 。\] Desktop.ini 的 ShellClassInfo 區段必須包含擴充功能的 CLSID，如下所示：


```
[.ShellClassInfo]
CLSID={Extension CLSID}
```



## <a name="opening-a-view-of-a-namespace-extension"></a>開啟命名空間延伸模組的視圖

當使用者流覽到連接點時，Windows 檔案總管會自動建立根資料夾的視圖。 您也可以藉由將副檔名為 CLSID 的 Explorer.exe 明確地啟動為引數，來建立一個 view。 比方說，您可以使用這個方法，從快捷方式功能表或快捷方式啟動擴充功能的觀點。 例如，若要啟動包含樹狀檢視的 MyExtension，您可以使用下列命令字串。


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID}
```



替代的命令字串可以用來啟動延伸模組內的物件檢視。 這項功能對於使用資料夾檢視的延伸模組很有用，例如，可讓使用者查看其中一個壓縮檔案的內容。


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID},objectname
```



*Objectname* 參數是要查看之物件的名稱。 WindowsExplorer 會將名稱轉換為其對應的 PIDL，並將 PIDL 傳遞至新的資料夾物件的 [**IPersistFolder：： Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize)方法。

> [!Note]  
> CLSID 字串的前面必須加上一對冒號 (：： ) 或命令將會失敗。 上述兩個範例命令列中使用的斜線-e (/e) 旗標會指示 Windows 檔案總管顯示樹狀檢視。 旗標必須以逗號分隔，並以兩個冒號分隔。 如果您不想要樹狀檢視，請省略/e 旗標和逗號。

 

 

 



