---
title: 'WINBIO_VERSION 結構 (Winbio \_ 類型 .h) '
description: 包含生物特徵辨識服務提供者元件的軟體版本號碼。
ms.assetid: b9d08e10-00db-4f3f-9e27-6063aafa4151
keywords:
- WINBIO_VERSION 結構 Windows 生物特徵辨識架構 API
- PWINBIO_VERSION 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_VERSION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de81dd3da7f37e473a65caaf3e4cd52c8fd2f6732dced45f43245cb4e4c5c905
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909113"
---
# <a name="winbio_version-structure"></a>WINBIO \_ 版本結構

**WINBIO \_ 版本** 結構包含生物特徵辨識服務提供者元件的軟體版本號碼。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_VERSION {
  DWORD MajorVersion;
  DWORD MinorVersion;
} WINBIO_VERSION, *PWINBIO_VERSION;
```



## <a name="members"></a>成員

<dl> <dt>

**MajorVersion**
</dt> <dd>

包含主要版本號碼的 **DWORD** 。

</dd> <dt>

**MinorVersion**
</dt> <dd>

包含次要版本號碼的 **DWORD** 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式結構](client-application-structures.md)
</dt> <dt>

[**WINBIO \_ BSP \_ 架構**](winbio-bsp-schema.md)
</dt> <dt>

[**WINBIO \_ 單元 \_ 架構**](winbio-unit-schema.md)
</dt> </dl>

 

 





