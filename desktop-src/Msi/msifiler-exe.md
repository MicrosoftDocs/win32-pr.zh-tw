---
description: MsiFiler.exe 會根據來原始目錄，在檔案資料表中填入檔案版本、語言和大小。 它也可以使用檔案雜湊來更新 MsiFileHash 資料表。
ms.assetid: cc3db60b-0b1d-4582-8b40-0b55f83e00be
title: Msifiler.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2d7aeceae7abd8a9786079788e68c7d7bda35ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991709"
---
# <a name="msifilerexe"></a>Msifiler.exe

MsiFiler.exe 會根據來原始目錄，在檔案 [資料表](file-table.md) 中填入檔案版本、語言和大小。 它也可以使用檔案雜湊來更新 [MsiFileHash 資料表](msifilehash-table.md) 。

## <a name="syntax"></a>Syntax

**msifiler.exe-d** *{database}* **\[ -v \] \[ -h \] \[ -s ALTSOURCE \]**

## <a name="command-line-options"></a>命令列選項

Msifiler.exe 會使用下列不區分大小寫的命令列選項。 斜線分隔符號也可以用來取代虛線。



| 選項 | 參數   | Description                                                                                                                                                                  |
|--------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -d     | *database*  | 要更新的資料庫 ( .msi 檔案) 。                                                                                                                              |
| -v     |             | 使用詳細資訊模式。                                                                                                                                                            |
| -H     |             | 填入 [MsiFileHash 資料表](msifilehash-table.md)。 如果資料表不存在，就會建立資料表。 MsiFileHash 資料表只能搭配未建立版本檔使用。 |
| -S     | *ALTSOURCE* | ALTSOURCE 會指定用來尋找檔案的替代目錄。                                                                                                              |



 

此工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Installer 開發工具](windows-installer-development-tools.md)
</dt> <dt>

[使用目錄資料表](using-the-directory-table.md)
</dt> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



