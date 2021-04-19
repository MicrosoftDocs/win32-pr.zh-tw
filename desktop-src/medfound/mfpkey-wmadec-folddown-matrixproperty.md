---
description: 指定作者提供的折迭係數，可針對比編碼的資料流程所包含的通道更少的通道來解碼多頻道音訊。
ms.assetid: f6737c05-4b39-4209-9985-9402b28cf316
title: 'MFPKEY_WMADEC_FOLDDOWN_MATRIX 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e92cb2495863d319c7f755d7d72f475ccf1eda75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998082"
---
# <a name="mfpkey_wmadec_folddown_matrix-property"></a>MFPKEY \_ WMADEC \_ FOLDDOWN \_ MATRIX 屬性

指定作者提供的折迭係數，可針對比編碼的資料流程所包含的通道更少的通道來解碼多頻道音訊。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMACFoldDownXToYChannels

g \_ wszWMACFoldXToYChannelsZ

## <a name="data-type"></a>資料類型

**VT \_ 陣列 \| vt \_ I4**

## <a name="remarks"></a>備註

音訊解碼器可作為 DirectX 媒體物件 (的) 或媒體基礎轉換 (MFT) 。 如需何時將某個解碼器作為一或一個 MFT 的詳細資訊，請參閱 [編解碼器物件](codecobjects.md)底下的個別編解碼器參考頁面。

當您使用解碼器做為，則此解碼器可以執行通道折迭，而且您可以藉由呼叫 [**IMediaObject：： GetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-getoutputtype)來列舉折迭輸出媒體類型。

當您使用解碼器做為 MFT 時，此解碼器預設不會執行任何折迭，且不會提供折迭輸出媒體類型。 只有當您使用 **MFPKEY \_ WMADEC \_ FOLDDOWN \_ MATRIX** 屬性來設定自訂折迭係數時，才會執行做為 MFT 的解碼器。

如果音訊解碼器 MFT 上未設定 **MFPKEY \_ WMADEC \_ FOLDDOWN \_ MATRIX** 屬性，而您想要執行折迭，您可以使用 (作為) 音訊 RESAMPLER 數位訊號處理器的 MFT。

這個屬性的值是一個字串，其中包含以逗號分隔的整數值清單中的折迭係數。 此清單必須針對編碼內容中的每個通道包含一些整數，等於已解碼內容中的通道數目。

如果係數為零，要在字串中使用的值必須是 "-2147483648"; 否則，會使用方程式： 20 \* 65536 \* log10 (x) 來計算值。

係數會依通道遮罩順序列出，如同 mmreg .h 標頭檔中包含的通道遮罩常數所定義。 因此，6對2通道中的前兩個值會向下折迭，代表左方輸出通道的部分，以及由6個通道資料流程中中央左邊通道所組成的右側輸出通道。

只有當作者提供的折迭值與編碼的內容一起保存時，才應該設定這個屬性。 否則，請讓該解碼器進行自己的計算。

Windows Media 音訊10專業版編解碼器目前僅支援折迭至兩個通道。

如果 [ [MFPKEY \_ WMADEC \_ SPKRCFG](mfpkey-wmadec-spkrcfgproperty.md) ] 屬性設定為 [DSSPEAKER 範圍]，則編解碼器會忽略作者提供的折迭係數，並向下折迭為可由接收者的矩陣編解碼器處理的雙聲道信號。 **\_** 這可讓環繞設備傳遞四個通道。 只有當來源為5.1 時，才支援此模式。 編解碼器只能將8個通道折迭為2個通道。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
