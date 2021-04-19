---
title: WMDM_FORMATCODE 列舉
description: WMDM \_ FORMATCODE 列舉型別會定義格式代碼清單，以說明在裝置上傳送的內容類型。
ms.assetid: 203d9bdf-cbbd-4d06-8292-26c8a472e2aa
keywords:
- WMDM_FORMATCODE 列舉 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_FORMATCODE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04db31578f36455fdf77bb4044ad45e5ca9f9a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000660"
---
# <a name="wmdm_formatcode-enumeration"></a>WMDM \_ FORMATCODE 列舉

**WMDM \_ FORMATCODE** 列舉型別會定義格式代碼清單，以說明在裝置上傳送的內容類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_FORMATCODE { 
  WMDM_FORMATCODE_NOTUSED,
  WMDM_FORMATCODE_ALLIMAGES,
  WMDM_FORMATCODE_UNDEFINED,
  WMDM_FORMATCODE_ASSOCIATION,
  WMDM_FORMATCODE_SCRIPT,
  WMDM_FORMATCODE_EXECUTABLE,
  WMDM_FORMATCODE_TEXT,
  WMDM_FORMATCODE_HTML,
  WMDM_FORMATCODE_DPOF,
  WMDM_FORMATCODE_AIFF,
  WMDM_FORMATCODE_WAVE,
  WMDM_FORMATCODE_MP3,
  WMDM_FORMATCODE_AVI,
  WMDM_FORMATCODE_MPEG,
  WMDM_FORMATCODE_ASF,
  WMDM_FORMATCODE_RESERVED_FIRST,
  WMDM_FORMATCODE_RESERVED_LAST,
  WMDM_FORMATCODE_IMAGE_UNDEFINED,
  WMDM_FORMATCODE_IMAGE_EXIF,
  WMDM_FORMATCODE_IMAGE_TIFFEP,
  WMDM_FORMATCODE_IMAGE_FLASHPIX,
  WMDM_FORMATCODE_IMAGE_BMP,
  WMDM_FORMATCODE_IMAGE_CIFF,
  WMDM_FORMATCODE_IMAGE_GIF,
  WMDM_FORMATCODE_IMAGE_JFIF,
  WMDM_FORMATCODE_IMAGE_PCD,
  WMDM_FORMATCODE_IMAGE_PICT,
  WMDM_FORMATCODE_IMAGE_PNG,
  WMDM_FORMATCODE_IMAGE_TIFF,
  WMDM_FORMATCODE_IMAGE_TIFFIT,
  WMDM_FORMATCODE_IMAGE_JP2,
  WMDM_FORMATCODE_IMAGE_JPX,
  WMDM_FORMATCODE_IMAGE_RESERVED_FIRST,
  WMDM_FORMATCODE_IMAGE_RESERVED_LAST,
  WMDM_FORMATCODE_UNDEFINEDFIRMWARE,
          WMDM_FORMATCODE_WBMP
,
                  WMDM_FORMATCODE_JPEGXR
,
  WMDM_FORMATCODE_WINDOWSIMAGEFORMAT,
  WMDM_FORMATCODE_UNDEFINEDAUDIO,
  WMDM_FORMATCODE_WMA,
  WMDM_FORMATCODE_OGG,
  WMDM_FORMATCODE_AAC,
  WMDM_FORMATCODE_AUDIBLE,
  WMDM_FORMATCODE_FLAC,
          WMDM_FORMATCODE_QCELP
,
          WMDM_FORMATCODE_AMR
,
  WMDM_FORMATCODE_UNDEFINEDVIDEO,
  WMDM_FORMATCODE_WMV,
  WMDM_FORMATCODE_MP4,
  WMDM_FORMATCODE_MP2,
          WMDM_FORMATCODE_3G2
,
                  WMDM_FORMATCODE_AVCHD
,
                  WMDM_FORMATCODE_ATSCTS
,
                          WMDM_FORMATCODE_DVBTS
,
  WMDM_FORMATCODE_UNDEFINEDCOLLECTION,
  WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM,
  WMDM_FORMATCODE_ABSTRACTIMAGEALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOALBUM,
  WMDM_FORMATCODE_ABSTRACTVIDEOALBUM,
  WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST,
  WMDM_FORMATCODE_ABSTRACTCONTACTGROUP,
  WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER,
  WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION,
  WMDM_FORMATCODE_WPLPLAYLIST,
  WMDM_FORMATCODE_M3UPLAYLIST,
  WMDM_FORMATCODE_MPLPLAYLIST,
  WMDM_FORMATCODE_ASXPLAYLIST,
  WMDM_FORMATCODE_PLSPLAYLIST,
  WMDM_FORMATCODE_UNDEFINEDDOCUMENT,
  WMDM_FORMATCODE_ABSTRACTDOCUMENT,
  WMDM_FORMATCODE_XMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT,
  WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT,
  WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET,
  WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT,
  WMDM_FORMATCODE_UNDEFINEDMESSAGE,
  WMDM_FORMATCODE_ABSTRACTMESSAGE,
  WMDM_FORMATCODE_UNDEFINEDCONTACT,
  WMDM_FORMATCODE_ABSTRACTCONTACT,
  WMDM_FORMATCODE_VCARD2,
  WMDM_FORMATCODE_VCARD3,
  WMDM_FORMATCODE_UNDEFINEDCALENDARITEM,
  WMDM_FORMATCODE_ABSTRACTCALENDARITEM,
  WMDM_FORMATCODE_VCALENDAR1,
  WMDM_FORMATCODE_VCALENDAR2,
  WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE,
  WMDM_FORMATCODE_MEDIA_CAST,
  WMDM_FORMATCODE_SECTION,
                                  WMDM_FORMATCODE_3G2A

} WMDM_FORMATCODE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WMDM_FORMATCODE_NOTUSED"></span><span id="wmdm_formatcode_notused"></span>**WMDM \_ FORMATCODE \_ NOTUSED**
</dt> <dd>

