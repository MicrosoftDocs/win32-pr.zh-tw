---
description: 示範工作列圖示重迭和進度列。
title: 工作列週邊設備狀態範例
ms.topic: article
ms.date: 05/31/2018
ms.assetid: E4B693FB-EE7D-47d0-A5D8-91205AD4A3DC
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 793c09853e3174f426b7b41685f2593daaae9b6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991746"
---
# <a name="taskbar-peripheral-status-sample"></a>工作列週邊設備狀態範例

示範工作列圖示重迭和進度列。

本主題包含下列各節。

-   [說明](#description)
-   [需求](#requirements)
-   [下載範例](#downloading-the-sample)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)
-   [相關主題](#related-topics)

## <a name="description"></a>Description

這個範例會建立一個範例工作列按鈕，其示範如何使用 [**ITaskbarList3：： SetOverlayIcon**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setoverlayicon) ，方法是讓您套用從功能表中選擇的各種重迭。

此範例也提供在按鈕上模擬進度指標的選項，示範如何使用 [**ITaskbarList3：： SetProgressState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressstate) 和 [**ITaskbarList3：： SetProgressValue**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-itaskbarlist3-setprogressvalue) ，方法是先顯示不定的進度指標 (TBPF \_ 不定) ，然後使用一般比例指標 (TBPF \_ 正常) 。

## <a name="requirements"></a>規格需求



| 產品                                | 最小產品版本 |
|----------------------------------------|-------------------------|
| Windows                                | Windows 7               |
| Windows Software Development Kit (SDK) | 7.0                     |



 

## <a name="downloading-the-sample"></a>下載範例

| Location      | 路徑 URL                                                                                             |
|---------------|------------------------------------------------------------------------------------------------------|
| GitHub  | [TaskBarPeripheralStatus 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TaskbarPeripheralStatus) |

## <a name="building-the-sample"></a>建立範例

若要從命令提示字元建立範例：

1.  開啟 [命令提示字元] 視窗，並流覽至 **TaskbarPeripheralStatus** 專案目錄。
2.  輸入 `msbuild PeripheralStatus.sln`。

若要使用 Microsoft Visual Studio (慣用的) 來建立範例：

1.  開啟 Windows 檔案總管，然後流覽至 **TaskbarPeripheralStatus** 專案目錄。
2.  按兩下 PeripheralStatus .sln 檔案的圖示，在 Visual Studio 中開啟專案。
3.  從 [ **組建** ] 功能表選取 [ **建立方案**]。

## <a name="running-the-sample"></a>執行範例

1.  流覽至包含新可執行檔的目錄， (例如， `C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\WinUI\Shell\AppShellIntegration\TaskbarPeripheralStatus\Win32\Debug`) ，請使用命令提示字元或 Windows 檔案總管。

    -   如果使用命令列，請輸入 `PeripheralStatus.exe` 。
    -   如果使用 Windows 檔案總管，請按兩下 PeripheralStatus.exe 的圖示。

    新視窗隨即開啟，其中會有相關聯的工作列按鈕。

2.  若要示範重迭，請從視窗的 [**週邊狀態**] 功能表選擇 [重迭 **1** ] 或 [重迭 **2** ] 選擇的重迭會出現在工作列按鈕上。 若要移除重迭，請選擇 [ **清除** 覆迭]。
3.  若要示範進度列，請從視窗的 [**週邊狀態**] 功能表選擇 [**模擬進度**]。 工作列按鈕會顯示不定的進度指示器，然後切換至一般指標。
4.  從視窗 **的 [** 檔案]**功能表選擇 [** 結束]，以結束程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[工作列擴充功能](taskbar-extensions.md)
</dt> </dl>

 

 



