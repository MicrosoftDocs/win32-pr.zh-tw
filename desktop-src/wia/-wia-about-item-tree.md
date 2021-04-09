---
description: 在 Windows Vista 中，Windows 映像取得 (WIA) 專案樹狀結構已大幅變更。
ms.assetid: dda87bcc-2315-4f0d-87a0-d5a33d5d929a
title: 關於 IWiaItem2 專案樹狀結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4d3e7d39319c7b1c94f88612c5d571f17f2a027
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849360"
---
# <a name="about-the-iwiaitem2-item-tree"></a>關於 IWiaItem2 專案樹狀結構

在 Windows Vista 中，Windows 映像取得 (WIA) 專案樹狀結構已大幅變更。 [**IWiaItem2**](-wia-iwiaitem2.md) 專案用來代表裝置屬性和裝置資料。 映射應用程式會看到 Windows 映像取得 (WIA) 2.0 裝置作為專案的階層式樹狀結構，其中包含代表裝置本身的根專案，以及代表可程式化資料來源、影像或包含影像之資料夾等專案的子專案。

-   [應用程式專案](#application-items)
-   [專案旗標](#item-flags)
-   [專案類別](#item-categories)
-   [根專案](#root-item)
-   [資料項目](#data-item)
-   [相關主題](#related-topics)

## <a name="application-items"></a>應用程式專案

應用程式可以看到的 WIA 2.0 專案樹狀結構與 WIA 2.0 迷你驅動程式所建立和維護的樹狀結構不同。 當迷你驅動程式建立樹狀結構時，WIA 2.0 服務會使用此 WIA 2.0 專案樹狀結構作為指南，以建立可供影像應用程式查看的樹狀結構複本。 複製之樹狀結構中的專案稱為 *應用程式* 專案。 迷你驅動程式所建立之樹狀結構中的專案稱為 *驅動程式* 專案。

WIA 專案可以代表掃描器的檔送紙器的可程式化資料來源，或是儲存在該裝置上的資料。 WIA 裝置應該分成個別的專案，以描述該裝置所產生的不同資料。

例如，支援平板掃描和檔送紙器掃描的 WIA 掃描器可能會分成兩個子專案。 其中一個代表平板掃描功能，另一個則代表檔送送掃描功能。

在平台掃描器上配置並同時掃描的多個映射可以放在一個資料夾中。 使用分割篩選 ([**IWiaSegmentationFilter**](-wia-iwiasegmentationfilter.md)) 之後，每個影像或子領域都可以建立為資料夾的子專案。

將相片儲存 ( 「電影」 ) 的相機裝置的 WIA 樹狀目錄可以分成代表資料夾、子資料夾和相片的專案。

## <a name="item-flags"></a>專案旗標

WIA 專案旗標有助於分類特定 WIA 專案的內容或支援的行為。 WIA 專案旗標分為兩個群組。

1.  專案狀態旗標會報告 WIA 專案的目前狀態，例如 [**WiaItemTypeDisconnected**](-wia-wia-item-type-flags.md)、 **WiaItemTypeDeleted** 等等。
2.  專案資料標記法/使用方式旗標會報告 WIA 專案代表的資料，或在傳送時可能產生的資料。 例如， [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) 是一個資料表示旗標，會向應用程式指出與目前 WIA 專案相關聯的資料是影像資料，而且應該具有影像資料屬性。 **WIA \_IPA \_ 專案 \_ 旗標** 是一種專案使用方式旗標，會告知應用程式可設定 wia 專案，並遵循一組預先定義的設定規則（以 [**WIA \_ IPA \_ 專案 \_ 類別**](-wia-wiaitempropcommonitem.md) 為依據），而且設定可能會變更每個資料傳輸的結果。  (如需類別目錄定義的詳細資訊，請參閱 [專案類別](#item-categories) 目錄專案類別目錄。 ) 

下圖顯示 WIA 專案樹狀結構的範例，以及可能與每個專案相關聯的各種旗標。

![樹狀目錄中專案的專案旗標範例](images/scannertree1.jpg)

## <a name="item-categories"></a>專案類別

使用 [**wia \_ IPA \_ 專案 \_ 類別目錄**](-wia-wiaitempropcommonitem.md) 屬性值，將 WIA 專案分組成類別目錄。 這些類別定義要如何處理或使用 WIA 專案。 例如，如果專案代表已完成的檔案 (WIA \_ 類別目錄 \_ 已完成檔案 \_) ，則 wia 應用程式應該假設資料是靜態的，而且位於裝置上。 如果專案代表送紙器 (WIA \_ 類別 \_ 送紙器) ，應用程式應該會預期它包含所需的檔送紙器內容，並如同檔送紙器般運作。

WIA 定義的類別如下：

-   WIA \_ 類別 \_ AUTO
-   WIA \_ 類別 \_ 送紙器
-   WIA \_ 類別 \_ 膠捲
-   WIA \_ 類別 \_ 已完成檔案 \_
-   WIA \_ 類別的 \_ 平板

例如，掃描器的平板專案可能會將 [**wia \_ IPA \_ 專案 \_ 旗標**](-wia-wiaitempropcommonitem.md) 設為 [**WiaItemTypeImage**](-wia-wia-item-type-flags.md)、 **WiaItemTypeTransfer** 和 **WiaItemTypeProgrammableDataSource**，並將 [ **wia \_ IPA \_ 專案 \_ 類別目錄** ] 屬性設定為 [wia 類別] \_ \_ 平板。

下表顯示具有專案旗標和 WIA 專案的 WIA 類別目錄群組。 此資料表不包含由 WIA 定義之 WIA 專案旗標的完整清單。



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>WIA 分類</th>
<th>有效的 WIA 專案旗標</th>
<th>WIA 屬性集</th>
<th>WIA 專案</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>WIA_CATEGORY_AUTO</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFile</strong></a></li>
</ul></td>
<td>屬性集包含自動設定的掃描器屬性。</td>
<td>代表掃描器自動設定掃描設定的 WIA auto 專案。</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FEEDER</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
</ul></td>
<td>屬性集包括送紙器掃描器控制項屬性， (通常是影像和檔專屬屬性集) 。</td>
<td>WIA 送紙器專案，包括代表檔前端和上一頁頁面的子專案。</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FILM</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
</ul></td>
<td>屬性集包含膠捲掃描器控制項屬性， (通常是影像和檔特定屬性集) 。</td>
<td>WIA 膠捲專案，包括代表個別掃描畫面格的子專案。</td>
</tr>
<tr class="even">
<td>WIA_CATEGORY_FINISHED_FILE</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeAudio</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeVideo</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
</ul></td>
<td>此專案上設定的屬性取決於所報告的專案類型。 例如， <a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a> 應該包含某些影像專案屬性，例如每圖元的位等等。</td>
<td>WIA 儲存專案（包括代表已完成檔案內容的子專案） (資料檔案，例如 JPEG、HTML、TXT 等) 。</td>
</tr>
<tr class="odd">
<td>WIA_CATEGORY_FLATBED</td>
<td><ul>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeProgrammableDataSource</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeImage</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeDocument</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeTransfer</strong></a></li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeFolder</strong></a>—如果掃描器支援多重專案掃描，可能會出現此情況。</li>
<li><a href="-wia-wia-item-type-flags.md"><strong>WiaItemTypeGenerated</strong></a>：如果應用程式在多專案掃描會話期間產生 WIA 專案，可能會出現此情況。</li>
</ul></td>
<td>屬性集包含平台掃描器控制項屬性， (通常是影像和檔特定屬性集) 。</td>
<td>WIA 平板專案，包括代表掃描器平板玻璃上掃描之區域的子專案。</td>
</tr>
</tbody>
</table>



 

下圖顯示 WIA 專案樹狀結構的範例，以及可能與每個專案相關聯的各種類別。

![樹狀目錄中專案的專案類別範例](images/scannertree2.jpg)

## <a name="root-item"></a>根專案

WIA 根專案是以 [**WiaItemTypeRoot**](-wia-wia-item-type-flags.md) 和 **WiaItemTypeDevice** 旗標標記的資料夾專案，代表裝置本身。 它包含像是製造商、裝置名稱和驅動程式屬性的裝置屬性，例如驅動程式版本和使用者介面類別別識別碼 (CLSID) 。 影像應用程式會藉由呼叫 [**IWiaDevMgr2：： CreateDevice**](-wia-iwiadevmgr2-createdevice.md) 方法，取得 WIA 專案樹狀結構的根。 應用程式會透過列舉樹狀結構，使用根項目來取得個別子 WIA 專案的存取權 (查看 [**IEnumWiaItem2**](-wia-ienumwiaitem2.md)) 。

## <a name="data-item"></a>Data Item

任何可以用來傳送資料的專案都會被視為資料項目。 這包括以 [**WiaItemTypeProgrammableDataSource**](-wia-wia-item-type-flags.md) 旗標標記的專案。

資料夾專案和 nonfolder 專案可以藉由使用 [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) 旗標標記來公開傳輸資料的能力。 具有此旗標設定的任何專案都必須提供下列 WIA 專案屬性：

-   [**WIA \_ IPA \_ 訪問 \_ 許可權**](-wia-wiaitempropcommonitem.md)
-   [**WIA \_ IPA \_ 專案 \_ 大小**](-wia-wiaitempropcommonitem.md)
-   [**WIA \_ IPA \_ 緩衝區 \_ 大小**](-wia-wiaitempropcommonitem.md)
-   [**WIA \_ IPA \_ 格式**](-wia-wiaitempropcommonitem.md)
-   [**WIA \_ IPA \_ 慣用 \_ 格式**](-wia-wiaitempropcommonitem.md)
-   [**WIA \_ IPA \_ TYMED**](-wia-wiaitempropcommonitem.md)
-   [**WIA \_ IPA \_ \_ 副檔名**](-wia-wiaitempropcommonitem.md)

以 [**WiaItemTypeTransfer**](-wia-wia-item-type-flags.md) 旗標標記的可程式化資料來源專案，也必須提供資料項目目必要屬性集。

根據專案的旗標設定，WIA 資料項目可能會有其他屬性。 例如，使用 [**WiaItemTypeImage**](-wia-wia-item-type-flags.md) 旗標標記的 WIA 專案應該有影像特定的資訊屬性，例如 [**WIA \_ IPA \_ DEPTH**](-wia-wiaitempropcommonitem.md) 和 **wia \_ IPA \_ \_ \_ 行數**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

**參考**
</dt> <dt>

[**IWiaItem2**](-wia-iwiaitem2.md)
</dt> <dt>

[**IEnumWiaItem2**](-wia-ienumwiaitem2.md)
</dt> <dt>

[**IWiaDevMgr2**](-wia-iwiadevmgr2.md)
</dt> </dl>

 

 



