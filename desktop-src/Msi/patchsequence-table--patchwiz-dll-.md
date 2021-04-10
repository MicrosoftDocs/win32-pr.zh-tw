---
description: PatchSequence 資料表是用來產生修補程式中的 MsiPatchSequence 資料表。 資料表需要 Windows Installer&160; 3.0 提供的 PATCHWIZ.DLL 版本 \# 。
ms.assetid: bdeccb3b-57c0-4424-9602-348b8048fd46
title: 'PatchSequence 資料表 (PATCHWIZ.DLL) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 382e940d3c0cb6c7be2c8360ab98f2afaf13c799
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852731"
---
# <a name="patchsequence-table-patchwizdll"></a>PatchSequence 資料表 (PATCHWIZ.DLL) 

PatchSequence 資料表是用來產生修補程式中的 [MsiPatchSequence 資料表](msipatchsequence-table.md) 。 資料表需要 Windows Installer 3.0 提供的 [PATCHWIZ.DLL](patchwiz-dll.md) 版本。

下表識別 PatchSequence 資料表的資料行。



| Column      | 類型       | 答案 | Nullable |
|-------------|------------|-----|----------|
| PatchFamily | 識別碼 | Y   | N        |
| 目標      | Text       | Y   | Y        |
| 順序    | 版本    |     | Y        |
| 取代   | 整數    |     | Y        |



 

### <a name="columns"></a>資料行

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

指出此修補程式所屬序列系列的識別碼。

[目標] 和 [PatchFamily] 資料行中的值會一起定義資料表的主要索引鍵。 屬於多個時序系列，或有不同順序（視目標的產品代碼而定）的修補程式可以針對每個配對各有一個資料列。 這個值是用來填入屬於修補程式之 [MsiPatchSequence 資料表](msipatchsequence-table.md) 的 PatchFamily 資料行。

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>目標
</dt> <dd>

目標資料行是用來依產品代碼篩選 PatchFamily。

此資料行中的 Null 值表示此 PatchFamily 適用于修補程式的所有目標。 如果此資料行包含 [TargetImages 資料表](targetimages-table-patchwiz-dll-.md)的外鍵，則會抓取指定之影像的產品代碼，並在 [MsiPatchSequence 資料表](msipatchsequence-table.md)的新修補程式資料列中，用來填入產品代碼值。 如果此資料行包含 GUID，則會使用 GUID 來填入 MsiPatchSequence 資料表中資料列的產品代碼值。

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列
</dt> <dd>

[順序] 資料行中的值會用來填入新修補檔案之 [MsiPatchSequence 資料表](msipatchsequence-table.md) 的 [順序] 資料行。

如果值為 Null，則會自動產生序號。

</dd> <dt>

<span id="Supersede"></span><span id="supersede"></span><span id="SUPERSEDE"></span>取代
</dt> <dd>

此欄位中的 **msidbPatchSequenceSupersedeEarlier** 或1值表示此修補程式會取代此修補程式所屬序列系列中較早的 [小型更新](small-updates.md) 。

此資料行中的值是用來設定 [MsiPatchSequence 資料表](msipatchsequence-table.md) 中新修補程式資料列的 [屬性] 資料行。

</dd> </dl>

### <a name="remarks"></a>備註

從 Windows Installer 3.0 開始提供。

 

 



