---
description: 指定編碼影片的中繼框架寬度。
ms.assetid: 805bd587-31af-49b8-b5ab-2dcf2a3f81c5
title: 'MFPKEY_FORCEFRAMEWIDTH 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8d04e30f5fd5d2ecc7055553e17eaf86199b62be8d3dd861b9f82246947212f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939831"
---
# <a name="mfpkey_forceframewidth-property"></a>MFPKEY \_ FORCEFRAMEWIDTH 屬性

指定編碼影片的中繼框架寬度。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCForceFrameWidth

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="remarks"></a>備註

您可以設定此值和 [MFPKEY \_ FORCEFRAMEHEIGHT](mfpkey-forceframeheightproperty.md) 屬性，以強制編碼器以小於輸入或輸出框架大小的框架大小來編碼影片串流。 解碼時，影片將會調整大小為其原始輸入解析度。

任一軸的有效框架維度都是2到8192圖元。 框架維度必須可以整除2。

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

 

 




