---
description: 影片交錯
ms.assetid: 2911ae57-1703-4a9d-bd33-94af1e0f8804
title: 影片交錯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 340c727f8faaaf20ff82eff58d0c651601071dea
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474334"
---
# <a name="video-interlacing"></a>影片交錯

本主題說明媒體來源和解碼器應該如何處理交錯的影片內容。

若要正確地解碼和轉譯交錯的影片，需要下列資訊：

-   漸進式或交錯式。 影片串流可以包含漸進式的框架、交錯的框架，或兩者的混合。

-   現場支配。 欄位支配會描述先出現的欄位、上方欄位或下方欄位。

-   重複第一個欄位。 當框架是漸進式的，但資料流程是交錯式時，會在3:2 的下拉中使用此旗標。 在此內容中，第一個欄位可以是欄位的上限或下限。

-   交錯的欄位或單一欄位。 範例可以保留單一欄位或兩個交錯的欄位。 如果範例包含單一欄位，範例高度會是框架高度的一半，因為此範例只包含框架的一半掃描行。 除非來源內容的特性另外決定，否則建議使用交錯欄位。

任何這些特性都可以從一個範例變更為下一個範例。 不過，在串流處理開始之前，影片元件需要知道整體內容的相關事項。 例如，如果影片是交錯的，則增強的影片轉譯器 (EVR) 需要為去交錯保留視訊記憶體。 另一方面，如果影片完全是漸進式框架，EVR 可以優化轉譯管線。 將去交錯步驟新增至管線會增加轉譯延遲。

交錯的相關資訊會儲存在兩個位置：

-   資料流程中交錯的一般資訊會放在媒體類型中。 如需媒體類型的詳細資訊，請參閱 [媒體類型](media-types.md)。

-   可隨著每個範例變更的資訊會放在範例上做為屬性。 如需範例的詳細資訊，請參閱 [媒體範例](media-samples.md)。

## <a name="interlace-information-in-the-media-type"></a>媒體類型中的隔行資訊

媒體類型上的 [**MF \_ MT \_ 交錯 \_ 模式**](mf-mt-interlace-mode-attribute.md) 屬性描述整個資料流程如何交錯。 這個屬性的值是 [**MFVideoInterlaceMode**](/windows/desktop/api/mfobjects/ne-mfobjects-mfvideointerlacemode) 列舉的成員。 影片媒體類型應該一律有此屬性。

-   如果資料流程只包含漸進式框架（沒有交錯框架），請使用 MFVideoInterlace \_ 累進。
-   如果資料流程只包含交錯的框架，而且每個範例都包含兩個交錯的欄位，請使用 MFVideoInterlace \_ FieldInterleavedUpperFirst 或 MFVideoInterlace \_ FieldInterleavedLowerFirst。
-   如果資料流程只包含交錯的框架，而且每個範例都包含單一欄位，請使用 MFVideoInterlace \_ FieldSingleUpper 或 MFVideoInterlace \_ FieldSingleLower。 如果欄位在上方和下方都是替代欄位，則這兩個值的使用方式並不重要。 如果格式只包含上方欄位，或只包含較低的欄位，請設定對應至內容的值。
-   如果資料流程包含混合式和漸進式框架，或如果欄位支配參數，請將媒體類型設定為 MFVideoInterlace \_ MixedInterlaceOrProgressive。 使用範例屬性來描述每個畫面格。

下表摘要說明此屬性。



| MF \_ MT \_ 交錯 \_ 模式                       | 交錯？ | 範例                                  | 第一個欄位    |
|-----------------------------------------------|-------------|------------------------------------------|----------------|
| MFVideoInterlace \_ 漸進式                 | 否          | 漸進式框架                        | 不適用 |
| MFVideoInterlace \_ FieldInterleavedUpperFirst  | 是         | 交錯欄位                       | 上一個    |
| MFVideoInterlace \_ FieldInterleavedLowerFirst  | 是         | 交錯欄位                       | 先較低    |
| MFVideoInterlace \_ FieldSingleUpper            | 是         | 單一欄位                             | 上一個    |
| MFVideoInterlace \_ FieldSingleLower            | 是         | 單一欄位                             | 先較低    |
| MFVideoInterlace \_ MixedInterlaceOrProgressive | 可能不同    | 交錯的欄位或漸進式框架 | 可能不同       |



 

