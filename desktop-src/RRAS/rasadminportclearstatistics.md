---
title: 'RasAdminPortClearStatistics 函式 (Rassapi) '
description: RasAdminPortClearStatistics 函式會重設計數器，此計數器代表 RAS \_ 埠統計資料結構中 RasAdminPortGetInfo 函數所報告的各種統計資料 \_ 。 計數器會重設為零，並開始累積。
ms.assetid: d2ce4652-1034-4ded-aa26-2678c719d5b9
keywords:
- RasAdminPortClearStatistics 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminPortClearStatistics
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57943fbefcba1625c7badff25827c62eaca8a8c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977707"
---
# <a name="rasadminportclearstatistics-function"></a>RasAdminPortClearStatistics 函式

\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。 它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。 應用程式應該使用 [**MprAdminPortClearStats**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportclearstats) 函式。\]

**RasAdminPortClearStatistics** 函式會重設計數器，此計數器代表 [**RAS \_ 埠 \_ 統計資料**](ras-port-statistics-str.md)結構中 [**RasAdminPortGetInfo**](rasadminportgetinfo.md)函數所報告的各種統計資料。 計數器會重設為零，並開始累積。

## <a name="syntax"></a>語法


```C++
DWORD RasAdminPortClearStatistics(
  _In_ const WCHAR *lpszServer,
  _In_ const WCHAR *lpszPort
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszServer* \[在\]
</dt> <dd>

以 null 結束的 Unicode 字串指標，指定 RAS 伺服器的名稱。 \\ \\ 請以下列格式指定開頭為 "" 字元的名稱： \\ \\ *servername*。

</dd> <dt>

*lpszPort* \[在\]
</dt> <dd>

以 null 結束的 Unicode 字串指標，指定伺服器上的埠名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值可能是下列錯誤碼。



| 值                                                                                                 | 意義                                   |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>**錯誤 \_ 開發人員 \_ 不 \_ 存在**</dt> </dl> | 指定的埠無效。<br/> |



 

此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

**RasAdminPortClearStatistics** 函式會清除伺服器上的統計資料，而不是在進行呼叫的應用程式中的本機。 這表示，針對監視指定埠的任何其他應用程式，也會重設統計資料。

如果 *lpszPort* 埠是多重連結連接的一部分， **RasAdminPortClearStatistics** 會重設指定之埠的統計資料，而函式也會重設多重連結連接的累計統計資料。 不過，此函式不會影響屬於多重連結連接之其他埠的個別統計資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------------|----------------------------------------------------------------------------------------|
| 用戶端支援結束<br/> | Windows 2000 Professional<br/>                                                   |
| 伺服器支援結束<br/> | Windows 2000 Server<br/>                                                         |
| 標頭<br/>                | <dl> <dt>Rassapi。h</dt> </dl>   |
| 程式庫<br/>               | <dl> <dt>Rassapi .lib</dt> </dl> |
| DLL<br/>                   | <dl> <dt>Rassapi.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端存取服務 (RAS) 總覽](about-remote-access-service.md)
</dt> <dt>

[RAS 伺服器管理功能](ras-server-administration-functions.md)
</dt> <dt>

[**RAS \_ 埠 \_ 統計資料**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

