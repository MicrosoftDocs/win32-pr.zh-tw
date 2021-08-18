---
description: 指定音訊內容的平均音量層級。
ms.assetid: eabb36ff-300f-4ed1-aca3-9415627ac1a7
title: 'MFPKEY_WMADRC_AVGREF 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf7d3575b81ca878c610aed95ca25f73fa94c292ec16f9245a72a3a9515198c7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118973237"
---
# <a name="mfpkey_wmadrc_avgref-property"></a>MFPKEY \_ WMADRC \_ AVGREF 屬性

指定音訊內容的平均音量層級。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMADRCAverageReference

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="remarks"></a>備註

處理內容之後，您可以從編碼器取得此值。 您也可以在解碼器上設定此值以用於動態範圍控制項，但只有在已設定 [MFPKEY \_ WMADEC \_ DRCMODE](mfpkey-wmadec-drcmodeproperty.md) 屬性時，才會有作用。

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

 

 
