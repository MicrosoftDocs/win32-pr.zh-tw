---
title: Windows功能區架構範例
description: 本節所包含的主題會提供支援 Windows 功能區架構檔的程式碼範例詳細資料。
ms.assetid: 79d092c9-347b-4b8f-8ba4-a8f696ce6a85
ms.topic: article
ms.date: 07/13/2021
ms.openlocfilehash: 44fa4ae8a10956bdea34b0145b1af34156ff0db0
ms.sourcegitcommit: 63c93e0ad0b48d60b11008767196718feb475cb0
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/13/2021
ms.locfileid: "113691637"
---
# <a name="windows-ribbon-framework-samples"></a>Windows功能區架構範例

本節所包含的主題會提供支援 Windows 功能區架構檔的程式碼範例詳細資料。

## <a name="download-information"></a>下載資訊

您可以從[Microsoft 下載中心](https://www.microsoft.com/download/details.aspx?id=9620)以獨立 Microsoft Visual Studio 專案形式下載 Windows 功能區架構範例，或將其安裝為[Windows 軟體開發套件 (SDK) ](https://developer.microsoft.com/windows/downloads/sdk-archive/)的一部分。

## <a name="samples"></a>範例

| 範例                                                                               | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [SimpleRibbon 範例](windowsribbon-sample1.md)<br/>                          | 這個程式碼範例示範如何執行簡單 Windows 功能區應用程式。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| [CoNtextPopup 範例](windowsribbon-contextpopupsample.md)<br/>               | 這個程式碼範例會示範使用 CoNtextPopups 來執行 Windows 功能區應用程式所需的標記和程式碼。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| [DropDownColorPicker 範例](windowsribbon-dropdowncolorpickersample.md)<br/> | 這個程式碼範例會示範使用 Windows 功能區 DropDownColorPicker 控制項所需的標記和程式碼。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [資源庫範例](windowsribbon-gallerysample.md)<br/>                         | 這個程式碼範例會示範使用功能區架構中包含的不同資源庫控制項類型所需的標記和程式碼。 此範例包含的程式碼可以用來以動態方式將專案填入至資源庫，以及處理可支援結果導向 UI 的特殊資源庫預覽事件。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [HTMLEditRibbon 範例](windowsribbon-htmleditribbonsample.md)<br/>           | 這個程式碼範例會示範將現有的 Microsoft Foundation 類別 (MFC) 應用程式，以使用 Windows 功能區所需的標記和程式碼。 其建立方式是取得現有的 MFC HTMLEdit 範例應用程式，並修改其程式碼和資源，以使用 Windows 功能區。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| [FontControl 範例](windowsribbon-fontcontrolsample.md)<br/>                 | 這個程式碼範例會示範在 Windows 功能區應用程式內執行 FontControl 所需的標記和程式碼。 <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
## <a name="support"></a>支援

[Windows 功能區開發論壇](https://social.msdn.microsoft.com/Forums/windowsdesktop/home?forum=windowsribbondevelopment)可討論主題，並詢問與開發 Windows 功能區應用程式相關的問題。

## <a name="minimum-requirements"></a>最低需求



| 需求 | 值 |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端               | Windows 7<br/> Windowsvista Service Pack 2 (SP2) 和[適用于 Windows Vista 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)<br/>         |
| 最低支援的伺服器               | Windows Server 2008 R2<br/> Windowsserver 2008 SP2 和[Windows server 2008 的平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)<br/> |
| Windows Software Development Kit (SDK) | 7.0                                                                                                                                                                      |
| 標頭檔和 IDL 檔案                   | uiribbon .h、uiribbon .idl                                                                                                                                                 |



 

> [!Note]  
> 適用于[Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx)的 Windows Vista 和 platform update 的[平臺更新](https://msdn.microsoft.com/library/dd378748.aspx)是一組執行時間程式庫，可讓開發人員將 Windows 功能區應用程式的目標設為 Windows Vista 和 Windows 伺服器2008。 所有 Windows Vista 和 Windows Server 2008 客戶都可以透過 Windows Update 取得平臺更新。 需要適用于[Windows Server 2008](https://msdn.microsoft.com/library/dd378748.aspx) [Windows Vista](https://msdn.microsoft.com/library/dd378748.aspx)或平臺更新的協力廠商應用程式，可以讓 Windows Update 偵測是否已安裝必要的更新;如果不是，Windows Update 會在背景中下載並安裝它。

 

 

 





