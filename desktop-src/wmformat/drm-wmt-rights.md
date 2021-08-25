---
title: 'WMT_RIGHTS 列舉 (Wmdrmsdk .h) '
description: 定義可在 DRM 授權中指定的許可權。
ms.assetid: 9c034ca0-83e9-4a4c-8e98-96e2a95fd97c
keywords:
- WMT_RIGHTS 列舉 windows 媒體格式
- 列舉 windows 媒體格式
topic_type:
- apiref
api_name:
- WMT_RIGHTS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3a48c9ce3a276f060ac90dd15100ca8612e35116e124588e27f4ee36c1a0b8a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930738"
---
# <a name="wmt_rights-enumeration"></a>WMT \_ 許可權列舉

**WMT \_ 許可權** 列舉類型會定義可在 DRM 授權中指定的許可權。

## <a name="syntax"></a>Syntax


```C++
typedef enum WMT_RIGHTS { 
  WMT_RIGHT_PLAYBACK                 = 0x00000001,
  WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE  = 0x00000002,
  WMT_RIGHT_COPY_TO_CD               = 0x00000008,
  WMT_RIGHT_COPY_TO_SDMI_DEVICE      = 0x00000010,
  WMT_RIGHT_ONE_TIME                 = 0x00000020,
  WMT_RIGHT_SAVE_STREAM_PROTECTED    = 0x00000040,
  WMT_RIGHT_COPY                     = 0x00000080,
  WMT_RIGHT_COLLABORATIVE_PLAY       = 0x00000100,
  WMT_RIGHT_SDMI_TRIGGER             = 0x00010000,
  WMT_RIGHT_SDMI_NOMORECOPIES        = 0x00020000
} ;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WMT_RIGHT_PLAYBACK"></span><span id="wmt_right_playback"></span>**WMT \_ 右 \_ 播放**
</dt> <dd>

指定不受限制地播放內容的許可權。

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_NON_SDMI_DEVICE"></span><span id="wmt_right_copy_to_non_sdmi_device"></span>**將 \_ WMT \_ 右移 \_ 至 \_ 非 \_ SDMI \_ 裝置**
</dt> <dd>

指定將內容複寫到裝置的許可權，不符合 (SDMI) 的安全數位音樂方案。

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_CD"></span><span id="wmt_right_copy_to_cd"></span>**WMT \_ RIGHT \_ 複製 \_ 到 \_ CD**
</dt> <dd>

指定將內容複寫到 CD 的許可權。

</dd> <dt>

<span id="WMT_RIGHT_COPY_TO_SDMI_DEVICE"></span><span id="wmt_right_copy_to_sdmi_device"></span>**WMT \_ RIGHT \_ 複製 \_ 到 \_ SDMI \_ 裝置**
</dt> <dd>

指定將內容複寫到符合 SDMI 規範之裝置的許可權。

</dd> <dt>

<span id="WMT_RIGHT_ONE_TIME"></span><span id="wmt_right_one_time"></span>**WMT \_ 右移 \_ 一 \_ 次**
</dt> <dd>

指定僅一次播放內容的許可權。

</dd> <dt>

<span id="WMT_RIGHT_SAVE_STREAM_PROTECTED"></span><span id="wmt_right_save_stream_protected"></span>**WMT \_ 已 \_ 保護正確的儲存 \_ 資料流程 \_**
</dt> <dd>

指定從伺服器儲存內容的許可權。

</dd> <dt>

<span id="WMT_RIGHT_COPY"></span><span id="wmt_right_copy"></span>**WMT \_ RIGHT \_ COPY**
</dt> <dd>

指定複製內容的許可權。 Windows媒體 DRM 10 會使用 (OPLs) 的輸出保護層級，來控制可將內容複寫到其中的裝置。

</dd> <dt>

<span id="WMT_RIGHT_COLLABORATIVE_PLAY"></span><span id="wmt_right_collaborative_play"></span>**WMT \_ RIGHT \_ 協同作業 \_ 播放**
</dt> <dd>

指定在線上案例中播放內容的許可權，其中多個參與者可將歌曲從其集合投稿至共用播放清單。

</dd> <dt>

<span id="WMT_RIGHT_SDMI_TRIGGER"></span><span id="wmt_right_sdmi_trigger"></span>**WMT \_ RIGHT \_ SDMI \_ 觸發程式**
</dt> <dd>

保留供未來使用。 請勿使用。

</dd> <dt>

<span id="WMT_RIGHT_SDMI_NOMORECOPIES"></span><span id="wmt_right_sdmi_nomorecopies"></span>**WMT \_ RIGHT \_ SDMI \_ NOMORECOPIES**
</dt> <dd>

保留供未來使用。 請勿使用。

</dd> </dl>

## <a name="remarks"></a>備註

這些值是位旗標，因此可以藉由結合位 **or** 運算子來設定一或多個值。

使用 Windows 媒體 DRM 10 時， **WMT \_ right \_ copy \_ 至 \_ 非 \_ sdmi \_ 裝置**、 **WMT \_ right \_ copy \_ 至 \_ SDMI \_ 裝置**，並由 **WMT \_ right \_ copy** 取代 **WMT \_ RIGHT \_ 複製 \_ 至 \_ CD** 。 您可以使用 (OPLs) 的輸出保護層級，來指定可複製內容之裝置的限制。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdrmsdk。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**列舉類型**](drm-enumeration-types.md)
</dt> </dl>

 

 





