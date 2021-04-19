---
description: 指定 h.264 video remux MFT 是否應將圖片標示為乾淨點，以取得更好的搜尋能力。 這可能會在搜尋不符合規範的最終將檔案中進行搜尋。
ms.assetid: BB521E13-40A4-4643-B071-76B8CBC62074
title: 'MFT_REMUX_MARK_I_PICTURE_AS_CLEAN_POINT 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c9fe8398507f6d7af5d0e4bf45a36a4454f220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985633"
---
# <a name="mft_remux_mark_i_picture_as_clean_point-attribute"></a>MFT \_ REMUX \_ 將 \_ 我 \_ 的圖片標示 \_ 為 \_ 乾淨 \_ 點屬性

指定 h.264 video remux MFT 是否應將圖片標示為乾淨點，以取得更好的搜尋能力。 這可能會在搜尋不符合規範的最終將檔案中進行搜尋。

## <a name="data-type"></a>資料類型

**Bool** 儲存為 **UINT32**

## <a name="remarks"></a>備註

清理點圖片應依定義壓縮 IDR 圖片。

這不建議用來錄製或 remuxing 操作檔案，除非這類練習會產生一些中繼虛擬操作檔案來進行影片編輯。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                             |
| 標頭<br/>                   | <dl> <dt>Mftransform。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Mftransform .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[依字母順序排列的媒體基礎屬性清單](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




