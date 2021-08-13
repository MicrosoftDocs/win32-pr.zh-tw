---
description: 可設定的啟動程式可執行檔 (Setup.exe) 和設定工具 ( Msistuff.exe) 隨附于 Windows SDK 開發人員的 Windows Installer 元件中。
ms.assetid: 95fcea5c-b107-48b7-9ae8-84629353c554
title: 設定 Setup.exe 資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3c181453f689b7f2c273ba8726097e5d1cd134d1b9675c8ffc42de42d902b89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118638727"
---
# <a name="configuring-the-setupexe-resources"></a>設定 Setup.exe 資源

可設定的啟動程式可執行檔 (Setup.exe) 和設定工具 ( [Msistuff.exe](msistuff-exe.md)) 隨附于 Windows SDK[開發人員的 Windows Installer 元件](platform-sdk-components-for-windows-installer-developers.md)中。 藉由使用 Msistuff.exe 設定 Setup.exe 中的資源，開發人員可以輕鬆地建立 Windows Installer 套件的 web 安裝。 如需詳細資訊，請參閱 [網際網路下載](internet-download-bootstrapping.md)啟動載入。

輸入下列命令列將以[URL 為基礎的 Windows Installer 安裝範例](a-url-based-windows-installer-installation-example.md)中所述的範例來設定資源。

`MsiStuff setup.exe /u https://www.blueyonderairlines.com/Products/MySetup /d MySetup.msi /n MySetup /v 150 /i https://www.blueyonderairlines.com/Products/Common/InstMsi /a Ansi/Instmsi.exe /w Unicode/Instmsi.exe`

[繼續](sign-setup-exe-and-mysetup-msi.md)

 

 



