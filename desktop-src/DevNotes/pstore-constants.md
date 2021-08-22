---
description: PStore 會使用下列常數。
ms.assetid: 4bdccb86-2e0e-461c-9a74-184861b7db1e
title: 'PStore 常數 (Pstore) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_E_OK
- PST_E_TYPE_EXISTS
- PST_AUTHENTICODE
- PST_BINARY_CHECK
- PST_SECURITY_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 69a82241e8f270389c5385143e83973d380f5671e30e2086749a75c984670cf0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119386038"
---
# <a name="pstore-constants"></a>PStore 常數

\[受保護的儲存體 (Pstore) 可在 Windows 伺服器2003和 Windows XP 中使用。 它僅適用于 Windows Server 2008 和 Windows Vista 中的唯讀作業，但在後續版本中可能無法使用。 Pstore 會使用較舊的資料保護執行。 強烈建議您使用 [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) 和 [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) 函數所提供的更強資料保護。\]

PStore 會使用下列常數。

受保護的儲存體錯誤碼



| 常數/值                                                                                                                                                                                                                               | 描述                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| <span id="PST_E_OK"></span><span id="pst_e_ok"></span><dl> <dt>**PST \_E \_ OK**</dt> <dt>0x00000000L</dt> </dl>                             | 作業成功。<br/>                           |
| <span id="PST_E_TYPE_EXISTS"></span><span id="pst_e_type_exists"></span><dl> <dt>**PST \_E \_ 類型 \_ 存在**</dt> <dt>0x800C0004L</dt> </dl> | 資料項目目已存在於受保護的儲存體中。 <br/> |



存取子句值



| 常數/值                                                                                                                                                                                                                                      | 描述                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PST_AUTHENTICODE"></span><span id="pst_authenticode"></span><dl> <dt>**PST \_AUTHENTICODE**</dt> <dt>1</dt> </dl>                       | 指向 [**PST \_ AUTHENTICODEDATA**](pst-authenticodedata.md) 結構。<br/> |
| <span id="PST_BINARY_CHECK_"></span><span id="pst_binary_check_"></span><dl> <dt> **PST \_ 二進位 \_ 檢查**</dt> <dt>2</dt> </dl>                   | 指向 **PST \_ BINARYCHECKDATA** 結構。<br/>                              |
| <span id="PST_SECURITY_DESCRIPTOR"></span><span id="pst_security_descriptor"></span><dl> <dt>**PST \_安全 \_ 描述項**</dt> <dt>4</dt> </dl> | 指向有效的 Windows 安全描述項。 <br/>                              |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Pstore。h</dt> </dl> |



 

 
