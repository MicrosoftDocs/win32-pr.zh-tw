---
description: 下列範例顯示如何使用 Windows Installer 3.0 和更新版本，以撰寫修補程式的順序來套用修補程式。
ms.assetid: 98771652-cec2-4371-8132-a741cf8431fb
title: 多個修補範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2d10274531ac4906ef61a49caee9ccbcde98bbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106983575"
---
# <a name="multiple-patching-example"></a>多個修補範例

下列範例顯示如何使用 Windows Installer 3.0 和更新版本，以撰寫修補程式的順序來套用修補程式。

## <a name="example"></a>範例

在此範例中，有三個修補程式： QFE1、QFE2 和 ServicePack1，而且每個都有 [MsiPatchSequence](msipatchsequence-table.md) 資料表。 這些修補程式已撰寫成要套用至1.0 版的應用程式。



| 修補程式名稱   | 修補類型    | 序號 |
|--------------|---------------|-----------------|
| QFE1         | Small Update  | 1.1.0           |
| QFE2         | Small Update  | 1.2.0           |
| ServicePack1 | 次要升級 | 1.3.0           |



 

每個修補程式的 [MsiPatchSequence](msipatchsequence-table.md) 資料表只有一筆記錄，其中包含 patch 系列、產品代碼和序號。 這三個修補程式全都套用至相同的產品，而且屬於相同的 patch 系列（名為 AppPatch）。 沒有任何修補程式具有 **msidbPatchSequenceSupersedeEarlier** 屬性。

QFE1 [small update](small-updates.md)的[MsiPatchSequence 資料表](msipatchsequence-table.md)。 

| PatchFamily | ProductCode                            | 順序 | 屬性 |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.1.0    |            |



 

QFE2 [small update](small-updates.md)的[MsiPatchSequence 資料表](msipatchsequence-table.md)。 

| PatchFamily | ProductCode                            | 順序 | 屬性 |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.2.0    |            |



 

用於 ServicePack1[次要升級](minor-upgrades.md)的[MsiPatchSequence 資料表](msipatchsequence-table.md)。 

| PatchFamily | ProductCode                            | 順序 | 屬性 |
|-------------|----------------------------------------|----------|------------|
| AppPatch    | {18A9233C-0B34-4127-A966-C257386270BC} | 1.3.0    |            |



 

如果使用者安裝1.0 版的產品，然後再套用 QFE2，然後在稍後決定要套用 QFE1，Windows Installer 可確保在 QFE2 上 QFE1 套用修補應用程式的有效順序。 如果使用者套用 ServicePack1，然後在日後套用 QFE2 和 QFE1，Windows Installer 可確保修補應用程式在產品上的有效順序 QFE1 在 QFE2 之前，以及在 ServicePack1 之前。

如果 ServicePack1 在其 [MsiPatchSequence](msipatchsequence-table.md)資料表的 Attributes 資料行中設定 **msidbPatchSequenceSupersedeEarlier** ，這表示 service PACK 包含 QFE1 和 QFE2 中的所有變更。 在此情況下，套用 ServicePack1 時，不會套用 QFE1 和 QFE2。

**Windows Installer 2.0：** 不支援。 早于 Windows Installer 3.0 的版本，每個交易只可安裝一個修補程式，而修補程式會依照提供的順序套用。 在上述範例中，如果先套用 QFE2，然後套用 QFE1，則這是兩筆交易，而修補程式會套用至順序 QFE2 中的應用程式1.0 版，後面接著 QFE1。 如果先套用 ServicePack1，則 QFE1 或 QFE2 無法套用於稍後的交易，因為 ServicePack1 是變更應用程式版本的次要升級。 QFE1 和 QFE2 只能套用至應用程式的1.0 版。

 

 



