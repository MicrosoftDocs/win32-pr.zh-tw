---
description: Msimerg.exe 是命令列公用程式，它會使用 MsiDatabaseMerge 將參考資料庫合併至基底資料庫。
ms.assetid: db0c9ae5-a8e8-4eff-ae14-67dcce352483
title: Msimerg.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02ed496f74cdddec7b53f5f343bc852dd828f4e66f34a166f77af079f04ed328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119679518"
---
# <a name="msimergexe"></a>Msimerg.exe

Msimerg.exe 是命令列公用程式，它會使用 [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) 將參考資料庫 [合併](merges-and-transforms.md) 至基底資料庫。

此工具僅適用于[Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

## <a name="syntax"></a>Syntax

**Msimerg** *{基底資料庫} {參考資料庫}*

如果兩個資料庫之間有合併衝突，則會將衝突資訊放置在 \_ MergeErrors 資料表中。

## <a name="command-line-options"></a>命令列選項

無。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows安裝程式開發工具](windows-installer-development-tools.md)
</dt> <dt>

[已發行的版本、工具和可轉散發套件](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



