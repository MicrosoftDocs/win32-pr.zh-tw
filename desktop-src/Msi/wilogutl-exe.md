---
description: Wilogutl.exe 有助於分析 Windows Installer 安裝中的記錄檔，並顯示在記錄檔中找到之錯誤的建議解決方案。
ms.assetid: 09aa03ba-992f-47ab-999b-ebdfe85c1ea7
title: Wilogutl.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6734b22afa6aa5d464f3d6b01555e54f240e006b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476024"
---
# <a name="wilogutlexe"></a>Wilogutl.exe

Wilogutl.exe 有助於分析 Windows Installer 安裝中的記錄檔，並顯示在記錄檔中找到之錯誤的建議解決方案。

不會顯示非重大錯誤。 Wilogutl.exe 可以在無訊息模式下執行，也可以使用使用者介面 (UI) 。 此工具會在 UI 和無訊息模式中，以文字檔的形式產生報表。 它最適合用於詳細的 Windows Installer 記錄檔，但也適用于不詳細的記錄檔。 如需詳細資訊，請參閱[記錄](logging.md)。

此工具僅適用于[Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

## <a name="syntax"></a>Syntax

**wilogutl.exe***\[<options>\]\[<source file>\]\[<options>\]\[<report file directory>\]*

您可以使用下列命令列以安靜模式執行。

**wilogutl/q/l** *c： \\ mymsilog。記錄* **/o** *c \\ outputdir \\*

**wilogutl/q/l** *c： \\ mymsilog .log*

## <a name="command-line-options"></a>命令列選項

Wilogutl.exe 使用下列不區分大小寫的命令列選項。 虛線分隔符號可以用來取代斜線。



| 選項 | Description                                                                                                                                                                                     |
|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 無   | 在 UI 模式中執行，不需要命令列選項。                                                                                                                                                   |
| /q     | 指定無訊息模式。 Wilogutl.exe 會產生報表檔案，而且不會顯示使用者介面。                                                                                            |
| /l     | 指定要分析之記錄檔的名稱。 使用無訊息模式時，需要這個選項。                                                                                           |
| /o     | 指定報告檔案的輸出目錄。 只有在以無訊息模式執行時，才會使用這個輸出路徑。 如果選項不存在，就會將報告放在 C： \\ WiLogResults 目錄中。 |



 

以 UI 模式執行時，Wilogutl.exe 會顯示下列對話方塊。




| Name | 描述 | 
|------|-------------|
| Windows安裝程式詳細資訊記錄分析器 | Windows Installer 詳細資訊記錄分析器] 對話方塊可讓使用者選取要分析的記錄檔：<ul><li>[<strong>開啟</strong>] 按鈕會在記事本中開啟檔案。 您可以使用預覽區域來確認已選取正確的記錄檔。</li><li>[ <strong>分析</strong> ] 按鈕會開始記錄檔分析，並顯示詳細的 [記錄檔] 視圖對話方塊。</li></ul> | 
| 詳細記錄檔視圖 | [詳細記錄檔視圖] 對話方塊會顯示記錄的錯誤資訊。 使用 [<strong>上</strong><strong>一步] 和 [下一步]</strong>按鈕，流覽多個錯誤。 若要顯示非嚴重錯誤，請選取 [ <strong>顯示忽略的調試錯誤</strong> ] 核取方塊。 系統會顯示用來執行記錄安裝之電腦上的安裝程式版本。 如果使用較高的許可權來執行已記錄的安裝，則會選取 [提高許可權的 <strong>安裝</strong> ] 核取方塊，並在 [ <strong>用戶端許可權詳細資料</strong> ] 和 [ <strong>伺服器端許可權詳細資料</strong> ] 文字方塊中提供資訊。 [詳細記錄檔視圖] 對話方塊包含下列按鈕：<br /><ul><li><strong>狀態</strong> -顯示 [功能和元件狀態] 對話方塊。</li><li><strong>屬性</strong> -顯示內容對話方塊。</li><li><strong>原則</strong> -顯示原則對話方塊。</li><li><strong>Html 批註記錄</strong> 檔-顯示記錄檔，表示為批註的 html 檔案。</li><li><strong>儲存結果</strong> -將報表檔案儲存至指定的目錄。</li><li><strong>錯誤訊息</strong> 說明-顯示安裝程式錯誤訊息說明。</li><li>說明-顯示 Windows Installer 安裝程式記錄<strong>分析器的說明</strong>。</li><li><strong>如何讀取記錄</strong> 檔-顯示記錄檔說明文件。</li></ul> | 
| 功能和元件狀態 | [ <strong>功能和元件狀態</strong> ] 對話方塊會顯示功能和元件的狀態：<ul><li>[ <strong>功能</strong> ] 欄會顯示安裝套件中的功能名稱。</li><li>[ <strong>元件</strong> ] 欄會顯示安裝套件中的元件名稱。</li><li>[ <strong>已安裝</strong> ] 欄會顯示安裝結束時的功能或元件狀態。</li><li>[ <strong>要求</strong> ] 欄會在安裝功能或元件的狀態時，顯示使用者的選取專案。</li><li>[ <strong>動作</strong> ] 欄會顯示安裝程式針對功能或元件所採取的動作。</li></ul>如需詳細資訊，請參閱 <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetcomponentstatea"><strong>MsiGetComponentState</strong></a> 和 <a href="/windows/desktop/api/Msiquery/nf-msiquery-msigetfeaturestatea"><strong>MsiGetFeatureState</strong></a>。<br /> | 
| 屬性 | [屬性] 對話方塊會在安裝結束時顯示 Windows Installer<a href="properties.md">屬性</a>及其值。 您可以依名稱或依值排序屬性：<ul><li>[ <strong>客戶</strong> 端] 索引標籤會顯示安裝的用戶端部分的屬性和值。</li><li>[ <strong>伺服器</strong> ] 索引標籤會顯示安裝期間伺服器部分的屬性和值。</li><li>[ <strong>嵌套</strong> ] 索引標籤會顯示任何 <a href="concurrent-installations.md">並行安裝</a>的屬性和值。</li></ul> | 
| 原則 | [原則] 對話方塊會在安裝後顯示 <a href="system-policy.md">系統原則</a> 集：<ul><li>針對原則設定 0 (零) 組值表示原則未啟用。</li><li>值 1 (1) 表示已啟用原則。</li><li>值為？  (問號) 表示原則值不會記錄在記錄檔中。</li></ul>如果您需要的原則值不在記錄檔中，請嘗試使用 Regedit.exe 檢查電腦上的登錄機碼是否安裝失敗。<br /> | 




 

