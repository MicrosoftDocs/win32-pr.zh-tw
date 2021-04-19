---
description: 指定 Advanced 系統格式 (ASF) 檔案是否為廣播或可搜尋。 此值會對應至在 ASF 規格中定義之檔案屬性物件的旗標欄位。
ms.assetid: 427f0dca-f945-4c89-a87a-a7c86291b1c5
title: 'MF_PD_ASF_FILEPROPERTIES_FLAGS 屬性 (Wmcontainer) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee294642188a0f2e22143feeca6791fea591cbb9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977075"
---
# <a name="mf_pd_asf_fileproperties_flags-attribute"></a>MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 旗標屬性

指定 Advanced 系統格式 (ASF) 檔案是否為廣播或可搜尋。 此值會對應至在 ASF 規格中定義之檔案屬性物件的旗標欄位。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

此屬性適用于 ASF 內容的表示描述項。 屬性的值是下列旗標的位 OR：



| 旗標 | 描述                                                                                                                                                                                                                                                                                       |
|------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x01 | 廣播旗標。 檔案正在建立的進程中。                                                                                                                                                                                                                                      |
| 0x02 | 搜尋旗標。 檔案是可搜尋的。<br/> 如果有音訊資料流程，且最大的資料封包大小等於最小的資料封包大小，檔案就是可搜尋的。 如果檔案中有音訊串流和影片串流，且具有相符的簡單索引物件，它也可以是可搜尋的。<br/> |



 

[**IMFASFContentInfo：： GeneratePresentationDescriptor**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfcontentinfo-generatepresentationdescriptor)方法會從 ASF 中繼資料產生這個屬性。

如果已設定廣播旗標，表示描述項中的下列屬性無效：

-   [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 檔案 \_ 識別碼**](mf-pd-asf-fileproperties-file-id-attribute.md)
-   [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 建立 \_ 時間**](mf-pd-asf-fileproperties-creation-time-attribute.md)
-   [**MF \_ PD \_ ASF \_ FILEPROPERTIES 封 \_ 包**](mf-pd-asf-fileproperties-packets-attribute.md)
-   [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 播放 \_ 持續時間**](mf-pd-asf-fileproperties-play-duration-attribute.md)
-   [**MF \_ PD \_ ASF \_ FILEPROPERTIES \_ 傳送 \_ 持續時間**](mf-pd-asf-fileproperties-send-duration-attribute.md)

此外， [**mf \_ pd \_ asf \_ FILEPROPERTIES \_ MAX \_ packet \_ size**](mf-pd-asf-fileproperties-max-packet-size-attribute.md) 屬性和 [**MF \_ pd \_ asf \_ FILEPROPERTIES \_ MIN \_ packet \_ size**](mf-pd-asf-fileproperties-min-packet-size-attribute.md) 屬性值會設定為實際的封包大小。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Wmcontainer。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[**IMFPresentationDescriptor**](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)
</dt> <dt>

[展示描述項屬性](presentation-descriptor-attributes.md)
</dt> <dt>

[ASF 標頭物件](asf-file-structure.md)
</dt> <dt>

[簡報描述項](presentation-descriptors.md)
</dt> </dl>

 

 




