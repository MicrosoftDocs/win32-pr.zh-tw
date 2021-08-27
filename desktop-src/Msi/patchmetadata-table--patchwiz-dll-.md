---
description: PatchMetadata 資料表包含移除修補程式所需之 Windows Installer 修補程式的相關資訊，以及新增/移除程式所使用的資訊。
ms.assetid: 09a06de4-0713-4e92-ab29-f34f6c94b677
title: 'PatchMetadata 資料表 (PATCHWIZ.DLL) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af760fbe286cf37cdb3aefe389ee8d09d7a759d3
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475444"
---
# <a name="patchmetadata-table-patchwizdll"></a>PatchMetadata 資料表 (PATCHWIZ.DLL) 

PatchMetadata 資料表包含移除修補程式所需之 Windows Installer 修補程式的相關資訊，以及新增/移除程式所使用的資訊。 PatchMetadata 資料表中的所有屬性都會加入至 .msp 檔案的 [MsiPatchMetadata 資料表](msipatchmetadata-table.md) 中，以取得修補程式。

PatchMetadata 資料表在 patch 建立屬性檔中是必要的， (. pcp 檔案中的 MinimumRequiredMsiVersion 等於300的) [檔案。](properties-table-patchwiz-dll-.md) 如果 MinimumRequiredMsiVersion 不等於300，則資料表是選擇性的。

PatchMetadata 資料表具有下列資料行。



| Column   | 類型 | 答案 | Nullable |
|----------|------|-----|----------|
| 公司  | text | Y   | Y        |
| 屬性 | text | Y   | N        |
| 值    | text |     | Y        |



 

### <a name="columns"></a>資料行

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>公司
</dt> <dd>

公司名稱。 空白欄位 (Null 值) 表示此資料列包含其中一個標準中繼資料屬性。 公司可以將資料列加入至資料表，並在此欄位中輸入公司名稱，以擴充屬性集。

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產
</dt> <dd>

中繼資料屬性的名稱。 PatchMetadata 資料表中需要 AllowRemoval、ManufacturerName、TargetProductName、MoreInfoURL、DisplayName、Description 和分類屬性。 如果 [公司] 欄位是空的，則這個欄位必須包含下列其中一個標準中繼資料屬性 (Null 值) 。




| 屬性 | 描述 | 
|----------|-------------|
| AllowRemoval | 整數值，指出修補程式是否為 <a href="uninstallable-patches.md">可卸載修補程式</a>。 如果 [值] 欄位包含 0 (零) ，就無法移除修補程式。 如果 [值] 欄位包含1個 (一個) ，則修補程式是可卸載修補程式。 此為必要屬性。這個屬性已註冊，而且可以使用 <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> 函數來取得其值。<br /> | 
| ManufacturerName | 字串值，其中包含應用程式的製造商名稱。 這是必要屬性。 | 
| MinorUpdateTargetRTM | 表示修補程式以產品的 RTM 版本或最新的主要升級修補程式為目標。 在包含順序資訊的次要升級修補程式中撰寫此選用屬性，以指出修補程式會移除產品 RTM 版本的所有修補程式，或最新的主要升級修補程式。 從 Windows Installer 3.1 開始，可以使用這個屬性。<blockquote>[!Note]<br />若要要求安裝 Windows Installer 3.1 以套用修補程式，請在 pcp 檔案的<a href="properties-table-patchwiz-dll-.md">Properties 資料表</a>中，將 MinimumRequiredMsiVersion 屬性設定為310。</blockquote><br /><br /> | 
| TargetProductName | 包含應用程式或目標應用程式套件名稱的字串值。 這是必要屬性。 | 
| MoreInfoURL | 字串值，包含指向此修補程式資訊的 URL。 這個必要屬性已註冊，而且可以使用 <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> 函數來取得其值。 從 Windows XP Service Pack 2 (SP2) 開始，此值可以是 [新增/移除程式] 中顯示之修補程式的支援連結。<br /> | 
| CreationTimeUTC | 字串值，包含 .msp 檔的建立時間，格式為 mm-dd-yy HH： MM (月-日-年小時：分鐘) 。 這是選用屬性。 | 
| DisplayName | 字串值，包含適用于公開顯示之修補程式的標題。 這是必要屬性。 這個屬性已註冊，而且可以使用 <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> 函數來取得其值。 從 Windows XP SP2 開始，此值是在 Windows XP sp2 開頭的 [新增/移除程式] 中顯示的修補程式名稱。<br /> | 
| Description | 包含修補程式簡短描述的字串值。 這是必要屬性。 | 
| 分類 | 字串值，包含由 patch 作者定義的任意更新分類。 例如，修補程式作者可以指定將每個修補程式分類為一個修正程式、安全性匯總、重大更新、更新、Service Pack 或更新彙總套件。 這是必要屬性。 | 
| OptimizedInstallMode | 如果這個屬性設定為 1 (要在交易中套用的所有修補程式中的一個) ，則會盡可能將修補程式的應用程式優化。 如需詳細資訊，請參閱 <a href="patch-optimization.md">修補程式優化</a>。 從 Windows Installer 3.1 開始提供。 | 




 

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值
</dt> <dd>

中繼資料屬性的值。 這絕對不能是 Null 或空字串。 這個值可以當地語系化。

</dd> </dl>

### <a name="remarks"></a>備註

從 Windows Installer 3.0 開始提供。

所有撰寫至 PatchMetadata 資料表的屬性都會新增至 msp 檔案的 MsiPatchMetadata 資料表中。 AllowRemoval、MoreInfoURL 和 DisplayName 屬性都會註冊，而且可透過 [**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)存取。

 

 




