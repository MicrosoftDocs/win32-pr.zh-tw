---
description: 包含 EAPOL 設定參數。
ms.assetid: 4157a643-86f2-4f6f-8517-6207b11ea9a1
title: 'EAPOL_INTF_PARAMS 結構 (Wzcsapi .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EAPOL_INTF_PARAMS
api_type:
- HeaderDef
api_location:
- wzcsapi.h
ms.openlocfilehash: 3359454196735b8100ea40a9b4add2e8e0398c336bf254eb507b0a4e63a86e1e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685238"
---
# <a name="eapol_intf_params-structure"></a>EAPOL \_ INTF \_ PARAMS 結構

\[**EAPOL \_Windows \_** Vista 和 Windows Server 2008 已不再支援 INTF 參數。 相反地，請使用 [原生 WIFI API](native-wifi-reference.md)，它會提供類似的功能。 如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。\]

包含 EAPOL 設定參數。

## <a name="syntax"></a>語法


```C++
typedef struct _EAPOL_INTF_PARAMS {
  DWORD dwVersion;
  DWORD dwReserved2;
  DWORD dwEapFlags;
  DWORD dwEapType;
  DWORD dwSizeOfSSID;
  BYTE  bSSID[MAX_NETWORK_NAME_LENGTH];
} EAPOL_INTF_PARAMS, *PEAPOL_INTF_PARAMS;
```



## <a name="members"></a>成員

<dl> <dt>

**dwVersion**
</dt> <dd>

呼叫端的版本。 預設值為 0。

</dd> <dt>

**dwReserved2**
</dt> <dd>

保留供未來使用。

</dd> <dt>

**dwEapFlags**
</dt> <dd>

未使用。

</dd> <dt>

**dwEapType**
</dt> <dd>

要使用的 EAP 延伸模組類型。 針對 EAP-TLS，將0x00000026 設為0x00000013，並針對 PEAP 設定為。

</dd> <dt>

**dwSizeOfSSID**
</dt> <dd>

網路識別碼的大小。

</dd> <dt>

**bSSID**
</dt> <dd>

網路識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

Windows SDK 不提供標頭檔 wzcsapi。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                 |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                 |
| 用戶端支援結束<br/>    | WindowsXP SP3<br/>                                                       |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Wzcsapi。h</dt> </dl> |



 

 




