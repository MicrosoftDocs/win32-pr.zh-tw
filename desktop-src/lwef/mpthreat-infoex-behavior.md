---
title: 'MPTHREAT_INFOEX_BEHAVIOR 結構 (MpClient .h) '
description: 包含行為修改特定的資訊。
ms.assetid: 762E755F-5BA1-476D-B395-6617093309C5
keywords:
- MPTHREAT_INFOEX_BEHAVIOR 結構舊版 Windows 環境功能
- PMPTHREAT_INFOEX_BEHAVIOR 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPTHREAT_INFOEX_BEHAVIOR
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cb0bc00aeb56aec38b88f2590211c705079834f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686326"
---
# <a name="mpthreat_infoex_behavior-structure"></a>MPTHREAT \_ INFOEX \_ 行為結構

包含行為修改特定的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct tagMPTHREAT_INFOEX_BEHAVIOR {
  ULARGE_INTEGER         SignatureID;
  ULONGLONG              EngineVersion;
  ULONGLONG              ASDeltaSignatureVersion;
  ULONGLONG              AVDeltaSignatureVersion;
  MP_HASH_TYPE           HashType;
  DWORD                  FidelityValue;
  MP_MIDL_STRING  LPWSTR HashValue;
  MP_MIDL_STRING  LPWSTR TargetFileName;
  MP_MIDL_STRING  LPWSTR TargetFileHash;
} MPTHREAT_INFOEX_BEHAVIOR, *PMPTHREAT_INFOEX_BEHAVIOR;
```



## <a name="members"></a>成員

<dl> <dt>

**SignatureID**
</dt> <dd>

類型： **ULARGE \_ 整數**

</dd> <dd>

偵測時引擎提供的行為修改簽章識別碼。

</dd> <dt>

**EngineVersion**
</dt> <dd>

類型： **ULONGLONG**

</dd> <dd>

引擎模組版本。

</dd> <dt>

**ASDeltaSignatureVersion**
</dt> <dd>

類型： **ULONGLONG**

</dd> <dd>

防毒軟體簽章版本。

</dd> <dt>

**AVDeltaSignatureVersion**
</dt> <dd>

類型： **ULONGLONG**

</dd> <dd>

防毒軟體特徵碼版本

</dd> <dt>

**HashType**
</dt> <dd>

類型： **[ **MP \_ HASH \_ 類型**](mp-hash-type.md)**

</dd> <dd>

使用的雜湊類型。 請參閱 [**MP \_ HASH \_ 類型**](mp-hash-type.md)。

</dd> <dt>

**FidelityValue**
</dt> <dd>

類型： **DWORD**

</dd> <dd>

精確度值。

</dd> <dt>

**HashValue**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

檔案的雜湊。

</dd> <dt>

**TargetFileName**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

目標檔案的路徑和名稱。

</dd> <dt>

**TargetFileHash**
</dt> <dd>

類型： **MP \_ MIDL \_ STRING LPWSTR**

</dd> <dd>

目標檔案的雜湊。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>MpClient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MP \_ HASH \_ 類型**](mp-hash-type.md)
</dt> </dl>

 

 





