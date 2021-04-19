---
title: 'RasAdminPortGetInfo 函式 (Rassapi) '
description: RasAdminPortGetInfo 函式會在指定的伺服器上抓取指定埠的相關資訊。
ms.assetid: 22837685-62a4-4e55-b88f-11019d5d4154
keywords:
- RasAdminPortGetInfo 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminPortGetInfo
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d80c55b3182ec930732344cb7857f99c0dc411
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983133"
---
# <a name="rasadminportgetinfo-function"></a>RasAdminPortGetInfo 函式

\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。 它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。 應用程式應該使用 [**MprAdminPortGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportgetinfo) 函式。\]

**RasAdminPortGetInfo** 函式會在指定的伺服器上抓取指定埠的相關資訊。

## <a name="syntax"></a>語法


```C++
DWORD RasAdminPortGetInfo(
  _In_  const WCHAR               *lpszServer,
  _In_  const WCHAR               *lpszPort,
  _Out_       RAS_PORT_1          *pRasPort1,
  _Out_       RAS_PORT_STATISTICS *pRasStats,
  _Out_       RAS_PARAMETERS      **ppRasParams
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

</dd> <dt>

*pRasPort1* \[擴展\]
</dt> <dd>

[**RAS \_ 埠 \_ 1**](ras-port-1-str.md)結構的指標，該函式會填入埠的狀態相關資訊。

</dd> <dt>

*pRasStats* \[擴展\]
</dt> <dd>

[**RAS \_ 埠 \_ 統計**](ras-port-statistics-str.md)結構的指標，該函式會填入與埠相關的統計資料。

</dd> <dt>

*ppRasParams* \[擴展\]
</dt> <dd>

指標變數的指標，此變數會接收 [**RAS \_ 參數**](ras-parameters-str.md) 結構陣列的位址。 每個結構都包含媒體專用索引鍵的名稱，例如 MAXCONNECTBPS 及其相關聯的值。 當應用程式完成此記憶體時，請呼叫 [**RasAdminFreeBuffer**](rasadminfreebuffer.md) 函式來釋放它。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值可以是下列其中一個錯誤碼。



| 值                                                                                                     | 意義                                                                          |
|-----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------|
| <dl> <dt>**錯誤 \_ 開發人員 \_ 不 \_ 存在**</dt> </dl>     | 指定的埠無效。<br/>                                        |
| <dl> <dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt> </dl> | 記憶體不足，無法配置 *ppRasParams* 陣列的緩衝區。<br/> |



 

此函數沒有任何延伸的錯誤資訊;請勿呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

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

[**RAS \_ 參數**](ras-parameters-str.md)
</dt> <dt>

[**RAS \_ 埠 \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**RAS \_ 埠 \_ 統計資料**](ras-port-statistics-str.md)
</dt> <dt>

[**RasAdminFreeBuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

