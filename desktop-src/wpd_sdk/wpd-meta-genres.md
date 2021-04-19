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
ms.openlocfilehash: 1f6ff4875474776df1e2436e0209e6d863f5b3e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995650"
---
# <a name="wpd_meta_genres-enumeration"></a><span data-ttu-id="534e6-103">WPD \_ 中繼內容 \_ 列舉</span><span class="sxs-lookup"><span data-stu-id="534e6-103">WPD\_META\_GENRES enumeration</span></span>

<span data-ttu-id="534e6-104">**WPD \_ META \_** content-type 列舉型別描述媒體檔案的廣泛類型。</span><span class="sxs-lookup"><span data-stu-id="534e6-104">The **WPD\_META\_GENRES** enumeration type describes a broad genre type of a media file.</span></span>

## <a name="syntax"></a><span data-ttu-id="534e6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="534e6-105">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="534e6-106">常數</span><span class="sxs-lookup"><span data-stu-id="534e6-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="534e6-107"><span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**\_ \_ \_ 未使用的 WPD 中繼類型**</span><span class="sxs-lookup"><span data-stu-id="534e6-107"><span id="WPD_META_GENRE_UNUSED"></span><span id="wpd_meta_genre_unused"></span>**WPD\_META\_GENRE\_UNUSED**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-108">尚未設定內容類型，或不適用。</span><span class="sxs-lookup"><span data-stu-id="534e6-108">The genre has not been set, or is not applicable.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-109"><span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**WPD \_ 中繼 \_ 類型 \_ 一般 \_ 音樂 \_ 音訊 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="534e6-109"><span id="WPD_META_GENRE_GENERIC_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_music_audio_file"></span>**WPD\_META\_GENRE\_GENERIC\_MUSIC\_AUDIO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-110">這是一般的音樂檔案， (只) 音訊。</span><span class="sxs-lookup"><span data-stu-id="534e6-110">This is a generic music file (audio only).</span></span>

</dd> <dt>

