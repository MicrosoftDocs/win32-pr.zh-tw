---
title: 桌面應用程式範例
description: 桌面應用程式範例
ms.assetid: 3736dd01-b02f-4056-b19b-0e7cc6c9aa67
keywords:
- Windows媒體裝置管理員、範例
- 裝置管理員，範例
- 桌面應用程式、範例
- WindowsMedia 裝置管理員，桌面應用程式範例
- 裝置管理員，桌面應用程式範例
- wmdmapp 範例應用程式
- 範例，桌面應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a14e8037ccf963f26637711cd6d0e77ea7d2b4ff3cede72fcbded6600226d36c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584242"
---
# <a name="sample-desktop-application"></a>桌面應用程式範例

Windows 媒體裝置管理員隨附一個範例桌面應用程式，稱為 wmdmapp。 此應用程式具有圖形化使用者介面，可讓您流覽連線的裝置、在裝置上建立播放清單，以及將媒體檔案拖曳至裝置。

這個範例應用程式是由兩個部分所組成：

-   wmdapp.exe，此可執行檔會顯示視窗並執行大部分的使用者介面和程式的基本功能，以及
-   proghelp.dll，此為應用程式執行公用程式函式的 helper DLL。 您必須在建立專案之後註冊這個 DLL。

若要編譯範例應用程式，您可以使用 Visual Studio。 下一節將說明如何完成這項操作：

-   [使用 Visual Studio 編譯範例應用程式](compiling-the-sample-application-using-visual-studio.md)

編譯專案之後，請註冊 proghelp.dll 檔案。 若要註冊此 DLL，請開啟命令提示字元，然後流覽至包含此 DLL 的目錄並輸入 `regsvr32 proghelp.dll` 。

 

 




