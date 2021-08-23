---
title: 'SNMP 錯誤碼 (Snmp. h) '
description: Microsoft 會實行 SNMPv2C 規格所定義的下列 SNMP 錯誤碼。
ms.assetid: 7e7e2bc0-a058-4853-b736-1946e64a0c4a
topic_type:
- apiref
api_name:
- SNMP_ERRORSTATUS_NOERROR
- SNMP_ERRORSTATUS_TOOBIG
- SNMP_ERRORSTATUS_NOSUCHNAME
- SNMP_ERRORSTATUS_BADVALUE
- SNMP_ERRORSTATUS_READONLY
- SNMP_ERRORSTATUS_GENERR
- SNMP_ERRORSTATUS_NOACCESS
- SNMP_ERRORSTATUS_WRONGTYPE
- SNMP_ERRORSTATUS_WRONGLENGTH
- SNMP_ERRORSTATUS_WRONGENCODING
- SNMP_ERRORSTATUS_WRONGVALUE
- SNMP_ERRORSTATUS_NOCREATION
- SNMP_ERRORSTATUS_INCONSISTENTVALUE
- SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE
- SNMP_ERRORSTATUS_COMMITFAILED
- SNMP_ERRORSTATUS_UNDOFAILED
- SNMP_ERRORSTATUS_AUTHORIZATIONERROR
- SNMP_ERRORSTATUS_NOTWRITABLE
- SNMP_ERRORSTATUS_INCONSISTENTNAME
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583394dfc3093f4f0d5cf3d7c7cef68d7ff6d57930e3abf957d857defec227c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119008926"
---
# <a name="snmp-error-codes"></a>SNMP 錯誤碼

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用[Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 Microsoft 對 ws-atomictransaction 的實。\]

Microsoft 會實行 SNMPv2C 規格所定義的下列 SNMP 錯誤碼。



