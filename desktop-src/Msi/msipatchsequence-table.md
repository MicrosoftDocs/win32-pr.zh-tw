---
description: MsiPatchSequence 資料表包含安裝程式所需的所有資訊，以判斷相對於所有其他修補程式的小型更新修補程式順序。
ms.assetid: ae8319ad-8136-4201-9fcf-ea58ce05f88b
title: MsiPatchSequence 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc529c0f7d1a4cdd1bab568f64507922d6e28f539636600f88dea603c4fe1a52
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119519798"
---
# <a name="msipatchsequence-table"></a>MsiPatchSequence 資料表

MsiPatchSequence 資料表包含安裝程式所需的所有資訊，以判斷相對於所有其他修補程式的 [小型更新](small-updates.md) 修補程式順序。 資料表必須在 patch 檔案的資料庫中，而不是在修補程式的轉換中。 套用 [主要升級](major-upgrades.md) 修補程式時，安裝程式會忽略此資料表。 套用 [次要升級](minor-upgrades.md) 修補程式時，安裝程式只會使用此資料表來識別不得排序的已取代修補程式。

**MsiPatchSequence 資料表** 具有下列資料行。



| Column      | 類型                         | 答案 | Nullable |
|-------------|------------------------------|-----|----------|
| PatchFamily | [識別碼](identifier.md) | Y   | N        |
| ProductCode | [GUID](guid.md)             | Y   | Y        |
| 順序    | [版本](version.md)       | N   | N        |
| 屬性  | [整數](integer.md)       | N   | Y        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="PatchFamily"></span><span id="patchfamily"></span><span id="PATCHFAMILY"></span>PatchFamily
</dt> <dd>

指定修補程式是在此欄位中命名之修補程式系列的成員。 相同修補系列中以相同產品版本為目標的修補程式，會依 [順序] 資料行中的值進行排序。 修補程式系列內的修補程式會依照順序遞增順序套用至目標產品。 PatchFamily 也可用來判斷要取代的修補程式。 修補程式可能會在多個資料列中列出，而且如果它適用于多個產品或包含多個修正，則屬於多個修補程式系列。

Windows Installer 不會以任何不同的方式來解讀 PatchFamily 值，而不是比較是否等於其他 PatchFamily 值。 PatchFamily 值在一組修補程式以目標的 ProductCode 中必須是唯一的。 在複雜的修補案例中，PatchFamily 識別碼可能必須是全域唯一的。

</dd> <dt>

<span id="ProductCode"></span><span id="productcode"></span><span id="PRODUCTCODE"></span>ProductCode
</dt> <dd>

此欄位中的值是選擇性的。 如果在此欄位中輸入 [產品代碼](product-codes.md) GUID，並將修補程式套用至指定的產品，則會將修補程式排序並套用為指定之 PatchFamily 的成員。 如果在此欄位中輸入產品代碼 GUID，而修補程式未套用至 [ProductCode] 所指定的產品，則會忽略此資料列。 如果 [ProductCode] 中的值為 Null，則會將修補程式排序並套用為所有修補目標的 PatchFamily 成員，而不論產品程式碼為何。

修補程式可能會在相同的 PatchFamily 中有多個資料列，而修補程式的目標每個產品都有不同的 ProductCode。 PatchFamily 的一個資料列可以針對 ProductCode 指定 Null。 如果目標產品符合具有非 Null 的 ProductCode 的資料列，安裝程式會使用相符的資料列，並使用 Null 的 ProductCode 來忽略該資料列。 如果指定的產品代碼沒有符合目標，修補程式就會排序，並套用為所有修補目標的 PatchFamily 成員，而不論產品代碼為何。

</dd> <dt>

<span id="Sequence"></span><span id="sequence"></span><span id="SEQUENCE"></span>序列
</dt> <dd>

[順序] 資料行中的值會指定此修補程式在指定 PatchFamily 中的順序。 順序中的值是以 [版本](version.md) 資料的格式表示。 值包含1到4個欄位，且每個欄位的範圍為0到65535。 PatchFamily 的成員會依順序值的遞增順序排序並套用至目標產品。 例如，下列六個值會增加：1、1.1、1.2、2.01、2.01.1、2.01.1.1。

</dd> <dt>

<span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性
</dt> <dd>

如果資料列中有 **msidbPatchSequenceSupersedeEarlier** 屬性，表示 [小型更新](small-updates.md) 修補程式會取代相同 PatchFamily 中具有較小順序值的所有修補程式所提供的更新。 此修補套裝程式含在指定的 PatchFamily 中，舊版修補程式所提供的所有修正。 此屬性並不表示在所有情況下，此修補程式都會取代先前的修補程式，因為較舊的修補程式可以屬於多個修補程式系列。

在任何情況下， [小的更新](small-updates.md) 修補程式無法取代 [次要升級](minor-upgrades.md) 或 [重大升級](major-upgrades.md) 修補程式（即使已設定 **msidbPatchSequenceSupersedeEarlier** ）。 

| 名稱                                   | 值 | 意義                                                           |
|----------------------------------------|-------|-------------------------------------------------------------------|
|                                        | 0x00  | 指出簡單的排序值。                              |
| **msidbPatchSequenceSupersedeEarlier** | 0x01  | 表示取代此系列中較早修補程式的修補程式。 |



 

</dd> </dl>

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



