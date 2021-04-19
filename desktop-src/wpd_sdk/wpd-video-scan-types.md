---
description: WPD \_ 影片 \_ 掃描 \_ 類型列舉類型說明如何編碼影片檔案中的欄位。
ms.assetid: ea0dab57-6783-4d02-a43c-414e313f1e80
title: 'WPD_VIDEO_SCAN_TYPES 列舉 (PortableDevice .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_VIDEO_SCAN_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: a636bc95fd3d25de20c2df413576a504c4fa1b96
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995186"
---
# <a name="wpd_video_scan_types-enumeration"></a>WPD \_ 影片 \_ 掃描 \_ 類型列舉

**WPD \_ 影片 \_ 掃描 \_ 類型** 列舉類型說明如何編碼影片檔案中的欄位。

## <a name="syntax"></a>Syntax


```C++
typedef enum WPD_VIDEO_SCAN_TYPES { 
  WPD_VIDEO_SCAN_TYPE_UNUSED                           = 0,
  WPD_VIDEO_SCAN_TYPE_PROGRESSIVE                      = 1,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST    = 2,
  WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST    = 3,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST         = 4,
  WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST         = 5,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE                  = 6,
  WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE  = 7
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_UNUSED"></span><span id="wpd_video_scan_type_unused"></span>**\_未使用的 WPD 影片 \_ 掃描 \_ 類型 \_**
</dt> <dd>

尚未為此影片檔案定義掃描類型，或不適用。

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_PROGRESSIVE"></span><span id="wpd_video_scan_type_progressive"></span>**WPD \_ 影片 \_ 掃描 \_ 類型 \_ 漸進式**
</dt> <dd>

漸進式掃描影片檔案。

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_upper_first"></span>**WPD \_ 影片 \_ 掃描 \_ 類型 \_ 欄位 \_ 交錯 \_ 上方 \_**
</dt> <dd>

一種交錯的影片檔案，其中的欄位是替代的，而第) 1 行 (的欄位則是先繪製。 如需詳細資訊，請參閱＜備註＞一節。

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_INTERLEAVED_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_interleaved_lower_first"></span>**\_ \_ \_ \_ \_ \_ 先交錯較低 \_ 的 WPD 影片掃描類型欄位**
</dt> <dd>

一種交錯的影片檔案，其中的欄位是替代的，而第) 2 行 (的欄位則是先繪製。 如需詳細資訊，請參閱本節後面的「備註」。

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_UPPER_FIRST"></span><span id="wpd_video_scan_type_field_single_upper_first"></span>**WPD \_ VIDEO \_ SCAN \_ TYPE \_ 欄位 \_ SINGLE \_ \_ FIRST**
</dt> <dd>

一種交錯的影片檔案，其中的欄位會以連續範例的形式傳送，而第1行) 的上方欄位 (則會先繪製。 如需詳細資訊，請參閱本節後面的「備註」。

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_FIELD_SINGLE_LOWER_FIRST"></span><span id="wpd_video_scan_type_field_single_lower_first"></span>**WPD \_ 影片 \_ 掃描 \_ 類型 \_ 欄位 \_ 的 \_ \_ 第一個較低**
</dt> <dd>

一種交錯的影片檔案，其中的欄位會以連續範例的形式傳送，而第) 2 行 (的較低欄位則會先傳送。

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE"></span><span id="wpd_video_scan_type_mixed_interlace"></span>**WPD \_ 影片 \_ 掃描 \_ 類型 \_ 混合 \_ 交錯**
</dt> <dd>

混合交錯模式的影片檔案。

</dd> <dt>

<span id="WPD_VIDEO_SCAN_TYPE_MIXED_INTERLACE_AND_PROGRESSIVE"></span><span id="wpd_video_scan_type_mixed_interlace_and_progressive"></span>**WPD \_ 影片 \_ 掃描 \_ 類型 \_ 混合 \_ 交錯 \_ 和 \_ 漸進**
</dt> <dd>

混合交錯和漸進模式的影片檔案。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉是由 [WPD \_ VIDEO \_ SCAN \_ TYPE](properties-and-attributes.md) 屬性所使用。

這兩種類型的交錯檔案格式是由這個列舉所指定。 **WPD \_影片 \_ 掃描 \_ 類型 \_ 欄位 \_ 交錯** 指的是一種檔案格式，它會在掃描的欄位替換時傳遞框架，而資料會逐行進行，如下所示：

**畫面 1**

欄位1：行1

欄位2：行1

欄位1：第2行

欄位2：第2行

欄位1：第3行

欄位2：第3行

...

**WPD \_影片 \_ 掃描 \_ 類型 \_ 欄位 \_ SINGLE** 指的是一種檔案格式，其中每個欄位都會儲存在掃描行的單一區塊中，而且會依序儲存欄位，如下所示：

**畫面 1**

欄位1：行1

欄位1：第2行

欄位1：第3行

...

其次

欄位2：行1

欄位2：第2行

欄位2：第3行

...

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>PortableDevice。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**結構和列舉類型**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




