---
description: Windows Installer 在使用32位或64位 Windows 的電腦上以服務方式執行。
ms.assetid: c02fc401-0c9c-49f6-adcc-ed36bdb18fca
title: 關於64位作業系統上的 Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11fe9969a3fc1ccd9b63f6bd75b145f9dbc7d8c4
ms.sourcegitcommit: 9c8ddec1e955f181beecad0478c1fb79013b5e9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/21/2021
ms.locfileid: "104195609"
---
# <a name="about-windows-installer-on-64-bit-operating-systems"></a>關於64位作業系統上的 Windows Installer

Windows Installer 在使用32位或64位 Windows 的電腦上以服務方式執行。 2.0 版之前的安裝程式版本只能在32位作業系統上安裝和管理32位 Windows Installer 套件。 請注意，您無法在32位作業系統上公告或安裝64位應用程式。

Windows Installer 封裝必須指定為32位或64位封裝;它不能指定為中性。 在使用64位作業系統的電腦上，Windows Installer 服務裝載于64位進程，以安裝32位和64位套件。 Windows Installer 在執行64位作業系統的電腦上安裝三種類型的 Windows Installer 套件：

-   僅包含32位元件的32位封裝。
-   包含一些32位元件的64位套件。
-   僅包含64位元件的64位套件。

下列各節描述兩種類型的 Windows Installer 封裝和64位封裝的 Windows Installer 所提供的新安裝程式屬性。

[32位 Windows Installer 套件](32-bit-windows-installer-packages.md)

[64位 Windows Installer 套件](64-bit-windows-installer-packages.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用64位 Windows Installer 套件](using-64-bit-windows-installer-packages.md)
</dt> </dl>

 

 



