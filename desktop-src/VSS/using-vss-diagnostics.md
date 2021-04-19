---
description: Vsdiagview 和 Vssagent 是您可用來對 VSS 應用程式進行疑難排解的工具。請注意，這些工具組含在適用于 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 中。
ms.assetid: 2c1270a6-38c7-40d5-a194-0a6795557b9f
title: 使用 VSS 診斷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3d1733c2780670507b39c1db91cb3b2f7035a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986350"
---
# <a name="using-vss-diagnostics"></a>使用 VSS 診斷

Vsdiagview 和 Vssagent 是您可用來對 VSS 應用程式進行疑難排解的工具。

> [!Note]  
> 這些工具組含在適用于 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 中。 您可以從下載 Windows SDK [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) 。

 

在 Windows SDK 安裝中，您可以在 `%Program Files(x86)%\Windows Kits\8.1\bin\x64` 64 位 windows) 的 (和 `%Program Files(x86)%\Windows Kits\8.1\bin\x86` 32 位 windows) 的 (中找到這些工具。

## <a name="gathering-data"></a>正在收集資料

您可以使用 Vssagent 命令來收集資料。

**使用 Vssagent 收集資料**

1.  若要從命令列收集資料，請使用 Vssagent 命令，如下所示：

    **vssagent-收集** *XmlFileName * * * .xml**

2.  若要查看輸出檔，請參閱下列「查看資料」一節。

## <a name="viewing-data"></a>查看資料

您可以使用 Vsdiagview 應用程式來查看使用 Vssagent 命令收集的資料。 Vsdiagview 會顯示有關電腦的下列資訊：

-   電腦的相關資訊，例如作業系統版本、可用記憶體總計和 CPU 速度
-   VSS 二進位檔的名稱和版本號碼
-   磁片和磁片區裝置的名稱和屬性
-   任何 COM + 應用程式的名稱和屬性
-   可以用來診斷 VSS 問題的事件記錄檔名稱
-   任何 VSS 寫入器及其處理事件的名稱
-   其他作業系統檔案的相關資訊

**使用 Vsdiagview 來查看資料**

1.  在 [檔案] 功能表中，選擇 [ **開啟** ] 以流覽檔案。  (預設位置為 C： \\ vssdiag。 ) 
2.  按一下 [ **開啟** ] 以查看資料。

 

 



