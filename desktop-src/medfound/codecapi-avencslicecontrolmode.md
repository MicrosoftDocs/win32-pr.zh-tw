---
description: 指定配量控制模式。 有效值為 0、1 和 2。
ms.assetid: 5269DB79-639C-4F67-B885-BF1274CDB635
title: 'CODECAPI_AVEncSliceControlMode 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0aef928a3938b2f0756d2e84b6836da194823dab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936563"
---
# <a name="codecapi_avencslicecontrolmode-property"></a>CODECAPI \_ AVEncSliceControlMode 屬性

指定配量控制模式。 有效值為 0、1 和 2。

## <a name="data-type"></a>資料類型

**ULONG** (VT \_ UI4) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncSliceControlMode**

## <a name="property-value"></a>屬性值

配量控制項模式值：



| 值                                                                        | 意義                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 將此值設定為0，表示 [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) 屬性將會以每個配量的巨大區塊單位來指定配量大小。<br/>     |
| <dl> <dt>1</dt> </dl> | 將此值設定為1，表示 [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) 屬性將會以每個配量的位數單位來指定配量大小。<br/>            |
| <dl> <dt>2</dt> </dl> | 將此值設定為2表示 [CODECAPI \_ AVEncSliceControlSize](codecapi-avencslicecontrolsize.md) 屬性將會以每個配量的巨大區塊資料列單位來指定配量大小。<br/> |



 

編碼器會傳回它所支援的值。

## <a name="remarks"></a>備註

**H.264/AVC 編碼器：**

建議編碼器支援 [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)、 [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)和 [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)。

如果 [](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)未針對 CODECAPI AVEncSliceControlMode 呼叫 SetValue \_ ，則 CODECAPI AVEncSliceControlMode 的 [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) \_ 可能會傳回 **VFW \_ E \_ CODECAPI \_ 沒有目前的 \_ \_ 值**。 [**GetDefaultValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getdefaultvalue) 可能會傳回 **VFW \_ E CODECAPI NO CODECAPI AVEncSliceControlMode 的 \_ \_ \_ 預設值** \_ 。

建議的預設值為 2 (每個配量) 的 MB 資料列大小。

這是靜態 API，這表示應用程式在編碼器執行時，會贏得變更。

## <a name="examples"></a>範例


```C++
if (pCodecAPI->IsSupported(&CODECAPI_AVEncSliceControlMode) == S_OK) {                
     VARIANT var;
     var.vt = VT_UI4;
     var.ulVal =ulSliceMode;
     pCodecAPI->SetValue(&CODECAPI_AVEncSliceControlMode, &var);
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

