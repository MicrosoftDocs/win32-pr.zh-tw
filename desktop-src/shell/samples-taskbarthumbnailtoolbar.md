---
description: 示範縮圖工具列、內嵌于視窗縮圖預覽中的作用中工具列控制項，用來提供視窗的按鍵命令存取權，而不需要使用者還原或啟動應用程式的視窗。
title: 工作列縮圖工具列範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4936FF67-19EE-4963-BE4C-3D40350C64A9
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: cd16ee40bfb480b3e7eacef2bc4681e61fdb24ace1ac68985e2016ce11b7c0e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118219627"
---
# <a name="taskbar-thumbnail-toolbar-sample"></a>工作列縮圖工具列範例

示範縮圖工具列、內嵌于視窗縮圖預覽中的作用中工具列控制項，用來提供視窗的按鍵命令存取權，而不需要使用者還原或啟動應用程式的視窗。

本主題包含下列各節。

-   [說明](#description)
-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)
-   [相關主題](#related-topics)

## <a name="description"></a>Description

這個範例示範如何提供簡單的工具列給工作列縮圖預覽。 工具列包含三個按鈕。 按一下按鈕會顯示一個視窗，以確認按鈕已啟用。 以下是示範的 Api：

-   [**ITaskbarList3::ThumbBarAddButtons**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbaraddbuttons)
-   [**ITaskbarList3::ThumbBarSetImageList**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-thumbbarsetimagelist)
-   [**THUMBBUTTON**](/windows/desktop/api/Shobjidl_core/ns-shobjidl_core-thumbbutton) 結構

## <a name="requirements"></a>規格需求



| 產品                                | 最小產品版本 |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>下載範例

| Location      | 路徑 URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [TaskbarThumbnailToolbar 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarThumbnailToolbar) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **TaskbarThumbnailToolbar** 專案目錄。
2.  輸入 `msbuild ThumbnailToolbar.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **TaskbarThumbnailToolbar** 專案目錄。
2.  按兩下 ThumbnailToolbar .sln 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  流覽至包含新可執行檔的目錄， (例如， `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarThumbnailToolbar\Debug`) ，請使用命令提示字元或 Windows 檔案總管。

    -   如果使用命令列，請輸入 `ThumbnailToolbar.exe` 。
    -   如果使用 Windows 檔案總管，請按兩下 ThumbnailToolbar.exe 的圖示。

    新視窗隨即開啟，其中會有相關聯的工作列按鈕。

2.  將游標停留在 **ThumbnailToolbar** 工作列按鈕上，讓預覽顯示。 按一下三個按鈕的其中一個 (綠色、黃色、紅色) 顯示在預覽的工具列中。
3.  從視窗 **的 [** 檔案]**功能表選擇 [** 結束]，以結束程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作列擴充功能](taskbar-extensions.md)
</dt> </dl>

 

 



