---
description: 指出範例是否為隨機存取點。
ms.assetid: 03d4bfd8-1148-4551-8e71-05cfba2e15fa
title: 'MFSampleExtension_CleanPoint 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7181c08b19382a6b9d9da0475ec0a7a0522bd132dc10a2da1da4531d631d02d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118241495"
---
# <a name="mfsampleextension_cleanpoint-attribute"></a>MFSampleExtension \_ CleanPoint 屬性

指出範例是否為隨機存取點。

## <a name="data-type"></a>資料類型

**BOOL** 儲存為 **UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample)

## <a name="remarks"></a>備註

這個屬性會套用至範例。 如果屬性為 **TRUE**，則此範例為隨機存取點，而解碼可以從此範例開始。 否則，此範例不是隨機存取點。

如果未設定此屬性，則預設值為 **FALSE**。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="examples"></a>範例


```C++
inline BOOL IsRandomAccessPoint(IMFSample *pSample)
{
    // Check for the "clean point" attribute. Default to FALSE.
    return MFGetAttributeUINT32(pSample, MFSampleExtension_CleanPoint, FALSE);
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | WindowsVista \[ desktop apps \| UWP 應用程式\]<br/>                              |
| 最低支援的伺服器<br/> | WindowsServer 2008 \[ desktop app \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[範例屬性](sample-attributes.md)
</dt> <dt>

[媒體範例](media-samples.md)
</dt> </dl>

 

 




