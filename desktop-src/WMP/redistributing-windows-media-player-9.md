---
title: 轉散發 Windows Media Player 9 系列
description: 轉散發 Windows Media Player 9 系列
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f48da20123255ae08a0993d361a95deb8ed335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021991"
---
# <a name="redistributing-windows-media-player-9-series"></a>轉散發 Windows Media Player 9 系列

您可以使用下列其中一個安裝程式，在 Windows XP 上安裝 Windows Media Player 9 系列。

-   MPSetupXP.exe
-   MPSetup.exe

> [!Note]  
> MPSetup.exe 是 MPSetupXP.exe 安裝程式的超集合。 它包含 Windows XP 之前發行的作業系統所需的檔案。 在 Windows XP 上執行時，MPSetup.exe 的功能相當於 MPSetupXP.exe，但安裝程式檔案大小卻較大，因為它尚未針對安裝在 Windows XP 作業系統上進行優化。

 

您可以使用下列安裝程式，在 Windows 98 Second Edition、Windows Millennium Edition 或 Windows 2000 上安裝 Windows Media Player 9 系列。

-   MPSetup.exe

以下是安裝時不含 UI 的命令列範例，且不會重新開機或重新開機提示。


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> /P： \# e 參數會指定在 Windows Media Player 安裝期間應該快取 Windows Media Player 安裝套件。 此命令可用來處理未來的作業系統升級。 只有公司 IT 系統管理員才能省略這個命令。 在 \# 命令列中不應包含/p： e 的唯一情況是當您擁有目標系統，並知道目標系統永遠不會升級至較新的作業系統時。 例如，如果您要在 Windows 2000 上安裝 Windows Media Player 9 系列，而且電腦可能會在未來升級為 Windows XP，則必須 \# 在命令列上使用/p： e。 否則，在 Windows XP 安裝之後，將會以 Windows XP 的 Windows Media Player 檔案覆寫 Windows Media Player 的檔案。

 

下表顯示您可以搭配 Windows Media Player 9 系列安裝程式使用的其他參數。



| 參數              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | 防止程式庫遷移。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | 建立嵌套的系統還原點。 如果您的應用程式會建立系統還原點，以將 Windows Media Player 還原點嵌入應用程式還原點內，請使用此程式。                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | 不允許建立系統還原點。 此旗標將會停用建立系統還原點。 在大部分情況下，此旗標不應用於一般軟體轉散發。 只有當您可以代表使用者明確選擇不支援將 Windows Media Player 檔案復原至舊版播放程式時，才應該使用此選項。 此旗標只能用於公司部署或原始設備製造商 (OEM) 安裝。 |



 

## <a name="notes"></a>備註

-   命令列參數會區分大小寫。
-   當您隱藏重新開機提示時，必須檢查 InstallResult 登錄機碼，並處理呼叫安裝程式中的重新開機通知。
-   Windows Media Player 9 系列也會安裝 Windows Media 格式執行時間，因此不需要在相同的軟體轉散發套件中同時包含 Windows Media Player 散發套件和 Windows Media Format runtime 散發套件。 因此，如果您在安裝中包含 MPSetup.exe 或 MPSetupXP.exe，就不需要包含 WMFdist.exe。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**轉散發 Windows Media Player 軟體**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




