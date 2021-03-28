---
description: 示範如何在 Windows 檔案總管命名空間中的資料夾或專案上接聽 Shell 變更通知。
title: 變更通知監看員範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 02A7C5B4-94F2-4c35-9290-4C816E5CF63A
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 5d0ac6ccb2dd2328d81b77d03bffc68dfa9a70cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193952"
---
# <a name="change-notify-watcher-sample"></a>變更通知監看員範例

示範如何在 Windows 檔案總管命名空間中的資料夾或專案上接聽 Shell 變更通知。

本主題包含下列各節。

-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)

## <a name="requirements"></a>規格需求



| 產品                                | 最小產品版本 |
|----------------------------------------|-------------------------|
| Windows                                | Windows Vista           |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>下載範例

| Location      | 路徑 URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [ChangeNotifyWatcher 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appplatform/ChangeNotifyWatcher) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **ChangeNotifyWatcher** 專案目錄。
2.  輸入 `msbuild ChangeNotifyWatcher.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **ChangeNotifyWatcher** 專案目錄。
2.  按兩下 ChangeNotifyWatcher .sln 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2.  在命令提示字元處，輸入 `ChangeNotifyWatcher.exe`。 或者，從 Windows 檔案總管按兩下 ChangeNotifyWatcher.exe 的圖示。
3.  若要示範效果， (AppUserModelIDs 的應用程式使用者模型識別碼) 選取要監看的資料夾，方法是按一下 **[挑選 ...]** ，或從 Windows 檔案總管視窗的資料夾拖放至範例的清單視圖中。

 

 



