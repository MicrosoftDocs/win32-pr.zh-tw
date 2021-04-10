---
description: Msitool 是可讓您用來建立工具和自訂動作的 makefile。
ms.assetid: c05da933-7e0e-4fbb-a936-517902a363c4
title: Msitool mak
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c3dad9fd65aaa880e9fdb38369843907104dea4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115192"
---
# <a name="msitoolmak"></a>Msitool mak

Msitool 是可讓您用來建立工具和自訂動作的 makefile。 它可搭配 Visual C++ 4.0 版或更新版本使用。 如需詳細資訊，請參閱標頭檔。 它需要在包含這個檔案之前定義一組值。 開發人員通常會將它們放在 .cpp 的開頭，而由 C 編譯器略過 ifdef。 同樣地，資源也會新增至 .cpp 檔案的結尾。 如需詳細資訊，請參閱範例。

VCBIN 可以定義至找到 Visual C++ 工具的目錄，或 makefile 使用 MSVCDIR 和 MSDEVDIR。 如果未定義，則不會指定位置，假設工具位於路徑上。 Visual C++ 5.0 版中的環境變數有個問題，就是如果兩者都不在您的路徑上，連結器就找不到 Msdis100.dll。 如果您將它從 MSDEVDIR 複製到 MSVCDIR，它就會運作。 另一個選項是複製 Msdis100.dll，並 Rc.exe Rcdll.dll 至 MSVCDIR，並將 VCBIN 設定為該。

此工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Installer 開發工具](windows-installer-development-tools.md)
</dt> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