交錯的欄位和單一欄位不能混用。 從一個切換到另一個需要變更媒體類型。

## <a name="interlace-flags-on-samples"></a>範例上的交錯旗標

可從某個範例變更為下一個樣本的資訊會使用範例屬性來表示。 您可以使用 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 介面來取得或設定這些屬性。

本節所列的所有交錯屬性都有布林值。 實際上，每個屬性都可以有三個值： **TRUE**、 **FALSE** 或未設定。 如果未設定屬性，則會從媒體類型取得值。 如果已設定屬性，此值會覆寫媒體類型。 某些旗標和媒體類型的組合無效。




| 屬性 | 描述 | 
|-----------|-------------|
| <a href="mfsampleextension-interlaced-attribute.md">MFSampleExtension_Interlaced</a> | 若 <strong>為 TRUE</strong>，則框架為交錯式。 如果 <strong>為 FALSE</strong>，則表示框架為漸進式。<br /> 如果媒體類型為 MFVideoInterlace_MixedInterlaceOrProgressive，請在每個範例上設定此屬性。<br /> | 
| <a href="mfsampleextension-bottomfieldfirst-attribute.md">MFSampleExtension_BottomFieldFirst</a> | 此旗標的意義取決於範例是否包含交錯欄位或單一欄位。<br /><ul><li>交錯欄位：如果 <strong>為 TRUE</strong>，則較低的欄位為第一個。 如果 <strong>為 FALSE</strong>，則表示上方欄位為第一個。<br /></li><li>單一欄位：如果 <strong>為 TRUE</strong>，則範例包含較低的欄位。 如果 <strong>為 FALSE</strong>，則表示範例包含上方欄位。<br /></li></ul>如果媒體類型為 MFVideoInterlace_FieldSingleUpper、MFVideoInterlace_FieldSingleLower 或 MFVideoInterlace_MixedInterlaceOrProgressive，請在每個交錯範例上設定此屬性。<br /> | 
| <a href="mfsampleextension-repeatfirstfield-attribute.md">MFSampleExtension_RepeatFirstField</a> | 若 <strong>為 TRUE</strong>，則會重複第一個欄位。 如果 <strong>為 FALSE</strong> 或未設定，則不會重複第一個欄位。 | 
| <a href="mfsampleextension-singlefield-attribute.md">MFSampleExtension_SingleField</a> | 若 <strong>為 TRUE</strong>，則範例包含單一欄位。 如果 <strong>為 FALSE</strong>，則範例包含交錯的欄位。 | 




 

下表根據媒體類型顯示必要、選擇性或禁止的旗標。



| 媒體類型         | 交錯旗標                      | BottomFieldFirst 旗標                    | RepeatFirstField 旗標 | SingleField 旗標                     |
|--------------------|--------------------------------------|------------------------------------------|-----------------------|--------------------------------------|
| 漸進式        | 參數如果設定，則必須為 **FALSE**。 | 不要設定。                              | 不要設定。           | 不要設定。                          |
| 交錯欄位 | 參數如果設定，則必須為 **TRUE**。  | 參數如果設定，必須符合媒體類型。 | 不要設定。           | 參數如果設定，則必須為 **FALSE**。 |
| 單一欄位      | 參數如果設定，則必須為 **TRUE**。  | 必要。                                | 不要設定。           | 設定為 **TRUE**。                     |
| Mixed              | 必要。                            | 必要。                                | 必要。             | 參數如果設定，則必須為 **FALSE**。 |



 

在屬性為選擇性的情況下，媒體類型已定義資訊。 將屬性設定為相符（但不是必要）是有效的。

例如，如果媒體類型是 MFVideoInterlace \_ 累進，則表示資料流程中的所有框架都是漸進式的。 因此，您可以將 [ **MFSampleExtension \_ 交錯** ] 屬性設定為 [ **FALSE**]，或將屬性保留為 [未設定]。

## <a name="recommendations"></a>建議

本節包含各種內容類型的建議。

1. 影片是所有漸進式的畫面格。

