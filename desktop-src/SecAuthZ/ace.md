---
description: 列出目前定義的 ACE 類型。
ms.assetid: 980b8242-2ba2-469f-b834-da7d3fb22e14
title: 'ACE (Winnt. h) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afa93490c4cf74ac33e3b15eeb888f011f81aa2b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122470984"
---
# <a name="ace"></a>ACE

**ACE** 是 [*存取控制清單*](/windows/desktop/SecGloss/a-gly)中 (ACL) 的 [*存取控制專案*](/windows/desktop/SecGloss/a-gly)。

下表列出目前定義的 **ACE** 類型。




| ACE 類型 | 結構 | ACL 類型 | 
|----------|-----------|----------|
| <ul><li>允許存取</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace"><strong>ACCESS_ALLOWED_ACE</strong></a> | 酌情 | 
| <ul><li>允許存取</li><li>允許在存取檢查期間回呼</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_ace"><strong>ACCESS_ALLOWED_CALLBACK_ACE</strong></a> | 酌情 | 
| <ul><li>允許存取</li><li>物件特定</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_object_ace"><strong>ACCESS_ALLOWED_OBJECT_ACE</strong></a> | 酌情 | 
| <ul><li>允許存取</li><li>物件特定</li><li>允許在存取檢查期間回呼</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_allowed_callback_object_ace"><strong>ACCESS_ALLOWED_CALLBACK_OBJECT_ACE</strong></a> | 酌情 | 
| <ul><li>拒絕存取</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_ace"><strong>ACCESS_DENIED_ACE</strong></a> | 酌情 | 
| <ul><li>拒絕存取</li><li>允許在存取檢查期間回呼</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_ace"><strong>ACCESS_DENIED_CALLBACK_ACE</strong></a> | 酌情 | 
| <ul><li>拒絕存取</li><li>物件特定</li><li>允許在存取檢查期間回呼</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_callback_object_ace"><strong>ACCESS_DENIED_CALLBACK_OBJECT_ACE</strong></a> | 酌情 | 
| <ul><li>拒絕存取</li><li>物件特定</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-access_denied_object_ace"><strong>ACCESS_DENIED_OBJECT_ACE</strong></a> | 酌情 | 
| <ul><li>系統警示</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_ace"><strong>SYSTEM_ALARM_ACE</strong></a> | 系統 | 
| <ul><li>系統警示</li><li>允許在存取檢查期間回呼</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_ace"><strong>SYSTEM_ALARM_CALLBACK_ACE</strong></a> | 系統 | 
| <ul><li>系統警示</li><li>物件特定</li><li>允許在存取檢查期間回呼</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_callback_object_ace"><strong>SYSTEM_ALARM_CALLBACK_OBJECT_ACE</strong></a> | 系統 | 
| <ul><li>系統警示</li><li>物件特定</li></ul> | <a href="/windows/desktop/api/winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_ALARM_OBJECT_ACE</strong></a> | 系統 | 
| <ul><li>系統審核</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_ace"><strong>SYSTEM_AUDIT_ACE</strong></a> | 系統 | 
| <ul><li>系統審核</li><li>允許在存取檢查期間回呼</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_ace"><strong>SYSTEM_AUDIT_CALLBACK_ACE</strong></a> | 系統 | 
| <ul><li>系統審核</li><li>物件特定</li><li>允許在存取檢查期間回呼</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_audit_callback_object_ace"><strong>SYSTEM_AUDIT_CALLBACK_OBJECT_ACE</strong></a> | 系統 | 
| <ul><li>系統審核</li><li>物件特定</li></ul> | <a href="/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace"><strong>SYSTEM_AUDIT_OBJECT_ACE</strong></a> | 系統 | 




 

目前不支援系統警示和物件特定的系統警示 Ace。

> [!Note]  
> 每個 ACE 的開頭都是 [**ace \_ 標頭**](/windows/desktop/api/Winnt/ns-winnt-ace_header) 結構。 標頭之後的資料格式會根據標頭中指定的 ACE 類型而有所不同。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>Winnt (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AddAce**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-addace)
</dt> <dt>

[**存取 \_ 允許的 \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_allowed_ace)
</dt> <dt>

[**\_拒絕存取 \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-access_denied_ace)
</dt> <dt>

[**ACL**](/windows/desktop/api/Winnt/ns-winnt-acl)
</dt> <dt>

[**系統 \_ 警報 \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-system_alarm_object_ace)
</dt> <dt>

[**系統 \_ AUDIT \_ ACE**](/windows/desktop/api/Winnt/ns-winnt-system_audit_ace)
</dt> </dl>

