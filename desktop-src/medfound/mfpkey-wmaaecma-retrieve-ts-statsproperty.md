---
description: 指定語音捕獲 DSP 是否將時間戳記統計資料儲存在登錄中。
ms.assetid: c44462be-ccdf-4a49-bb77-6e816def4849
title: 'MFPKEY_WMAAECMA_RETRIEVE_TS_STATS 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c28f9812bb5f1324fcb1153b84f5a6704c7481c8356073fd02b8d95b57a8e497
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953498"
---
# <a name="mfpkey_wmaaecma_retrieve_ts_stats-property"></a>MFPKEY \_ WMAAECMA \_ 取得 \_ TS \_ 統計資料屬性

指定語音捕獲 DSP 是否將時間戳記統計資料儲存在登錄中。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ BOOL

## <a name="default-value"></a>預設值

VARIANT \_ FALSE

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

聲場回顯取消 (AEC) 演算法取決於音訊串流上的精確時間戳記。 事實上，時間戳記通常是完美的，而不同的音訊裝置可能會顯示不同的變異數和漂移率。 啟用 AEC 時，DSP 會收集時間戳記的相關統計資料，並使用此資訊來彌補是否有不准確。

如果這個屬性的值為 VARIANT \_ TRUE，則 DSP 會儲存在登錄中收集的統計資料。 下一次 DSP 使用同一組音訊裝置執行 AEC 時，會從登錄讀取統計資訊，讓 DSP 更有效率地執行。

如果您將這個屬性的值設為 VARIANT \_ TRUE，並且在篩選模式中使用 DSP，您也應該設定 [MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID](mfpkey-wmaaecma-devicepair-guidproperty.md) 屬性。 在來源模式中，這不是必要的。

這個屬性的預設值為 VARIANT \_ FALSE。 只有在啟用 AEC 處理時，DSP 才會使用這個屬性。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> <dt>

[語音捕獲 DSP](voicecapturedmo.md)
</dt> </dl>

 

 
