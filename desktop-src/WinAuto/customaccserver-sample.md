---
title: CustomAccServer 範例
description: CustomAccServer 範例
ms.assetid: 8c3636ef-0993-4ded-a3c0-05cf2de777bb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f7f8ee7d82361177af07aa7ad53a6137c39bc38
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088006"
---
# <a name="customaccserver-sample"></a>CustomAccServer 範例

本主題包含下列各節。

-   [說明](#description)
-   [下載資訊](#download-information)
-   [最低需求](#minimum-requirements)
-   [建立範例](#building-the-sample)
-   [執行範例](#running-the-sample)
-   [相關主題](#related-topics)

## <a name="description"></a>Description

這個範例示範如何針對簡單自訂控制項來執行 Microsoft Active Accessibility server。 控制項的可存取物件包含 (清單方塊) 的根項目，以及 (清單專案的子系。 ) 

## <a name="download-information"></a>下載資訊

CustomAccServer 範例會安裝為 [Microsoft Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windowsvista/bb980924.aspx) 的一部分，並可在下列位置中取得。



| Location    | 路徑/URL                                                                           |
|-------------|------------------------------------------------------------------------------------|
| Windows SDK | % Program Files% \\ Microsoft sdk \\ Windows \\ \[ 版本號碼 \] \\ 範例 \\ winui \\ msaa |



 

## <a name="minimum-requirements"></a>最低需求



| 產品          | 版本                         |
|------------------|---------------------------------|
| 作業系統 | Windows XP、Windows Server 2003 |
| Windows SDK      | 7.0                             |
| Visual Studio    | 2008                            |



 

## <a name="building-the-sample"></a>建立範例

若要使用 Visual Studio 2008 建立範例：

1.  執行 SDK 隨附的 Microsoft Windows 軟體開發套件 (SDK) 設定工具，以將 SDK include 目錄新增至 Visual Studio。
2.  開啟 Windows 檔案總管並流覽至專案目錄。
3.  按兩下 .sln (方案的圖示) 檔案，在 Visual Studio 中開啟專案。
4.  在 [ **組建** ] 功能表上，選取 [ **建立方案** ] 來建立方案。 應用程式將會建立在預設的 \\ Debug 或 \\ Release 目錄中。

若要從命令列建立範例，請參閱下列位置的 Windows SDK 版本資訊中建立範例：% Program Files% \\ Microsoft sdk \\ Windows \\ 7.0 \\ReleaseNotes.htm

## <a name="running-the-sample"></a>執行範例

若要執行範例：

1.  使用命令提示字元或 Windows 檔案總管，流覽至包含新可執行檔的目錄。
2.  在命令列中輸入 AccServer.exe，或按兩下 AccServer.exe 的圖示，從 Windows 檔案總管啟動它。

若要從 Visual Studio 執行，請按 F5 或按一下 [**調試**] 功能表中的 [**開始調試**]。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[範例](samples.md)
</dt> </dl>

 

 




