---
description: 指定音訊內容中發生的最高音量層級。
ms.assetid: 177311c4-c348-4d38-8c8d-b6690643529c
title: 'MFPKEY_WMADRC_PEAKREF 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88e91df613541f91f2efd2fd71ea38d7b1ca9a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971693"
---
# <a name="mfpkey_wmadrc_peakref-property"></a>MFPKEY \_ WMADRC \_ PEAKREF 屬性

指定音訊內容中發生的最高音量層級。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMADRCPeakReference

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="remarks"></a>備註

處理內容之後，您可以從編碼器取得此值。 您也可以在適用于動態範圍控制的解碼器上設定這個值。

如需動態範圍控制的詳細資訊，請參閱 web 文章 [Windows Media 音訊 Professional 編解碼器功能](/previous-versions/ms867218(v=msdn.10))。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
