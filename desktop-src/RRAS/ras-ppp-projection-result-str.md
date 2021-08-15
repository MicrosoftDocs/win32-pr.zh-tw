---
title: 'RAS_PPP_PROJECTION_RESULT 結構 (Rassapi .h) '
description: RAS \_ ppp \_ 投射 \_ 結果結構是用來報告埠之各種 PPP 投影作業的結果。
ms.assetid: 061b1b51-4b6f-4127-8ee5-8a1913a2aa99
keywords:
- RAS_PPP_PROJECTION_RESULT 結構 RAS
topic_type:
- apiref
api_name:
- RAS_PPP_PROJECTION_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ce1bb82b34490f8a1f3734225cbde1e761c575a2019a30db7790bfc7fa3c169
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789582"
---
# <a name="ras_ppp_projection_result-structure"></a>RAS \_ PPP \_ 投射 \_ 結果結構

\[Windows Vista 不支援 **RAS \_ PPP \_ 投射 \_ 結果** 結構。\]

**RAS \_ ppp \_ 投射 \_ 結果** 結構是用來報告埠之各種 PPP 投影作業的結果。

## <a name="syntax"></a>語法


```C++
typedef struct _RAS_PPP_PROJECTION_RESULT {
  RAS_PPP_NBFCP_RESULT nbf;
  RAS_PPP_IPCP_RESULT  ip;
  RAS_PPP_IPXCP_RESULT ipx;
  RAS_PPP_ATCP_RESULT  at;
} RAS_PPP_PROJECTION_RESULT;
```



## <a name="members"></a>成員

<dl> <dt>

**nbf**
</dt> <dd>

此為 [**RAS \_ ppp \_ NBFCP \_ 結果**](ras-ppp-nbfcp-result-str.md) 結構，會報告 PPP NetBEUI Framer (NBF) 投影作業的結果。

</dd> <dt>

**Ip**
</dt> <dd>

[**RAS \_ ppp \_ IPCP \_ 結果**](ras-ppp-ipcp-result-str.md)結構，會報告 PPP 網際網路通訊協定 (IP) 投影作業的結果。

</dd> <dt>

**Ipx**
</dt> <dd>

[**RAS \_ ppp \_ IPXCP \_ 結果**](ras-ppp-ipxcp-result-str.md)結構，會報告 PPP 網路封包 Exchange (IPX) 投射作業的結果。

</dd> <dt>

**at**
</dt> <dd>

[**RAS \_ PPP 的 \_ ATCP \_ 結果**](ras-ppp-atcp-result-str.md)結構。

</dd> </dl>

## <a name="remarks"></a>備註

此結構會報告 NetBEUI、TCP/IP 和 IPX 通訊協定的投射結果。 每個 PPP 結構都有一個 **dwError** 成員，指出結構中的其他資訊是否有效。 如果 **DWERROR** 沒有 \_ 錯誤，則其他資訊是有效的。 如果 **dwError** 是 winerror.h. h 或 Raserror 中的其中一個錯誤碼，則其他資訊無效。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Rassapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端存取服務 (RAS) 總覽](about-remote-access-service.md)
</dt> <dt>

[RAS 伺服器管理結構](ras-server-administration-structures.md)
</dt> <dt>

[**RAS \_ 埠 \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**RAS \_ PPP \_ ATCP \_ 結果**](ras-ppp-atcp-result-str.md)
</dt> <dt>

[**RAS \_ PPP \_ IPCP \_ 結果**](ras-ppp-ipcp-result-str.md)
</dt> <dt>

[**RAS \_ PPP \_ IPXCP \_ 結果**](ras-ppp-ipxcp-result-str.md)
</dt> <dt>

[**RAS \_ PPP \_ NBFCP \_ 結果**](ras-ppp-nbfcp-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





