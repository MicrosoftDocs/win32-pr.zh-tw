---
description: 重新整理特定無線區域網路介面的介面資訊。
ms.assetid: 584b95b7-3218-4e3e-b5d9-9542488af16b
title: 'WZCRefreshInterface 函式 (Wzcsapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WZCRefreshInterface
api_type:
- DllExport
api_location:
- Wzcsapi.dll
ms.openlocfilehash: 43f2b35215c930517d5352073c679a116388eb49aaa3bd6a3c567467e50be1a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064508"
---
# <a name="wzcrefreshinterface-function"></a>WZCRefreshInterface 函式

\[Windows Vista 和 Windows Server 2008 不支援 **WZCRefreshInterface** 。 相反地，請使用 [原生 WIFI API](native-wifi-reference.md)，它會提供類似的功能。 如需詳細資訊，請參閱 [關於原生 WIFI API](about-the-native-wifi-api.md)。\]

**WZCRefreshInterface** 函式會更新特定無線區域網路介面的介面資訊。

## <a name="syntax"></a>語法


```C++
DWORD WZCRefreshInterface(
  _In_  LPWSTR      pSrvAddr,
  _In_  DWORD       dwInFlags,
  _In_  PINTF_ENTRY pIntf,
  _Out_ LPDWORD     pdwOutFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSrvAddr* \[在\]
</dt> <dd>

字串的指標，其中包含要在其上執行此函式的電腦名稱稱。 如果此參數為 **Null**，則會在本機電腦上呼叫無線零設定服務。

如果指定的 *pSrvAddr* 參數是遠端電腦，則遠端電腦必須支援遠端 RPC 呼叫。

</dd> <dt>

*dwInFlags* \[在\]
</dt> <dd>

一組要重新整理的欄位，以及要採取的特定重新整理動作。 這是位元遮罩，可包含下列旗標的任何組合。



| 值                                                                                                                                                                                                                            | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INTF_DESCR"></span><span id="intf_descr"></span><dl> <dt>**INTF \_描述**</dt> <dt>0x00010000</dt> </dl>             | 重新整理無線區域網路介面的介面描述。<br/> 您可以呼叫 [**WZCQueryInterface**](wzcqueryinterface.md)函式，並在 *dwInFlags* 參數中設定 **INTF \_ 描述** 位，以抓取重新整理的介面描述。 介面描述會傳回給 **WZCQueryInterface** 函數所傳回之 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構的 **wszDescr** 成員。<br/>                                                           |
| <span id="INTF_NDISMEDIA"></span><span id="intf_ndismedia"></span><dl> <dt>**INTF \_NDISMEDIA**</dt> <dt>0x00020000</dt> </dl> | 重新整理無線區域網路介面的 NDIS 媒體資訊。<br/> 您可以呼叫 [**WZCQueryInterface**](wzcqueryinterface.md)函式，並在 *dwInFlags* 參數中設定 **INTF \_ NDISMEDIA** 位，以抓取重新整理的 NDIS 媒體資訊。 在 **pIntf** 函式所傳回 *WZCQueryInterface* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構的 **ulMediaState**、 **ulMediaType** 和 **ulPhysicalMediaType** 成員中，會傳回 NDIS 媒體資訊。<br/> |
| <span id="INTF_ALL_OIDS"></span><span id="intf_all_oids"></span><dl> <dt>**INTF \_所有 \_ oid**</dt> <dt>0xFFF00000</dt> </dl>   | 重新整理無線區域網路介面的所有 NDIS Oid。 此選項會更新無線區域網路介面的大部分資料。<br/> 您可以藉由呼叫 [**WZCQueryInterface**](wzcqueryinterface.md) 函式來取出重新整理的資訊。<br/>                                                                                                                                                                                                                                                                                   |



 

</dd> <dt>

*pIntf* \[在\]
</dt> <dd>

[**INTF \_ 專案**](intf-entry.md)結構的指標，其中包含要重新整理之介面的索引鍵。

</dd> <dt>

*pdwOutFlags* \[擴展\]
</dt> <dd>

已成功重新整理的一組欄位。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值可能是下列其中一個傳回碼。



| 傳回碼                                                                                              | 描述                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 領域 \_ 垃圾桶**</dt> </dl>     | 儲存體控制區塊已損毀。 如果無線零設定服務尚未初始化內建物件，則會傳回此錯誤。<br/>                                                                                                                      |
| <dl> <dt>**\_ \_ \_ 找不到錯誤檔案**</dt> </dl>   | 系統找不到指定的檔案。 如果 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構的 **wszGuid** 成員中的 GUID 與本機電腦上的任何無線區域網路介面不相符，就會傳回此錯誤。 <br/> |
| <dl> <dt>**錯誤 \_ 不正確 \_ 參數**</dt> </dl> | 參數不正確。 如果 *pIntf* 參數為 **Null**，就會傳回此錯誤。 如果 *pIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構的 **wszGuid** 成員為 **Null**，就會傳回此錯誤。 <br/>                            |
| <dl> <dt>**RPC \_ 狀態**</dt> </dl>               | 不同的錯誤碼。<br/>                                                                                                                                                                                                                                                    |



 

## <a name="remarks"></a>備註

*PIntf* 參數所指向之 [**INTF \_ 專案**](intf-entry.md)結構的 **WSZGUID** 成員，必須包含無線區域網路介面的介面 GUID。 您可以藉由呼叫 [**WZCEnumInterfaces**](wzcenuminterfaces.md) 函式來取出無線區域網路介面清單。

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

[**WZCEapolGetInterfaceParams**](wzceapolgetinterfaceparams.md)
</dt> <dt>

[**WZCEnumInterfaces**](wzcenuminterfaces.md)
</dt> <dt>

[**WZCQueryInterface**](wzcqueryinterface.md)
</dt> <dt>

[**INTF \_ 專案**](intf-entry.md)
</dt> </dl>

 

 




