---
title: 轉散發 Windows Media Player 11
description: 轉散發 Windows Media Player 11
ms.assetid: 3348821f-6d72-40c2-954b-0046ce502401
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674da0298196f0749a549670bf9bd7c4095b6e7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021222"
---
# <a name="redistributing-windows-media-player-11"></a>轉散發 Windows Media Player 11

您可以使用下列其中一個安裝程式，在 Windows XP 上安裝 Windows Media Player 11，其中 *localeId* 是地區設定識別碼。

-   wmp11-windowsxp-x86-*localeId*.exe
-   wmp11-windowsxp-x64-*localeId*

以下是安裝時不含 UI 的命令列範例，且不會重新開機或重新開機提示。


```
wmp11-windowsxp-x86-enu.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



下表顯示您可以搭配 Windows Media Player 11 安裝程式使用的其他參數。



| 參數              | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | 防止程式庫遷移。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | 建立嵌套的系統還原點。 如果您的應用程式會建立系統還原點，以將 Windows Media Player 還原點嵌入應用程式還原點內，請使用此程式。                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | 不允許建立系統還原點。 此旗標將會停用建立系統還原點。 在大部分情況下，此旗標不應用於一般軟體轉散發。 只有當您可以代表使用者明確選擇不支援將 Windows Media Player 檔案復原至舊版播放程式時，才應該使用此選項。 此旗標只能用於公司部署或原始設備製造商 (OEM) 安裝。 |
| /DefaultService        | 設定初始的線上商店。 如需詳細資訊，請參閱 [安裝線上商店的命令列參數](setup-command-line-parameters-for-online-stores.md)。                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**轉散發 Windows Media Player 軟體**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




