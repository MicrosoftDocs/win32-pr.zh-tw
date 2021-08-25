---
title: 'SNMPv1 陷阱類型 (Snmp. h) '
description: SNMPv1 陷阱類型會描述一組預先定義的一般陷阱類型，其格式化為符合 SNMPv1 陷阱 PDU 標準。
ms.assetid: 3a652b8f-2ae1-4f8c-b0d6-388bc9171427
topic_type:
- apiref
api_name:
- SNMP_GENERICTRAP_COLDSTART
- SNMP_GENERICTRAP_WARMSTART
- SNMP_GENERICTRAP_LINKDOWN
- SNMP_GENERICTRAP_LINKUP
- SNMP_GENERICTRAP_AUTHFAILURE
- SNMP_GENERICTRAP_EGPNEIGHLOSS
- SNMP_GENERICTRAP_ENTERSPECIFIC
api_location:
- Snmp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7067a6bf5aa1ea11135279484cb74722b8bcc197b507f6bba9b30e35630a2861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886238"
---
# <a name="snmpv1-trap-types"></a>SNMPv1 陷阱類型

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用[Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 Microsoft 對 ws-atomictransaction 的實。\]

SNMPv1 陷阱類型會描述一組預先定義的一般陷阱類型，其格式化為符合 SNMPv1 陷阱 PDU 標準。



| 常數                                                                                                                                                                                                          | 描述                                                                                                                                                                              |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SNMP_GENERICTRAP_COLDSTART"></span><span id="snmp_generictrap_coldstart"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ COLDSTART**</dt> </dl>             | 表示冷啟動陷阱。 代理程式正在以 managed 模式初始化通訊協定實體。 它可能會改變其視圖中的物件。<br/>                                               |
| <span id="SNMP_GENERICTRAP_WARMSTART"></span><span id="snmp_generictrap_warmstart"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ WARMSTART**</dt> </dl>             | 表示暖啟動陷阱。 代理程式正在重新初始化本身，但是它不會改變其視圖中的物件。<br/>                                                                    |
| <span id="SNMP_GENERICTRAP_LINKDOWN"></span><span id="snmp_generictrap_linkdown"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ LINKDOWN**</dt> </dl>                | 表示連結中斷的陷阱。 附加的介面已從 up 狀態變更為關閉狀態。 變數系結清單中的第一個變數會識別介面。<br/> |
| <span id="SNMP_GENERICTRAP_LINKUP"></span><span id="snmp_generictrap_linkup"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ LINKUP**</dt> </dl>                      | 指出連結的設陷。 附加的介面已從下開始變更為啟動狀態。 變數系結清單中的第一個變數會識別介面。<br/>   |
| <span id="SNMP_GENERICTRAP_AUTHFAILURE"></span><span id="snmp_generictrap_authfailure"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ AUTHFAILURE**</dt> </dl>       | 指出驗證失敗的陷阱。 SNMP 實體已傳送 SNMP 訊息，但其已宣告為屬於已知的社區。<br/>                                 |
| <span id="SNMP_GENERICTRAP_EGPNEIGHLOSS"></span><span id="snmp_generictrap_egpneighloss"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ EGPNEIGHLOSS**</dt> </dl>    | 表示 EGP 鄰居遺失陷阱。 EGP 對等已變更為關閉狀態。 變數系結清單中的第一個變數會識別 EGP 對等互連的 IP 位址。<br/>   |
| <span id="SNMP_GENERICTRAP_ENTERSPECIFIC"></span><span id="snmp_generictrap_enterspecific"></span><dl> <dt>**SNMP \_ GENERICTRAP \_ ENTERSPECIFIC**</dt> </dl> | 表示企業特定的陷阱。 發生特殊事件。 它是在 *specificTrap* 參數中以企業特定值識別。<br/>               |



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

 

