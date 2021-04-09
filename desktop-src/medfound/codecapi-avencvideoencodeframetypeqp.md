---
description: 指定 (I、P 或 B 的框架類型)  (已套用的) 的量化參數。
ms.assetid: 6331033F-7EEB-41B3-B166-29686D4AADB6
title: 'CODECAPI_AVEncVideoEncodeFrameTypeQP 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76e68e0cb6cbdc076dbf523f3ae9dfd7b5870f47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111860"
---
# <a name="codecapi_avencvideoencodeframetypeqp-property"></a>CODECAPI \_ AVEncVideoEncodeFrameTypeQP 屬性

指定 (I、P 或 B 的框架類型)  (已套用的) 的量化參數。

## <a name="data-type"></a>資料類型

**ULONGULONG** (VT \_ UI8) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoEncodeFrameTypeQP**

## <a name="remarks"></a>備註

針對不同的框架類型，支援設定量化參數 (QP) 的編碼器 (I、P、B) ，除了 [CODECAPI \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)之外，還應該公開此 API。 如果編碼器只針對所有框架類型支援單一的 QP，則只支援 CODECAPI \_ AVEncVideoEncodeQP。

這是動態編碼屬性，表示可以在編碼會話期間隨時設定新的值。

**H.264/AVC 編碼器：**

編碼器應支援 [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)、 [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)和 [**GetParameterRange**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)。

一組 4 16 位欄位是用來指定固定-QP 編碼的框架 QPs。 這些欄位包括：

-   **Bits 0-15：** 用於 I 框架的 QP，有效範圍為 \[ 0，51 \] 。
-   **Bits 16-31：** 用於 P 框架的 QP，有效範圍為 \[ 0，51 \] 。
-   **Bits 32-47：** 用於 B 框架、有效範圍 \[ 0、51的 QP\]
-   **Bits 48-63：** 已保留

當支援此 CodecAPI 時，編碼器應支援 I、P 和 B 的框架類型上的 QP 設定。

預設值應該是0x0000001a001a001a。 適用于 I、P 和 B 的 QP 等於26。

當 [CODECAPI \_ AVEncVideoSelectLayer](codecapi-avencvideoselectlayer.md) 選取特定的時態圖層時，CODECAPI AVEncVideoEncodeFrameTypeQP 的 [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue) \_ 應該在該時態圖層上為 I、P 和 B 框架設定 QP。 根據預設，它會在基底時態層時態圖層0上為 I、P 和 B 框架設定 QP。

[CODECAPI \_AVEncVideoMaxQP](codecapi-avencvideomaxqp.md) 和 [CODECAPI \_ AVEncVideoMinQP](codecapi-avencvideominqp.md) 應該用來定義和限制所有圖片類型、I、P 和 B QPs 的 QP 範圍。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                        |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎屬性](media-foundation-properties.md)
</dt> </dl>

 

