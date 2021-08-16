---
title: " (Snmp 的 PDU 類型值) "
description: Pdu 類型值會用在 PDU 的 [pdu \_ 類型] 欄位中，以描述其類型。
ms.assetid: 9d7a3f1c-7940-428b-a4e0-3c9e61dd755f
topic_type:
- apiref
api_name:
- SNMP_PDU_GET
- SNMP_PDU_GETNEXT
- SNMP_PDU_RESPONSE
- SNMP_PDU_SET
- SNMP_PDU_V1TRAP
- SNMP_PDU_GETBULK
- SNMP_PDU_INFORM
- SNMP_PDU_TRAP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e9346c313efccda6d3635da51919f52fae37dd901cc73cf1f119bffdf9c22c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009206"
---
# <a name="pdu-type-values"></a>PDU 類型值

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用[Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 Microsoft 對 ws-atomictransaction 的實。\]

Pdu 類型值會用在 PDU 的 [ **pdu \_ 類型** ] 欄位中，以描述其類型。



| 常數                                                                                                                                                                   | 描述                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_PDU_GET"></span><span id="snmp_pdu_get"></span><dl> <dt>**SNMP \_ PDU \_ GET**</dt> </dl>                | 搜尋並從指定的 SNMP 變數取得值。<br/>                                       |
| <span id="SNMP_PDU_GETNEXT"></span><span id="snmp_pdu_getnext"></span><dl> <dt>**SNMP \_ PDU \_ GETNEXT**</dt> </dl>    | 搜尋並取出 SNMP 變數的值，而不知道變數的確切名稱。<br/> |
| <span id="SNMP_PDU_RESPONSE"></span><span id="snmp_pdu_response"></span><dl> <dt>**SNMP \_ PDU \_ 回應**</dt> </dl> | 回復 SNMP \_ pdu \_ 取得或 snmp \_ pdu \_ GETNEXT 要求。<br/>                                      |
| <span id="SNMP_PDU_SET"></span><span id="snmp_pdu_set"></span><dl> <dt>**SNMP \_ PDU \_ 設定**</dt> </dl>                | 將值儲存在指定的 SNMP 變數中。<br/>                                                       |
| <span id="SNMP_PDU_V1TRAP"></span><span id="snmp_pdu_v1trap"></span><dl> <dt>**SNMP \_ PDU \_ V1TRAP**</dt> </dl>       | 指出 PDU 設陷格式化以符合 SNMPv1 標準。<br/>                     |
| <span id="SNMP_PDU_GETBULK"></span><span id="snmp_pdu_getbulk"></span><dl> <dt>**SNMP \_ PDU \_ GETBULK**</dt> </dl>    | 使用單一要求來搜尋和取出多個值。<br/>                                        |
| <span id="SNMP_PDU_INFORM"></span><span id="snmp_pdu_inform"></span><dl> <dt>**SNMP \_ PDU \_ 通知**</dt> </dl>       | 表示通知要求 PDU。<br/>                                                                  |
| <span id="SNMP_PDU_TRAP"></span><span id="snmp_pdu_trap"></span><dl> <dt>**SNMP \_ PDU \_ 陷阱**</dt> </dl>             | 警示管理系統在 SNMPv2C 下的特殊事件。<br/>                             |



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
</dt> <dt>

[SNMP 常數](snmp-constants.md)
</dt> </dl>

 

