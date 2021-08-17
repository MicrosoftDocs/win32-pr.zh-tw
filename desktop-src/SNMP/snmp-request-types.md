---
title: 'Snmp 要求類型 (Snmp. h) '
description: SNMP 要求類型是用來描述 SNMP 服務要求擴充代理程式執行的操作。
ms.assetid: a359977f-2edb-4ffd-acba-e14ec8e92544
topic_type:
- apiref
api_name:
- SNMP_EXTENSION_GET
- SNMP_EXTENSION_GET_NEXT
- SNMP_EXTENSION_GET_BULK
- SNMP_EXTENSION_SET_TEST
- SNMP_EXTENSION_SET_COMMIT
- SNMP_EXTENSION_SET_UNDO
- SNMP_EXTENSION_SET_CLEANUP
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74c4dfdfc6d65e63b8cd00956627eef9e831c46c6979e44634067b1e29defc4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142991"
---
# <a name="snmp-request-types"></a>SNMP 要求類型

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用[Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 Microsoft 對 ws-atomictransaction 的實。\]

SNMP 要求類型是用來描述 SNMP 服務要求擴充代理程式執行的操作。



| 常數/值                                                                                                                                                                                                                                                          | 描述                                                                                                                                                                                                                                                 |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_EXTENSION_GET"></span><span id="snmp_extension_get"></span><dl> <dt>**SNMP \_擴充功能 \_ 取得**</dt> <dt>SNMP \_ PDU \_ GET</dt> </dl>                       | 取出指定變數值的值。<br/>                                                                                                                                                                                         |
| <span id="SNMP_EXTENSION_GET_NEXT"></span><span id="snmp_extension_get_next"></span><dl> <dt>**SNMP \_擴充功能 \_ 取得 \_ 下一個**</dt> <dt>SNMP \_ PDU \_ GETNEXT</dt> </dl>   | 取得所指定變數的詞典編纂後置值。<br/>                                                                                                                                                          |
| <span id="SNMP_EXTENSION_GET_BULK"></span><span id="snmp_extension_get_bulk"></span><dl> <dt>**SNMP \_擴充功能 \_ 取得 \_ 大量**</dt> <dt>SNMP \_ PDU \_ GETBULK</dt> </dl>   | 使用單一要求來搜尋和取出多個值。<br/>                                                                                                                                                                                       |
| <span id="SNMP_EXTENSION_SET_TEST"></span><span id="snmp_extension_set_test"></span><dl> <dt>**SNMP \_ 延伸模組 \_ 設定 \_ 測試**</dt> </dl>                                                                           | 驗證指定之變數的值。 這項作業會將認可要求期間成功寫入作業的機率最大化。 如需詳細資訊，請參閱 [**SnmpExtensionQueryEx**](/windows/desktop/api/Snmp/nf-snmp-snmpextensionqueryex) 函數。<br/> |
| <span id="SNMP_EXTENSION_SET_COMMIT"></span><span id="snmp_extension_set_commit"></span><dl> <dt>**SNMP \_延伸模組 \_ 設定 \_ 認可**</dt> <dt>SNMP \_ PDU \_ 設定</dt> </dl> | 將新值寫入指定的變數。<br/>                                                                                                                                                                                                 |
| <span id="SNMP_EXTENSION_SET_UNDO"></span><span id="snmp_extension_set_undo"></span><dl> <dt>**SNMP \_ 延伸模組 \_ 設定 \_ 復原**</dt> </dl>                                                                           | 將所指定變數的值重設為其在認可要求之前的值。<br/>                                                                                                                                                           |
| <span id="SNMP_EXTENSION_SET_CLEANUP"></span><span id="snmp_extension_set_cleanup"></span><dl> <dt>**SNMP \_ 延伸模組 \_ 設定 \_ 清除**</dt> </dl>                                                                  | 釋放在先前的要求和作業中配置的資源。<br/>                                                                                                                                                                             |



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

 

