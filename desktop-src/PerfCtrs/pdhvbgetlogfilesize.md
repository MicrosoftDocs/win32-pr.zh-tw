---
description: PdhVbGetLogFileSize 函數會傳回指定之記錄檔的大小。 此函數會呼叫 PdhGetLogFileSize。
ms.assetid: 8f4fbb68-b0f5-4163-ae6e-5b7139a35adf
title: PdhVbGetLogFileSize 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbGetLogFileSize
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 0b9f490477704086bd9aa8c53dd32456d486471e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979154"
---
# <a name="pdhvbgetlogfilesize-function"></a>PdhVbGetLogFileSize 函式

**PdhVbGetLogFileSize** 函數會傳回指定之記錄檔的大小。 此函數會呼叫 [**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)。

> [!IMPORTANT]
> 本主題所描述的功能可能會在未來變更或無法使用。 相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。

函式 PdhVbGetLogFileSize ( \_ ByVal HLog 作為 PDH \_ hLog， \_ ByRef LlSize， \_ ) 為 DWORD 的 LONG

## <a name="parameters"></a>參數

<dl> <dt>

*hLog* \[在\]
</dt> <dd>

記錄檔的控制碼。 [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)函數會傳回這個控制碼。

</dd> <dt>

*llSize* \[擴展\]
</dt> <dd>

接收記錄檔大小之變數的指標（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函數成功，它會傳回0。

如果函式失敗，則傳回值為 [系統錯誤碼](/windows/desktop/Debug/system-error-codes) 或 [PDH 錯誤碼](pdh-error-codes.md)。 以下是可能的值。



| 傳回碼                                                                                                | Description                                                                                            |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <dt>**PDH \_ \_ 緩衝區不足**</dt> </dl>   | 要求的資料大於提供的緩衝區。 無法傳回要求的資料。<br/> |
| <dl> <dt>**PDH \_ 不正確 \_ 引數**</dt> </dl>      | 一或多個字串緩衝區的大小不正確。<br/>                                  |
| <dl> <dt>**PDH \_ 不正確 \_ 控制碼**</dt> </dl>        | 控制碼不是有效的 PDH 物件。<br/>                                                       |
| <dl> <dt>**PDH \_ 記錄 \_ 檔 \_ 開啟 \_ 錯誤**</dt> </dl> | 無法開啟指定的記錄檔。<br/>                                                      |
| <dl> <dt>**\_ \_ \_ 找不到 PDH 檔案**</dt> </dl>       | 找不到指定的檔案。<br/>                                                          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 程式庫<br/>                  | <dl> <dt>Pdh. .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PdhGetLogFileSize**](/windows/desktop/api/Pdh/nf-pdh-pdhgetlogfilesize)
</dt> <dt>

[**PdhVbOpenLog**](pdhvbopenlog.md)
</dt> <dt>

[**PdhVbUpdateLog**](pdhvbupdatelog.md)
</dt> </dl>

 

