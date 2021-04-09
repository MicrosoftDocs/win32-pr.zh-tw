---
title: 'WINBIO_IDENTITY_TYPE 常數 (Winbio \_ 類型 .h) '
description: 指定 WINBIO 身分識別結構中所包含之身分識別資訊的格式 \_ 。
ms.assetid: 27A01538-9B26-4A29-8ADB-ED9C5D5808B3
topic_type:
- apiref
api_name:
- WINBIO_ID_TYPE_NULL
- WINBIO_ID_TYPE_WILDCARD
- WINBIO_ID_TYPE_GUID
- WINBIO_ID_TYPE_SID
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dad068c6838f0a3a675970b7c9359b12ea8faa2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934149"
---
# <a name="winbio_identity_type-constants"></a>WINBIO 身分 \_ 識別 \_ 類型常數

下列 **WINBIO \_ 識別 \_ 類型** 常數可用來指定 WINBIO 身分 [**\_ 識別**](winbio-identity.md) 結構中所包含之身分識別資訊的格式。



| 常數                                                                                                                                                                                      | 描述                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| <span id="WINBIO_ID_TYPE_NULL"></span><span id="winbio_id_type_null"></span><dl> <dt>**WINBIO \_ 識別碼 \_ 類型 \_ Null**</dt> </dl>             | 範本沒有相關聯的識別碼。 <br/>            |
| <span id="WINBIO_ID_TYPE_WILDCARD"></span><span id="winbio_id_type_wildcard"></span><dl> <dt>**WINBIO \_ ID \_ 類型 \_ 萬用字元**</dt> </dl> | 結構符合所有範本識別。<br/> |
| <span id="WINBIO_ID_TYPE_GUID"></span><span id="winbio_id_type_guid"></span><dl> <dt>**WINBIO \_ 識別碼 \_ 類型 \_ GUID**</dt> </dl>             | GUID 可識別範本。<br/>                |
| <span id="WINBIO_ID_TYPE_SID"></span><span id="winbio_id_type_sid"></span><dl> <dt>**WINBIO \_ 識別碼 \_ 類型 \_ SID**</dt> </dl>                | 帳戶 SID 會識別範本。<br/>        |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式常數](client-application-constants.md)
</dt> <dt>

[**WINBIO 身分 \_ 識別**](winbio-identity.md)
</dt> </dl>

 

 





