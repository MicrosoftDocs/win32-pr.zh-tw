---
description: TcpIp_Fail 類別-這個類別是 TCP/IP 失敗事件的事件種類類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 1fe20b8c-b8f1-4db0-af78-1ebfc40b2bbd
title: TcpIp_Fail 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- TcpIp_Fail
- TcpIp_Fail.Proto
- TcpIp_Fail.FailureCode
api_type:
- NA
api_location: ''
ms.openlocfilehash: 897c42a1c2530d3e41d1f937d5d59356a2913e2b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108105846"
---
# <a name="tcpip_fail-class"></a>TcpIp \_ 失敗類別

這個類別是 TCP/IP 失敗事件的事件種類類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[EventType{17}, EventTypeName{"Fail"}]
class TcpIp_Fail : TcpIp
{
  uint16 Proto;
  uint16 FailureCode;
};
```

## <a name="members"></a>成員

**TcpIp \_ Fail** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**TcpIp \_ 失敗** 類別具有這些屬性。

<dl> <dt>

**[FailureCode]**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

失敗的原因。 可以是下列其中一個程式碼：

<dl> <dt>

<span id="ERROR_INSUFFICIENT_RESOURCES"></span><span id="error_insufficient_resources"></span>**錯誤 \_\_資源不足** (1) 
</dt> <dt>

<span id="ERROR_TOO_MANY_ADDRESSES"></span><span id="error_too_many_addresses"></span>**錯誤 \_太 \_ 多 \_ 位址** (2) 
</dt> <dt>

<span id="ERROR_ADDRESS_EXISTS"></span><span id="error_address_exists"></span>**錯誤 \_位址 \_ 存在** (3) 
</dt> <dt>

<span id="ERROR_INVALID_ADDRESS"></span><span id="error_invalid_address"></span>**錯誤 \_不正確 \_ 位址** (4) 
</dt> <dt>

<span id="ERROR_OTHER"></span><span id="error_other"></span>**錯誤 \_其他** (5) 
</dt> <dt>

<span id="ERROR_TIMEWAIT_ADDRESS_EXIST"></span><span id="error_timewait_address_exist"></span>**錯誤 \_TIMEWAIT \_ 位址 \_ 存在** (6) 
</dt> </dl>

</dd> <dt>

**原**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

識別通訊協定。 可以是下列值之一：



| 值                                                                                                                                                                                                  | 意義                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span id="AF_INET"></span><span id="af_inet"></span><dl> <dt>**AF \_INET**</dt> <dt>2</dt> </dl>     | 第四版網際網路協定 (IPv4) 位址系列。<br/>  |
| <span id="AF_INET6"></span><span id="af_inet6"></span><dl> <dt>**AF \_INET6**</dt> <dt>23</dt> </dl> | 網際網路通訊協定第6版 (IPv6) 位址系列。<br/> |



 

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Tcpip.sys**](tcpip.md)
</dt> </dl>

 

 




