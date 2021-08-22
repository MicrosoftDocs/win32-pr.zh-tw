---
title: 'MPFASTPATH_DATA 結構 (MpClient .h) '
description: FastPath 更新通知。
ms.assetid: E19F153D-DD46-4E27-9A4B-33586794DAC2
keywords:
- MPFASTPATH_DATA 結構舊版 Windows 環境功能
- PMPFASTPATH_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPFASTPATH_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e138e9c45657cfc4ebeba1d1dbeed38070b6e07d09c512ec96835a04702d0c8a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119556148"
---
# <a name="mpfastpath_data-structure"></a>MPFASTPATH \_ 資料結構

FastPath 更新通知。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPFASTPATH_DATA {
  MP_SIGNATURE_TYPE         SignatureType;
  MP_FASTPATH_TYPE          FastPathSignatureType;
  MP_MIDL_STRING LPWSTR     FastPathSignatureVersion;
  ULARGE_INTEGER            CompilationTimestamp;
  MP_PERSISTENCE_LIMIT_TYPE PersistenceType;
  MP_MIDL_STRING LPWSTR     PersistenceValue;
  MP_MIDL_STRING LPWSTR     PersistencePath;
  MP_REMOVAL_REASON         Reason;
} MPFASTPATH_DATA, *PMPFASTPATH_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**SignatureType**
</dt> <dd>

Type： **[ **MP \_ SIGNATURE \_ TYPE**](mp-signature-type.md)**

</dd> <dd>

簽章類型。

</dd> <dt>

**FastPathSignatureType**
</dt> <dd>

類型： **[ **MP \_ FASTPATH \_ 類型**](mp-fastpath-type.md)**

</dd> <dd>

FastPath 簽章類型。

</dd> <dt>

**FastPathSignatureVersion**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

FastPath 簽章版本 (選擇性) 。

</dd> <dt>

**CompilationTimestamp**
</dt> <dd>

類型： **ULARGE \_ 整數**

</dd> <dd>

編譯 timestamp (UTC) 。

</dd> <dt>

**PersistenceType**
</dt> <dd>

類型： **[ **MP \_ 持續性 \_ 限制 \_ 類型**](mp-persistence-limit-type.md)**

</dd> <dd>

持續性類型 (選擇性) 。

</dd> <dt>

**PersistenceValue**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

持續性值 (選擇性) 。

</dd> <dt>

**PersistencePath**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

持續性路徑 (選擇性) 。

</dd> <dt>

**原因**
</dt> <dd>

類型： **[ **MP \_ 移除 \_ 原因**](mp-removal-reason.md)**

</dd> <dd>

移除簽章的原因。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MP \_ FASTPATH \_ 類型**](mp-fastpath-type.md)
</dt> <dt>

[**MP \_ 持續性 \_ 限制 \_ 類型**](mp-persistence-limit-type.md)
</dt> <dt>

[**MP \_ SIGNATURE \_ 類型**](mp-signature-type.md)
</dt> </dl>

 

 





