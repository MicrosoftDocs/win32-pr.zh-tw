---
description: 指定編碼器是否必須包含在轉碼拓撲中。
ms.assetid: 73f23aed-d1b9-4821-b1ca-0a07f02b6913
title: 'MF_TRANSCODE_DONOT_INSERT_ENCODER 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92d3f8fc5dabfd3e4c55c6242ba9b8f52b6f5c2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973887"
---
# <a name="mf_transcode_donot_insert_encoder-attribute"></a>MF \_ 轉碼 \_ 沒有 \_ 插入 \_ 編碼器屬性

指定編碼器是否必須包含在轉碼拓撲中。

[**MFCreateTranscodeTopology**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetranscodetopology)函式會在拓撲建立期間檢查這個屬性。 如果未設定此屬性，則會將編碼器插入轉碼拓撲中。

## <a name="data-type"></a>資料類型

**UINT32**



| 值                                                                        | 意義                                                                                                           |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | 編碼器會插入轉碼拓撲中。<br/>                                                      |
| <dl> <dt>1</dt> </dl> | 編碼器不會包含在轉碼拓撲中。 來源節點連接至輸出節點。<br/> |



 

## <a name="remarks"></a>備註

這個屬性的 GUID 常數是從 mfuuid 匯出。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                            |
| 標頭<br/>                   | <dl> <dt>Mfidl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[媒體基礎屬性](media-foundation-attributes.md)
</dt> </dl>

 

 




