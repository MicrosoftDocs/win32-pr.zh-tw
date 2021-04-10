---
title: HTMLEditRibbon 範例
description: 這個程式碼範例會示範將現有的 Microsoft Foundation 類別 (MFC) 應用程式，以使用 Windows 功能區所需的標記和程式碼。
ms.assetid: 1505aaea-76d2-47bc-bdc9-12e761da93f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f98d4d76508b812d86a4dab38f8dcec96dadc52
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024809"
---
# <a name="htmleditribbon-sample"></a>HTMLEditRibbon 範例

這個程式碼範例會示範將現有的 Microsoft Foundation 類別 (MFC) 應用程式，以使用 Windows 功能區所需的標記和程式碼。 其建立方式是取得現有的 MFC HTMLEdit 範例應用程式，並修改其程式碼和資源以使用 Windows 功能區。

-   [備註](#remarks)
-   [使用量](#usage)
    -   [建立範例](#building-the-sample)
    -   [執行範例](#running-the-sample)
-   [支援](#support)
-   [最低需求](#minimum-requirements)

## <a name="remarks"></a>備註

針對 MFC 範例，請參閱 [HTMLEdit 範例：包裝 INTERNET EXPLORER MSHTML 編輯控制項](https://msdn.microsoft.com/library/ea8hhwb6(VS.80).aspx)。

## <a name="usage"></a>使用方式

HTMLEditRibbon 範例可從 [Microsoft 下載中心](https://www.microsoft.com/DOWNLOADS/en/default.aspx) 下載為獨立 Microsoft Visual Studio 專案，或安裝為 [Windows 軟體開發套件 (SDK) ](https://msdn.microsoft.com/windows/bb980924.aspx)的一部分。

-   Microsoft 下載中心： [Windows 功能區範例](https://www.microsoft.com/downloads/details.aspx?familyid=141e13e8-b10b-4356-aaa5-609b2981574a&displaylang=en)
-   Windows 軟體開發套件 (SDK)  (標準安裝路徑) ：% ProgramFiles% \\ Microsoft sdk \\ Windows \\ \[ 版本號碼 \] \\ 範例 \\ winui \\ WindowsRibbon \\ HTMLEditRibbon

### <a name="building-the-sample"></a>建立範例

將範例下載至您的硬碟。

安裝適用于 Windows 7 的 Windows SDK，然後開啟其 [組建環境命令] 視窗。 在 [開始] 功能表中，指向 [所有程式]、[Microsoft Windows SDK]，然後按一下 CMD 殼層。

若要組建建置環境命令視窗的範例，您必須先移至範例的來源目錄 在命令提示字元中，輸入 MSBUILD。

若要在 Microsoft Visual Studio 中建置範例，請載入範例方案或專案檔，然後按下 CTRL+SHIFT+B。

### <a name="running-the-sample"></a>執行範例

若要從 [組建環境] 命令視窗執行範例，請執行 \\ 範例源資料夾所包含的 bin Debug 或 bin 發行資料夾中的 .exe 檔案。 \\

若要在 Visual Studio 中執行編譯後的範例並進行偵錯，請按 F5。

## <a name="support"></a>支援

[Windows 功能區開發論壇](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment)可以討論主題，並詢問與開發 Windows 功能區應用程式相關的問題。

## <a name="minimum-requirements"></a>最低需求



| 需求 | 值 |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows 7<br/> Windows Vista Service Pack 2 (SP2) 和 [Windows vista 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| 最低支援的伺服器 | Windows Server 2008 R2<br/> Windows server 2008 SP2 和 [Windows server 2008 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows SDK              | 7.0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| 標頭檔和 IDL 檔案     | uiribbon .h、uiribbon .idl                                                                                                                                                 |



 

> [!Note]  
> Windows [vista 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx) 和 [windows Server 2008 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx) 是一組執行時間程式庫，可讓開發人員將 windows 功能區應用程式的目標設為 Windows vista 和 windows Server 2008。 所有 Windows Vista 和 Windows Server 2008 客戶都可以透過 Windows Update 取得平臺更新。 需要 [適用于 Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx) 或 [Windows Server 2008 平臺更新](https://msdn.microsoft.com/library/dd378748.aspx) 的協力廠商應用程式，可以 Windows Update 偵測是否已安裝必要的更新;如果不是，Windows Update 會在背景中下載並安裝它。

 

 

 





