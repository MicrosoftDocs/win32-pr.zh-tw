---
description: CAPICOM \_ 憑證 \_ 尋找 \_ 類型列舉類型會定義用來尋找特定憑證的搜尋準則類型。 此列舉類型是在 CAPICOM 2.0 中引進。
ms.assetid: d71436e5-d921-4b84-8028-301d8fc4aedb
title: 'CAPICOM_CERTIFICATE_FIND_TYPE 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_FIND_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: c5c867b230ba2045d97619d7f55e257bd7803b74
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982932"
---
# <a name="capicom_certificate_find_type-enumeration"></a>CAPICOM \_ 憑證 \_ 尋找 \_ 類型列舉

**CAPICOM \_ 憑證 \_ 尋找 \_ 類型** 列舉類型會定義用來尋找特定憑證的搜尋準則類型。 此列舉類型是在 CAPICOM 2.0 中引進。

## <a name="members"></a>成員



| member                                                | 描述                                                                                                                                 | 值 |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ 憑證 \_ 尋找 \_ SHA1 \_ 雜湊**            | 傳回符合指定之 SHA1 雜湊的憑證。<br/>                                                                             | 0     |
| **CAPICOM \_ 憑證 \_ 尋找 \_ 主體 \_ 名稱**         | 傳回主體名稱完全或部分符合指定主體名稱的憑證。<br/>                                   | 1     |
| **CAPICOM \_ 憑證 \_ 尋找 \_ 簽發者 \_ 名稱**          | 傳回簽發者名稱完全或部分符合指定簽發者名稱的憑證。<br/>                                     | 2     |
| **CAPICOM \_ 憑證 \_ 尋找 \_ 根 \_ 名稱**            | 傳回根主體名稱完全或部分符合指定之根主體名稱的憑證。<br/>                         | 3     |
| **CAPICOM \_ 憑證 \_ 尋找 \_ 範本 \_ 名稱**        | 傳回範本名稱符合指定範本名稱的憑證。<br/>                                                      | 4     |
| **CAPICOM \_ 憑證 \_ 尋找 \_ 延伸模組**             | 傳回副檔名符合指定副檔名的憑證。<br/>                                                  | 5     |
| **CAPICOM \_ 憑證 \_ 尋找 \_ 擴充 \_ 屬性**    | 傳回具有擴充屬性的憑證，其屬性識別碼符合指定的屬性識別碼。<br/>           | 6     |
| **CAPICOM \_ 憑證 \_ 尋找 \_ 應用程式 \_ 原則**   | 傳回存放區中的憑證，其中包含增強金鑰使用方法擴充功能或屬性（property）與使用識別碼合併。<br/> | 7     |
| **CAPICOM \_ 憑證 \_ 尋找 \_ 憑證 \_ 原則**   | 傳回包含指定之原則 OID 的憑證。<br/>                                                                          | 8     |
| **CAPICOM \_ 憑證 \_ 尋找 \_ 時間 \_ 有效**           | 傳回時間有效的憑證。<br/>                                                                                        | 9     |
| **CAPICOM \_ 憑證 \_ 尋找 \_ 時間 \_ 尚未 \_ \_ 生效** | 傳回時間尚未生效的憑證。<br/>                                                                                | 10    |
| **CAPICOM \_ 憑證 \_ 尋找 \_ 時間已 \_ 過期**         | 傳回時間已過期的憑證。<br/>                                                                                     | 11    |
| **CAPICOM \_ 憑證 \_ 尋找 \_ 金鑰 \_ 使用方式**            | 傳回包含金鑰的憑證，可使用指定的方式來使用。<br/>                                                  | 12    |



## <a name="remarks"></a>備註

**CAPICOM \_ 憑證 \_ 尋找 \_ 類型** 列舉類型是由 certificate [**. find**](certificates-find.md)方法所使用。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|--------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本<br/>                |
| 標頭<br/>          | <dl> <dt>Capicom</dt> </dl> |



 

 




