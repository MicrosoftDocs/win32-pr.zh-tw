---
description: 指定語音捕獲 DSP 是否使用來源模式或篩選模式。
ms.assetid: d1d3beba-678c-48fd-ad12-45e0418e1236
title: 'MFPKEY_WMAAECMA_DMO_SOURCE_MODE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ec9dd01be5a020047410362b2fdfc27fd8d703a393e3ae2f557b1dd3a42bf80
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555298"
---
# <a name="mfpkey_wmaaecma_dmo_source_mode-property"></a>MFPKEY \_ WMAAECMA \_ DMO \_ SOURCE \_ MODE 屬性

指定語音捕獲 DSP 是否使用來源模式或篩選模式。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

僅可使用 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)。

## <a name="data-type"></a>資料類型

VT \_ BOOL

## <a name="default-value"></a>預設值

VARIANT \_ TRUE

## <a name="applies-to"></a>套用至

-   [語音捕獲 DSP](voicecapturedmo.md)

## <a name="remarks"></a>備註

在來源模式中，應用程式不需要將輸入資料傳送給 DSP，因為 DSP 會自動從音訊裝置提取資料。 在篩選模式中，應用程式必須將輸入資料傳送給 DSP。

這個屬性可以具有下列值。



| 值          | 描述  |
|----------------|--------------|
| VARIANT \_ FALSE | 篩選模式。 |
| VARIANT \_ TRUE  | 來源模式。 |



 

> [!Note]  
> 當 DMO 處於來源模式時，您應該只呼叫 [**IMediaObject：： SetOutputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setoutputtype)來設定輸出資料流程格式，而不要呼叫 [**IMediaObject：： SetInputType**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-setinputtype)來設定輸入資料流程格式。 否則 DMO 初始化將會失敗。

 

如果這個屬性的值為 VARIANT \_ TRUE，則表示 DSP 的輸入為零。 如果值為 VARIANT \_ FALSE，則根據 [MFPKEY \_ WMAAECMA \_ 系統 \_ 模式](mfpkey-wmaaecma-system-modeproperty.md) 屬性的值而定，DSP 會有一或兩個輸入，如下表所示。



| 值                     | 輸入數目 |
|---------------------------|------------------|
| OPTIBEAM \_ 陣列 \_ 和 \_ AEC | 2                |
| \_ \_ 僅限 OPTIBEAM 陣列     | 1                |
| 單一 \_ 通道 \_ AEC      | 2                |
| 單一 \_ 通道 \_ NSAGC    | 1                |



 

> [!Note]  
> 只有具有單一輸入的模式，才可使用來自 DirectShow 9.0 API 的包裝函式篩選器 DMO。

 

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

 

 
