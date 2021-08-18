---
description: Microsoft Windows Installer 接受統一資源定位器 (URL) 作為修補程式的有效來源。
ms.assetid: 11a65123-a8bd-46d8-a416-4fc2f2f1e121
title: 從網際網路下載並安裝修補程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f85f662279ac929d831bb69acc597358c8eddc509738fc71a43df44ec186120c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947352"
---
# <a name="downloading-and-installing-a-patch-from-the-internet"></a>從網際網路下載並安裝修補程式

Microsoft Windows Installer 接受統一資源定位器 (URL) 作為[修補程式](patch-packages.md)的有效來源。 若要在上安裝位於 web 伺服器的修補程式 https://MyWeb/MyPatch.msp ，請使用下列命令列：

**msiexec/p https://MyWeb/MyPatch.msp**

若要避免非預期的結果，請按一下網頁上顯示修補檔案 URL 的連結，不要啟動修補程式。 您也可以使用如下的腳本來安裝修補程式：


```VB
<SCRIPT LANGUAGE="VBScript"> 
<!-- 
Dim Installer
On Error Resume Next
set Installer=CreateObject("WindowsInstaller.Installer")
Installer.ApplyPatch "https://server/share/patch.msp", "", 0, "REINSTALL=ALL REINSTALLMODE=omus"
set Installer=Nothing
-->
</SCRIPT>
```



請注意，因為 [**安裝程式**](installer-object.md) 物件在使用者的電腦上未標示為 [SafeForScripting](safeforscripting.md) ，所以使用者需要調整其瀏覽器的安全性設定，範例才能正確運作。

如需詳細資訊，請參閱[撰寫安全安裝](guidelines-for-authoring-secure-installations.md)和[數位簽章和 Windows Installer](digital-signatures-and-windows-installer.md)的指導方針。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[修補套件](patch-packages.md)
</dt> <dt>

[建立修補程式套件](creating-a-patch-package.md)
</dt> <dt>

[修補自訂應用程式](patching-customized-applications.md)
</dt> <dt>

[從網際網路下載安裝](downloading-an-installation-from-the-internet.md)
</dt> </dl>

 

 



