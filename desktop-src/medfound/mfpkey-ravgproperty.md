---
description: 指定平均位元速率（以每秒位數為單位），用於2次傳遞、變數位速率 (VBR) 編碼。
ms.assetid: 88a1888f-7bfb-4e24-9d48-92cfde02a14f
title: 'MFPKEY_RAVG 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90fd5435498a8a0c247d9363f02e2e767b46c5ab17ce36cc5a41feab54ed5277
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120113288"
---
# <a name="mfpkey_ravg-property"></a>MFPKEY \_ RAVG 屬性

指定平均位元速率（以每秒位數為單位），用於2次傳遞、變數位速率 (VBR) 編碼。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCAvgBitrate

## <a name="data-type"></a>資料類型

VT \_ I4

## <a name="remarks"></a>備註

在受限制和不受限制的 VBR 中，此值是橫跨內容持續時間的平均位元速率。

您必須為兩個雙通路的 VBR 編碼模式設定這個值。 開始處理範例之後，必須等到您完成串流的編碼之後，才能查詢此值。 編碼器會將此值的要求解讀為編碼會話結束的信號;您處理的下一個範例會被視為新會話的開頭。

您也可以在1遍的 VBR 編碼會話結束時讀取這個屬性。

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

 

 