未使用任何格式代碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_ALLIMAGES"></span><span id="wmdm_formatcode_allimages"></span>**WMDM \_ FORMATCODE \_ ALLIMAGES**
</dt> <dd>

格式化可用於查詢所有影像的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINED"></span><span id="wmdm_formatcode_undefined"></span>**\_ \_ 未定義的 WMDM FORMATCODE**
</dt> <dd>

格式化用來查詢所有未定義物件的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_ASSOCIATION"></span><span id="wmdm_formatcode_association"></span>**WMDM \_ FORMATCODE \_ 關聯**
</dt> <dd>

格式化程式碼，用來定義兩個物件之間的連結。

</dd> <dt>

<span id="WMDM_FORMATCODE_SCRIPT"></span><span id="wmdm_formatcode_script"></span>**WMDM \_ FORMATCODE \_ 腳本**
</dt> <dd>

格式化腳本檔案的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_EXECUTABLE"></span><span id="wmdm_formatcode_executable"></span>**WMDM \_ FORMATCODE \_ 可執行檔**
</dt> <dd>

格式化可執行檔的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_TEXT"></span><span id="wmdm_formatcode_text"></span>**WMDM \_ FORMATCODE \_ 文字**
</dt> <dd>

格式化文字檔的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_HTML"></span><span id="wmdm_formatcode_html"></span>**WMDM \_ FORMATCODE \_ HTML**
</dt> <dd>

格式化 HTML 檔案的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_DPOF"></span><span id="wmdm_formatcode_dpof"></span>**WMDM \_ FORMATCODE \_ DPOF**
</dt> <dd>

用來表示數位列印順序格式的程式碼格式。

</dd> <dt>

<span id="WMDM_FORMATCODE_AIFF"></span><span id="wmdm_formatcode_aiff"></span>**WMDM \_ FORMATCODE \_ .AIFF**
</dt> <dd>

