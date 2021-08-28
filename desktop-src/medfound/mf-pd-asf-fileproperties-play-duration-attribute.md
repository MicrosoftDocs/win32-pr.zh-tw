---
description: 指定播放 Advanced 系統格式所需的時間， (ASF) 檔，以 100-毫微秒單位表示。
ms.assetid: 3d36808b-aa13-4205-ad92-97e951ee827e
title: 'MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fc0e4609f70fa96a0e08339e496b1d7ed6ac7004108ec56ff870ed6f4e7fcb6c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104344"
---
# <a name="mf_pd_asf_fileproperties_play_duration-attribute"></a>MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 播放 \_ 持續時間屬性

指定播放 Advanced 系統格式所需的時間， (ASF) 檔，以 100-毫微秒單位表示。

此值包含預先進行的時間。 若要取得實際的播放持續時間，請取得 [ [**MF \_ PD \_ duration**](mf-pd-duration-attribute.md) ] 屬性的值。 但是，如果預先進行的值大於播放持續時間，則 [ **MF \_ PD \_ 持續時間** ] 的值為零。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="remarks"></a>備註

此屬性適用于 ASF 內容的表示描述項。

[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。

## <a name="examples"></a>範例


```C++
HRESULT GetPlayDuration(
    IMFASFContentInfo *pContentInfo,  // An initialized ContentInfo object. 
    UINT64 *pcbPlayDuration           // Receives the play duration.
    )
{
    IMFPresentationDescriptor* pPD = NULL;

    HRESULT hr = pContentInfo->GeneratePresentationDescriptor(&pPD);
    if (SUCCEEDED(hr))
    {
        hr = pPD->GetUINT64(MF_PD_ASF_FILEPROPERTIES_PLAY_DURATION, pcbPlayDuration);
        pPD->Release();
    }
    return hr;
}

```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Wmcontainer。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[**IMFAttributes：： SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF 標頭物件](asf-file-structure.md)
</dt> <dt>

[簡報描述項](presentation-descriptors.md)
</dt> </dl>

 

 




