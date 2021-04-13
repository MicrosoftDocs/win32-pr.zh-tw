---
title: 'RtmGetNextRoute 函式 (Rtm. h) '
description: RtmGetNextRoute 函數會從資料表中指定的路由子集傳回下一個路由。
ms.assetid: 0f413276-2ace-4216-a1a0-1b3061bacc4a
keywords:
- RtmGetNextRoute 函式 RAS
topic_type:
- apiref
api_name:
- RtmGetNextRoute
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8592855e0c30cef2ed43b7818badd336bc2ab6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508783"
---
# <a name="rtmgetnextroute-function"></a>RtmGetNextRoute 函式

\[此 API 已由 [路由表管理員第2版](about-routing-table-manager-version-2.md) api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**RtmGetNextRoute** 函數會從資料表中指定的路由子集傳回下一個路由。

## <a name="syntax"></a>語法


```C++
DWORD RtmGetNextRoute(
  _In_    DWORD ProtocolFamily,
  _In_    DWORD EnumerationFlags,
  _Inout_ PVOID Route
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ProtocolFamily* \[在\]
</dt> <dd>

指定要取出的通訊協定系列（例如 IP 或 IPX）。

</dd> <dt>

*EnumerationFlags* \[在\]
</dt> <dd>

指定應列舉的路由。 此參數會將已刪除的路由集合限制為下列旗標所定義子集，以及 *CriteriaRoute* 參數所指向之結構的對應成員中的值。 旗標與 [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)中使用的旗標相同。

</dd> <dt>

*路由* \[in、out\]
</dt> <dd>

在輸入時， *路由* 指向通訊協定系列特定的結構， ( [**rtm \_ IP \_ 路由**](rtm-ip-route.md) 或 [**rtm \_ IPX \_ 路由**](rtm-ipx-route.md)) 。

呼叫的函式會提供此結構的成員值。 這些值與 *EnumerationFlags* 參數搭配使用時，會指定要從中傳回路由的集合。

在輸出中， *路由* 會指向接收符合指定準則之第一個路由的結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值不會是 **\_ 錯誤**。

如果函式失敗，則傳回值是下列其中一個錯誤碼。



| 值                                                                                                       | 描述                                                             |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 不正確 \_ 參數**</dt> </dl>    | 其中一個參數無效。<br/>                            |
| <dl> <dt>**錯誤 \_ 沒有 \_ 路由**</dt> </dl>            | 沒有符合指定準則的路由。<br/>       |
| <dl> <dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt> </dl> | 資源不足，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

路由會依下列順序傳回：

1.  網路編號
2.  路由通訊協定
3.  介面識別碼
4.  下個躍點位址

這個函式的效率比對應的列舉控制碼函數低。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                          |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                               |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                     |
| 標頭<br/>                   | <dl> <dt>Rtm. h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Rtm .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Rtm.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[路由表管理員第1版參考](routing-table-manager-version-1-reference.md)
</dt> <dt>

[路由表管理員第1版函數](routing-table-manager-version-1-functions.md)
</dt> <dt>

[**RtmCloseEnumerationHandle**](rtmcloseenumerationhandle.md)
</dt> <dt>

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmEnumerateGetNextRoute**](rtmenumerategetnextroute.md)
</dt> <dt>

[**RtmGetFirstRoute**](rtmgetfirstroute.md)
</dt> </dl>

 

 





