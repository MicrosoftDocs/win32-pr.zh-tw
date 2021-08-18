---
description: MsiPatchMetadata 資料表包含移除修補程式以及新增/移除程式所使用之 Windows Installer 修補程式的相關資訊。
ms.assetid: b1c30e16-6c91-451a-8b75-7ddbcefcc092
title: MsiPatchMetadata 資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7094e644ff02caa1cbf4b3e53e5761740ff9a5492c92ca746404b1d243e09285
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012896"
---
# <a name="msipatchmetadata-table"></a>MsiPatchMetadata 資料表

MsiPatchMetadata 資料表包含移除修補程式以及 **新增/移除程式** 所使用之 Windows Installer 修補程式的相關資訊。

未在修補資料庫中安裝此資料表的修補程式 ( .msp 檔) 無法移除，而且會遺失 [ **新增/移除程式**] 中的部分資訊。 資料表必須在 patch 檔案的資料庫中，而不是在修補程式的轉換中。

MsiPatchMetadata 資料表具有下列資料行。



| Column   | 類型                         | 答案 | Nullable |
|----------|------------------------------|-----|----------|
| 公司  | [識別碼](identifier.md) | Y   | Y        |
| 屬性 | [識別碼](identifier.md) | Y   | N        |
| 值    | [Text](text.md)             | N   | N        |



 

## <a name="columns"></a>資料行

<dl> <dt>

<span id="Company"></span><span id="company"></span><span id="COMPANY"></span>公司
</dt> <dd>

公司名稱。 空白欄位 (Null 值) 表示資料列包含 Windows Installer 的其中一個標準中繼資料屬性。 如需詳細資訊，請參閱本主題的「備註」一節。

藉由將資料列加入至資料表，並在此欄位中輸入公司名稱，您可以新增任何公司來擴充屬性集。

</dd> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>財產
</dt> <dd>

中繼資料屬性的名稱。

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>價值
</dt> <dd>

中繼資料屬性的值。 這絕對不能是 Null 或空字串。

</dd> </dl>

## <a name="remarks"></a>備註

可在 Windows Installer 3.0 和更新版本中使用。

在 [公司名稱] 欄位中包含 Null 值的 MsiPatchMetadata 資料表中，資料列會參考下列其中一個標準 Windows Installer 中繼資料屬性。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>屬性</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AllowRemoval</td>
<td>指出修補程式是否為 <a href="uninstallable-patches.md">可卸載修補程式</a>。 如果 [值] 欄位包含 0 (零) ，就無法移除修補程式。 如果 [值] 欄位包含一個 (1) ，則修補程式是可卸載修補程式。會註冊此屬性，並使用 <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> 函數來取得其值。 <br/></td>
</tr>
<tr class="even">
<td>ManufacturerName</td>
<td>應用程式的製造商名稱。</td>
</tr>
<tr class="odd">
<td>MinorUpdateTargetRTM</td>
<td>表示修補程式以產品的 RTM 版本或最新的主要升級修補程式為目標。 在包含順序資訊的次要升級修補程式中撰寫此選用屬性，以指出修補程式會移除產品 RTM 版本的所有修補程式，或最新的主要升級修補程式。 這個屬性可在 Windows Installer 3.1 和更新版本中使用。 <br/></td>
</tr>
<tr class="even">
<td>TargetProductName</td>
<td>應用程式或目標應用程式套件的名稱。</td>
</tr>
<tr class="odd">
<td>MoreInfoURL</td>
<td>提供此修補程式特定資訊的 URL。 這個屬性已註冊，而且可以使用 <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> 函數來取得其值。 從 Windows XP Service Pack 2 (SP2) 開始，此值可以是 [<strong>新增/移除程式</strong>] 中顯示之修補程式的支援連結。<br/></td>
</tr>
<tr class="even">
<td>CreationTimeUTC</td>
<td>.Msp 檔的建立時間，格式為 mm-yy HH： MM (month-day-year hour：分鐘) 。</td>
</tr>
<tr class="odd">
<td>DisplayName</td>
<td>適用于公開顯示的修補程式標題。 這個屬性會註冊，而且可以使用 <a href="/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa"><strong>MsiGetPatchInfoEx</strong></a> 函數來取得其值。 從 Windows XP SP2 開始，此值是在 [<strong>新增/移除程式</strong>] 中顯示之修補程式的名稱。<br/></td>
</tr>
<tr class="even">
<td>描述</td>
<td>修補程式的簡短描述。</td>
</tr>
<tr class="odd">
<td>分類</td>
<td>字串值，包含由 patch 作者定義的任意更新分類。 例如，修補程式作者可以指定將每個修補程式分類為一個修正程式、安全性匯總、重大更新、更新、Service Pack 或更新彙總套件。 這是必要屬性。</td>
</tr>
<tr class="even">
<td>OptimizeCA</td>
<td>指出 Windows Installer 是否應該在套用修補程式時略過自訂動作。 這可以減少套用修補程式所需的時間。 OptimizeCA 屬性可以有下列其中一個值：<br/>
<ul>
<li>0-不要略過任何自訂動作。</li>
<li>1-略過屬性和目錄指派自訂動作。 <a href="custom-action-type-35.md">自訂動作類型 35</a> 和 <a href="custom-action-type-51.md">自訂動作類型 51</a> 可以是屬性和目錄指派自訂動作。</li>
<li>2-略過不屬於屬性或目錄指派的立即自訂動作。 立即自訂動作不會在 <a href="customaction-table.md">CustomAction 資料表</a>的 Type 資料行中包含 msidbCustomActionTypeInScript 選項。</li>
<li>4-略過腳本內執行的自訂動作。</li>
</ul>
所有要安裝的修補程式或未略過自訂動作的 OptimizeCA 值都必須相同。 例如，如果安裝了兩個修補程式，且 OptimizeCA 分別設定為值1和2，則不會略過任何自訂動作。 <br/> 處理多個新的修補程式時，可以結合 OptimizeCA 的值。 如果所有修補程式都有 1 (值中包含一個) ，則會略過所有屬性和目錄指派自訂動作。 如果某個修補程式的屬性值為 3 (三個) ，其中一個修補程式的值為 1 (一個屬性) ，則會略過屬性和目錄指派自訂動作。 不過，其他立即的自訂動作會執行，因為並非所有要求的修補程式都會略過。 <br/></td>
</tr>
<tr class="odd">
<td>OptimizedInstallMode</td>
<td>如果這個屬性設定為 1 (要在交易中套用的所有修補程式中的一個) ，則會盡可能將修補程式的應用程式優化。 如需詳細資訊，請參閱 <a href="patch-optimization.md">修補程式優化</a>。 從 Windows Installer 3.1 開始提供。</td>
</tr>
</tbody>
</table>



 

## <a name="validation"></a>驗證

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




