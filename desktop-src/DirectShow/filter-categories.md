---
description: 下表列出 DirectShow 篩選準則分類的 clsid。
ms.assetid: cab4e2c9-eab9-4836-adfc-870490ca5b6b
title: 篩選準則分類
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb4e8c2b5e5f9e477633774cb24e707aa9d71060
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122476324"
---
# <a name="filter-categories"></a>篩選準則分類

下表列出 DirectShow 篩選準則分類的 clsid。

-   [DirectShow篩選準則分類](#directshow-filter-categories)
-   [其他篩選準則類別](#other-filter-categories)
-   [DirectShow篩選中繼分類](#directshow-filter-meta-category)
-   [DMO類別](#dmo-categories)
-   [相關主題](#related-topics)

## <a name="directshow-filter-categories"></a>DirectShow篩選準則分類

此處所列的類別是由 [篩選器](filter-mapper.md)對應程式所列舉。 不過，根據預設，篩選器對應程式會忽略具有最大值的類別 \_ \_ 不 \_ 使用或較少。 如需詳細資訊，請參閱 [**IFilterMapper2：： EnumMatchingFilters**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-enummatchingfilters)。 此處所列的所有類別也可以使用 [系統裝置](system-device-enumerator.md)列舉值來列舉。

下列類別宣告于 Uuid. h 中。 包含標頭檔 Dshow .h。




| 易記名稱 | CLSID | 優點 | 
|---------------|-------|-------|
| 音訊捕獲來源 | <strong>CLSID_AudioInputDeviceCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| 音訊壓縮機 | <strong>CLSID_AudioCompressorCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| 音訊轉譯器 | <strong>CLSID_AudioRendererCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| 裝置控制篩選 | <strong>CLSID_DeviceControlCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| DirectShow過濾 器 | <strong>CLSID_LegacyAmFilterCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| 外部轉譯器 | <strong>CLSID_TransmitCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| Midi 轉譯器 | <strong>CLSID_MidiRendererCategory</strong> | <strong>MERIT_NORMAL</strong> | 
| 影片捕獲來源 | <strong>CLSID_VideoInputDeviceCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| 影片壓縮機 | <strong>CLSID_VideoCompressorCategory</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM 串流解壓縮裝置 | <strong>CLSID_DVDHWDecodersCategory</strong><blockquote>[!Note]<br />此類別包含硬體 DVD 解碼器。</blockquote><br /> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM 串流捕獲裝置 | <strong>AM_KSCATEGORY_CAPTURE</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM 串流處理的縱橫條裝置 | <strong>AM_KSCATEGORY_CROSSBAR</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM 串流轉譯裝置 | <strong>AM_KSCATEGORY_RENDER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM 串流的 t/分隔裝置 | <strong>AM_KSCATEGORY_SPLITTER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM 串流電視音訊裝置 | <strong>AM_KSCATEGORY_TVAUDIO</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM 串流電視調諧器裝置 | <strong>AM_KSCATEGORY_TVTUNER</strong> | <strong>MERIT_DO_NOT_USE</strong> | 
| WDM 串流 VBI 編解碼器 | <strong>AM_KSCATEGORY_VBICODEC</strong> | <strong>MERIT_DO_NOT_USE</strong> | 




 

下列類別宣告于標頭檔 Ks 中。



| 易記名稱                          | CLSID                                   | 優點                   |
|----------------------------------------|-----------------------------------------|-------------------------|
| WDM 串流通訊轉換 | **KSCATEGORY \_ COMMUNICATIONSTRANSFORM** | **\_ \_ 未 \_ 使用的業績** |
| WDM 串流資料轉換          | **KSCATEGORY \_ DATATRANSFORM**           | **\_ \_ 未 \_ 使用的業績** |
| WDM 串流介面轉換     | **KSCATEGORY \_ INTERFACETRANSFORM**      | **\_ \_ 未 \_ 使用的業績** |
| WDM 串流 Mixer 裝置            | **KSCATEGORY \_ 混音器**                   | **\_ \_ 未 \_ 使用的業績** |



 

下列類別宣告于標頭檔 Bdamedia 中。 包含下列標頭檔： ks. h、ksmedia .h 和 bdamedia。



| 易記名稱                       | CLSID                                       | 優點                   |
|-------------------------------------|---------------------------------------------|-------------------------|
| BDA 網路提供者               | **KSCATEGORY \_ BDA \_ 網路 \_ 提供者**      | **一般的業績 \_**       |
| BDA 接收器元件             | **KSCATEGORY \_ BDA \_ 接收器 \_ 元件**    | **\_ \_ 未 \_ 使用的業績** |
| BDA 轉譯篩選               | **KSCATEGORY \_ IP \_ 接收**                    | **\_ \_ 未 \_ 使用的業績** |
| BDA 來源篩選                  | **KSCATEGORY \_ BDA \_ 網路 \_ 調諧器**         | **\_ \_ 未 \_ 使用的業績** |
| BDA 傳輸資訊轉譯器 | **KSCATEGORY \_ BDA \_ 傳輸 \_ 資訊** | **一般的業績 \_**       |



 

> [!Note]  
> 在 [DirectShow 篩選準則] 類別下註冊的解碼器 (CLSID \_ LegacyAmFilterCategory) 。

 

## <a name="other-filter-categories"></a>其他篩選準則類別

您可以使用系統裝置列舉值來列舉此處所列的類別，但不會對篩選器對應程式顯示這些類別，而且[智慧連線](intelligent-connect.md)不會使用這些類別。

下列類別宣告于標頭檔 Qedit 中。



| 易記名稱            | CLID                             | 優點                   |
|--------------------------|----------------------------------|-------------------------|
|  (1 輸入) 的影片效果  | **CLSID \_ VideoEffects1Category** | **\_ \_ 未 \_ 使用的業績** |
|  (2 輸入的影片效果)  | **CLSID \_ VideoEffects2Category** | **\_ \_ 未 \_ 使用的業績** |



 

這些類別包含[DirectShow 編輯服務](directshow-editing-services.md)的影片效果和轉換：

-   「影片效果 (1 輸入) 」包含影片效果。
-   「影片效果 (2 輸入) 」包含影片轉換。

如需詳細資訊，請參閱 [列舉效果和轉換](enumerating-effects-and-transitions.md)。

下列類別宣告于標頭檔 Uuid. h 中。 包含標頭檔 Dshow .h。



| 易記名稱       | CLID                                | 優點                   |
|---------------------|-------------------------------------|-------------------------|
| EncAPI 編碼器     | **CLSID \_ MediaEncoderCategory**     | **\_ \_ 未 \_ 使用的業績** |
| EncAPI Multiplexers | **CLSID \_ MediaMultiplexerCategory** | **\_ \_ 未 \_ 使用的業績** |



 

## <a name="directshow-filter-meta-category"></a>DirectShow篩選 Meta-Category



| 易記名稱                 | CLSID                            | 優點          |
|-------------------------------|----------------------------------|----------------|
| ActiveMovie 篩選準則分類 | **CLSID \_ ActiveMovieCategories** | 不適用 |



 

此中繼類別包含篩選分類的清單。 如果篩選準則類別未出現在這份清單中，則[篩選器](filter-mapper.md)對應程式會忽略類別，這表示篩選準則不適用於[智慧型連線](intelligent-connect.md)。

若要列舉篩選類別目錄的清單，請使用值 CLSID ActiveMovieCategories 來呼叫 [**ICreateDevEnum：： CreateClassEnumerator**](/windows/desktop/api/Strmif/nf-strmif-icreatedevenum-createclassenumerator) \_ 。 這個方法所傳回的名字標記支援下列屬性。



| 屬性名稱  | 描述                                                                            |
|----------------|----------------------------------------------------------------------------------------|
| 友好 | 類別名稱 (VT \_ BSTR) 。                                                              |
| 調        | 類別 (VT \_ I4) 。 如果這個屬性不存在，請視為 **「 \_ \_ 未 \_ 使用**」。 |
| CLSID        | 類別 CLSID (VT \_ BSTR) 。                                                             |



 

若要在此清單中加入新的篩選準則類別，請呼叫 [**IFilterMapper2：： CreateCategory**](/windows/desktop/api/Strmif/nf-strmif-ifiltermapper2-createcategory)。

## <a name="dmo-categories"></a>DMO類別

DirectX 媒體物件 (DMOs) 使用 DirectShow 篩選器的不同列舉機制。 如需詳細資訊，請參閱[註冊 DMO](registering-a-dmo.md)。 不過，您可以使用系統裝置列舉值來列舉 DMO 分類。 這些標記系結至[DMO 包裝](dmo-wrapper-filter.md)函式篩選，並使用 DMO 自動初始化篩選。

此外，某些 DMO 類別會對應到 DirectShow 篩選準則類別，以供智慧型 connect 之用：



| DMO類別                    | DirectShow等效              |
|---------------------------------|------------------------------------|
| **DMOCATEGORY \_ 音訊 \_ 編碼器** | **CLSID \_ AudioCompressorCategory** |
| **DMOCATEGORY \_ 音訊 \_ 解碼器** | **CLSID \_ LegacyAmFilterCategory**  |
| **DMOCATEGORY \_ 影片 \_ 編碼器** | **CLSID \_ VideoCompressorCategory** |
| **DMOCATEGORY \_ 影片 \_ 解碼器** | **CLSID \_ LegacyAmFilterCategory**  |



 

請注意，影片效果和音訊效果類別未對應到任何 DirectShow 分類。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[常數和 Guid](constants-and-guids.md)
</dt> <dt>

[列舉裝置和篩選器](enumerating-devices-and-filters.md)
</dt> <dt>

[智慧型連線](intelligent-connect.md)
</dt> <dt>

[登錄機碼的版面配置](layout-of-the-registry-keys.md)
</dt> <dt>

[使用篩選器對應程式](using-the-filter-mapper.md)
</dt> <dt>

[使用系統裝置列舉值](using-the-system-device-enumerator.md)
</dt> </dl>

 

 




