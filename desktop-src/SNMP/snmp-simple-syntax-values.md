---
title: 'SNMP 簡單語法值 (Snmp. h) '
description: SNMP 簡單語法值是用來表示 SNMP 變數類型。
ms.assetid: 42b681e5-721d-4d41-bc1a-c9f0005cde87
topic_type:
- apiref
api_name:
- ASN_INTEGER
- ASN_BITS
- ASN_OCTETSTRING
- ASN_NULL
- ASN_OBJECTIDENTIFIER
- ASN_INTEGER32
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cee6a40b4f63b7ce701b8232b310b2f73bac42d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104375"
---
# <a name="snmp-simple-syntax-values"></a>SNMP 簡單語法值

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]

SNMP 簡單語法值是用來表示 SNMP 變數類型。



| 常數                                                                                                                                                                           | 描述                                                           |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------|
| <span id="ASN_INTEGER"></span><span id="asn_integer"></span><dl> <dt>**ASN \_ 整數**</dt> </dl>                            | 表示32位帶正負號的整數變數。<br/>                |
| <span id="ASN_BITS"></span><span id="asn_bits"></span><dl> <dt>**ASN \_ 位**</dt> </dl>                                     | 表示變數，其為已命名位的列舉。<br/> |
| <span id="ASN_OCTETSTRING"></span><span id="asn_octetstring"></span><dl> <dt>**ASN \_ OCTETSTRING**</dt> </dl>                | 表示八位字串變數。<br/>                        |
| <span id="ASN_NULL"></span><span id="asn_null"></span><dl> <dt>**ASN \_ Null**</dt> </dl>                                     | 表示 **Null** 值。<br/>                                |
| <span id="ASN_OBJECTIDENTIFIER"></span><span id="asn_objectidentifier"></span><dl> <dt>**ASN \_ OBJECTIDENTIFIER**</dt> </dl> | 指出物件識別碼變數。<br/>                   |
| <span id="ASN_INTEGER32"></span><span id="asn_integer32"></span><dl> <dt>**ASN \_ INTEGER32**</dt> </dl>                      | 表示32位帶正負號的整數值。<br/>                   |



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

 

