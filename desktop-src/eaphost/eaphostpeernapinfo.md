---
title: 'EapHostPeerNapInfo 結構 (Eaphostpeerapis .h) '
description: 包含 EAP 要求者 (NAP) 資訊的網路存取保護。
ms.assetid: 703eda56-5932-44d5-ae7f-0a6328d82237
keywords:
- EapHostPeerNapInfo 結構 EAPHost
topic_type:
- apiref
api_name:
- EapHostPeerNapInfo
api_location:
- eaphostpeerapis.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5fe91c88f633f2e42599938e45e1291c90f1ec9c08559a84f132f3af9269de39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118274534"
---
# <a name="eaphostpeernapinfo-structure"></a>EapHostPeerNapInfo 結構

**EapHostPeerNapInfo** 結構包含 EAP 要求者 (NAP) 資訊的網路存取保護。

## <a name="syntax"></a>語法


```C++
typedef struct _tagEapHostPeerNapInfo {
  ISOLATION_STATE isolationState;
  ProbationTime   probationTime;
  UINT32          stringCorrelationIdLength;
} EapHostPeerNapInfo;
```



## <a name="members"></a>成員

<dl> <dt>

**isolationState**
</dt> <dd>

指定電腦之 NAP 隔離狀態的 [**隔離 \_ 狀態**](/windows/desktop/api/eaphostpeertypes/ne-eaphostpeertypes-isolation_state) 結構。 隔離狀態決定授與的網路存取層級。

</dd> <dt>

**probationTime**
</dt> <dd>

**ProbationTime** 結構，指定連接將在中斷之後離開隔離所需的時間。 **ProbationTime** 結構與 [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)結構相同。

</dd> <dt>

**stringCorrelationIdLength**
</dt> <dd>

遵循此結構之 NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes) 的長度（以位元組為單位）。

</dd> </dl>

## <a name="remarks"></a>備註

**EapHostPeerNapInfo** 結構會在 RPC 位元組資料流程中 **WCHAR** 資料類型的 NAP [stringCorrelationId](/windows/desktop/NAP/nap-datatypes)之前。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                   |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                      |
| 標頭<br/>                   | <dl> <dt>Eaphostpeerapis。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[EAPHost 要求者結構](eap-host-supplicant-structures.md)
</dt> <dt>

[**EapHostPeerGetAuthStatus**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetauthstatus)
</dt> <dt>

[**EapHostPeerMethodAuthParams**](/windows/win32/api/eaphostpeertypes/ne-eaphostpeertypes-eaphostpeerauthparams)
</dt> </dl>

 