-   將 [媒體類型] 設定為 [ \_ 漸進式 MFVideoInterlace]。

-   請勿設定 **MFSampleExtension \_ 交錯** 屬性，或在每個畫面格上將其設定為 **FALSE** 。

-   請勿設定 **MFSampleExtension \_ BottomFieldFirst**、 **MFSampleExtension \_ RepeatFirstField** 或 **MFSampleExtension \_ SingleField** 屬性。

2. 影片是具有相同現場支配的所有交錯欄位。 範例包含交錯的欄位。

-   將 [媒體類型] 設定為 [MFVideoInterlace \_ FieldInterleavedUpperFirst] 或 [MFVideoInterlace \_ FieldInterleavedLowerFirst]。

-   請勿設定 **MFSampleExtension \_ 交錯** 屬性，或在每個畫面格上將其設定為 **TRUE** 。

-   請勿設定 **MFSampleExtension \_ BottomFieldFirst** 屬性，或設定每個畫面格的值以符合媒體類型。

-   請勿設定 **MFSampleExtension \_ RepeatFirstField** 屬性，或在每個畫面格上將其設定為 **FALSE** 。

-   請勿設定 **MFSampleExtension \_ SingleField** 屬性，或在每個畫面格上將其設定為 **FALSE** 。

3. 影片包含混合式和漸進式的框架，其中包含重複的欄位和不同的現場支配 (例如 DVD 影片) 。

-   將 [媒體類型] 設定為 [MFVideoInterlace \_ MixedInterlaceOrProgressive]。

-   在每個畫面上，設定 **MFSampleExtension \_ 交錯** 式、 **MFSampleExtension \_ BottomFieldFirst** 和 **MFSampleExtension \_ RepeatFirstField** 屬性。

-   請勿設定 **MFSampleExtension \_ SingleField** 屬性，或在每個畫面格上將其設定為 **FALSE** 。

4. 影片是交錯的，範例包含單一欄位。

-   將 [媒體類型] 設定為 [MFVideoInterlace \_ FieldSingleUpper] 或 [MFVideoInterlace \_ FieldSingleLower]。

-   在每個畫面上，設定 **MFSampleExtension \_ BottomFieldFirst** 屬性。

-   請勿設定 **MFSampleExtension \_ 交錯** 屬性，或在每個畫面格上將其設定為 **TRUE** 。

-   請勿設定 **MFSampleExtension \_ RepeatFirstField** 屬性，或在每個畫面格上將其設定為 **FALSE** 。

-   請勿設定 **MFSampleExtension \_ SingleField** 屬性，或在每個畫面格上將其設定為 **TRUE** 。

大部分的影片內容都屬於上述其中一種類別。

## <a name="mpeg-2-mappings"></a>MPEG-2 對應

針對 MPEG-2 內容，請使用下列對應將 MPEG-2 旗標轉換成媒體基礎範例屬性。

**圖片 \_ 結構**



| 值         | Sample 屬性                                                                                                        |
|---------------|-------------------------------------------------------------------------------------------------------------------------|
| 框架         | **MFSampleExtension \_SingleField**  =  **FALSE**                                                                          |
| 頂端 \_ 欄位    | **MFSampleExtension \_SingleField**  =  **TRUE**<br/> **MFSampleExtension \_BottomFieldFirst**  =  **FALSE**<br/> |
| 底部 \_ 欄位 | **MFSampleExtension \_SingleField**  =  **TRUE**<br/> **MFSampleExtension \_BottomFieldFirst**  =  **TRUE**<br/>  |



 

**漸進式 \_ 框架**



| 值 | Sample 屬性                              |
|-------|-----------------------------------------------|
| 0     | **MFSampleExtension \_交錯** 式  =  **TRUE**  |
| 1     | **MFSampleExtension \_交錯** 式  =  **FALSE** |



 

**top \_ 欄位 \_ first**



| 值 | Sample 屬性                                    |
|-------|-----------------------------------------------------|
| 0     | **MFSampleExtension \_BottomFieldFirst**  =  **TRUE**  |
| 1     | **MFSampleExtension \_BottomFieldFirst**  =  **FALSE** |



 

**重複 \_ 第一個 \_ 欄位**



