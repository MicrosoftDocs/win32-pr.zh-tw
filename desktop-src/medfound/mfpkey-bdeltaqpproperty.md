---
description: 指定在錨點框架的圖片 quantizer 與 B 型框架的圖片 quantizer 之間的差異增加。
ms.assetid: 8ab9401b-6fed-4178-955f-2e0bf950bf60
title: 'MFPKEY_BDELTAQP 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e37bf5b319707e0bb5bf5a722b119b6078ac07d5ba0fe20978f0a212786ee268
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873802"
---
# <a name="mfpkey_bdeltaqp-property"></a>MFPKEY \_ BDELTAQP 屬性

指定在錨點框架的圖片 quantizer 與 B 型框架的圖片 quantizer 之間的差異增加。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCBDeltaQP

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

0

## <a name="remarks"></a>備註

Picture quantizer (QP) 是一種測量框架壓縮方式的度量。 較高的值表示較高的壓縮比率。 您可以設定以半點遞增的方式設定 QP。 B 型框架通常會在與錨點框架的 QP 相同或高於0.5 的 QP 上進行壓縮。 您可以藉由指定大於0的 B 型框架 QP 差異，以更高的壓縮比例壓縮 B 框架。

B 型框架 delta QP 只能以整數遞增的方式設定。 這個屬性必須設定為介於0到31之間的整數值。 建議值為1。

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

 

 




