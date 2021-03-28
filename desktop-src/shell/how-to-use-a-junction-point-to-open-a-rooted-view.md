---
description: 您可以使用登錄來指定流覽到連接點將會開啟根視圖，而不是關聯擴充功能內容的預設視圖。
title: 如何透過登錄開啟連接點的根目錄檢視
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa51e87ccb541e995300cb010f82c79e33112e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192681"
---
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-the-registry"></a>如何透過登錄開啟連接點的根目錄檢視

您可以使用登錄來指定流覽到連接點將會開啟根視圖，而不是關聯擴充功能內容的預設視圖。

## <a name="instructions"></a>指示


若要指定流覽到連接點應該開啟根視圖，請新增 **開啟** 的 \\ **命令**，並 **探索** \\ **命令** 子機碼至您延伸模組的 **CLSID** 子機碼，並將其預設值指派給此處顯示的命令列：

```
HKEY_CLASSES_ROOT
   CLSID
      {Extension CLSID}
         Shell
            Open
               Command
                  (Default) = %SYSTEMROOT%\explorer.exe/e,/root,"%1"
            Explore
               Command
                  (Default) = %SYSTEMROOT%\explorer.exe/e,/root,"%1"
```

當您加入這些值之後，就會啟動 Explorer.exe 的實例，以在使用者選取連接點時，將延伸模組的內容顯示為根視圖。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[指定命名空間延伸模組的位置](nse-junction.md)
</dt> <dt>

[如何透過快捷方式檔案開啟連接點的根目錄檢視](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> </dl>

 

 



