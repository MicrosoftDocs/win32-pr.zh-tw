---
title: 'RAS_PPP_IPXCP_RESULT 結構 (Rassapi .h) '
description: RAS \_ ppp \_ IPXCP \_ 結果結構是用來報告通訊埠的 PPP 網際網路封包交換 (IPX) 投影作業的結果。
ms.assetid: e1236e1b-f0ef-46cf-a12f-35529215752c
keywords:
- RAS_PPP_IPXCP_RESULT 結構 RAS
topic_type:
- apiref
api_name:
- RAS_PPP_IPXCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bb7ca4d006bd1a1df5a645799998b463c0b14f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025172"
---
# <a name="ras_ppp_ipxcp_result-structure"></a>RAS \_ PPP \_ IPXCP \_ 結果結構

\[Windows Vista 不支援 **RAS \_ PPP \_ IPXCP \_ 結果** 結構。\]

**RAS \_ ppp \_ IPXCP \_ 結果** 結構是用來報告通訊埠的 PPP 網際網路封包交換 (IPX) 投影作業的結果。

## <a name="syntax"></a>語法


```C++
typedef struct _RAS_PPP_IPXCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPXADDRESSLEN + 1];
} RAS_PPP_IPXCP_RESULT;
```



## <a name="members"></a>成員

<dl> <dt>

**dwError**
</dt> <dd>

指出 IPX 投影作業的結果。 沒有錯誤的值 \_ 表示成功，在這種情況下， **wszAddress** 成員是有效的。 如果投射作業不成功，則 **dwError** 是 winerror.h .H 或 Raserror 的錯誤碼。

</dd> <dt>

**wszAddress**
</dt> <dd>

以 null 終止的 Unicode 字串，指定指派給遠端用戶端的 IPX 位址。 這個字串具有 * net ***。**_節點_ 表單。

</dd> </dl>

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

[**RAS \_ PPP \_ 投射 \_ 結果**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