用來代表音訊交換檔案格式的程式碼格式。

</dd> <dt>

<span id="WMDM_FORMATCODE_WAVE"></span><span id="wmdm_formatcode_wave"></span>**WMDM \_ FORMATCODE \_ WAVE**
</dt> <dd>

格式化用於 WAV 檔案的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_MP3"></span><span id="wmdm_formatcode_mp3"></span>**WMDM \_ FORMATCODE \_ MP3**
</dt> <dd>

格式化用於 MP3 檔案的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_AVI"></span><span id="wmdm_formatcode_avi"></span>**WMDM \_ FORMATCODE \_ AVI**
</dt> <dd>

格式化 AVI 檔案所用的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_MPEG"></span><span id="wmdm_formatcode_mpeg"></span>**WMDM \_ FORMATCODE \_ MPEG**
</dt> <dd>

格式化用於 MPEG 檔案的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_ASF"></span><span id="wmdm_formatcode_asf"></span>**WMDM \_ FORMATCODE \_ ASF**
</dt> <dd>

用來代表 Advanced 系統格式的程式碼 (ASF) 檔。

</dd> <dt>

<span id="WMDM_FORMATCODE_RESERVED_FIRST"></span><span id="wmdm_formatcode_reserved_first"></span>**\_ \_ 先保留 WMDM \_ FORMATCODE**
</dt> <dd>

將第一個範圍中的第一個程式碼格式化為圖片傳輸通訊協定的保留範圍 (PTP) 。

</dd> <dt>

<span id="WMDM_FORMATCODE_RESERVED_LAST"></span><span id="wmdm_formatcode_reserved_last"></span>**\_ \_ 上次保留的 WMDM FORMATCODE \_**
</dt> <dd>

將最後一個保留給 PTP 的範圍中的程式碼格式化。

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_UNDEFINED"></span><span id="wmdm_formatcode_image_undefined"></span>**\_未定義的 WMDM FORMATCODE \_ 映射 \_**
</dt> <dd>

格式化程式碼，用來代表未定義類型的和影像。

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_EXIF"></span><span id="wmdm_formatcode_image_exif"></span>**WMDM \_ FORMATCODE \_ 影像 \_ EXIF**
</dt> <dd>

針對 EXIF 檔案格式化程式碼。 也用於 WMDM \_ FORMATCODE \_ image \_ .Jp2 或 WMDM \_ FORMATCODE \_ IMAGE \_ JPX 未涵蓋的 JPEG 影像。

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFFEP"></span><span id="wmdm_formatcode_image_tiffep"></span>**WMDM \_ FORMATCODE \_ 影像 \_ TIFFEP**
</dt> <dd>

將用於電子攝影的標記影像檔案格式類型影像的程式碼格式化 (TIFF/EP) 

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_FLASHPIX"></span><span id="wmdm_formatcode_image_flashpix"></span>**WMDM \_ FORMATCODE \_ 影像 \_ FLASHPIX**
</dt> <dd>

為 FPX 類型的檔案格式化程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_BMP"></span><span id="wmdm_formatcode_image_bmp"></span>**WMDM \_ FORMATCODE \_ 影像 \_ BMP**
</dt> <dd>

為 BMP 類型的檔案格式化程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_CIFF"></span><span id="wmdm_formatcode_image_ciff"></span>**WMDM \_ FORMATCODE \_ 影像 \_ CIFF**
</dt> <dd>

使用相機影像檔案格式來格式化影像的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_GIF"></span><span id="wmdm_formatcode_image_gif"></span>**WMDM \_ FORMATCODE \_ 影像 \_ GIF**
</dt> <dd>

格式化 GIF 檔案的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JFIF"></span><span id="wmdm_formatcode_image_jfif"></span>**WMDM \_ FORMATCODE \_ 影像 \_ JFIF**
</dt> <dd>