| 常數/值                                                                                                                                                                                                                                                                              | 描述                                                                                                                                                    |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_ERRORSTATUS_NOERROR"></span><span id="snmp_errorstatus_noerror"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ >aad-userreadusingalternativesecurityid-noerror**</dt> <dt>0</dt> </dl>                                      | 代理程式報告傳輸期間未發生任何錯誤。<br/>                                                                                      |
| <span id="SNMP_ERRORSTATUS_TOOBIG"></span><span id="snmp_errorstatus_toobig"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ TOOBIG**</dt> <dt>1</dt> </dl>                                         | 代理程式無法將要求的 SNMP 操作的結果放在單一 SNMP 訊息中。<br/>                                                     |
| <span id="SNMP_ERRORSTATUS_NOSUCHNAME"></span><span id="snmp_errorstatus_nosuchname"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ NOSUCHNAME**</dt> <dt>2</dt> </dl>                             | 要求的 SNMP 作業識別未知的變數。<br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_BADVALUE"></span><span id="snmp_errorstatus_badvalue"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ BADVALUE**</dt> <dt>3</dt> </dl>                                   | 要求的 SNMP 操作嘗試變更變數，但卻指定了語法或值錯誤。<br/>                                            |
| <span id="SNMP_ERRORSTATUS_READONLY"></span><span id="snmp_errorstatus_readonly"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ READONLY**</dt> <dt>4</dt> </dl>                                   | 要求的 SNMP 操作嘗試根據變數的社區設定檔變更不允許變更的變數。<br/>         |
| <span id="SNMP_ERRORSTATUS_GENERR"></span><span id="snmp_errorstatus_generr"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ GENERR**</dt> <dt>5</dt> </dl>                                         | 在要求的 SNMP 作業期間，此處所列的錯誤除外。<br/>                                                          |
| <span id="SNMP_ERRORSTATUS_NOACCESS"></span><span id="snmp_errorstatus_noaccess"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ NOACCESS**</dt> <dt>6</dt> </dl>                                   | 無法存取指定的 SNMP 變數。<br/>                                                                                                      |
| <span id="SNMP_ERRORSTATUS_WRONGTYPE"></span><span id="snmp_errorstatus_wrongtype"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ WRONGTYPE**</dt> <dt>7</dt> </dl>                                | 值指定的類型與變數所需的類型不一致。<br/>                                                            |
| <span id="SNMP_ERRORSTATUS_WRONGLENGTH"></span><span id="snmp_errorstatus_wronglength"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ WRONGLENGTH**</dt> <dt>8</dt> </dl>                          | 值指定的長度與變數所需的長度不一致。<br/>                                                        |
| <span id="SNMP_ERRORSTATUS_WRONGENCODING"></span><span id="snmp_errorstatus_wrongencoding"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ WRONGENCODING**</dt> <dt>9</dt> </dl>                    | 值包含抽象語法標記法 (一)  (asn.1) 編碼，與欄位的 asn.1 標記不一致。<br/>                           |
| <span id="SNMP_ERRORSTATUS_WRONGVALUE"></span><span id="snmp_errorstatus_wrongvalue"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ WRONGVALUE**</dt> <dt>10</dt> </dl>                            | 無法將值指派給變數。<br/>                                                                                                       |
| <span id="SNMP_ERRORSTATUS_NOCREATION"></span><span id="snmp_errorstatus_nocreation"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ NOCREATION**</dt> <dt>11</dt> </dl>                            | 變數不存在，且代理程式無法建立該變數。<br/>                                                                                        |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTVALUE"></span><span id="snmp_errorstatus_inconsistentvalue"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ INCONSISTENTVALUE**</dt> <dt>12</dt> </dl>       | 值與其他 managed 物件的值不一致。<br/>                                                                                     |
| <span id="SNMP_ERRORSTATUS_RESOURCEUNAVAILABLE"></span><span id="snmp_errorstatus_resourceunavailable"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ RESOURCEUNAVAILABLE**</dt> <dt>13</dt> </dl> | 將值指派給變數需要配置目前無法使用的資源。<br/>                                                |
| <span id="SNMP_ERRORSTATUS_COMMITFAILED"></span><span id="snmp_errorstatus_commitfailed"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ COMMITFAILED**</dt> <dt>14</dt> </dl>                      | 未發生任何驗證錯誤，但未更新任何變數。<br/>                                                                                       |
| <span id="SNMP_ERRORSTATUS_UNDOFAILED"></span><span id="snmp_errorstatus_undofailed"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ UNDOFAILED**</dt> <dt>15</dt> </dl>                            | 未發生任何驗證錯誤。 有些變數因為無法復原其指派而更新。<br/>                                    |
| <span id="SNMP_ERRORSTATUS_AUTHORIZATIONERROR"></span><span id="snmp_errorstatus_authorizationerror"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ AUTHORIZATIONERROR**</dt> <dt>16</dt> </dl>    | 發生授權錯誤。<br/>                                                                                                                    |
| <span id="SNMP_ERRORSTATUS_NOTWRITABLE"></span><span id="snmp_errorstatus_notwritable"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ NOTWRITABLE**</dt> <dt>17</dt> </dl>                         | 變數存在，但代理程式無法修改它。<br/>                                                                                                 |
| <span id="SNMP_ERRORSTATUS_INCONSISTENTNAME"></span><span id="snmp_errorstatus_inconsistentname"></span><dl> <dt>**SNMP \_ERRORSTATUS \_ INCONSISTENTNAME**</dt> <dt>18</dt> </dl>          | 變數不存在;因為命名物件實例與其他 managed 物件的值不一致，所以代理程式無法建立該代理程式。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                        |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Snmp。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Simple Network Management Protocol (SNMP) 概觀](simple-network-management-protocol-snmp-.md)
</dt> <dt>

[SNMP 參考](snmp-reference.md)
</dt> </dl>

 

