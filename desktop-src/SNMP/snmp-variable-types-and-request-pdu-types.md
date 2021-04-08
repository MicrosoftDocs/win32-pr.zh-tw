---
title: SNMP 變數類型和要求 PDU 類型
description: 某些 SNMP 變數類型和要求 PDU 類型的定義已變更。 Snmp 檔會將舊類型對應至對應的新類型。
ms.assetid: 2d87aeee-6fcb-4837-b091-6a9def8a9acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d656add1b177b50e24b30a11d9fe008dcdfdf9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682771"
---
# <a name="snmp-variable-types-and-request-pdu-types"></a>SNMP 變數類型和要求 PDU 類型

\[SNMP 可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 相反地，請使用 [Windows 遠端管理](/windows/desktop/WinRM/portal)，也就是 MICROSOFT 對 ws-atomictransaction 的實。\]

某些 SNMP 變數類型和要求 PDU 類型的定義已變更。 Snmp 檔會將舊類型對應至對應的新類型。

## <a name="modified-snmp-variable-types"></a>修改後的 SNMP 變數類型

當您開發使用 Microsoft SNMP 管理 API 的管理員應用程式時，您應該使用下表所列的新 SNMP 變數類型。 資料表會列出舊的 SNMP 變數類型與對應的新變數類型。

| 舊變數類型        | 新變數類型 |
|--------------------------|-------------------|
| ASN \_ RFC1155 \_ IPADDRESS  | ASN \_ IPADDRESS    |
| ASN \_ RFC1155 \_ 計數器    | ASN \_ COUNTER32    |
| ASN RFC1155 量測計 \_ \_      | ASN \_ GAUGE32      |
| ASN \_ RFC1155 \_ TIMETICKS  | ASN \_ TIMETICKS    |
| ASN \_ RFC1155 不 \_ 透明     | ASN 不 \_ 透明       |
| ASN \_ RFC1213 \_ DISPSTRING | ASN \_ OCTETSTRING  |



 

## <a name="modified-snmp-pdu-request-types"></a>修改過的 SNMP PDU 要求類型

當您開發使用 Microsoft SNMP 管理 API 的管理員應用程式時，您應該使用下表所列的新 SNMP PDU 類型。 資料表會列出舊的 SNMP PDU 類型與相對應的新 PDU 類型。

| 舊的 PDU 類型                 | 新的 PDU 類型        |
|------------------------------|---------------------|
| ASN \_ RFC1157 \_ GETREQUEST     | SNMP \_ PDU \_ GET      |
| ASN \_ RFC1157 \_ GETNEXTREQUEST | SNMP \_ PDU \_ GETNEXT  |
| ASN \_ RFC1157 \_ GETRESPONSE    | SNMP \_ PDU \_ 回應 |
| ASN \_ RFC1157 \_ SETREQUEST     | SNMP \_ PDU \_ 設定      |
| ASN \_ RFC1157 \_ 陷阱           | SNMP \_ PDU \_ V1TRAP   |



 

 

 