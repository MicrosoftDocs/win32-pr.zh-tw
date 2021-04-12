---
description: Msival2.exe 是一種命令列公用程式，可執行一組內部一致性評估工具（面向）。
ms.assetid: c48f4584-732a-468d-a651-2c09ce3c9ddd
title: Msival2.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b70ca2ccdeaf72c5191f292a8fa3f9b4de5dd9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195275"
---
# <a name="msival2exe"></a>Msival2.exe

Msival2.exe 是一種命令列公用程式，可執行一組 [內部一致性評估工具（面向）](internal-consistency-evaluators-ices.md)。

此工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

如需有關 Ices-003 和 .CUB 檔案的詳細資訊，請參閱 [使用內部一致性評估](using-internal-consistency-evaluators.md)工具。

## <a name="syntax"></a>Syntax

**Msival2** *{DATABASE} {.cub file} \[ -f \] \[ -l {Logfile} \] \[ -i {ice id} \[ \] \] ： {ICE id} ...*

## <a name="command-line-options"></a>命令列選項

Msival2.exe 會使用下列不區分大小寫的命令列選項。 斜線分隔符號也可以用來取代虛線。



| 選項 | Description                                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| -f     | 篩選出顯示結果中的所有參考訊息。 會顯示所有其他類型的訊息。                                                                                                                                                                                              |
| -i     | 依照指定的順序，僅執行命令列上所列的 Ices-003。 每個 ICE 自訂動作都應該列出，因為它出現在 .CUB 檔案的 [CustomAction 資料表](customaction-table.md) 中。 如果省略這個選項，此工具會執行由 .CUB 檔案的作者指定的一組預設的一組。 |
| -l     | 將結果寫入指定的檔案。 檔案不能已經存在。 如果檔案存在，則不會覆寫該檔案。                                                                                                                                                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Installer 開發工具](windows-installer-development-tools.md)
</dt> <dt>

[內部一致性評估工具-Ices-003](internal-consistency-evaluators-ices.md)
</dt> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



