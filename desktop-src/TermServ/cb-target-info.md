---
title: 'CB_TARGET_INFO 結構 (Cbclient .h) '
description: 包含目的電腦的相關資訊，以及應重新導向連入連接的 IP 位址。
ms.assetid: 60612E10-9D82-4F38-87F7-B24F51E6EBDA
ms.tgt_platform: multiple
keywords:
- CB_TARGET_INFO 結構遠端桌面服務
- PCB_TARGET_INFO 結構指標遠端桌面服務
topic_type:
- apiref
api_name:
- CB_TARGET_INFO
api_location:
- Cbclient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9bbb982636449075b758ac61178f5e97da47ce7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384210"
---
# <a name="cb_target_info-structure"></a>CB \_ 目標 \_ 資訊結構

包含目的電腦的相關資訊，以及應重新導向連入連接的 IP 位址。 此結構會搭配 [**IConnectionBrokerClient：： GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md) 方法使用。

## <a name="syntax"></a>語法


```C++
typedef struct {
  WCHAR ServerName[128];
  DWORD AddressCount;
  WCHAR Addresses[CB_MAX_ADDRESSES][CB_IPADDRESS_LEN];
} CB_TARGET_INFO, *PCB_TARGET_INFO;
```



## <a name="members"></a>成員

<dl> <dt>

**ServerName**
</dt> <dd>

代表目標伺服器的完整功能變數名稱。 針對遠端桌面虛擬化 (RDV) 案例，此成員為 **Null**。 針對 (RDSH) 案例的遠端桌面工作階段主機，此成員包含重新導向連入連線的伺服器名稱。

</dd> <dt>

**AddressCount**
</dt> <dd>

**位址** 陣列中的有效專案數。

</dd> <dt>

**位址**
</dt> <dd>

字串陣列，包含重新導向連入連接的 IP 位址。 這個陣列中的有效元素數目是在 **AddressCount** 成員中指定的。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                        |
| 標頭<br/>                   | <dl> <dt>Cbclient。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConnectionBrokerClient::GetTargetInfo**](iconnectionbrokerclient-gettargetinfo.md)
</dt> </dl>

 

 





