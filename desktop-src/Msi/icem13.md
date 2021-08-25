---
description: ICEM13 會確認合併模組不包含發行者原則和設定元件。
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678b89e14cb699bb6207be5c2e14473de2a743494b47ff5ae5e0ccda2a9cc9cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894278"
---
# <a name="icem13"></a>ICEM13

ICEM13 會確認合併模組不包含發行者原則和設定元件。 Publisher 原則和設定元件不應該包含在要用於轉散發的合併模組中，因為這可能會影響使用者電腦上的其他應用程式。

此 ICEM 可在 Windows Installer 2.0 SDK 和更新版本提供的 Mergemod 檔中找到。 如需詳細資訊，請參閱[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

## <a name="result"></a>結果

如果 ICEM13 在合併模組的 [MsiAssembly 資料表](msiassembly-table.md) （屬於發行者原則或設定元件）的 [元件] 欄位中找到指定的元件，則會張貼一則警告訊息。

## <a name="example"></a>範例

ICEM13 會在 [MsiAssembly 資料表](msiassembly-table.md) 中找到具有元件 ' 1 ' 的資料列，而該資料表中的元件 \[ \] 欄位是已包含在合併模組中的發行者原則或設定元件，以張貼下列警告訊息。

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

您可以使用 Windows Installer 安裝發行者原則和設定元件，不建議在合併模組中重新分配這些元件。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Merge Module ICE 參考](merge-module-ice-reference.md)
</dt> </dl>

 

 



