---
description: 指定編碼器將用來編碼內容的傳遞數。
ms.assetid: 71a21976-ed92-4cd6-946c-fa6268895531
title: 'MFPKEY_PASSESUSED 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94ab020c4b683dc87ced3ffda8665b6b0e62b65cf81001c23c00b39f64ba146b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117873044"
---
# <a name="mfpkey_passesused-property"></a>MFPKEY \_ PASSESUSED 屬性

指定編碼器將用來編碼內容的傳遞數。 讀寫。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCPassesUsed

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="default-value"></a>預設值

1

## <a name="remarks"></a>備註

此值不能超過 [MFPKEY \_ PASSESRECOMMENDED](mfpkey-passesrecommendedproperty.md)的值。

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

 

 




