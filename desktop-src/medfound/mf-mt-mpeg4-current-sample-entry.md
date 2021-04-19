---
description: 在 MPEG 4 媒體類型的 [範例描述] 方塊中指定目前的專案。
ms.assetid: c8c36abf-6905-4874-a6d2-90dd0725421b
title: 'MF_MT_MPEG4_CURRENT_SAMPLE_ENTRY 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c1f2a43eef1a520a49f5cfbb889f13149fa249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984982"
---
# <a name="mf_mt_mpeg4_current_sample_entry-attribute"></a>MF \_ MT \_ MPEG4 \_ 目前的 \_ 範例 \_ 專案屬性

在 MPEG 4 媒體類型的 [範例描述] 方塊中指定目前的專案。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="getset"></a>取得/設定

若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。

若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。

## <a name="applies-to"></a>適用於

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)

## <a name="remarks"></a>備註

在 [檔] 或 [3GP] 檔案中，[範例描述] 方塊描述檔案中資料流程所使用的編碼方式。 [範例描述] 方塊可以包含多個專案。 這個屬性會指定要使用的專案。 值是清單中以零為起始的索引。

目前唯一支援的值是0。 屬性已定義為未來的擴充性。

MPEG-2 檔案來源一律會將值設定為0。 3GP 檔接收會忽略這個屬性的值（如果有的話）。

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                  |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體類型屬性](media-type-attributes.md)
</dt> <dt>

[MF \_ MT \_ MPEG4 \_ 範例 \_ 說明](mf-mt-mpeg4-sample-description.md)
</dt> </dl>

 

 




