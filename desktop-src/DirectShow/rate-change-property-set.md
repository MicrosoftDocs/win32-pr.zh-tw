---
description: 速率變更屬性集可讓 MPEG-2 來源/剖析器篩選器變更播放速率。 MPEG-2 解碼器應該支援此屬性集。 DVD 導覽器和資料流程緩衝區引擎都會使用此屬性集來控制播放速率。
ms.assetid: f88c64ce-af76-49fe-8ebd-029928506243
title: '速率變更屬性集 (Dvdmedia .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5299b744869a4c9a12b50a9e738104999aab5dcd19a800fc0ac3ddb3717e8617
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119747408"
---
# <a name="rate-change-property-set"></a>速率變更屬性集

速率變更屬性集可讓 MPEG-2 來源/剖析器篩選器變更播放速率。 MPEG-2 解碼器應該支援此屬性集。 DVD 導覽器和資料流程緩衝區引擎都會使用此屬性集來控制播放速率。



| 標籤 | 值 |
|-------------------|-------------------------------|
| 屬性集 GUID | AM \_ KSPROPSETID \_ TSRateChange |



 



| 屬性識別碼                                                                   | 描述                                                                            |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [**AM \_ RATE \_ CorrectTS**](am-rate-correctts-property.md)                     | 通知解碼器導覽器正在設定正確的時間戳記。             |
| AM \_ RATE \_ ExactRateChange                                                     | 已過時。                                                                              |
| [**AM \_ RATE \_ MaxFullDataRate**](am-rate-maxfulldatarate-property.md)         | 查詢解碼器的最大資料速率。                               |
| [**AM \_ RATE \_ QueryFullFrameRate**](am-rate-queryfullframerate-property.md)   | 查詢解碼器的最大全畫面播放速率的解碼器。                         |
| [**AM \_ RATE \_ QueryLastRateSegPTS**](am-rate-querylastratesegpts-property.md) | 查詢解碼器，以取得最近設定之速率區段的開始時間。 |
| [**AM \_ RATE \_ SimpleRateChange**](am-rate-simpleratechange-property.md)       | 將速率變更傳送至解碼器。                                                    |
| AM \_ RATE \_ Step                                                                | 已過時。 請參閱 [框架逐步執行屬性集](frame-stepping-property-set.md)。          |
| [**AM \_ RATE \_ UseRateVersion**](am-rate-userateversion-property.md)           | 指定要使用的速率變更機制版本。                           |



 

## <a name="remarks"></a>備註

在這個屬性集的內容中，rate 會測量相對於參考時鐘的時間戳記前進的速率。 對播放速度的反向進行評分。 例如，如果播放速度為2x，則時間戳記必須以標準速率增加到1/2。 這會轉譯成更快的播放速度，因為樣本的轉譯速度早于一般。

範例會傳送至具有時間戳記的時間戳記等於以1x 速率表示的呈現時間的解碼器。 此解碼器必須將輸出範例上的時間戳記調整為目前速率的正確呈現時間。 例如，如果速率是 1/2 (表示播放速度為 2x) ，則此解碼器必須將時間戳記調整為1/2。 一般來說，只有 I 個框架具有時間戳記。 此解碼器必須插入 B 和 P 框架的時間戳記。 請注意，在進行反向播放時，時間戳記會持續增加，時間戳記永遠不會再向下。

已定義兩個版本的速率變更屬性集，版本1.0 和1.1 版。 預設行為是由1.0 版提供。 建議使用解碼器廠商支援1.1 版，因為它提供更流暢的播放體驗。 DVD 導覽器目前使用1.0 版。 資料流程緩衝區引擎使用1.1 版。

### <a name="rate-change-version-10"></a>速率變更版本1。0

1.0 版的速率變更屬性集會定義 MPEG-2 的預設行為。

來源篩選藉由設定 [**AM \_ rate \_ SimpleRateChange**](am-rate-simpleratechange-property.md) 屬性來發出速率變更的信號。 這個屬性的資料是新的速率，以及當速率生效時輸入範例的開始時間。 此解碼器會維護暫止速率變更的佇列，並依開始時間排序。

在 DVD 導覽器變更為非1x 的速度之前，它會提供所有暫止的範例、暫時將速率設定為1.0，以及排清圖形。 然後，它會設定新的費率。 所有速率變更都會排定在目前 VOBU 的結尾， (video 物件單位) 。 請注意，清除圖形會將呈現時間重設為零。

DVD 導覽器以 *平滑模式* 或 *掃描模式* 操作。 在平滑模式中，它會將每個畫面格傳送給解碼器，包括 B 框架和 P 框架。 當播放速度大於零但小於解碼器的 maxmimum 資料速率時，DVD 導覽器會使用平滑模式。 如果播放速度小於零 (反轉播放) ，或超過解碼器的最大資料速率，則 DVD 瀏覽器會使用掃描模式，在此模式中，它只會將 I 框架傳送至解碼器。 在非常高的速度下，它可能會略過一些框架;例如，它可能會傳送其他每個畫面格。

根據預設，DVD 導覽器會靜音非1.0 的音訊串流。 您可以藉由呼叫 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) 與 DVD AudioDuringFFwdRew 旗標來變更此項 \_ 。

### <a name="rate-change-version-11"></a>速率變更版本1。1

速率變更屬性集的1.1 版遵循與1.0 版相同的基本原則，但有下列差異：

-   來源篩選器會藉由設定 [**AM \_ 速率 \_ UseRateVersion**](am-rate-userateversion-property.md) 屬性，來指示要使用版本1.1 的解碼器。 否則，此解碼器應使用1.0 版的行為。
-   來源篩選不會在速率變更之間清除圖形。 因此，時間戳記會在速率變更界限之間進行單純的增加，而不是重設為零。
-   來源篩選器不會針對特定參考時間將速率變更排入佇列，而是會指定將速率變更套用至解碼器的 *最轉寄範例*，並在解碼器傳出佇列的開頭定義為範例。 若要這樣做，來源篩選器會使用 [**AM \_ RATE \_ SimpleRateChange**](am-rate-simpleratechange-property.md) 屬性，但會將開始時間設定為-1。
-   來源篩選器可以查詢解碼器，以取得最近排入佇列之速率變更的開始時間。 基於此目的，它會使用 [**AM \_ RATE \_ QueryLastRateSegPTS**](am-rate-querylastratesegpts-property.md) 屬性。
-   來源篩選不會捨棄範例。 如果速率超過解碼器的最大資料速率，則應該視需要卸載框架。
-   無論音訊解碼器的最大資料速率為何，來源篩選都不會將音訊串流靜音。 如果播放速度超過解碼器的最大速率，音訊解碼器可以卸載範例。 不過，它仍應維持排程費率變更的佇列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Dvdmedia。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[屬性集](property-sets.md)
</dt> </dl>

 

 




