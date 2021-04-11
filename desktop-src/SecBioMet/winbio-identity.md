---
title: 'WINBIO_IDENTITY 結構 (Winbio \_ 類型 .h) '
description: 包含與生物識別範本相關聯的識別值。
ms.assetid: 58a5f4ba-2f58-466c-90fd-9480c3c095db
keywords:
- WINBIO_IDENTITY 結構 Windows 生物特徵辨識架構 API
topic_type:
- apiref
api_name:
- WINBIO_IDENTITY
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8092754b9107029e0be5800bbd5bc98bc3efb91c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103997"
---
# <a name="winbio_identity-structure"></a>WINBIO \_ 識別結構

**WINBIO \_ 識別** 結構包含與生物特徵辨識範本相關聯的識別值。

## <a name="syntax"></a>語法


```C++
typedef struct _WINBIO_IDENTITY {
  WINBIO_IDENTITY_TYPE Type;
  union {
    ULONG  Null;
    ULONG  Wildcard;
    GUID   TemplateGuid;
    struct {
      ULONG Size;
      UCHAR Data[SECURITY_MAX_SID_SIZE];
    } AccountSid;
  } Value;
} WINBIO_IDENTITY;
```



## <a name="members"></a>成員

<dl> <dt>

**型別**
</dt> <dd>

指定此結構中所包含之身分識別資訊的格式。 這個值可以是下列其中一個值：



| 值                                                                                                                                                                                         | 意義                                                                         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <dt>**WINBIO \_ 識別碼 \_ 類型 \_ Null**</dt> </dl>             | 範本沒有相關聯的識別碼。<br/>                                   |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <dt>**WINBIO \_ ID \_ 類型 \_ 萬用字元**</dt> </dl> | 結構符合所有範本識別。<br/>                       |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <dt>**WINBIO \_ 識別碼 \_ 類型 \_ GUID**</dt> </dl>             | 結構包含與範本相關聯的 GUID。<br/>          |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <dt>**WINBIO \_ 識別碼 \_ 類型 \_ SID**</dt> </dl>                | 結構包含與範本相關聯的帳戶 SID。<br/> |



 

</dd> <dt>

**值**
</dt> <dd>

可以包含下列其中一個值的聯集：

<dl> <dt>

**Null**
</dt> <dd>

如果 **類型** 成員是 **WINBIO \_ 識別碼 \_ 型別 \_ 為 Null**，則會包含1。

</dd> <dt>

**通 配 符**
</dt> <dd>

如果 **類型** 成員是 **WINBIO \_ 識別碼 \_ 類型 \_ 萬用字元**，則包含1。

</dd> <dt>

**TemplateGuid**
</dt> <dd>

包含128位 GUID 值，如果 **類型** 成員是 **WINBIO \_ 識別碼 \_ 型別 \_ guid**，則會識別範本。

</dd> <dt>

**AccountSid**
</dt> <dd>

結構，如果 **類型** 成員是 **WINBIO \_ 識別碼 \_ 類型 \_ sid**，則包含帳戶 SID。

<dl> <dt>

**大小**
</dt> <dd>

SID 中的字元數。

</dd> <dt>

**資料**
</dt> <dd>

包含 SID 的不帶正負號字元陣列。 陣列目前的大小上限為68個字元。

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>備註

下列函式會使用此結構：

-   [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)
-   [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)
-   [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)
-   [**WinBioGetCredentialState**](/windows/desktop/api/Winbio/nf-winbio-winbiogetcredentialstate)
-   [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)
-   [**WinBioRemoveCredential**](/windows/desktop/api/Winbio/nf-winbio-winbioremovecredential)
-   [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify)
-   [**WinBioVerifyWithCallback**](/windows/desktop/api/Winbio/nf-winbio-winbioverifywithcallback)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式結構](client-application-structures.md)
</dt> </dl>

 

 





