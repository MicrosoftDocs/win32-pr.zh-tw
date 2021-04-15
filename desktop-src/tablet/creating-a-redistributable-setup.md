---
description: 若要將啟用筆墨的應用程式散發到未執行 Windows Vista 或 Windows XP Tablet PC Edition 2005 (也就是執行 Windows XP、Windows Server 2003 或 Windows 2000) 的電腦，您必須在安裝程式中包含必要的合併模組。
ms.assetid: 97515703-0bf4-4230-ae35-181b48b70c40
title: 建立可轉散發安裝程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ad9b9ec8b10032d4a2bb44cca52e5c2f4178b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510757"
---
# <a name="creating-a-redistributable-setup"></a>建立可轉散發安裝程式

若要將啟用筆墨的應用程式散發到未執行 Windows Vista 或 Windows XP Tablet PC Edition 2005 (也就是執行 Windows XP、Windows Server 2003 或 Windows 2000) 的電腦，您必須在安裝程式中包含必要的合併模組。

Mstpcrt .msm merge 模組包含 Windows Installer 安裝共用檔案所需的所有檔案、資源、登錄專案和安裝程式邏輯，而其他平臺需要這些檔案才能執行針對 Tablet PC 開發的非受控應用程式。 Windows Installer ( .msi) 檔會使用 Mstpcrt。 若為使用 [**InkDivider**](inkdivider-class.md) 物件的應用程式，您也必須轉散發 InkDiv .msm。 針對使用 managed 元件的應用程式，您也必須包含這些受管理元件的合併模組檔案。

下表說明 Windows XP Tablet PC Edition 軟體發展工具組 (SDK) 隨附的合併模組檔案。



| 可轉散發合併模組 | Description                                                                                                                    | 檔案                                                       |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| InkDiv .msm<br/>        | 安裝 [**InkDivider**](inkdivider-class.md) 物件的非受控版本。<br/>                                | InkDiv.dll<br/>                                       |
| Mstpcrt .msm<br/>       | 安裝 Tablet PC Platform 版本1.0 的非受控元件。<br/>                                            | Gdiplus.dll、InkEd.dll、Tpcps.dll、Wisptis.exe<br/>   |
| Msvcp60 .msm<br/>       | 安裝 Microsoft Visual C++ runtime 的元件。<br/>                                                            | Msvcp60.dll<br/>                                      |
| Msvcrt.lib .msm<br/>        | 安裝 Microsoft Visual C runtime 的元件。<br/>                                                              | Msvcrt.dll<br/>                                       |
| Tpcman17 .msm<br/>      | 安裝 Tablet PC 平臺執行時間的 managed 元件。 需要安裝 mstpcrt .msm 檔。<br/> | Microsoft.Ink.dll，Microsoft.Ink.resources.dll<br/>   |
| iaCOM .msm<br/>         | 安裝 InkAnalysis API 的自動化元件。<br/>                                                          | IACom.dll<br/>                                        |
| iacore .msm<br/>        | 安裝 InkAnalysis API 的基本類別元件。<br/>                                                          | IACore.dll<br/> IALoader.dll<br/>               |
| IAWinFrm .msm<br/>      | 安裝 InkAnalysis API 的 managed 程式庫元件。<br/>                                                     | Microsoft.Ink.Analysis.dll<br/>                       |
| IAWinFX .msm<br/>       | 安裝 InkAnalysis API 的 Windows Presentation Foundation 元件。<br/>                                     | IAWinFX.dll<br/>                                      |
| 日誌 .msm<br/>       | 安裝「日誌讀取器」元件。<br/>                                                                             | Journal.dll<br/> Microsoft.ink.journal.dll<br/> |
| rtscom .msm<br/>        | 安裝 StylusInput 命名空間的自動化元件。<br/>                                                    | Rtscom.dll<br/>                                       |



 

> [!Note]  
> 若要使用受管理元件合併模組中包含的 Microsoft .NET Framework 功能，您必須已在目的電腦上安裝此架構的 Service Pack 2。

 

## <a name="reduced-feature-set"></a>縮減功能集

啟用筆墨的應用程式會將滑鼠事件視為畫筆移動，以模擬使用 tablet 畫筆。 使用者可以新增筆跡、清除筆跡和儲存筆跡檔。 但是，不是執行 Windows XP Tablet PC Edition 的使用者無法使用辨識和手勢。

Mstpcrt 不包含 Windows 筆記本或 Tablet PC 輸入面板。

[**PenInputPanel**](peninputpanel-class.md)物件無法在 Windows XP Tablet PC Edition 以外的任何作業系統上運作。

## <a name="deployment"></a>部署

> [!Note]  
> 如果您的應用程式使用 managed 程式碼，您也必須部署架構。 安裝 Tablet PC 受管理的元件之前，必須先安裝此架構。

 

若要將 Mstpcrt 包含在 Microsoft Visual Studio .NET 安裝專案中：

1.  在 [方案總管中，選取您的安裝專案。
2.  在 [專案] 功能表上，按一下 [ **加入**]，然後按一下 [ **合併模組**]。
    > [!Note]  
    > 您也可以用滑鼠右鍵按一下 [方案總管中的安裝程式專案名稱，按一下 [**加入**]，然後選取 [**合併模組**]，以連線到 [**加入模組**] 對話方塊。

     

3.  在 [ **新增模組** ] 對話方塊中，流覽至並選取 [ **Mstpcrt**]。
4.  按一下 [開啟]。

Mstpcrt 會加入至您的安裝專案，並顯示在方案總管視窗中。

Windows Installer 將合併模組中包含的檔案新增至 Program Files 資料夾。 若要使用這些檔案，終端使用者必須使用可存取 [Program Files] 資料夾的帳戶登入。

> [!Note]  
> 您必須將 [SelfRegModules 動作](../msi/selfregmodules-action.md) 和 [SelfUnregModules 動作](../msi/selfunregmodules-action.md) 動作新增至安裝順序。 [MsiPublishAssemblies 動作](../msi/msipublishassemblies-action.md)和[MsiUnpublishAssemblies 動作](/windows/desktop/Msi/msiunpublishassemblies-action)動作會從這些動作的安裝順序中收到其順序。

 

 

