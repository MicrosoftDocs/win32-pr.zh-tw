---
description: 這個類別是磁片 i/o 事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 630fb6c6-b505-4384-ab7b-ee898d95bd41
title: DiskIo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 0e91f5e8b84d77b0938f35da69a84c26fa0f34a4da63bce40330484a29e19b5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118395299"
---
# <a name="diskio-class"></a>DiskIo 類別

這個類別是磁片 i/o 事件的父類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[Guid("{3d6fa8d4-fe05-11d0-9dda-00c04fd7ba7c}")]
class DiskIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

**DiskIo** 類別不會定義任何成員。

## <a name="remarks"></a>備註

若要在 NT 核心記錄會話中啟用磁片 i/o 事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 磁片 \_ IO** 旗標。 您也可以指定下列一或多個旗標：

-   **事件 \_ 追蹤 \_ 旗標 \_ 磁片 \_ IO \_ 初始化**
-   **事件 \_ 追蹤 \_ 旗標 \_ 驅動程式**

事件追蹤取用者可以藉由呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式並將 [**DiskIoGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，來為磁片 i/o 事件執行特殊處理。 使用下列事件種類來識別使用事件時的實際磁片 i/o 事件。



| 事件類型                                                                      | 描述                                                                                                                                                   |
|---------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **活動 \_追蹤 \_ 類型 \_ IO \_ 讀取** (事件種類值為 10) <br/>             | 讀取事件。 [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) MOF 類別會定義此事件的事件資料。                                              |
| **活動 \_追蹤 \_ 類型 \_ IO \_ 寫入** (事件種類值為 11) <br/>            | 寫入事件。 [**DiskIo \_ TypeGroup1**](diskio-typegroup1.md) MOF 類別會定義此事件的事件資料。                                             |
| **活動 \_追蹤 \_ 類型 \_ IO \_ READ \_ INIT** (事件種類值為 12) <br/>       | 初始化讀取事件。 [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) MOF 類別會定義此事件的事件資料。                                   |
| **活動 \_追蹤 \_ 類型 \_ IO \_ WRITE \_ INIT** (事件種類值為 13) <br/>      | 初始化寫入事件。 [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) MOF 類別會定義此事件的事件資料。                                  |
| **活動 \_追蹤 \_ 類型 \_ IO \_ FLUSH** (事件種類值為 14) <br/>            | 初始化寫入事件。 [**DiskIo \_ TypeGroup3**](diskio-typegroup3.md) MOF 類別會定義此事件的事件資料。                                  |
| **活動 \_追蹤 \_ 類型 \_ IO \_ FLUSH \_ INIT** (事件種類值為 15) <br/>      | 初始化 flush 事件。 [**DiskIo \_ TypeGroup2**](diskio-typegroup2.md) MOF 類別會定義此事件的事件資料。                                  |
| **活動 \_追蹤 \_ 類型 \_ IO 重新 \_ 導向 \_ INIT** (事件種類值為 16) <br/> | 初始化重新導向的事件。 重新導向的 IO 事件可用來將磁片 io 對應到 wim 中的檔案名 (wim) 的 Windows 映像格式。                  |
| 事件種類值為52<br/>                                               | 驅動程式完成要求事件。 [**DriverCompleteRequest**](drivercompleterequest.md) MOF 類別會定義此事件的事件資料。                    |
| 事件種類值為53<br/>                                               | 驅動程式完成要求傳回事件。 [**DriverCompleteRequestReturn**](drivercompleterequestreturn.md) MOF 類別會定義此事件的事件資料。 |
| 事件種類值為37<br/>                                               | 驅動程式完成常式事件。 [**DriverCompletionRoutine**](drivercompletionroutine.md) MOF 類別會定義此事件的事件資料。              |
| 事件種類值為34<br/>                                               | 驅動程式主要函式呼叫事件。 [**DriverMajorFunctionCall**](drivermajorfunctioncall.md) MOF 類別會定義此事件的事件資料。             |
| 事件種類值為35<br/>                                               | 驅動程式主要函式呼叫傳回事件。 [**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md) MOF 類別會定義此事件的事件資料。  |



 

磁片 i/o 提供者無法識別磁片 i/o 事件期間所讀取或寫入的檔案。 若要抓取與磁片 i/o 事件相關聯的檔案名，請啟用 file I/0 事件提供者。

系統會在 i/o 完成時間記錄磁片 i/o 事件。 若要判斷 i/o 作業的開始時間，請使用初始化事件，例如事件 \_ 追蹤 \_ 類型 \_ IO \_ READ \_ INIT。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DiskIo \_ TypeGroup1**](diskio-typegroup1.md)
</dt> <dt>

[**DiskIo \_ TypeGroup2**](diskio-typegroup2.md)
</dt> <dt>

[**DiskIo \_ TypeGroup3**](diskio-typegroup3.md)
</dt> <dt>

[**DriverCompleteRequest**](drivercompleterequest.md)
</dt> <dt>

[**DriverCompleteRequestReturn**](drivercompleterequestreturn.md)
</dt> <dt>

[**DriverCompletionRoutine**](drivercompletionroutine.md)
</dt> <dt>

[**DriverMajorFunctionCall**](drivermajorfunctioncall.md)
</dt> <dt>

[**DriverMajorFunctionReturn**](drivermajorfunctionreturn.md)
</dt> </dl>

 

 
