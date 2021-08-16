---
description: 表示在產生的檔案中，moov 會在 mdat box 之前寫入。
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: 'MF_MPEG4SINK_MOOV_BEFORE_MDAT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e98614484beee5187364570e3c5517ba0f61e0d77161484b59af93a9f5a6512c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104734"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a>\_ \_ \_ MDAT 屬性之前的 MF MPEG4SINK MOOV \_

表示在產生的檔案中，' mdat ' 方塊之前會寫入 ' moov '。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

Mpeg4 媒體接收器的預設行為是在 [mdat] 方塊後面寫入 ' moov '。 設定這個屬性會導致產生的檔案在 ' mdat ' 方塊之前寫入 ' moov '。

為了讓 mpeg4 接收使用此屬性，傳入的位元組資料流程在的搜尋或遠端中不一定要太慢。

這項功能牽涉到額外的檔案複製/remuxing。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 \[桌面應用程式 \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> </dl>

 

 