為 JFIF 類型的檔案格式化程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PCD"></span><span id="wmdm_formatcode_image_pcd"></span>**WMDM \_ FORMATCODE \_ 影像 \_ PCD**
</dt> <dd>

為相片 cd 類型的影像格式化程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PICT"></span><span id="wmdm_formatcode_image_pict"></span>**WMDM \_ FORMATCODE \_ 影像 \_ PICT**
</dt> <dd>

格式為 PICT 類型影像的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_PNG"></span><span id="wmdm_formatcode_image_png"></span>**WMDM \_ FORMATCODE \_ 影像 \_ PNG**
</dt> <dd>

格式化 PNG 類型影像的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFF"></span><span id="wmdm_formatcode_image_tiff"></span>**WMDM \_ FORMATCODE \_ 影像 \_ TIFF**
</dt> <dd>

格式化 TIFF 類型檔案的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_TIFFIT"></span><span id="wmdm_formatcode_image_tiffit"></span>**WMDM \_ FORMATCODE \_ 影像 \_ TIFFIT**
</dt> <dd>

使用影像技術來格式化具有標記之影像檔案格式的影像程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JP2"></span><span id="wmdm_formatcode_image_jp2"></span>**WMDM \_ FORMATCODE \_ 影像 \_ .jp2**
</dt> <dd>

格式化 jpeg200 影像的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_JPX"></span><span id="wmdm_formatcode_image_jpx"></span>**WMDM \_ FORMATCODE \_ 影像 \_ JPX**
</dt> <dd>

使用延伸的靜止影像註冊來格式化以 JPEG200 為基礎之影像的程式碼。 副檔名通常是 jpf 或. jpx。

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_RESERVED_FIRST"></span><span id="wmdm_formatcode_image_reserved_first"></span>**\_ \_ \_ 先保留 WMDM FORMATCODE \_ 映射**
</dt> <dd>

將第一個範圍中的第一個程式碼格式化為在 PTP 中為影像參考保留的範圍。

</dd> <dt>

<span id="WMDM_FORMATCODE_IMAGE_RESERVED_LAST"></span><span id="wmdm_formatcode_image_reserved_last"></span>**上次保留的 WMDM \_ FORMATCODE \_ 映射 \_ \_**
</dt> <dd>

針對在 PTP 中為影像參考保留的範圍中的最後一個格式的程式碼進行格式化。

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDFIRMWARE"></span><span id="wmdm_formatcode_undefinedfirmware"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDFIRMWARE**
</dt> <dd>

未定義固件時格式化程式碼。

</dd> <dt>

<span id="________WMDM_FORMATCODE_WBMP_"></span><span id="________wmdm_formatcode_wbmp_"></span>**WMDM \_FORMATCODE \_ .WBMP** 
</dt> <dd>

 ( 的無線應用程式通訊協定點陣圖格式化程式碼。 .wbmp) 影像。

</dd> <dt>

<span id="________________WMDM_FORMATCODE_JPEGXR_"></span><span id="________________wmdm_formatcode_jpegxr_"></span>**WMDM \_FORMATCODE \_ JPEGXR** 
</dt> <dd>

格式化 HD 相片影像的程式碼

</dd> <dt>

<span id="WMDM_FORMATCODE_WINDOWSIMAGEFORMAT"></span><span id="wmdm_formatcode_windowsimageformat"></span>**WMDM \_ FORMATCODE \_ WINDOWSIMAGEFORMAT**
</dt> <dd>

格式化 Windows 映像格式的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDAUDIO"></span><span id="wmdm_formatcode_undefinedaudio"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDAUDIO**
</dt> <dd>

格式化未定義類型之音訊檔案的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_WMA"></span><span id="wmdm_formatcode_wma"></span>**WMDM \_ FORMATCODE \_ WMA**
</dt> <dd>

Windows Media 音訊 (WMA) 檔的格式程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_OGG"></span><span id="wmdm_formatcode_ogg"></span>**WMDM \_ FORMATCODE \_ OGG**
</dt> <dd>

