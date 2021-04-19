---
description: 包含訊息驗證碼 (MAC) 。
ms.assetid: be5515fd-1936-46b8-9fc8-8d1f87048c38
title: 'D3D_OMAC 結構 (D3d9types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3D_OMAC
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 21c710b21c31147f7208ddd1637426aeafb60234
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971984"
---
# <a name="d3d_omac-structure"></a>D3D \_ OMAC 結構

包含訊息驗證碼 (MAC) 。

## <a name="syntax"></a>語法


```C++
typedef struct _D3D_OMAC {
  BYTE Omac[D3D_OMAC_SIZE];
} D3D_OMAC;
```



## <a name="members"></a>成員

<dl> <dt>

**Omac**
</dt> <dd>

位元組陣列，其中包含訊息的密碼編譯 MAC 值。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>D3d9types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 影片結構](direct3d-video-structures.md)
</dt> </dl>

 

 




