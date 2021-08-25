---
description: ICEM11 會確認可設定的合併模組會列出模組 ModuleIgnoreTable 資料表中的 ModuleConfiguration 資料表和 ModuleSubstitution 資料表。
ms.assetid: f0199137-0a40-40ca-b3cf-ff8eef4309cc
title: ICEM11
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 157248d62f43a0b1a791220e2aeb917ba8273d31b93de69078f9876cddbd2748
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119894428"
---
# <a name="icem11"></a>ICEM11

ICEM11 會確認可設定的合併模組會列出模組[ModuleIgnoreTable 資料表](moduleignoretable-table.md)中的[ModuleConfiguration 資料表](moduleconfiguration-table.md)和[ModuleSubstitution 資料表](modulesubstitution-table.md)。 這可確保無法辨識可設定合併模組 (小於2.0 版的合併工具，) 不會將這些資料表複製到目標資料庫。

此 ICEM 可在 Windows Installer 2.0 SDK 和更新版本提供的 Mergemod 檔中找到。 如需詳細資訊，請參閱[Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。

## <a name="result"></a>結果

如果模組包含未列于 ModuleIgnoreTable 資料表中的 ModuleConfiguration 或 ModuleSubstitution 資料表，ICEM11 會張貼錯誤。

## <a name="example"></a>範例

ICEM11 會針對包含如下所示資料庫專案的模組，張貼下列錯誤訊息。

``` syntax
Error The module contains a ModuleConfiguration or ModuleSubstitution 
table. These tables must be listed in the ModuleIgnoreTable table.
```

[ModuleConfiguration](moduleconfiguration-table.md) (部分) 



| 名稱     | 格式 | 類型   | CoNtextData | DefaultValue |
|----------|--------|--------|-------------|--------------|
| IconKey1 | 1      | Binary | 圖示        | DefaultIcon  |



 

[ModuleSubstitution](modulesubstitution-table.md)



| 資料表   | 資料列              | 資料行 | 值        |
|---------|------------------|--------|--------------|
| 控制 | Dialog1;Control1 | Text   | \[IconKey1\] |



 

[ModuleIgnoreTable](moduleignoretable-table.md)



| 資料表               |
|---------------------|
| ModuleConfiguration |



 

若要修正這個錯誤，請在 ModuleIgnoreTable 資料表中同時包含 ModuleSubstitution 和 ModuleConfiguration 資料表。

## <a name="table-used-during-execution"></a>執行期間所使用的資料表

[ModuleSubstitution](modulesubstitution-table.md)

[ModuleConfiguration](moduleconfiguration-table.md)

[ModuleIgnoreTable](moduleignoretable-table.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Merge Module ICE 參考](merge-module-ice-reference.md)
</dt> </dl>

 

 



