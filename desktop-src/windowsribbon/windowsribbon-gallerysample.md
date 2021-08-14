---
title: 資源庫範例
description: 這個程式碼範例會示範使用 Windows 功能區架構中包含的不同資源庫控制項類型所需的標記和程式碼。
ms.assetid: 1a462f4e-e75a-40cf-9c52-0bad0a645d57
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 8c62e8955e737ac78ee5543c0a12febc5436bacd7f9d739bc9af02bacd555d2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118706704"
---
# <a name="gallery-sample"></a>資源庫範例

這個程式碼範例會示範使用 Windows 功能區架構中包含的不同資源庫控制項類型所需的標記和程式碼。 此範例包含的程式碼可以用來以動態方式將專案填入至資源庫，以及處理可支援結果導向 UI 的特殊資源庫預覽事件。

- [使用量](#usage)
  - [建立範例](#building-the-sample)
  - [執行範例](#running-the-sample)
- [支援](#support)
- [最低需求](#minimum-requirements)
- [相關主題](#related-topics)

## <a name="usage"></a>使用量

您可以從[Microsoft 下載中心](https://www.microsoft.com/download/details.aspx?id=9620)以獨立 Microsoft Visual Studio 專案形式下載 Windows 功能區架構範例，或將其安裝為[Windows 軟體開發套件 (SDK) ](https://developer.microsoft.com/windows/downloads/sdk-archive/)的一部分。

- Windows軟體發展工具組 (SDK)  (標準安裝路徑) ：% ProgramFiles% \\ Microsoft sdk \\ Windows \\ \[ 版本號碼 \] \\ 範例 \\ winui \\ WindowsRibbon 資源 \\ 庫

### <a name="building-the-sample"></a>建立範例

下載範例。

安裝 Windows 7 的 Windows SDK，然後開啟其 [組建環境命令] 視窗。 在 [開始] 功能表中，指向 [所有程式]、[Microsoft Windows SDK]，然後按一下 CMD 殼層。

若要組建建置環境命令視窗的範例，您必須先移至範例的來源目錄 在命令提示字元中，輸入 MSBUILD。

若要在 Microsoft Visual Studio 中建置範例，請載入範例方案或專案檔，然後按下 CTRL+SHIFT+B。

### <a name="running-the-sample"></a>執行範例

若要從 [建立環境] 命令視窗執行範例，請執行 \\ 範例源資料夾所包含的 bin Debug 或 bin 發行資料夾中的 .exe 檔案 \\ 。

若要在 Visual Studio 中執行編譯後的範例並進行偵錯，請按 F5。

## <a name="support"></a>支援

[Windows 功能區開發論壇](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment)可討論主題，並詢問與開發 Windows 功能區應用程式相關的問題。

## <a name="minimum-requirements"></a>最低需求



| 需求 | 值 |
|--------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端 | Windows 7<br/> Windowsvista Service Pack 2 (SP2) 和[適用于 Windows Vista 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| 最低支援的伺服器 | Windows Server 2008 R2<br/> Windowsserver 2008 SP2 和[Windows server 2008 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows SDK              | 7.0                                                                                                                                                                      |
| Visual Studio            | 2008                                                                                                                                                                     |
| 標頭檔和 IDL 檔案     | uiribbon .h、uiribbon .idl                                                                                                                                                 |



 

> [!Note]  
> 適用于[Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)的 Windows Vista 和 platform update 的[平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)是一組執行時間程式庫，可讓開發人員將 Windows 功能區應用程式的目標設為 Windows Vista 和 Windows 伺服器2008。 所有 Windows Vista 和 Windows Server 2008 客戶都可以透過 Windows Update 取得平臺更新。 需要適用于[Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)或平臺更新的協力廠商應用程式，可以讓 Windows Update 偵測是否已安裝必要的更新;如果不是，Windows Update 會在背景中下載並安裝它。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用資源庫](ribbon-controls-galleries.md)
</dt> <dt>

[下拉式方塊](windowsribbon-controls-combobox.md)
</dt> <dt>

[下拉式圖庫](windowsribbon-controls-dropdowngallery.md)
</dt> <dt>

[功能區中的資源庫](windowsribbon-controls-inribbongallery.md)
</dt> <dt>

[分割按鈕資源庫](windowsribbon-controls-splitbuttongallery.md)
</dt> <dt>

[集合屬性](windowsribbon-reference-properties-collection.md)
</dt> </dl>

 

 