在 Ogg 容器中為 Vorbis 編碼的音訊檔案格式化程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_AAC"></span><span id="wmdm_formatcode_aac"></span>**WMDM \_ FORMATCODE \_ AAC**
</dt> <dd>

 (AAC) 檔格式化高階音訊編碼的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_AUDIBLE"></span><span id="wmdm_formatcode_audible"></span>**WMDM \_ FORMATCODE \_ 聲音**
</dt> <dd>

格式化音效檔的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_FLAC"></span><span id="wmdm_formatcode_flac"></span>**WMDM \_ FORMATCODE \_ FLAC**
</dt> <dd>

將無失真音訊編解碼器的格式程式碼格式化 (FLAC) 檔。

</dd> <dt>

<span id="________WMDM_FORMATCODE_QCELP_"></span><span id="________wmdm_formatcode_qcelp_"></span>**WMDM \_FORMATCODE \_ QCELP** 
</dt> <dd>

QCELP) 編解碼器檔案的 Qualcomm 程式碼驚喜線性預測的格式程式碼 (。

</dd> <dt>

<span id="________WMDM_FORMATCODE_AMR_"></span><span id="________wmdm_formatcode_amr_"></span>**WMDM \_FORMATCODE \_ AMR** 
</dt> <dd>

 (AMR) 編解碼器檔案的自動調整多速率音訊格式的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDVIDEO"></span><span id="wmdm_formatcode_undefinedvideo"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDVIDEO**
</dt> <dd>

針對具有未定義類型的影片檔案格式化程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_WMV"></span><span id="wmdm_formatcode_wmv"></span>**WMDM \_ FORMATCODE \_ WMV**
</dt> <dd>

Windows Media 視訊 (WMV) 檔格式化程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_MP4"></span><span id="wmdm_formatcode_mp4"></span>**WMDM \_ FORMATCODE \_**
</dt> <dd>

將檔案的格式設定為程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_MP2"></span><span id="wmdm_formatcode_mp2"></span>**WMDM \_ FORMATCODE \_ .mp2**
</dt> <dd>

.MP2 檔案的格式程式碼。

</dd> <dt>

<span id="________WMDM_FORMATCODE_3G2_"></span><span id="________wmdm_formatcode_3g2_"></span>**WMDM \_FORMATCODE \_ .3g2** 
</dt> <dd>

.3G2 的格式程式碼 (3GPP2) 多媒體容器格式。 此類型的檔案可能包含音訊、影片或文字。

</dd> <dt>

<span id="________________WMDM_FORMATCODE_AVCHD_"></span><span id="________________wmdm_formatcode_avchd_"></span>**WMDM \_FORMATCODE \_ AVCHD** 
</dt> <dd>

AVCHD (Advanced Video 編碼高定義) 影片檔案的格式化程式碼。

</dd> <dt>

<span id="________________WMDM_FORMATCODE_ATSCTS_"></span><span id="________________wmdm_formatcode_atscts_"></span>**WMDM \_FORMATCODE \_ ATSCTS** 
</dt> <dd>

Advanced 電視 Systems 委員會的格式程式碼 (ATSCTS) 格式標準。

</dd> <dt>

<span id="________________________WMDM_FORMATCODE_DVBTS_"></span><span id="________________________wmdm_formatcode_dvbts_"></span>**WMDM \_FORMATCODE \_ DVBTS** 
</dt> <dd>

在符合 DVB-T 標準的 MPEG-2 傳輸串流中，將 MPEG-2 影片的程式碼和 MPEG-2 圖層 II 或 AC-3 的格式設定為音訊。

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCOLLECTION"></span><span id="wmdm_formatcode_undefinedcollection"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCOLLECTION**
</dt> <dd>

針對未定義類型的集合格式化程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMULTIMEDIAALBUM"></span><span id="wmdm_formatcode_abstractmultimediaalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMULTIMEDIAALBUM**
</dt> <dd>

格式化多媒體專輯的程式碼，其中物件包含多媒體專輯的屬性，以及選擇性的資料。 任何包含的資料都是與 MTP 規格相關的未定義格式。

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTIMAGEALBUM"></span><span id="wmdm_formatcode_abstractimagealbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTIMAGEALBUM**
</dt> <dd>

格式化影像專輯的程式碼，其中物件包含影像專輯的屬性，以及選擇性的資料。 任何包含的資料都是與 MTP 規格相關的未定義格式。

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTAUDIOALBUM"></span><span id="wmdm_formatcode_abstractaudioalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTAUDIOALBUM**
</dt> <dd>

格式化音訊專輯的程式碼，其中物件包含音訊專輯的屬性，以及選擇性的資料。 任何包含的資料都是與 MTP 規格相關的未定義格式。

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTVIDEOALBUM"></span><span id="wmdm_formatcode_abstractvideoalbum"></span>**WMDM \_ FORMATCODE \_ ABSTRACTVIDEOALBUM**
</dt> <dd>

影片專輯的格式程式碼，其中物件包含影片專輯的屬性，以及選擇性的資料。 任何包含的資料都是與 MTP 規格相關的未定義格式。

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTAUDIOVIDEOPLAYLIST"></span><span id="wmdm_formatcode_abstractaudiovideoplaylist"></span>**WMDM \_ FORMATCODE \_ ABSTRACTAUDIOVIDEOPLAYLIST**
</dt> <dd>

格式化音訊/影片播放清單的程式碼，其中物件包含音訊/視頻播放清單的屬性，以及選擇性的資料。 任何包含的資料都是與 MTP 規格相關的未定義格式。

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCONTACTGROUP"></span><span id="wmdm_formatcode_abstractcontactgroup"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCONTACTGROUP**
</dt> <dd>

為連絡人群組格式化程式碼，其中物件包含連絡人群組的屬性，以及選擇性的資料。 任何包含的資料都是與 MTP 規格相關的未定義格式。

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMESSAGEFOLDER"></span><span id="wmdm_formatcode_abstractmessagefolder"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMESSAGEFOLDER**
</dt> <dd>

格式化訊息資料夾的程式碼，其中物件包含訊息資料夾的屬性，以及選擇性的資料。 任何包含的資料都是與 MTP 規格相關的未定義格式。

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCHAPTEREDPRODUCTION"></span><span id="wmdm_formatcode_abstractchapteredproduction"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCHAPTEREDPRODUCTION**
</dt> <dd>

以章節化生產格式的程式碼，其中的物件包含章節化生產和（選擇性）資料的屬性。 任何包含的資料都是與 MTP 規格相關的未定義格式。

</dd> <dt>

<span id="WMDM_FORMATCODE_WPLPLAYLIST"></span><span id="wmdm_formatcode_wplplaylist"></span>**WMDM \_ FORMATCODE \_ WPLPLAYLIST**
</dt> <dd>

格式化以 Windows Media 播放清單格式化的播放清單程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_M3UPLAYLIST"></span><span id="wmdm_formatcode_m3uplaylist"></span>**WMDM \_ FORMATCODE \_ M3UPLAYLIST**
</dt> <dd>

格式化具有 M3U 格式之播放清單的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_MPLPLAYLIST"></span><span id="wmdm_formatcode_mplplaylist"></span>**WMDM \_ FORMATCODE \_ MPLPLAYLIST**
</dt> <dd>

格式化具有 MPL 格式之播放清單的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_ASXPLAYLIST"></span><span id="wmdm_formatcode_asxplaylist"></span>**WMDM \_ FORMATCODE \_ ASXPLAYLIST**
</dt> <dd>

使用 ASX 格式化的播放清單來格式化程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_PLSPLAYLIST"></span><span id="wmdm_formatcode_plsplaylist"></span>**WMDM \_ FORMATCODE \_ PLSPLAYLIST**
</dt> <dd>

格式化具有另外格式之播放清單的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDDOCUMENT"></span><span id="wmdm_formatcode_undefineddocument"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDDOCUMENT**
</dt> <dd>

格式化未定義類型之檔的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTDOCUMENT"></span><span id="wmdm_formatcode_abstractdocument"></span>**WMDM \_ FORMATCODE \_ ABSTRACTDOCUMENT**
</dt> <dd>

格式化檔的程式碼，其中物件包含檔的屬性和資料（選擇性）。 任何包含的資料都是與 MTP 規格相關的未定義格式。

</dd> <dt>

<span id="WMDM_FORMATCODE_XMLDOCUMENT"></span><span id="wmdm_formatcode_xmldocument"></span>**WMDM \_ FORMATCODE \_**
</dt> <dd>

格式化 XML 檔的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTWORDDOCUMENT"></span><span id="wmdm_formatcode_microsoftworddocument"></span>**WMDM \_ FORMATCODE \_ MICROSOFTWORDDOCUMENT**
</dt> <dd>

格式化 Microsoft Word 檔的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_MHTCOMPILEDHTMLDOCUMENT"></span><span id="wmdm_formatcode_mhtcompiledhtmldocument"></span>**WMDM \_ FORMATCODE \_ MHTCOMPILEDHTMLDOCUMENT**
</dt> <dd>

為編譯的 HTML 檔案格式化程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTEXCELSPREADSHEET"></span><span id="wmdm_formatcode_microsoftexcelspreadsheet"></span>**WMDM \_ FORMATCODE \_ MICROSOFTEXCELSPREADSHEET**
</dt> <dd>

為 Microsoft Excel 試算表格式化程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_MICROSOFTPOWERPOINTDOCUMENT"></span><span id="wmdm_formatcode_microsoftpowerpointdocument"></span>**WMDM \_ FORMATCODE \_ MICROSOFTPOWERPOINTDOCUMENT**
</dt> <dd>

格式化 Microsoft PowerPoint 檔的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDMESSAGE"></span><span id="wmdm_formatcode_undefinedmessage"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDMESSAGE**
</dt> <dd>

格式化未定義類型之訊息的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTMESSAGE"></span><span id="wmdm_formatcode_abstractmessage"></span>**WMDM \_ FORMATCODE \_ ABSTRACTMESSAGE**
</dt> <dd>

格式化訊息的程式碼，其中物件包含訊息的屬性和選擇性的資料。 任何包含的資料都是與 MTP 規格相關的未定義格式。

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCONTACT"></span><span id="wmdm_formatcode_undefinedcontact"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCONTACT**
</dt> <dd>

針對未定義類型的連絡人格式化程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCONTACT"></span><span id="wmdm_formatcode_abstractcontact"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCONTACT**
</dt> <dd>

針對連絡人的格式程式碼，其中物件包含連絡人的屬性，以及選擇性的資料。 任何包含的資料都是與 MTP 規格相關的未定義格式。

</dd> <dt>

<span id="WMDM_FORMATCODE_VCARD2"></span><span id="wmdm_formatcode_vcard2"></span>**WMDM \_ FORMATCODE \_ VCARD2**
</dt> <dd>

格式化具有 vcard 第2版格式之電子卡的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_VCARD3"></span><span id="wmdm_formatcode_vcard3"></span>**WMDM \_ FORMATCODE \_ VCARD3**
</dt> <dd>

格式化具有 vcard 第3版格式之電子卡的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDCALENDARITEM"></span><span id="wmdm_formatcode_undefinedcalendaritem"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDCALENDARITEM**
</dt> <dd>

格式化未定義類型之電子日曆專案的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_ABSTRACTCALENDARITEM"></span><span id="wmdm_formatcode_abstractcalendaritem"></span>**WMDM \_ FORMATCODE \_ ABSTRACTCALENDARITEM**
</dt> <dd>

格式化行事曆專案的程式碼，其中物件包含行事曆專案的屬性，以及選擇性的資料。 任何包含的資料都是與 MTP 規格相關的未定義格式。

</dd> <dt>

<span id="WMDM_FORMATCODE_VCALENDAR1"></span><span id="wmdm_formatcode_vcalendar1"></span>**WMDM \_ FORMATCODE \_ VCALENDAR1**
</dt> <dd>

格式化具有 vcalendar 版本1格式的電子行事曆專案的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_VCALENDAR2"></span><span id="wmdm_formatcode_vcalendar2"></span>**WMDM \_ FORMATCODE \_ VCALENDAR2**
</dt> <dd>

格式為 vcalendar 版本2的電子行事曆專案格式化程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_UNDEFINEDWINDOWSEXECUTABLE"></span><span id="wmdm_formatcode_undefinedwindowsexecutable"></span>**WMDM \_ FORMATCODE \_ UNDEFINEDWINDOWSEXECUTABLE**
</dt> <dd>

格式化未定義類型之 Windows 型可執行檔的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_MEDIA_CAST"></span><span id="wmdm_formatcode_media_cast"></span>**WMDM \_ FORMATCODE \_ 媒體 \_ 轉換**
</dt> <dd>

格式化媒體轉換物件的程式碼。

</dd> <dt>

<span id="WMDM_FORMATCODE_SECTION"></span><span id="wmdm_formatcode_section"></span>**WMDM \_ FORMATCODE \_ 區段**
</dt> <dd>

將包含在另一個物件中之資料區段的程式碼格式化。

</dd> <dt>

<span id="________________________________WMDM_FORMATCODE_3G2A_"></span><span id="________________________________wmdm_formatcode_3g2a_"></span>**WMDM \_FORMATCODE \_ 3G2A** 
</dt> <dd>

3G2A 的格式程式碼 (3GPP2A) 多媒體容器格式。

</dd> </dl>

## <a name="remarks"></a>備註

若要探索裝置所支援的格式，應用程式可以使用 [**IWMDMDevice3：： GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty) 來查詢 **g \_ wszWMDMFormatsSupported** 裝置屬性。

若要探索特定格式的裝置功能，應用程式可以呼叫 [**IWMDMDevice3：： GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)。

應用程式可以在建立裝置上的儲存體時設定格式程式碼，方法是將 **g \_ wszWMDMFormatCode** 屬性包含在呼叫 [**IWMDMStorageControl3：： Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)的 *pMetaData* 參數中所傳遞的中繼資料中。

應用程式可以藉由呼叫 [**IWMDMStorage3：： GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata) 或 [**IWMDMStorage4：： GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata) 並取出 **g \_ wszWMDMFormatCode** 屬性，來查詢儲存體的格式代碼。

如果裝置支援在建立儲存體之後設定格式代碼，則應用程式可以使用 [**IWMDMStorage3：： >setmetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata) 來設定 **g \_ wszWMDMFormatCode** 屬性。 某些裝置在裝置上建立儲存體之後，可能不允許變更格式代碼。 因此，強烈建議您在 [**IWMDMStorageControl3：： Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3) 中，設定此屬性以及傳遞的中繼資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**列舉類型**](enumeration-types.md)
</dt> <dt>

[**IWMDMDevice3::GetFormatCapability**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getformatcapability)
</dt> <dt>

[**IWMDMDevice3：： GetProperty**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice3-getproperty)
</dt> <dt>

[**IWMDMStorage3：： GetMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-getmetadata)
</dt> <dt>

[**IWMDMStorage3：： >setmetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage3-setmetadata)
</dt> <dt>

[**IWMDMStorage4::GetSpecifiedMetadata**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorage4-getspecifiedmetadata)
</dt> <dt>

[**IWMDMStorageControl3::Insert3**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstoragecontrol3-insert3)
</dt> <dt>

[**中繼資料常數**](metadata-constants.md)
</dt> </dl>

 

 





