---
title: 'WINBIO_EXTENDED_ENROLLMENT_PARAMETERS 結構 (Winbio \_ adapter .h) '
description: 包含引擎介面卡建立註冊範本時所需的其他資訊。
ms.assetid: E8007316-0A9D-4F35-A266-273B2406D545
keywords:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS 結構 Windows 生物特徵辨識架構 API
- PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_EXTENDED_ENROLLMENT_PARAMETERS
api_location:
- Winbio_adapter.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b4f041d131bcee540a75a131b4179947fbe8e394
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464608"
---
# <a name="winbio_extended_enrollment_parameters-structure"></a>WINBIO \_ 延伸 \_ 註冊 \_ 參數結構

**WINBIO \_ 延伸 \_ 註冊 \_ 參數** 結構包含引擎介面卡建立註冊範本時所需的其他資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_EXTENDED_ENROLLMENT_PARAMETERS {
  SIZE_T                   Size;
  WINBIO_BIOMETRIC_SUBTYPE SubFactor;
} WINBIO_EXTENDED_ENROLLMENT_PARAMETERS, *PWINBIO_EXTENDED_ENROLLMENT_PARAMETERS;
```



## <a name="members"></a>成員

<dl> <dt>

**大小**
</dt> <dd>

**WINBIO \_ 延伸 \_ 註冊 \_ 參數** 結構的大小 (以位元組為單位) 。

</dd> <dt>

**SubFactor**
</dt> <dd>

其中一個 [**WINBIO \_ 生物特徵辨識 \_ 子類型常數**](winbio-biometric-subtype-constants.md) 值，可提供註冊的其他相關資訊。

</dd> </dl>

## <a name="remarks"></a>備註

Windows 生物特徵辨識架構在註冊作業期間，將此結構傳遞給 [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                                     |
| 標頭<br/>                   | <dl> <dt>Winbio \_ adapter .h (包括 Winbio \_ adapter .h) </dt> </dl> |



 

 





