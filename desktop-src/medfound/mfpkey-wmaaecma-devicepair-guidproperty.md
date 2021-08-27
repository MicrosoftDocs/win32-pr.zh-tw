---
description: 識別應用程式目前與語音捕獲 DSP 搭配使用之音訊裝置的組合。
ms.assetid: f87bef33-9a48-4568-b554-7eec34f0bd55
title: 'MFPKEY_WMAAECMA_DEVICEPAIR_GUID 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 174bbae3c83ef28ece7d05e36b0a05813078a9a9fba73ac7fae7dba25b67fb00
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973327"
---
# <a name="mfpkey_wmaaecma_devicepair_guid-property"></a>MFPKEY \_ WMAAECMA \_ DEVICEPAIR \_ GUID 屬性

識別應用程式目前與語音捕獲 DSP 搭配使用之音訊裝置的組合。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ CLSID

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

如果您在篩選模式中使用 DSP，且 [MFPKEY \_ WMAAECMA 抓取 \_ \_ TS \_ 統計](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) 資料屬性的值為 VARIANT TRUE，請設定此屬性 \_ 。

當 [**MFPKEY \_ WMAAECMA 抓取 \_ \_ TS \_ STATS**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) 屬性為 VARIANT 時 \_ ，DSP 會收集來自音訊裝置之時間戳記的統計資料，並將此資訊儲存在登錄中。 每個音訊捕獲裝置和音訊轉譯裝置的組合都會變更這些統計資料。 因此，應用程式必須指派 GUID 以識別使用中裝置的特定組合。 應用程式應該追蹤此 GUID，讓它可以在每次使用同一組音訊裝置時指派相同的 GUID。

如果您在來源模式中使用 DSP，則不需要設定此屬性。 DSP 會根據 [MFPKEY \_ WMAAECMA \_ DEVICE [ \_ 索引](mfpkey-wmaaecma-device-indexesproperty.md) ] 屬性的值自動產生 GUID。

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

 

 
