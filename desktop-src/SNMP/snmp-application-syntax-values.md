---
title: 'Snmp 應用程式語法值 (Snmp. h) '
description: 使用 Microsoft SNMP 管理 API 的管理應用程式會使用 SNMP 應用程式語法值。
ms.assetid: fa269f97-f9d3-49f4-b29b-8c4d71f075d0
topic_type:
- apiref
api_name:
- ASN_IPADDRESS
- ASN_COUNTER32
- ASN_GAUGE32
- ASN_TIMETICKS
- ASN_OPAQUE
- ASN_COUNTER64
- ASN_UINTEGER32
- ASN_RFC2578_UNSIGNED32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 787723780d5920aafc3c37c40ea995a675943d1e45873d5f30cd8cebb77b5b64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119009026"
---
# <a name="snmp-application-syntax-values"></a>SNMP 應用程式語法值

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用[Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 Microsoft 對 ws-atomictransaction 的實。\]

使用 Microsoft SNMP 管理 API 的管理應用程式會使用 SNMP 應用程式語法值。



| 常數                                                                                                                                                                                  | 描述                                                                                                                      |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------|
| <span id="ASN_IPADDRESS"></span><span id="asn_ipaddress"></span><dl> <dt>**ASN \_ IPADDRESS**</dt> </dl>                             | 表示 IP 位址變數。<br/>                                                                                     |
| <span id="ASN_COUNTER32"></span><span id="asn_counter32"></span><dl> <dt>**ASN \_ COUNTER32**</dt> </dl>                             | 指出計數器變數。<br/>                                                                                         |
| <span id="ASN_GAUGE32"></span><span id="asn_gauge32"></span><dl> <dt>**ASN \_ GAUGE32**</dt> </dl>                                   | 表示量測計變數。 此變數描述項合 RFC 1902 的 Unsigned32 類型。<br/>                  |
| <span id="ASN_TIMETICKS"></span><span id="asn_timeticks"></span><dl> <dt>**ASN \_ TIMETICKS**</dt> </dl>                             | 表示 timeticks 變數。<br/>                                                                                       |
| <span id="ASN_OPAQUE"></span><span id="asn_opaque"></span><dl> <dt>**ASN 不 \_ 透明**</dt> </dl>                                      | 表示不透明的變數。<br/>                                                                                         |
| <span id="ASN_COUNTER64"></span><span id="asn_counter64"></span><dl> <dt>**ASN \_ COUNTER64**</dt> </dl>                             | 指出計數器變數，此變數會在到達 (2 ^ 64) -1 的最大值之前增加。<br/>                           |
| <span id="ASN_UINTEGER32"></span><span id="asn_uinteger32"></span><dl> <dt>**ASN \_ UINTEGER32**</dt> </dl>                          | 表示32位不帶正負號的整數變數。 此變數描述項合 RFC 1442 的 UInteger32 類型。<br/> |
| <span id="ASN_RFC2578_UNSIGNED32"></span><span id="asn_rfc2578_unsigned32"></span><dl> <dt>**ASN \_ RFC2578 \_ UNSIGNED32**</dt> </dl> | 請參閱 ASN \_ GAUGE32。<br/>                                                                                                     |



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

 

