---
description: 取得指定無線區域網路介面的 EAPOL 設定參數。
ms.assetid: 3dce15be-879d-42e9-b8eb-96d52c004acb
title: 'WZCEapolGetInterfaceParams 函式 (Wzcsapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCEapolGetInterfaceParams
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: fa401e1b045b56b41f7406851c927c316b19d5486adc903af667383465bfd19f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117983925"
---
# <a name="wzceapolgetinterfaceparams-function"></a>WZCEapolGetInterfaceParams 函式

\[Windows Vista 和 Windows Server 2008 已不再支援 **WZCEapolGetInterfaceParams** 。 相反地，請使用 [原生 WIFI API](native-wifi-reference.md)，它會提供類似的功能。 如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。\]

**WZCEapolGetInterfaceParams** 函式會取得指定無線區域網路介面的 EAPOL 設定參數。

## <a name="syntax"></a>語法


```C++
DWORD WZCEapolGetInterfaceParams(
  _In_    LPWSTR            pSrvAddr,
  _In_    PWCHAR            pwszGuid,
  _In_    DWORD             dwSizeOfSSID,
  _In_    BYTE              *pbSSID,
  _Inout_ EAPOL_INTF_PARAMS *pIntfParams
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSrvAddr* \[在\]
</dt> <dd>

字串的指標，其中包含要在其上執行此函式的電腦名稱稱。 如果此參數為 **Null**，則會在本機電腦上呼叫無線零設定服務。

如果指定的 *pSrvAddr* 參數是遠端電腦，則遠端電腦必須支援遠端 RPC 呼叫。

</dd> <dt>

*pwszGuid* \[在\]
</dt> <dd>

要抓取資料之介面的 GUID。

</dd> <dt>

*dwSizeOfSSID* \[在\]
</dt> <dd>

要取出資料的網路識別碼大小。

</dd> <dt>

*pbSSID* \[在\]
</dt> <dd>

要抓取其資料的網路識別碼指標。

</dd> <dt>

*pIntfParams* \[in、out\]
</dt> <dd>

包含介面參數的 [**EAPOL \_ INTF \_ PARAMS 參數**](eapol-intf-params.md) 結構指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業 \_ 順利完成，則傳回錯誤成功; 否則會傳回 Windows 系統錯誤碼中的其中一個。

## <a name="remarks"></a>備註

如果 **WZCEapolGetInterfaceParams** 傳回錯誤 \_ 成功，呼叫端應該呼叫 [**>localfree**](/windows/win32/api/winbase/nf-winbase-localfree) 來釋出針對所傳回之資料所配置的內部緩衝區，而不再需要這項資訊。

> [!Note]  
> Windows SDK 中無法使用 *Wzcsapi .h* 標頭檔和 *Wzcsapi .lib* 匯入程式庫檔案。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows只有 XP （含 SP2） \[ 桌面應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | WindowsXP SP3<br/>                                                         |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Wzcsapi。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Wzcsapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
