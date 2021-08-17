---
title: 'RasAdminPortEnum 函式 (Rassapi) '
description: RasAdminPortEnum 函式會列舉指定的 RAS 伺服器上的所有埠。 針對伺服器上的每個通訊埠，此函式 \_ \_ 會傳回包含埠相關資訊的 RAS 埠0結構。
ms.assetid: ad23727c-8f54-4b10-9bc7-1425ac22bc88
keywords:
- RasAdminPortEnum 函式 RAS
topic_type:
- apiref
api_name:
- RasAdminPortEnum
api_location:
- Rassapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 989b86cbf78a47a62c8d98799ac18adf987cbe623dc92e703537c54b54bf892a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117788870"
---
# <a name="rasadminportenum-function"></a>RasAdminPortEnum 函式

\[這項功能僅提供給 Windows NT Server 4.0 的回溯相容性。 它會傳回 \_ \_ 未 \_ 在 Windows Server 2003 上執行的錯誤呼叫。 應用程式應該使用 [**MprAdminPortEnum**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminportenum) 函式。\]

**RasAdminPortEnum** 函式會列舉指定的 RAS 伺服器上的所有埠。 針對伺服器上的每個通訊埠，此函式會傳回包含埠相關資訊的 [**RAS \_ 埠 \_ 0**](ras-port-0-str.md) 結構。

## <a name="syntax"></a>語法


```C++
DWORD RasAdminPortEnum(
  _In_  const WCHAR       *lpszServer,
  _Out_       PRAS_PORT_0 *ppRasPort0,
  _Out_       WORD        *pcEntriesRead
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszServer* \[在\]
</dt> <dd>

以 null 結束的 Unicode 字串指標，指定 RAS 伺服器的名稱。 \\ \\ 請以下列格式指定開頭為 "" 字元的名稱： \\ \\ *servername*。

</dd> <dt>

*ppRasPort0* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收包含 [**RAS \_ 埠 \_ 0**](ras-port-0-str.md) 結構陣列的緩衝區指標。 當應用程式完成記憶體時，請呼叫 [**RasAdminFreeBuffer**](rasadminfreebuffer.md) 函式來釋放它。

</dd> <dt>

*pcEntriesRead* \[擴展\]
</dt> <dd>

16位變數的指標，此變數會接收在 *ppRasPort0* 陣列中傳回的 [**RAS \_ 埠 \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0)結構總數。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值可能是下列錯誤碼。



| 值                                                                                             | 意義                                                                                                                                     |
|---------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NERR \_ ItemNotFound**</dt> </dl> | 無法列舉任何埠。 這可能是因為伺服器上所有設定的埠目前正在用於撥出。<br/> |



 

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

[**RAS \_ 埠 \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**RasAdminFreeBuffer**](rasadminfreebuffer.md)
</dt> </dl>

 

