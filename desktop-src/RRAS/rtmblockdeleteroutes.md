---
title: 'RtmBlockDeleteRoutes 函式 (Rtm. h) '
description: RtmBlockDeleteRoutes 函數會刪除資料表中指定之路由子集內的所有路由。
ms.assetid: d191883d-da3d-4a91-92e6-4979db96f4a4
keywords:
- RtmBlockDeleteRoutes 函式 RAS
topic_type:
- apiref
api_name:
- RtmBlockDeleteRoutes
api_location:
- Rtm.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f830603bba4bcdf07bd7bc8c631ac17028301a795fc14ebbce6483ef72f81361
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073878"
---
# <a name="rtmblockdeleteroutes-function"></a>RtmBlockDeleteRoutes 函式

\[此 api 已由[路由表管理員第2版](about-routing-table-manager-version-2.md)api 取代，而且將無法在 Windows Server 2003 之外使用。 應用程式應該使用路由表管理員第2版 API。\]

**RtmBlockDeleteRoutes** 函數會刪除資料表中指定之路由子集內的所有路由。

## <a name="syntax"></a>語法


```C++
HANDLE RtmBlockDeleteRoutes(
  _In_ HANDLE ClientHandle,
  _In_ DWORD  EnumerationFlags,
  _In_ PVOID  CriteriaRoute
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ClientHandle* \[在\]
</dt> <dd>

識別要刪除之路由的用戶端和路由通訊協定的控制碼。

</dd> <dt>

*EnumerationFlags* \[在\]
</dt> <dd>

指定應列舉的路由。 此參數會將已刪除的路由集合限制為下列旗標所定義子集，以及 *CriteriaRoute* 參數所指向之結構的對應成員中的值。 旗標與 [**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md) 中使用的旗標相同，不同之處在于 RTM \_ 只有 \_ 最適合 \_ **RtmBlockDeleteRoutes** 的路由是多餘的。 最好是在刪除路由時調整最理想的路由，因此函式最終會刪除子集中的所有路由。

</dd> <dt>

*CriteriaRoute* \[在\]
</dt> <dd>

通訊協定系列特定路由結構的指標， ( [**rtm \_ IP \_ 路由**](rtm-ip-route.md) 或 [**rtm \_ IPX \_ 路由**](rtm-ipx-route.md)) 。 此結構中的成員值會對應至 *EnumerationFlags* 參數所指定的旗標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值不會是 \_ 錯誤。

如果函式失敗，則傳回值是下列其中一個錯誤碼。



| 值                                                                                                       | 描述                                                                                                |
|-------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 沒有 \_ 路由**</dt> </dl>            | 沒有具有指定準則的路由。<br/>                                           |
| <dl> <dt>**錯誤 \_ 不正確 \_ 控制碼**</dt> </dl>       | *ClientHandle* 參數無效。<br/>                                                      |
| <dl> <dt>**錯誤 \_ 不正確 \_ 參數**</dt> </dl>    | 一或多個輸入參數無效，例如列舉旗標無效。<br/> |
| <dl> <dt>**錯誤 \_ 的 \_ 系統 \_ 資源**</dt> </dl> | 資源不足，無法執行操作。<br/>                                    |
| <dl> <dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt> </dl>   | 記憶體不足，無法執行操作。<br/>                                        |



 

## <a name="remarks"></a>備註

函數會產生適當的通知訊息給所有已註冊的用戶端，包括呼叫者。

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

[**RtmCreateEnumerationHandle**](rtmcreateenumerationhandle.md)
</dt> <dt>

[**RtmRegisterClient**](rtmregisterclient.md)
</dt> </dl>

 

 





