---
description: 指定編解碼器是否應在編碼期間使用中位數篩選。
ms.assetid: adfca033-4679-4f36-a802-6dd5df7100c8
title: 'MFPKEY_FORCEMEDIANSETTING 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38d0aa154798e2ed42a7373a6e85a4b46f8eeb7b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "103853439"
---
# <a name="mfpkey_forcemediansetting-property"></a>MFPKEY \_ FORCEMEDIANSETTING 屬性

指定編解碼器是否應在編碼期間使用中位數篩選。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCForceMedianSetting

## <a name="data-type"></a>資料類型

VT \_ BOOL

## <a name="default-value"></a>預設值

FALSE

## <a name="remarks"></a>備註

中間值篩選會在計算畫面格之間的動作時，告訴編解碼器忽略雜訊和細微性。 這可以改善非常雜訊影片的品質，但可能會導致動作軌跡 (也稱為「尾端成品」，) 套用至「清理來源」影片時。

根據預設，編解碼器會使用內部邏輯來判斷是否應該使用中間值篩選。 如果設定此屬性，則會覆寫該邏輯。

> [!Note]  
> 此篩選與在許多影片編輯和後置處理應用程式中找到的中位數模糊篩選不同。

 

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

 

 




