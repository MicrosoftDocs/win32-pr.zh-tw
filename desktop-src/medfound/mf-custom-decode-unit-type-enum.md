---
description: 指定 IMFSample 在 MFSampleExtension ForwardedDecodeUnits 集合中包含的單位類型 \_ 。
ms.assetid: B74890ED-9586-475B-8C77-457ECB893980
title: 'MF_CUSTOM_DECODE_UNIT_TYPE 列舉 (Mfapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_CUSTOM_DECODE_UNIT_TYPE
api_type:
- HeaderDef
api_location:
- mfapi.h
ms.openlocfilehash: 97dd001cfb83f6ffec07035b77558fee591599b087e30dd3b819963db1b70405
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119104984"
---
# <a name="mf_custom_decode_unit_type-enumeration"></a>MF \_ 自訂解碼 \_ \_ 單位 \_ 類型列舉

指定 [**IMFSample**](/windows/desktop/api/mfobjects/nn-mfobjects-imfsample) 在 [MFSampleExtension \_ ForwardedDecodeUnits](mfsampleextension-forwardeddecodeunits.md) 集合中包含的單位類型。

## <a name="members"></a>成員



| member                    | 描述                                                             | 值 |
|---------------------------|-------------------------------------------------------------------------|-------|
| **MF \_ 解碼 \_ 單位 \_ NAL** | 單位類型是網路抽象層單位， (NALU) 。 <br/>     | 0     |
| **MF \_ 解碼 \_ 單位 \_ SEI** | 單位類型為補充增強資訊 (SEI) 。<br/> | 1     |



## <a name="remarks"></a>備註

## <a name="requirements"></a>需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                               |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



 

 




