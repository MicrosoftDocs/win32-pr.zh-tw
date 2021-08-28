---
title: 自訂圖示縮圖和即時預覽點陣圖
description: 示範如何自訂 iconic 縮圖和即時預覽點陣圖 (也稱為查看預覽) 。
ms.assetid: 43fe71e7-4e5c-46fb-876b-e26996071665
ms.topic: article
ms.date: 05/31/2018
ms.custom: project-verbatim
ms.openlocfilehash: 94fa65fd4cd80f837867a6a5d225ec43050cf0018c8116e8beae099ed1067025
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120022160"
---
# <a name="customize-an-iconic-thumbnail-and-a-live-preview-bitmap"></a>自訂圖示縮圖和即時預覽點陣圖

## <a name="description"></a>描述

您可以使用 Windows 7 桌面視窗管理員 (DWM) api 中引進的函式和訊息，自訂 iconic 縮圖和 *即時預覽* (或 *查看預覽*) 點陣圖。

具體而言，您會使用 [**DwmSetIconicThumbnail**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticonicthumbnail) 函數和 [**WM \_ SENDICONICTHUMBNAILBITMAP**](wm-dwmsendiconicthumbnail.md) 訊息來自訂 iconic 縮圖。 您也可以使用 [**DwmSetIconicLivePreviewBitmap**](/windows/win32/api/Dwmapi/nf-dwmapi-dwmseticoniclivepreviewbitmap) 函式和 [**WM \_ SENDICONICLIVEPREVIEWBITMAP**](wm-dwmsendiconiclivepreviewbitmap.md) 訊息來設定 iconic live preview 點陣圖。

如需使用 **DwmSetIconicThumbnail** 函數的範例應用程式，請參閱 [TabThumbnails 範例](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/shell/appshellintegration/TabThumbnails)。

下圖顯示轉換成自訂縮圖的預設縮圖。

![使用自訂點陣圖的原始縮圖影像和修改後縮圖影像的圖例](images/customthumbnail.jpg)

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|--------------------------|---------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows 7 或 Windows vista （含 Service Pack 2） (SP2) 和 Windows vista 的平臺更新                          |
| 最低支援的伺服器 | Windowsserver 2008 R2 或 Windows server 2008 Service Pack 2 (SP2) 和 Windows Server 2008 的平臺更新 |
| 最小 Windows SDK      | [Windows適用于 Windows 7 的軟體發展工具組 (SDK) ](https://msdn.microsoft.com/windows/bb980924.aspx)             |

## <a name="building-the-tabthumbnails-sample"></a>建立 TabThumbnails 範例

**若要使用 Microsoft Visual Studio (慣用方法來建立範例)**

1.  開啟 Windows 檔案總管，然後流覽至 TabThumbnails .sln 檔案所在的資料夾。
2.  按兩下方案檔 ( .sln) 開啟 Microsoft Visual Studio 中的檔案。
3.  在 [建置] 功能表上，按一下 [建置方案]。 應用程式是以預設的 \\ Debug 或 \\ Release 目錄來建立。

**若要使用命令提示字元建立範例**

1.  開啟 [命令提示字元] 視窗，並流覽至範例目錄。
2.  輸入 `msbuild TabThumbnails.sln`。

## <a name="related-topics"></a>相關主題

[桌面視窗管理員](dwm-overview.md)

[Windows 程式開發](/windows/desktop/win32-and-com-development)
