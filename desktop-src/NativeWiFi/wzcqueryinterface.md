---
description: 針對無線零設定服務所管理的無線區域網路介面，提供詳細的資訊。
ms.assetid: e1d2260b-a71f-481e-b505-b5d1a17ee221
title: 'WZCQueryInterface 函式 (Wzcsapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCQueryInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 36457eebf5c38b32bb46eb8cfa44cae104f1bc6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851787"
---
# <a name="wzcqueryinterface-function"></a>WZCQueryInterface 函式

\[Windows Vista 和 Windows Server 2008 已不再支援 **WZCQueryInterface** 。 請改用 [**WlanQueryInterface**](/windows/desktop/api/Wlanapi/nf-wlanapi-wlanqueryinterface) 函數。 如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。 \]

**WZCQueryInterface** 函式會針對無線零設定服務所管理的無線區域網路介面，提供詳細的資訊。

提供指定介面的詳細資訊。

## <a name="syntax"></a>語法


```C++
DWORD WZCQueryInterface(
  _In_    LPWSTR      pSrvAddr,
  _In_    DWORD       dwInFlags,
  _Inout_ PINTF_ENTRY pIntf,
  _Out_   LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSrvAddr* \[在\]
</dt> <dd>

字串的指標，其中包含要在其上執行此函式的電腦名稱稱。 如果此參數為 **Null**，則會在本機電腦上查詢無線零設定服務。

如果指定的 *pSrvAddr* 參數是遠端電腦，則遠端電腦必須支援遠端 RPC 呼叫。

</dd> <dt>

*dwInFlags* \[在\]
</dt> <dd>

要查詢的欄位。 這是位元遮罩，可包含下列旗標的任何組合。



| 值                                                                                                                                                                                                                                     | 意義                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DYNFLAGS"></span><span id="intf_dynflags"></span><dl> <dt>**INTF \_DYNFLAGS**</dt> <dt>0x00000010</dt> </dl>             | 傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中 **dwDynFlags** 成員的值。<br/>                                                                                                          |
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_描述**</dt> <dt>0x00010000</dt> </dl>                      | 傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中 **wszDescr** 成員的值。<br/>                                                                                                            |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_NDISMEDIA**</dt> <dt>0x00020000</dt> </dl>          | 傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中的 **ulMediaState**、 **ulMediaType** 和 **ulPhysicalMediaType** 成員的值。<br/>                                                        |
| <span id="INTF_PREFLIST"></span><span id="intf_preflist"></span><dl> <dt>**INTF \_PREFLIST**</dt> <dt>0x00040000</dt> </dl>             | 傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構之 **rdStSSIDList** 成員中的慣用網路清單。<br/>                                                                                    |
| <span id="INTF_CAPABILITIES"></span><span id="intf_capabilities"></span><dl> <dt>**INTF \_功能**</dt> <dt>0x00080000</dt> </dl> | 傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中的 **dwCapabilities** 和 **rdNicCapabilities** 成員的值。<br/>                                                                      |
| <span id="INTF_INFRAMODE"></span><span id="intf_inframode"></span><dl> <dt>**INTF \_INFRAMODE**</dt> <dt>0x00200000</dt> </dl>          | 傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中 **nInfraMode** 成員的值。<br/> **NInfraMode** 成員只有在某些介面內容狀態中才有效。<br/>                     |
| <span id="INTF_AUTHMODE"></span><span id="intf_authmode"></span><dl> <dt>**INTF \_AUTHMODE**</dt> <dt>0x00400000</dt> </dl>             | 傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中 **nAuthMode** 成員的值。 <br/> **NAuthMode** 成員只有在某些介面內容狀態中才有效。<br/>                      |
| <span id="INTF_WEPSTATUS"></span><span id="intf_wepstatus"></span><dl> <dt>**INTF \_WEPSTATUS**</dt> <dt>0x00800000</dt> </dl>          | 傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中 **nWepStatus** 成員的值。 <br/> **NWepStatus** 成員只有在某些介面內容狀態中才有效。<br/>                    |
| <span id="INTF_SSID"></span><span id="intf_ssid"></span><dl> <dt>**INTF \_SSID**</dt> <dt>0x01000000</dt> </dl>                         | 傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中 **rdSSID** 成員的值。<br/> **RdSSID** 成員只有在某些介面內容狀態中才有效。<br/>                             |
| <span id="INTF_BSSID"></span><span id="intf_bssid"></span><dl> <dt>**INTF \_BSSID**</dt> <dt>0x02000000</dt> </dl>                      | 傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構中 **rdBSSID** 成員的值。<br/> **RdBSSID** 成員只有在某些介面內容狀態中才有效。<br/>                           |
| <span id="INTF_BSSIDLIST"></span><span id="intf_bssidlist"></span><dl> <dt>**INTF \_BSSIDLIST**</dt> <dt>0x04000000</dt> </dl>          | 傳回 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構之 **rdBSSIDList** 成員中的網路可見清單。<br/> **RdBSSIDList** 成員只有在某些介面內容狀態中才有效。<br/> |



 

</dd> <dt>

*pIntf* \[in、out\]
</dt> <dd>

在輸入時，指向要查詢之介面索引鍵的指標。 在輸出時，為所要求介面資料的指標。 此參數是 [**INTF \_ 專案**](intf-entry.md) 結構的指標。

</dd> <dt>

*pdwOutFlags* \[擴展\]
</dt> <dd>

已成功抓取一組欄位。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值可能是下列其中一個傳回碼。



| 傳回碼                                                                                               | Description                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 領域 \_ 垃圾桶**</dt> </dl>      | 儲存體控制區塊已損毀。 如果無線零設定服務尚未初始化內建物件，則會傳回此錯誤。<br/>                                                                                                                      |
| <dl> <dt>**\_ \_ \_ 找不到錯誤檔案**</dt> </dl>    | 系統找不到指定的檔案。 如果 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構的 **wszGuid** 成員中的 GUID 與本機電腦上的任何無線區域網路介面不相符，就會傳回此錯誤。 <br/> |
| <dl> <dt>**錯誤 \_ 不正確 \_ 參數**</dt> </dl>  | 參數不正確。 如果 *pIntf* 參數為 **Null**，就會傳回此錯誤。 如果 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構的 **wszGuid** 成員為 **Null**，就會傳回此錯誤。 <br/>                            |
| <dl> <dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt> </dl> | 沒有足夠的記憶體可用來處理此要求，並配置記憶體給查詢結果。<br/>                                                                                                                                                                       |
| <dl> <dt>**RPC \_ 狀態**</dt> </dl>                | 不同的錯誤碼。<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>備註

*PIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構的 **WSZGUID** 成員，必須包含無線區域網路介面的介面 GUID。 您可以藉由呼叫 [**WZCEnumInterfaces**](wzcenuminterfaces.md) 函式來取出無線區域網路介面清單。

*PIntf* 所指向之 [**INTF \_ 專案**](intf-entry.md)結構的下列成員在呼叫 **WZCQueryInterface** 函式之前，必須先設定為0： **RdSSID**、 **rdBSSID**、 **rdBSSIDList**、 **rdStSSIDList** 和 **rdCtrlData**。

即使收到媒體連線和中斷線上活動，無線零設定服務也不會 automotically 更新媒體狀態。 應用程式應該在呼叫 WZCRefreshInterface 函式之前，藉由呼叫 [](wzcrefreshinterface.md)函式來強制執行媒體狀態重新 **整理，如果** 要要求 NDIS 媒體狀態 (\_ 會在 *dwInFlags* 參數) 中設定 INTF NDISMEDIA 位。

當 *dwInFlags* 參數包含 **INTF \_ BSSIDLIST** 時，如果可見的網路清單是空的，則 **WZCQueryInterface** 函數不會將 *dwOutFlags* 設定為 INTF **\_ BSSIDLIST** 。 當 *dwInFlags* 參數包含 **INTF \_ ssid** 時，如果沒有可用的 ssid， **WZCQueryInterface** 函式不會設定 *dwOutFlags* 與 **INTF \_ ssid** 。

如果 **WZCQueryInterface** 函式傳回錯誤 \_ 成功，呼叫端應該使用 *PIntf* 參數來呼叫 [**>localfree**](/windows/win32/api/winbase/nf-winbase-localfree)函式，以釋放配置給所傳回資料的內部緩衝區（一旦不再需要這項資訊）。 這會釋放 *rdCtrlData* 參數所指向 [**INTF \_ 專案**](intf-entry.md)結構的 **rdSSID**、 **rdBSSID**、 **rdBSSIDList**、 **rdStSSIDList** 和 **pIntf** 成員所使用的緩衝區。

> [!Note]  
> Windows SDK 中無法使用 *Wzcsapi .h* 標頭檔和 *Wzcsapi .lib* 匯入程式庫檔案。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                                   |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                   |
| 用戶端支援結束<br/>    | Windows XP （含 SP3）<br/>                                                         |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                         |
| 標頭<br/>                   | <dl> <dt>Wzcsapi。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Wzcsapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wzcsapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INTF \_ 專案**](intf-entry.md)
</dt> <dt>

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCRefreshInterface**](wzcrefreshinterface.md)
</dt> </dl>

 

 
