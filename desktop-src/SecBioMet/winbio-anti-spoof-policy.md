---
title: 'WINBIO_ANTI_SPOOF_POLICY 結構 (Winbio \_ 類型 .h) '
description: 表示使用者的 lnk-antispoofing 原則。
ms.assetid: 2B433AE8-21A0-4AF1-853C-9074527DB2E4
keywords:
- WINBIO_ANTI_SPOOF_POLICY 結構 Windows 生物特徵辨識架構 API
- PWINBIO_ANTI_SPOOF_POLICY 結構指標 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3da8b7811afb1de1ad464675125f125ef0ceab73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465829"
---
# <a name="winbio_anti_spoof_policy-structure"></a>WINBIO \_ 反 \_ 詐騙 \_ 原則結構

表示使用者的 lnk-antispoofing 原則。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_ANTI_SPOOF_POLICY {
  WINBIO_ANTI_SPOOF_POLICY_ACTION Action;
  WINBIO_POLICY_SOURCE            Source;
} WINBIO_ANTI_SPOOF_POLICY, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="members"></a>成員

<dl> <dt>

**動作**
</dt> <dd>

要針對 lnk-antispoofing 原則採取的動作類型。

</dd> <dt>

**來源**
</dt> <dd>

Lnk-antispoofing 原則的來源。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                                                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2016 \[ desktop 應用程式\]<br/>                                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WINBIO \_ 反 \_ 詐騙 \_ 原則 \_ 動作**](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[**WINBIO \_ 原則 \_ 來源**](winbio-policy-source.md)
</dt> <dt>

[**WINBIO \_ 非同步 \_ 結果**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> <dt>

[**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)
</dt> </dl>

 

 