<span data-ttu-id="534e6-111"><span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**WPD \_ 中繼 \_ 類型 \_ 一般 \_ 非 \_ 音樂 \_ 音訊 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="534e6-111"><span id="WPD_META_GENRE_GENERIC_NON_MUSIC_AUDIO_FILE"></span><span id="wpd_meta_genre_generic_non_music_audio_file"></span>**WPD\_META\_GENRE\_GENERIC\_NON\_MUSIC\_AUDIO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-112">這是一般非音樂音訊檔案，例如語音或音訊書籍。</span><span class="sxs-lookup"><span data-stu-id="534e6-112">This is a generic non-music audio file, for example, a speech or audio book.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-113"><span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**WPD \_ 中繼 \_ \_ 文字類型 \_ 語音 \_ 音訊 \_ 書籍 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="534e6-113"><span id="WPD_META_GENRE_SPOKEN_WORD_AUDIO_BOOK_FILES"></span><span id="wpd_meta_genre_spoken_word_audio_book_files"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_AUDIO\_BOOK\_FILES**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-114">這是音訊書籍檔。</span><span class="sxs-lookup"><span data-stu-id="534e6-114">This is an audio book file.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-115"><span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**WPD \_ 中繼 \_ 類型 \_ 語音 \_ \_ 檔 \_ 非 \_ 音訊 \_ 書籍**</span><span class="sxs-lookup"><span data-stu-id="534e6-115"><span id="WPD_META_GENRE_SPOKEN_WORD_FILES_NON_AUDIO_BOOK"></span><span id="wpd_meta_genre_spoken_word_files_non_audio_book"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_FILES\_NON\_AUDIO\_BOOK**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-116">這是一種非音訊書籍的語音音訊檔案，例如訪談或語音。</span><span class="sxs-lookup"><span data-stu-id="534e6-116">This is a spoken-word audio file that is not an audio book, for example, an interview or speech.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-117"><span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**WPD \_ \_ 說出 \_ 的 \_ 單字 \_ 新聞**</span><span class="sxs-lookup"><span data-stu-id="534e6-117"><span id="WPD_META_GENRE_SPOKEN_WORD_NEWS"></span><span id="wpd_meta_genre_spoken_word_news"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_NEWS**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-118">這是新聞音訊或影片檔案。</span><span class="sxs-lookup"><span data-stu-id="534e6-118">This is a news audio or video file.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-119"><span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**WPD \_ 中繼文字類型說話的 \_ \_ \_ 文字 \_ 交談 \_ 節目**</span><span class="sxs-lookup"><span data-stu-id="534e6-119"><span id="WPD_META_GENRE_SPOKEN_WORD_TALK_SHOWS"></span><span id="wpd_meta_genre_spoken_word_talk_shows"></span>**WPD\_META\_GENRE\_SPOKEN\_WORD\_TALK\_SHOWS**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-120">這是說話節目的音訊錄影。</span><span class="sxs-lookup"><span data-stu-id="534e6-120">This is an audio recording of a talk show.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-121"><span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**WPD \_ 中繼 \_ 類型 \_ 一般 \_ 影片 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="534e6-121"><span id="WPD_META_GENRE_GENERIC_VIDEO_FILE"></span><span id="wpd_meta_genre_generic_video_file"></span>**WPD\_META\_GENRE\_GENERIC\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-122">這是一般影片檔案。</span><span class="sxs-lookup"><span data-stu-id="534e6-122">This is a generic video file.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-123"><span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**WPD \_ 中繼 \_ 類型 \_ 新聞 \_ 影片 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="534e6-123"><span id="WPD_META_GENRE_NEWS_VIDEO_FILE"></span><span id="wpd_meta_genre_news_video_file"></span>**WPD\_META\_GENRE\_NEWS\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-124">這是新聞影片檔案。</span><span class="sxs-lookup"><span data-stu-id="534e6-124">This is a news video file.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-125"><span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**WPD \_ 中繼內容類型 \_ \_ 音樂 \_ 影片 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="534e6-125"><span id="WPD_META_GENRE_MUSIC_VIDEO_FILE"></span><span id="wpd_meta_genre_music_video_file"></span>**WPD\_META\_GENRE\_MUSIC\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-126">這是音樂影片檔案。</span><span class="sxs-lookup"><span data-stu-id="534e6-126">This is a music video file.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-127"><span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**WPD \_ 中繼內容類型 \_ \_ 首頁 \_ 影片 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="534e6-127"><span id="WPD_META_GENRE_HOME_VIDEO_FILE"></span><span id="wpd_meta_genre_home_video_file"></span>**WPD\_META\_GENRE\_HOME\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-128">這是首頁影片檔案。</span><span class="sxs-lookup"><span data-stu-id="534e6-128">This is a home video file.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-129"><span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**WPD \_ 中繼內容類型 \_ \_ 功能 \_ 影片 \_ \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="534e6-129"><span id="WPD_META_GENRE_FEATURE_FILM_VIDEO_FILE"></span><span id="wpd_meta_genre_feature_film_video_file"></span>**WPD\_META\_GENRE\_FEATURE\_FILM\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-130">這是功能電影的影片檔案。</span><span class="sxs-lookup"><span data-stu-id="534e6-130">This is a feature film video file.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-131"><span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**WPD \_ META \_ 類型 \_ 電視 \_ 影片 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="534e6-131"><span id="WPD_META_GENRE_TELEVISION_VIDEO_FILE"></span><span id="wpd_meta_genre_television_video_file"></span>**WPD\_META\_GENRE\_TELEVISION\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-132">這是電視節目的影片檔案。</span><span class="sxs-lookup"><span data-stu-id="534e6-132">This is a television program video file.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-133"><span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**WPD \_ 中繼 \_ 類型 \_ 訓練 \_ 教育 \_ 影片 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="534e6-133"><span id="WPD_META_GENRE_TRAINING_EDUCATIONAL_VIDEO_FILE"></span><span id="wpd_meta_genre_training_educational_video_file"></span>**WPD\_META\_GENRE\_TRAINING\_EDUCATIONAL\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-134">這是一項教育影片檔案。</span><span class="sxs-lookup"><span data-stu-id="534e6-134">This is an educational video file.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-135"><span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**WPD \_ META 內容類型 \_ \_ 相片 \_ 蒙太奇 \_ 影片 \_ 檔案**</span><span class="sxs-lookup"><span data-stu-id="534e6-135"><span id="WPD_META_GENRE_PHOTO_MONTAGE_VIDEO_FILE"></span><span id="wpd_meta_genre_photo_montage_video_file"></span>**WPD\_META\_GENRE\_PHOTO\_MONTAGE\_VIDEO\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-136">這是配備相片蒙太奇的影片檔案。</span><span class="sxs-lookup"><span data-stu-id="534e6-136">This is a video file featuring a photo montage.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-137"><span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**WPD \_ 中繼 \_ 類型 \_ 一般 \_ 非 \_ 音訊 \_ \_ 的非影片**</span><span class="sxs-lookup"><span data-stu-id="534e6-137"><span id="WPD_META_GENRE_GENERIC_NON_AUDIO_NON_VIDEO"></span><span id="wpd_meta_genre_generic_non_audio_non_video"></span>**WPD\_META\_GENRE\_GENERIC\_NON\_AUDIO\_NON\_VIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-138">這是沒有音訊或影片的檔案。</span><span class="sxs-lookup"><span data-stu-id="534e6-138">This is a file without audio or video.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-139"><span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**WPD \_ 中繼 \_ 類型 \_ 音訊 \_ 播客**</span><span class="sxs-lookup"><span data-stu-id="534e6-139"><span id="WPD_META_GENRE_AUDIO_PODCAST"></span><span id="wpd_meta_genre_audio_podcast"></span>**WPD\_META\_GENRE\_AUDIO\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-140">這是音訊播客。</span><span class="sxs-lookup"><span data-stu-id="534e6-140">This is an audio podcast.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-141"><span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**WPD \_ 中繼 \_ 類型 \_ 影片 \_ 播客**</span><span class="sxs-lookup"><span data-stu-id="534e6-141"><span id="WPD_META_GENRE_VIDEO_PODCAST"></span><span id="wpd_meta_genre_video_podcast"></span>**WPD\_META\_GENRE\_VIDEO\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-142">這是影片播客。</span><span class="sxs-lookup"><span data-stu-id="534e6-142">This is a video podcast.</span></span>

