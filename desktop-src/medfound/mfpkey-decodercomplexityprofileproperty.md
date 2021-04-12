---
description: 指定編碼內容的複雜性設定檔。
ms.assetid: 2e238d31-98b2-4c79-96b0-9e6949010a73
title: 'MFPKEY_DECODERCOMPLEXITYPROFILE 屬性 (Wmcodecdsp) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39544830a0a05e21779a637da61d3bcb310fcd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848819"
---
# <a name="mfpkey_decodercomplexityprofile-property"></a>MFPKEY \_ DECODERCOMPLEXITYPROFILE 屬性

指定編碼內容的複雜性設定檔。

## <a name="constant-for-ipropertybag"></a>IPropertyBag 的常數

g \_ wszWMVCDecoderComplexityProfile

## <a name="data-type"></a>資料類型

**VT \_ BSTR**

## <a name="remarks"></a>備註

只有在編碼完成後，您才可以讀取此值。

若為音訊，這個屬性會有下列其中一個值。



| 值 | 描述                                                                                    |
|-------|------------------------------------------------------------------------------------------------|
| L1  | 取樣率為 44.1 KHz 且最大位元速率為 161 Kbps 的標準編碼。         |
| L2  | 使用取樣率的標準編碼，最高可達 48 KHz，最大位元速率為 161 Kbps。         |
| L3  | 使用取樣率的標準編碼，最高可達 48 KHz，最大位元速率為 385 Kbps。         |
| "M0a" | 使用取樣率的專業編碼，最高可達48到 192 Kbps 之間的 48 KHz 和位元速率。  |
| "M0b" | 具有最高 48 KHz 和最大位元速率為 192 Kbps 之取樣率的專業編碼。      |
| M1  | 具有最高 48 KHz 和最大位元速率為 384 Kbps 之取樣率的專業編碼。      |
| M2  | 具有最高 96 KHz 和最大位元速率為 768 Kbps 之取樣率的專業編碼。      |
| M3  | 具有最高 96 KHz 和最大位元速率為 1.5 Mbps 之取樣率的專業編碼。      |
| N1  | 使用取樣率的無失真編碼，最高可達 48 KHz，最多2個通道。                |
| N2  | 使用取樣率高達 96 KHz 的無失真編碼，以及最多6個通道 (5.1 環繞) 。 |
| N3  | 使用取樣率高達 96 KHz 的無失真編碼，以及最多8個通道 (7.1 環繞) 。 |



 

針對影片，此屬性具有下列其中一個值：



| 值 | 描述                                                                       |
|-------|-----------------------------------------------------------------------------------|
| AP  | advanced profile (僅適用于 Windows Media 視訊 9 Advanced Profile 編解碼器)  |
| CP  | 不再支援                                                               |
| 多功能  | 主要設定檔                                                                      |
| SP-1  | 簡單設定檔                                                                    |



 

針對影片內容，您可以在開始編碼之前，先設定 [MFPKEY \_ DECODERCOMPLEXITYREQUESTED](mfpkey-decodercomplexityrequestedproperty.md) 來要求設定檔層級。 編解碼器會嘗試在要求的複雜性層級的參數內進行編碼，但您設定的其他設定將會優先使用。 在編碼之後，您應該一律檢查實際的複雜性設定檔值，以免無法接受您的要求。

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

 

 




