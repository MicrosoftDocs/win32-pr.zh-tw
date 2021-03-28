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
# <a name="how-to-open-a-rooted-view-of-a-junction-point-through-the-registry"></a><span data-ttu-id="520cd-103">如何透過登錄開啟連接點的根目錄檢視</span><span class="sxs-lookup"><span data-stu-id="520cd-103">How to Open a Rooted View of a Junction Point Through the Registry</span></span>

<span data-ttu-id="520cd-104">您可以使用登錄來指定流覽到連接點將會開啟根視圖，而不是關聯擴充功能內容的預設視圖。</span><span class="sxs-lookup"><span data-stu-id="520cd-104">You can use the registry to specify that browsing into a junction point will open a rooted view rather than the default view of the contents of the associated extension.</span></span>

## <a name="instructions"></a><span data-ttu-id="520cd-105">指示</span><span class="sxs-lookup"><span data-stu-id="520cd-105">Instructions</span></span>


<span data-ttu-id="520cd-106">若要指定流覽到連接點應該開啟根視圖，請新增 **開啟** 的 \\ **命令**，並 **探索** \\ **命令** 子機碼至您延伸模組的 **CLSID** 子機碼，並將其預設值指派給此處顯示的命令列：</span><span class="sxs-lookup"><span data-stu-id="520cd-106">To specify that browsing into a junction point should open a rooted view, add **Open**\\**Command** and **Explore**\\**Command** subkeys to your extension's **CLSID** subkey, with their default values assigned to the command lines shown here:</span></span>

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

<span data-ttu-id="520cd-107">當您加入這些值之後，就會啟動 Explorer.exe 的實例，以在使用者選取連接點時，將延伸模組的內容顯示為根視圖。</span><span class="sxs-lookup"><span data-stu-id="520cd-107">Once you've added those values, an instance of Explorer.exe is launched to display the contents of the extension as a rooted view when the user selects the junction point.</span></span>

## <a name="related-topics"></a><span data-ttu-id="520cd-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="520cd-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="520cd-109">指定命名空間延伸模組的位置</span><span class="sxs-lookup"><span data-stu-id="520cd-109">Specifying a Namespace Extension's Location</span></span>](nse-junction.md)
</dt> <dt>

[<span data-ttu-id="520cd-110">如何透過快捷方式檔案開啟連接點的根目錄檢視</span><span class="sxs-lookup"><span data-stu-id="520cd-110">How to Open a Rooted View of a Junction Point Through a Shortcut File</span></span>](how-to-use-a-shortcut-file-to-open-a-rooted-view.md)
</dt> </dl>

 

 



