---
description: Msistuff.exe 是一種命令列公用程式，可用來顯示或設定 Setup.exe 啟動程式可執行檔中的資源。
ms.assetid: df79574c-d0e7-45e3-97c1-d62f700260ce
title: Msistuff.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a29c3fd904f137679cf1ce42f3718be151e07c3368b03e6f2807dbfc08656ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145621"
---
# <a name="msistuffexe"></a>Msistuff.exe

Msistuff.exe 是一種命令列公用程式，可用來顯示或設定 Setup.exe 啟動程式可執行檔中的資源。

此工具僅適用于[Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

## <a name="syntax"></a>Syntax

**msistuff setup.exe** *選項 {value}*

如果在選項之後未指定任何資料，則會移除該資源。

## <a name="command-line-options"></a>命令列選項

Msistuff.exe 會使用下列不區分大小寫的命令列選項。 斜線分隔符號也可以用來取代虛線。 如果有一個選項列出多次，則只會使用最後一個專案。



| 選項               | 資源識別碼                  | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|----------------------|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 未指定任何選項 |                              | 顯示 Setup.exe 中可設定的資源。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **-u**               | ISETUPPROPNAME \_ BASEURL      | 設定 BaseURL，Setup.exe 的基底 URL 位置。 如果沒有任何值，Setup.exe 的位置預設為卸載式媒體。 只有以 URL 為基礎的安裝受限於 [**WinVerifyTrust**](/windows/win32/api/wintrust/nf-wintrust-winverifytrust)的檢查。 URL 上的尾端斜線是選擇性的。 可能會省略這個選項。                                                                                                                                                                                                                     |
| **-d**               | ISETUPPROPNAME \_ 資料庫     | 設定 Msi，.msi 檔案的名稱。 這是相對於 Setup.exe 程式位置之 .msi 檔案的相對路徑。 如果未指定-m 選項，就需要此選項。 -D 和-m 選項互斥。 兩者都不能同時指定。                                                                                                                                                                                                                                                    |
| **-m**               | ISETUPPROPNAME \_ 修補程式        | 設定 msp 檔案的名稱。 這是相對於 Setup.exe 程式位置之 .msp 檔的相對路徑。 如果未指定-d 選項，就需要此選項。 -M 和-d 選項互斥。 兩者都不能同時指定。                                                                                                                                                                                                                                                    |
| **-n**               | ISETUPPROPNAME \_ PRODUCTNAME  | 設定產品名稱，也就是產品的名稱。 這會為下載的使用者介面提供橫幅文字中所使用的名稱。 可能會省略這個選項。 如果省略，預設值為 "product"。                                                                                                                                                                                                                                                                                                                            |
| **-o**               | ISETUPPROPNAME \_ 操作    | 指定要執行的作業類型。 有效的值為 INSTALL、MINPATCH、MAJPATCH 和 INSTALLUPD。 如需這些選項的詳細資訊，請參閱 [網際網路下載](internet-download-bootstrapping.md)開機。                                                                                                                                                                                                                                                                                           |
| **-v**               | ISETUPPROPNAME \_ 最小 \_ MSI | 設定電腦上所需的最小 Msi 版本（Windows Installer 最小值）。 如果電腦上沒有 Windows Installer 的最小版本，則會安裝適當的[Instmsi.exe](instmsi-exe.md)以升級 Windows Installer。 這個屬性的值與 PID PAGECOUNT 值具有相同的格式 \_ 。 請參閱 [**頁面計數摘要**](page-count-summary.md) 屬性。 此值必須至少為200，也就是 Windows Installer 版本2.0 的值。 這是必要選項。 |
| **-i**               | ISETUPPROPNAME \_ INSTLOCATION | 設定 InstMsi url 位置（Windows Installer 升級可執行檔的基底 URL 位置）。 如果遺漏此值，升級可執行檔的位置會預設為 Setup.exe 的位置。 可能會省略這個選項。                                                                                                                                                                                                                                                                                                |
| **-a**               | ISETUPPROPNAME \_ INSTMSIA     | 設定 InstMsiA，Windows Installer 升級可執行檔的 ANSI 版本的名稱。 這是與 ISETUPPROPNAME INSTLOCATION 所指定之位置相對的 ANSI 版本 Instmsi.exe 相對路徑 \_ 。 這是必要選項。                                                                                                                                                                                                                                                                                   |
| **-w**               | ISETUPPROPNAME \_ INSTMSIW     | 設定 InstMsiW，Windows Installer 升級可執行檔的 Unicode 版本名稱。 這是相對於 ISETUPPROPNAME INSTLOCATION 所指定之位置的 Unicode 版本 Instmsi.exe 相對路徑 \_ 。 這是必要選項。                                                                                                                                                                                                                                                                             |
| **-p**               | ISETUPPROPNAME \_ 屬性   | 設定屬性 = 值字串。 這些是要包含在命令列中的屬性 = 值配對。 可能會省略這個選項。 此選項不能列出多次，且必須列在命令列上。 之後的所有命令列都會被視為 {value} 的一部分。                                                                                                                                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows安裝程式開發工具](windows-installer-development-tools.md)
</dt> <dt>

[網際網路下載啟動載入](internet-download-bootstrapping.md)
</dt> <dt>

[以 URL 為基礎的 Windows Installer 安裝範例](a-url-based-windows-installer-installation-example.md)
</dt> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 
