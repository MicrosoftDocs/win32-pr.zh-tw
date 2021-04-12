---
description: 為編碼的影片指定中繼框架高度。
ms.assetid: 7382ec31-6d59-4e8c-94eb-804786074038
title: 'MFPKEY_FORCEFRAMEHEIGHT 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8e4662ce56ea4c20d44abdd05641219bc6b94ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192259"
---
# <a name="mfpkey_forceframeheight-property"></a>MFPKEY \_ FORCEFRAMEHEIGHT 屬性

為編碼的影片指定中繼框架高度。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCForceFrameHeight

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="remarks"></a>備註

您可以設定此值和 [MFPKEY \_ FORCEFRAMEWIDTH](mfpkey-forceframewidthproperty.md) 屬性，以強制編碼器以小於輸入或輸出框架大小的框架大小來編碼影片串流。 解碼時，影片將會調整大小為其原始輸入解析度。

任一軸的有效框架維度都是2到8192圖元。 框架維度必須可以整除2。

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

 

 