## <a name="report-files"></a>報表檔案

在 [**詳細記錄檔視圖**] 對話方塊中執行無訊息模式分析或按一下 [**儲存結果**] 按鈕時，Windows Installer 安裝程式分析器] 工具會產生三個文字檔和一個 HTML 批註記錄檔。

下表將識別報表檔案中的名稱和內容。



| Name                      | 描述                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| logfilename \_summary.txt  | 摘要說明記錄檔。 列出詳細記錄檔視圖對話方塊和第一個錯誤所顯示的資訊。         |
| logfilename \_errors.txt   | 識別錯誤的數目、錯誤和建議的解決方案。 此檔案會列出重大和非重大錯誤。 |
| logfilename \_policies.txt | 識別在安裝結束時設定的原則名稱和值，如同在 [原則] 對話方塊中所設定。                       |
| 詳細資料 \_logfilename.htm  | HTML 批註記錄，其中包含色彩編碼的圖例。                                                                      |



 

## <a name="return-values"></a>傳回值

如果傳遞了不正確命令列引數給無訊息模式作業，Wilogutl.exe 不會執行任何動作，且進程會傳回下表中的其中一個值。



| 值 | 意義                                                                 |
|-------|-------------------------------------------------------------------------|
| 1     | 指定了錯誤的輸出目錄。                                      |
| 2     | 指定了不正確的記錄檔名稱。                                         |
| 3     | 已通過/q，但缺少記錄檔名稱所需的參數/l。 |
| 4     | 傳遞了/l，但缺少安靜模式所需的參數/q。        |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> <dt>

[Windows安裝程式開發工具](windows-installer-development-tools.md)
</dt> </dl>

 

 




