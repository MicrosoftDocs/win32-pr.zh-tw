---
description: 影片框架的寬度和高度（以圖元為單位）。
ms.assetid: 9f10a972-406f-47ef-b71c-86ed771c9a9a
title: 'MF_MT_FRAME_SIZE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d3d6278cdbd4c279c498839cb183b3331fe1efc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987811"
---
# <a name="mf_mt_frame_size-attribute"></a>MF \_ MT \_ 框架 \_ 大小屬性

影片框架的寬度和高度（以圖元為單位）。

## <a name="data-type"></a>資料類型

**UINT64**

## <a name="remarks"></a>備註

上方的32位包含寬度，而較低的32位則包含高度。

若要設定此屬性，請使用 [**MFSetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) 函數。 若要取得這個屬性，請使用 [**MFGetAttributeSize**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize) 函數。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="examples"></a>範例


```
// Helper function to set the frame size on a video media type.
inline HRESULT SetFrameSize(IMFMediaType *pType, UINT32 width, UINT32 height)
{
    return MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
}

// Helper function to get the frame size from a video media type.
inline HRESULT GetFrameSize(IMFMediaType *pType, UINT32 *pWidth, UINT32 *pHeight)
{
    return MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, pWidth, pHeight);
}
```



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

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 




