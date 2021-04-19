---
description: 包含提供給 IMFMediaStream：： RequestSample 方法之權杖的指標。
ms.assetid: 9403bb15-e912-4aa3-9af1-fef4a4f9b242
title: 'MFSampleExtension_Token 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d17331ad098f80c2676e9d057e1688a776cee305
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106978844"
---
# <a name="mfsampleextension_token-attribute"></a>MFSampleExtension \_ Token 屬性

包含提供給 [**IMFMediaStream：： RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) 方法之權杖的指標。

## <a name="data-type"></a>資料類型

**IUnknown \** _

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetUnknown* *](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)。

## <a name="applies-to"></a>適用於

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>備註

這個屬性會套用至媒體範例。 屬性的值是傳遞給 [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample)方法之 *PToken* 參數的 **IUnknown** 指標。 呼叫端會使用這個屬性來追蹤要求的狀態。

如果您要撰寫自訂媒體來源，則在媒體串流傳遞範例以回應 [**RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) 方法時，請在範例上設定此屬性，除非 *pToken* 的值為 **Null**。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista \[ 桌面應用程式 \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | Windows Server 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[範例屬性](sample-attributes.md)
</dt> <dt>

[媒體範例](media-samples.md)
</dt> </dl>

 

 




