---
description: Windows Installer 接受統一資源定位器 (URL) 作為安裝的有效來源。
ms.assetid: f1bb2dc0-4236-4bd7-89a2-f4416b5b9dda
title: 從網際網路下載安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b971129aa2df30bf567be67f0f244b60868ec11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978862"
---
# <a name="downloading-an-installation-from-the-internet"></a>從網際網路下載安裝

Windows Installer 接受統一資源定位器 (URL) 作為安裝的有效來源。 Windows Installer 可以從 URL 位置安裝套件、修補程式和轉換。

如果安裝資料庫位於 URL，則安裝程式會在開始安裝之前將資料庫下載至快取位置。 安裝程式也會從網際網路來源下載適用于使用者選取專案的檔案和封包檔。 如需詳細資訊，請參閱以 [URL 為基礎的 Windows Installer 安裝範例](a-url-based-windows-installer-installation-example.md) 。

例如，若要在 web 伺服器上安裝具有來源的封裝 https://server/share/package.msi ，您可以使用 [命令列](command-line-options.md) 選項來安裝封裝和設定 [公用](public-properties.md) 屬性。

msiexec/i https://server/share/package.msi *PROPERTY = VALUE*

如先前所示的命令列應該傳遞給安裝程式，以從網頁瀏覽器開始安裝。 一般而言，您不應該直接從瀏覽器內按兩下 .msi 檔案，以下載並安裝套件。 這會將 .msi 檔案下載至 [temporary Internet files] 資料夾，並將下列命令傳遞給安裝程式：

**msiexec/i c： \\ windows \\ temporary internet files \\package.msi**

如果封裝需要任何外部來源檔案或封包，則安裝會失敗，因為這些檔案與 .msi 檔案位於相同的位置。

請注意，因為 [**安裝程式**](installer-object.md) 物件在使用者的電腦上未標示為 [SafeForScripting](safeforscripting.md) ，所以使用者需要調整其瀏覽器的安全性設定，範例才能正確運作。

[**InstallProduct**](installer-installproduct.md)方法可以用來從瀏覽器執行先前的命令，作為按 click 事件。


```VB
'Downloading an Installation from the Internet
'The InstallProduct method could be used to run 
'the previous command from a browser as an on-click event.

<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.InstallProduct "https://server/share/package.msi", "PROPERTY=VALUE "
set Installer=Nothing
-->
</SCRIPT>
```



請注意，由於某些 web 伺服器會區分大小寫，因此 [檔案資料表中的 FileName](file-table.md) 欄位必須完全符合原始程式檔的大小寫，以確保支援網際網路下載。

請參閱 [從網際網路下載並安裝修補程式](downloading-and-installing-a-patch-from-the-internet.md)。 如需保護安裝和使用數位憑證的詳細資訊，請參閱 [撰寫安全安裝](guidelines-for-authoring-secure-installations.md) 和 [數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)的指導方針。 如需有關如何建立 Windows Installer 套件之 web 安裝的詳細資訊，請參閱 [網際網路下載](internet-download-bootstrapping.md)啟動載入。

## <a name="available-internet-protocols"></a>可用的網際網路通訊協定

從 Windows Server 2003 和 Windows XP 開始，安裝程式可以使用 HTTP、HTTPS 和檔案通訊協定。 安裝程式不支援 FTP 和 GOPHER 通訊協定。

Windows Installer 2.0 版可以使用 HTTP、FILE 和 FTP 通訊協定，而且無法使用 HTTPS 和 GOPHER 通訊協定。

 

 



