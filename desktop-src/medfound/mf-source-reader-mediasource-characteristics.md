---
description: 從來源讀取器取得媒體來源的特性。
ms.assetid: 4cd48b69-6f7b-4b13-86f3-b38969025f70
title: 'MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS 屬性 (Mfreadwrite) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5ec5461bc289517490ae11bdd507895cd1ad434c53b1665ac5c6394907f15a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118739963"
---
# <a name="mf_source_reader_mediasource_characteristics-attribute"></a>MF \_ 來源 \_ 讀取器 \_ MEDIASOURCE \_ 特性屬性

從 [來源讀取器](source-reader.md)取得媒體來源的特性。

## <a name="data-type"></a>資料類型

**UINT32**

值是 [**MFMEDIASOURCE \_ 特性**](/windows/desktop/api/mfidl/ne-mfidl-mfmediasource_characteristics)列舉中的位 **or** 旗標。

## <a name="remarks"></a>備註

若要取得這個屬性，請在來源讀取器上呼叫 [**IMFSourceReader：： GetPresentationAttribute**](/windows/desktop/api/mfreadwrite/nf-mfreadwrite-imfsourcereader-getpresentationattribute) 方法。 將 *dwStreamIndex* 參數設定為 [ **mf \_ 來源 \_ 讀取器 \_ MEDIASOURCE** ]，並將 *guidAttribute* 參數設定為 [mf \_ 來源 \_ 讀取器 \_ MEDIASOURCE] \_ 特性。

這個屬性的 **PROPVARIANT** 類型是 **VT \_ UI4**。

## <a name="examples"></a>範例


```C++
HRESULT GetSourceFlags(IMFSourceReader *pReader, ULONG *pulFlags)
{
    ULONG flags = 0;

    PROPVARIANT var;
    PropVariantInit(&var);

    HRESULT hr = pReader->GetPresentationAttribute(
        MF_SOURCE_READER_MEDIASOURCE, 
        MF_SOURCE_READER_MEDIASOURCE_CHARACTERISTICS, 
        &var);

    if (SUCCEEDED(hr))
    {
        hr = PropVariantToUInt32(var, &flags);
    }
    if (SUCCEEDED(hr))
    {
        *pulFlags = flags;
    }

    PropVariantClear(&var);
    return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | WindowsServer 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Mfreadwrite。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[來源讀取程式](source-reader.md)
</dt> </dl>

 

 