</dd> <dt>

<span data-ttu-id="534e6-143"><span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**WPD \_ 中繼 \_ 類型 \_ 混合 \_ 播客**</span><span class="sxs-lookup"><span data-stu-id="534e6-143"><span id="WPD_META_GENRE_MIXED_PODCAST"></span><span id="wpd_meta_genre_mixed_podcast"></span>**WPD\_META\_GENRE\_MIXED\_PODCAST**</span></span>
</dt> <dd>

<span data-ttu-id="534e6-144">這是包含音訊和影片的播客。</span><span class="sxs-lookup"><span data-stu-id="534e6-144">This is a podcast containing both audio and video.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="534e6-145">備註</span><span class="sxs-lookup"><span data-stu-id="534e6-145">Remarks</span></span>

<span data-ttu-id="534e6-146">此列舉是由 [ [WPD \_ 媒體 \_ META \_ ](media-properties.md) 內容類型] 屬性所使用。</span><span class="sxs-lookup"><span data-stu-id="534e6-146">This enumeration is used by the [WPD\_MEDIA\_META\_GENRE](media-properties.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="534e6-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="534e6-147">Requirements</span></span>



| <span data-ttu-id="534e6-148">需求</span><span class="sxs-lookup"><span data-stu-id="534e6-148">Requirement</span></span> | <span data-ttu-id="534e6-149">值</span><span class="sxs-lookup"><span data-stu-id="534e6-149">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="534e6-150">標頭</span><span class="sxs-lookup"><span data-stu-id="534e6-150">Header</span></span><br/> | <dl> <span data-ttu-id="534e6-151"><dt>PortableDevice。h</dt></span><span class="sxs-lookup"><span data-stu-id="534e6-151"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="534e6-152">另請參閱</span><span class="sxs-lookup"><span data-stu-id="534e6-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="534e6-153">**結構和列舉類型**</span><span class="sxs-lookup"><span data-stu-id="534e6-153">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




