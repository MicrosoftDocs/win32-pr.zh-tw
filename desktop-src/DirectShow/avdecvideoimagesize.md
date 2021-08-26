---
description: 取得已解碼影像的大小（以圖元為單位）。
ms.assetid: 2F0DD10F-CF7A-4A6F-91A9-E3828DF2B947
title: 'AVDecVideoImageSize 屬性 (Codecapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba4c059dfb1b2aebad4da10e54a3ecc1224a00d9cffcdb13dc7c87f4e29d4e83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000188"
---
# <a name="avdecvideoimagesize-property"></a>AVDecVideoImageSize 屬性

取得已解碼影像的大小（以圖元為單位）。

這是唯讀的屬性。

## <a name="data-type"></a>資料類型

**UINT32** (**VT \_ UI4**) 

## <a name="property-guid"></a>屬性 GUID

**CODECAPI \_ AVDecVideoImageSize**

## <a name="property-value"></a>屬性值

高16位包含寬度，而低16位則包含高度。

## <a name="remarks"></a>備註

通道數目包含 (LFE) 通道的低頻率效果（如果有的話）。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[ 桌面應用程式 \| UWP 應用程式\]<br/>                     |
| 最低支援的伺服器<br/> | Windows 2000 Server \[ desktop apps \| UWP 應用程式\]<br/>                           |
| 標頭<br/>                   | <dl> <dt>Codecapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[編解碼器 API 屬性](codec-api-properties.md)
</dt> <dt>

[**ICodecAPI 介面**](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




