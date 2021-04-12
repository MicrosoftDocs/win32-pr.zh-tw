---
description: 下表列出 DirectShow 篩選準則分類的 Clsid。
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: 篩選準則分類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f0c4ccb9443c405abcbd0b9afbd406d6faf2558a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104385569"
---
# <a name="filter-categories"></a>篩選準則分類

下表列出 DirectShow 篩選準則分類的 Clsid。

-   [DirectShow 篩選準則類別](#directshow-filter-categories)
-   [其他篩選準則類別](#other-filter-categories)
-   [DirectShow 濾波器中繼類別](#directshow-filter-meta-category)
-   [SQL-DMO 類別](#dmo-categories)
-   [相關主題](#related-topics)

## <a name="directshow-filter-categories"></a>DirectShow 篩選準則類別

此處所列的類別是由 [篩選器](filter-mapper.md)對應程式所列舉。 不過，根據預設，篩選器對應程式會忽略具有最大值的類別 \_ \_ 不 \_ 使用或較少。 如需詳細資訊，請參閱 [**IFilterMapper2：： EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters)。 此處所列的所有類別也可以使用 [系統裝置](system-device-enumerator.md)列舉值來列舉。

下列類別宣告于 Uuid. h 中。 包含標頭檔 Dshow .h。



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>易記名稱</th>
<th>CLSID</th>
<th>優點</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>音訊捕獲來源</td>
<td><strong>CLSID_AudioInputDeviceCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>音訊壓縮機</td>
<td><strong>CLSID_AudioCompressorCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>音訊轉譯器</td>
<td><strong>CLSID_AudioRendererCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>裝置控制篩選</td>
<td><strong>CLSID_DeviceControlCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>DirectShow 篩選</td>
<td><strong>CLSID_LegacyAmFilterCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>外部轉譯器</td>
<td><strong>CLSID_TransmitCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>Midi 轉譯器</td>
<td><strong>CLSID_MidiRendererCategory</strong></td>
<td><strong>MERIT_NORMAL</strong></td>
</tr>
<tr class="even">
<td>影片捕獲來源</td>
<td><strong>CLSID_VideoInputDeviceCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>影片壓縮機</td>
<td><strong>CLSID_VideoCompressorCategory</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>WDM 串流解壓縮裝置</td>
<td><strong>CLSID_DVDHWDecodersCategory</strong>
<blockquote>
[!Note]<br />
此類別包含硬體 DVD 解碼器。
</blockquote>
<br/></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>WDM 串流捕獲裝置</td>
<td><strong>AM_KSCATEGORY_CAPTURE</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>WDM 串流處理的縱橫條裝置</td>
<td><strong>AM_KSCATEGORY_CROSSBAR</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>WDM 串流轉譯裝置</td>
<td><strong>AM_KSCATEGORY_RENDER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>WDM 串流的 t/分隔裝置</td>
<td><strong>AM_KSCATEGORY_SPLITTER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>WDM 串流電視音訊裝置</td>
<td><strong>AM_KSCATEGORY_TVAUDIO</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="even">
<td>WDM 串流電視調諧器裝置</td>
<td><strong>AM_KSCATEGORY_TVTUNER</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
<tr class="odd">
<td>WDM 串流 VBI 編解碼器</td>
<td><strong>AM_KSCATEGORY_VBICODEC</strong></td>
<td><strong>MERIT_DO_NOT_USE</strong></td>
</tr>
</tbody>
</table>



 

下列類別宣告于標頭檔 Ks 中。



| 易記名稱                          | CLSID                                   | 優點                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| WDM 串流通訊轉換 | **KSCATEGORY \_ COMMUNICATIONSTRANSFORM** | **\_ \_ 未 \_ 使用的業績** |
| WDM 串流資料轉換          | **KSCATEGORY \_ DATATRANSFORM**           | **\_ \_ 未 \_ 使用的業績** |
| WDM 串流介面轉換     | **KSCATEGORY \_ INTERFACETRANSFORM**      | **\_ \_ 未 \_ 使用的業績** |
| WDM 串流混音器裝置            | **KSCATEGORY \_ 混音器**                   | **\_ \_ 未 \_ 使用的業績** |



 

下列類別宣告于標頭檔 Bdamedia 中。 包含下列標頭檔： ks. h、ksmedia .h 和 bdamedia。



| 易記名稱                       | CLSID                                       | 優點                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| BDA 網路提供者               | **KSCATEGORY \_ BDA \_ 網路 \_ 提供者**      | **一般的業績 \_**       |
| BDA 接收器元件             | **KSCATEGORY \_ BDA \_ 接收器 \_ 元件**    | **\_ \_ 未 \_ 使用的業績** |
| BDA 轉譯篩選               | **KSCATEGORY \_ IP \_ 接收**                    | **\_ \_ 未 \_ 使用的業績** |
| BDA 來源篩選                  | **KSCATEGORY \_ BDA \_ 網路 \_ 調諧器**         | **\_ \_ 未 \_ 使用的業績** |
| BDA 傳輸資訊轉譯器 | **KSCATEGORY \_ BDA \_ 傳輸 \_ 資訊** | **一般的業績 \_**       |



 

> [!Note]  
> 在「DirectShow 篩選」類別下註冊的解碼器 (CLSID \_ LegacyAmFilterCategory) 。

 

## <a name="other-filter-categories"></a>其他篩選準則類別

您可以使用系統裝置列舉值來列舉此處所列的類別，但不會對篩選器對應程式顯示這些類別，而且 [智慧連接](intelligent-connect.md)不會使用這些類別。

下列類別宣告于標頭檔 Qedit 中。



| 易記名稱            | CLID                             | 優點                   |
|--------------------------|----------------------------------|-------------------------|
|  (1 輸入) 的影片效果  | **CLSID \_ VideoEffects1Category** | **\_ \_ 未 \_ 使用的業績** |
|  (2 輸入的影片效果)  | **CLSID \_ VideoEffects2Category** | **\_ \_ 未 \_ 使用的業績** |



 

這些類別包含適用于 [DirectShow 編輯服務](directshow-editing-services.md)的影片效果和轉換：

-   「影片效果 (1 輸入) 」包含影片效果。
-   「影片效果 (2 輸入) 」包含影片轉換。

如需詳細資訊，請參閱 [列舉效果和轉換](enumerating-effects-and-transitions.md)。

下列類別宣告于標頭檔 Uuid. h 中。 包含標頭檔 Dshow .h。



| 易記名稱       | CLID                                | 優點                   |
|---------------------|-------------------------------------|-------------------------|
| EncAPI 編碼器     | **CLSID \_ MediaEncoderCategory**     | **\_ \_ 未 \_ 使用的業績** |
| EncAPI Multiplexers | **CLSID \_ MediaMultiplexerCategory** | **\_ \_ 未 \_ 使用的業績** |



 

## <a name="directshow-filter-meta-category"></a>DirectShow 篩選 Meta-Category



| 易記名稱                 | CLSID                            | 優點          |
|-------------------------------|----------------------------------|----------------|
| ActiveMovie 篩選準則分類 | **CLSID \_ ActiveMovieCategories** | 不適用 |



 

此中繼類別包含篩選分類的清單。 如果篩選準則類別未出現在此清單中，則 [篩選器](filter-mapper.md) 對應程式會忽略類別，這表示篩選準則無法用於 [智慧型連接](intelligent-connect.md)。

若要列舉篩選類別目錄的清單，請使用值 CLSID ActiveMovieCategories 來呼叫 [**ICreateDevEnum：： CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) \_ 。 這個方法所傳回的名字標記支援下列屬性。



| 屬性名稱  | 描述                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| 友好 | 類別名稱 (VT \_ BSTR) 。                                                              |
| 調        | 類別 (VT \_ I4) 。 如果這個屬性不存在，請視為 **「 \_ \_ 未 \_ 使用**」。 |
| CLSID        | 類別 CLSID (VT \_ BSTR) 。                                                             |



 

若要在此清單中加入新的篩選準則類別，請呼叫 [**IFilterMapper2：： CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory)。

## <a name="dmo-categories"></a>SQL-DMO 類別

DirectX 媒體物件 (DMOs) 使用與 DirectShow 篩選器不同的列舉機制。 如需詳細資訊，請參閱 [註冊 sql-dmo](registering-a-dmo.md)。 不過，您可以使用系統裝置列舉值來列舉 SQL-DMO 類別。 此名字會系結至 [Sql-dmo 包裝函式篩選器](dmo-wrapper-filter.md) ，並使用 sql-dmo 自動初始化篩選。

此外，某些 SQL-DMO 類別會對應至 DirectShow 篩選準則類別，以供智慧型 connect 之用：



| SQL-DMO 類別                    | DirectShow 對等              |
|---------------------------------|------------------------------------|
| **DMOCATEGORY \_ 音訊 \_ 編碼器** | **CLSID \_ AudioCompressorCategory** |
| **DMOCATEGORY \_ 音訊 \_ 解碼器** | **CLSID \_ LegacyAmFilterCategory**  |
| **DMOCATEGORY \_ 影片 \_ 編碼器** | **CLSID \_ VideoCompressorCategory** |
| **DMOCATEGORY \_ 影片 \_ 解碼器** | **CLSID \_ LegacyAmFilterCategory**  |



 

請注意，影片效果和音訊效果類別未對應到任何 DirectShow 類別。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[常數和 Guid](constants-and-guids.md)
</dt> <dt>

[列舉裝置和篩選器](enumerating-devices-and-filters.md)
</dt> <dt>

[智慧型連接](intelligent-connect.md)
</dt> <dt>

[登錄機碼的版面配置](layout-of-the-registry-keys.md)
</dt> <dt>

[使用篩選器對應程式](using-the-filter-mapper.md)
</dt> <dt>

[使用系統裝置列舉值](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