| 值 | Sample 屬性                                    |
|-------|-----------------------------------------------------|
| 0     | **MFSampleExtension \_RepeatFirstField**  =  **FALSE** |
| 1     | **MFSampleExtension \_RepeatFirstField**  =  **TRUE**  |



 

## <a name="single-field-samples"></a>Single-Field 範例

如果媒體類型為 [MFVideoInterlace \_ FieldSingleUpper] 或 [MFVideoInterlace \_ FieldSingleLower]，表示每個範例都包含單一欄位。 不過，媒體類型會描述整個框架。 因此，每個緩衝區只包含媒體類型中所指定的欄位行數一半。 例如，如果媒體類型將影片描述為720×480，則每個欄位都包含240掃描行，因此每個緩衝區只會包含240的圖元列。 如果您撰寫的元件會接受具有單一欄位範例的媒體類型，則當您存取緩衝區中的資料時，必須將這項事實納入考慮。

相同規則適用于幾何光圈 ([MF \_ mt \_ 幾何 \_ 光圈](mf-mt-geometric-aperture-attribute.md) 屬性) 和最小顯示光圈 ([MF \_ mt \_ 最小 \_ 顯示 \_ 光圈](mf-mt-minimum-display-aperture-attribute.md) 屬性) 。 這些區域是以整個框架（而非個別欄位）來指定。

## <a name="directshow-mappings"></a>DirectShow映射

在 DirectShow 中，每個範例交錯的資訊都包含在 **AM \_ sample2.xml \_ 屬性** 結構的 **dwTypeSpecificFlags** 成員中。 下表顯示媒體基礎的對等屬性。



| DirectShow 範例旗標              | 媒體基礎範例屬性                                                                                                                                                  |
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| AM \_ 影片 \_ 旗標 \_ 交錯 \_ 框 | **MFSampleExtension \_SingleField**  =  **FALSE**。                                                                                                                                    |
| AM \_ 影片 \_ 旗標 \_ FIELD1             | **MFSampleExtension \_交錯** 式  =  **TRUE**。<br/> **MFSampleExtension \_SingleField**  =  **TRUE**。<br/> **MFSampleExtension \_BottomFieldFirst**  =  **FALSE**。<br/> |
| AM \_ 影片 \_ 旗標 \_ FIELD2             | **MFSampleExtension \_交錯** 式  =  **TRUE**。<br/> **MFSampleExtension \_SingleField**  =  **TRUE**。<br/> **MFSampleExtension \_BottomFieldFirst**  =  **TRUE**。<br/>  |
| AM \_ 影片 \_ 旗標 \_ 編織              | **MFSampleExtension \_交錯** 式  =  **FALSE**。  (此旗標指出驅動程式不應將這兩個欄位進行逐行掃描。 )                                                         |
| AM \_ 影片 \_ 旗標 \_ FIELD1FIRST        | **MFSampleExtension \_BottomFieldFirst**  =  **FALSE**。 如果內容是交錯式的，而 AM \_ 影片 \_ 旗標 \_ FIELD1FIRST 旗標不存在，請將此屬性設定為 **TRUE**。        |
| AM \_ 影片 \_ 旗標 \_ 重複 \_ 欄位      | **MFSampleExtension \_RepeatFirstField**  =  **TRUE**。 如果 \_ 不存在「AM 影片 \_ 旗標 \_ 重複欄位」旗標 \_ ，請將此屬性設定為 **FALSE**。                                    |



 

如果 DirectShow 範例不包含範例旗標，請使用 **VIDEOINFOHEADER2** 結構的 **dwInterlaceFlags** 值：



| DirectShow 交錯旗標    | 媒體基礎範例屬性                    |
|------------------------------|------------------------------------------------------|
| AMINTERLACE \_ IsInterlaced    | **MFSampleExtension \_交錯** 式  =  **TRUE**。        |
| AMINTERLACE \_ 1FieldPerSample | **MFSampleExtension \_SingleField**  =  **TRUE**。       |
| AMINTERLACE \_ Field1First     | **MFSampleExtension \_BottomFieldFirst**  =  **FALSE**。 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[影片媒體類型](video-media-types.md)
</dt> <dt>

[媒體類型](media-types.md)
</dt> </dl>

 

 




