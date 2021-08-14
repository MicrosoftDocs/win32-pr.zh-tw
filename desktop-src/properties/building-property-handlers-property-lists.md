---
description: 在評估屬性策略之後，您必須決定要在 Windows 檔案總管 UI 中顯示哪些屬性，以及在何處顯示。
ms.assetid: b7af0491-2ece-42b5-8eea-32643854632f
title: 使用屬性清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68dc3f25b1f0223e62a969a5b0846bcbdcaaef9fd93b45c654c367a0c1fc949d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119397818"
---
# <a name="using-property-lists"></a>使用屬性清單

在評估屬性策略之後，您必須決定要在 Windows 檔案總管 UI 中顯示哪些屬性，以及在何處顯示。 有各種不同的位置會以唯讀方式顯示內容。 另一方面，屬性編輯只會在 [ **屬性** ] 對話方塊中啟用。 您可以透過 **預覽窗格** 中的 [**編輯屬性**] 連結或專案的快捷方式功能表來叫用該對話方塊。

屬性清單是以分號分隔的字串，其格式如下。


```
Prop:[flags]PropertyCanonicalName;[flags]PropertyCanonicalName;
```



下表顯示目前唯一可用的旗標。



| 旗標 | 描述                                                                                                                                                                                   |
|------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \*   | 請勿在 [ **預覽] 窗格** 中顯示內容，如 **PreviewDetails** 登錄機碼值中所指示。 如果未設定該屬性的值，請參閱下表後面的範例。 |



 

定義屬性清單之後，您可以透過 **HKEY \_ 類別 \_ 根目錄** 下的標準 [Shell 檔案關聯](../shell/fa-file-types.md)系統，將該字串儲存在登錄中。 下表摘要說明可在特定副檔名的登錄機碼底下指派之屬性清單的值。



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>值</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>FullDetails</td>
<td>屬性會顯示在 [內容<strong>] 對話方塊的</strong>[<strong>詳細資料</strong>] 索引標籤上。 這是檔案類型支援的完整屬性清單。</td>
</tr>
<tr class="even">
<td>PreviewDetails</td>
<td>屬性會顯示在 <strong>預覽窗格</strong>中。</td>
</tr>
<tr class="odd">
<td>PreviewTitle</td>
<td>屬性會顯示在 [ <strong>預覽] 窗格</strong> 的標題區域中，位於專案的縮圖旁邊。 專案的數目上限為3。 如果屬性清單包含的數目超過允許的數目上限，則會忽略其餘的專案。</td>
</tr>
<tr class="even">
<td>TileInfo</td>
<td>當清單視圖在 <strong>圖</strong> 格視圖模式中時，就會顯示內容。 專案的數目上限為3。 如果屬性清單包含的數目超過允許的數目上限，則會忽略其餘的專案。
<blockquote>
[!Note]<br />
此值存在於 Windows XP 中。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>ExtendedTileInfo</td>
<td>當清單視圖處於 <strong>擴充的並排</strong> 顯示模式時，會顯示專案的屬性。</td>
</tr>
<tr class="even">
<td>InfoTip</td>
<td>當使用者將滑鼠停留在專案上時，屬性會顯示在提示中。
<blockquote>
[!Note]<br />
此值存在於 Windows XP 中。
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td>QuickTip</td>
<td>當您很難直接從專案中取得屬性時，例如當必須透過慢速網路連接來存取專案時，就會顯示內容。 建議您在此處指定的屬性（例如類型或大小）不需要開啟檔案資料流程來決定其值。
<blockquote>
[!Note]<br />
此值存在於 Windows XP 中。
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

下列範例會使用 **RecipeKey** 的 ProgID 來定義 PreviewDetails 的配方檔案類型值。

```
HKEY_CLASSES_ROOT
   .recipe
      (Default) = Recipe File
   RecipeFile
      PreviewDetails = prop:*System.Title;*System.Author
```

如 [Shell 檔案關聯](../shell/fa-file-types.md) 主題所述，檔案關聯可以針對最常見的最常見形式來描述。 最特定的形式是單一副檔名，最常見的形式是套用至所有檔案和檔案資料夾的金鑰。 在這兩個極端之間，您也可以定義一個 [PROGID](../shell/fa-progids.md) 來將一組副檔名群組在一起 (例如，將 .jpg 和 jpeg 類型分組為 **jpegfile**) 。 當您定義屬性清單時，您應該針對 Progid 或在某些情況下，針對特定的副檔名來定義它們。 避免依賴廣泛的專案，例如 **AllFileSystemObjects** 金鑰。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[瞭解屬性處理常式](./building-property-handlers-properties.md)
</dt> <dt>

[使用種類名稱](./building-property-handlers-user-friendly-kind-names.md)
</dt> <dt>

[初始化屬性處理常式](./building-property-handlers-property-handlers.md)
</dt> <dt>

[註冊和散發屬性處理常式](./prophand-reg-dist.md)
</dt> <dt>

[屬性處理常式的最佳作法和常見問題](./prophand-bestprac-faq.yml)
</dt> </dl>

 

 
