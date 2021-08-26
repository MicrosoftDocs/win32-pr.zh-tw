---
description: 指定音訊內容中發生的最高音量層級。
ms.assetid: 177311c4-c348-4d38-8c8d-b6690643529c
title: 'MFPKEY_WMADRC_PEAKREF 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58013ba116b9217ad6c16c93e420a09872cd887c4d5068f7c5b5dd68bf013377
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953449"
---
# <a name="mfpkey_wmadrc_peakref-property"></a>MFPKEY \_ WMADRC \_ PEAKREF 屬性

指定音訊內容中發生的最高音量層級。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMADRCPeakReference

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="remarks"></a>備註

處理內容之後，您可以從編碼器取得此值。 您也可以在適用于動態範圍控制的解碼器上設定這個值。

如需動態範圍控制的詳細資訊，請參閱[Windows Media 音訊 Professional 編解碼器功能](/previous-versions/ms867218(v=msdn.10))的 web 文章。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Wmcodecdsp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

 
