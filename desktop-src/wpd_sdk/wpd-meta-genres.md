---
description: WPD \_ META \_ content-type 列舉型別描述媒體檔案的廣泛類型。
ms.assetid: a69cab70-5a45-4e75-abbd-230396c2b5ec
title: 'WPD_META_GENRES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_META_GENRES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 679bc47e2e8439c7f4cd5c3bcf26e6d6897910cfbfcaaaae3fe6dec6c9e0b8f9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118696518"
---
# <a name="wpd_meta_genres-enumeration"></a>WPD \_ 中繼內容 \_ 列舉

**WPD \_ META \_** content-type 列舉型別描述媒體檔案的廣泛類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_META_GENRES { 
  WPD_META_GENRE_UNUSED                            = 0x0,
  WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE          = 0x1,
  WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE      = 0x11,
  WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES      = 0x12,
  WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK  = 0x13,
  WPD_META_GENRE_SPOKEN_WORD_NEWS                  = 0x14,
  WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS            = 0x15,
  WPD_META_GENRE_GENERIC_VIDEO_FILE                = 0x21,
  WPD_META_GENRE_NEWS_VIDEO_FILE                   = 0x22,
  WPD_META_GENRE_MUSIC_VIDEO_FILE                  = 0x23,
  WPD_META_GENRE_HOME_VIDEO_FILE                   = 0x24,
  WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE           = 0x25,
  WPD_META_GENRE_TELEVISION_VIDEO_FILE             = 0x26,
  WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE   = 0x27,
  WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE          = 0x28,
  WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO       = 0x30,
  WPD_META_GENRE_AUDIO_PODCAST                     = 0x40,
  WPD_META_GENRE_VIDEO_PODCAST                     = 0x41,
  WPD_META_GENRE_MIXED_PODCAST                     = 0x42
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**\_ \_ \_ 未使用的 WPD 中繼類型**
</dt> <dd>

尚未設定內容類型，或不適用。

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**WPD \_ 中繼 \_ 類型 \_ 一般 \_ 音樂 \_ 音訊 \_ 檔案**
</dt> <dd>

這是一般的音樂檔案， (只) 音訊。

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**WPD \_ 中繼 \_ 類型 \_ 一般 \_ 非 \_ 音樂 \_ 音訊 \_ 檔案**
</dt> <dd>

這是一般非音樂音訊檔案，例如語音或音訊書籍。

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**WPD \_ 中繼 \_ \_ 文字類型 \_ 語音 \_ 音訊 \_ 書籍 \_ 檔案**
</dt> <dd>

這是音訊書籍檔。

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**WPD \_ 中繼 \_ 類型 \_ 語音 \_ \_ 檔 \_ 非 \_ 音訊 \_ 書籍**
</dt> <dd>

這是一種非音訊書籍的語音音訊檔案，例如訪談或語音。

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**WPD \_ \_ 說出 \_ 的 \_ 單字 \_ 新聞**
</dt> <dd>

這是新聞音訊或影片檔案。

</dd> <dt>

<span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**WPD \_ 中繼文字類型說話的 \_ \_ \_ 文字 \_ 交談 \_ 節目**
</dt> <dd>

這是說話節目的音訊錄影。

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**WPD \_ 中繼 \_ 類型 \_ 一般 \_ 影片 \_ 檔案**
</dt> <dd>

這是一般影片檔案。

</dd> <dt>

<span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**WPD \_ 中繼 \_ 類型 \_ 新聞 \_ 影片 \_ 檔案**
</dt> <dd>

這是新聞影片檔案。

</dd> <dt>

<span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**WPD \_ 中繼內容類型 \_ \_ 音樂 \_ 影片 \_ 檔案**
</dt> <dd>

這是音樂影片檔案。

</dd> <dt>

<span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**WPD \_ 中繼內容類型 \_ \_ 首頁 \_ 影片 \_ 檔案**
</dt> <dd>

這是首頁影片檔案。

</dd> <dt>

<span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**WPD \_ 中繼內容類型 \_ \_ 功能 \_ 影片 \_ \_ 檔案**
</dt> <dd>

這是功能電影的影片檔案。

</dd> <dt>

<span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**WPD \_ META \_ 類型 \_ 電視 \_ 影片 \_ 檔案**
</dt> <dd>

這是電視節目的影片檔案。

</dd> <dt>

<span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**WPD \_ 中繼 \_ 類型 \_ 訓練 \_ 教育 \_ 影片 \_ 檔案**
</dt> <dd>

這是一項教育影片檔案。

</dd> <dt>

<span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**WPD \_ META 內容類型 \_ \_ 相片 \_ 蒙太奇 \_ 影片 \_ 檔案**
</dt> <dd>

這是配備相片蒙太奇的影片檔案。

</dd> <dt>

<span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**WPD \_ 中繼 \_ 類型 \_ 一般 \_ 非 \_ 音訊 \_ \_ 的非影片**
</dt> <dd>

這是沒有音訊或影片的檔案。

</dd> <dt>

<span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**WPD \_ 中繼 \_ 類型 \_ 音訊 \_ 播客**
</dt> <dd>

這是音訊播客。

</dd> <dt>

<span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**WPD \_ 中繼 \_ 類型 \_ 影片 \_ 播客**
</dt> <dd>

這是影片播客。

</dd> <dt>

<span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**WPD \_ 中繼 \_ 類型 \_ 混合 \_ 播客**
</dt> <dd>

這是包含音訊和影片的播客。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉是由 [ [WPD \_ 媒體 \_ META \_ ](media-properties.md) 內容類型] 屬性所使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




