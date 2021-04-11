---
description: 指定編碼器所支援的最大參考框架。
ms.assetid: 023FD791-BD43-41F6-95D0-8BE800F51579
title: 'CODECAPI_AVEncVideoMaxNumRefFrame 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84e8f5a7794410012bd1a025e794e1fd23f4b332
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104116045"
---
# <a name="codecapi_avencvideomaxnumrefframe-property"></a>CODECAPI \_ AVEncVideoMaxNumRefFrame 屬性

指定編碼器所支援的最大參考框架。

## <a name="data-type"></a>資料類型

**ULONG** (VT \_ UI4) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVEncVideoMaxNumRefFrame**

## <a name="remarks"></a>備註

針對 h.264，這會對應至 h.264 規格中定義的 Sequence 參數 Set variable **max \_ num \_ ref \_ 框架** 。

**H.264/AVC 編碼器：**

編碼器可能會使用較少的參考框架，以遵守位流中指定的層級。

編碼器應支援 [**GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue)、 [**SetValue**](/windows/desktop/api/strmif/nf-strmif-icodecapi-setvalue)和 [**GetParameterRangee**](/windows/desktop/api/strmif/nf-strmif-icodecapi-getparameterrange)。

這是靜態屬性，表示只能在編碼會話開始之前設定。

建議的預設值為2。

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

 

