---
description: 這個類別是登錄事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 7ad92377-3fd7-47e0-b96e-bab530ea9d99
title: Registry_V1 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Registry_V1
api_type:
- NA
api_location: ''
ms.openlocfilehash: 320a2bce9213228be4ff5c1880d884ee9622b68c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972277"
---
# <a name="registry_v1-class"></a>登錄 \_ V1 類別

這個類別是登錄事件的父類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[Guid("{ae53722e-c863-11d2-8659-00c04fa321a1}"), EventVersion(1)]
class Registry_V1 : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

登錄 **\_ V1** 類別未定義任何成員。

## <a name="remarks"></a>備註

若要在 NT 核心記錄會話中啟用登錄事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗 \_** 標登錄。

事件追蹤取用者可以呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式，並將 **RegistryGuid** 指定為 *pGuid* 參數，以執行登錄事件的特殊處理。 使用事件時，請使用下列事件種類來識別實際的登錄事件。



| 事件類型                                                                       | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **活動 \_追蹤 \_ 類型 \_ REGCREATE** (事件種類值為 10) <br/>             | 建立索引鍵事件。 [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                                                                                                                                                                                                                                     |
| **活動 \_追蹤 \_ 類型 \_ REGDELETE** (事件種類值為 12) <br/>             | 刪除索引鍵事件。 [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                                                                                                                                                                                                                                     |
| **活動 \_追蹤 \_ 類型 \_ REGDELETEVALUE** (事件種類值為 15) <br/>        | 刪除值事件。 [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                                                                                                                                                                                                                                   |
| **活動 \_追蹤 \_ 類型 \_ REGENUMERATEKEY** (事件種類值為 17) <br/>       | 列舉索引鍵事件。 [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                                                                                                                                                                                                                                  |
| **活動 \_追蹤 \_ 類型 \_ REGENUMERATEVALUEKEY** (事件種類值為 18) <br/>  | 列舉值索引鍵事件。 [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                                                                                                                                                                                                                            |
| **活動 \_追蹤 \_ 類型 \_ REGFLUSH** (事件種類值為 21) <br/>              | 清除索引鍵事件。 [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                                                                                                                                                                                                                                      |
| **活動 \_追蹤 \_ 類型 \_ REGKCBDMP** (事件種類值為 22) <br/>             | 當登錄作業使用控制碼而非字串來參考子機碼時產生。 每個控制碼都會記錄這些事件一次，第一次是參考控制碼。 控制碼的重複參考不會產生多個事件。<br/> [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。<br/> **Windows 2000：** 不支援這個值。<br/> |
| **活動 \_追蹤 \_ 類型 \_ REGOPEN** (事件種類值為 11) <br/>               | 開啟金鑰事件。 [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                                                                                                                                                                                                                                       |
| **活動 \_追蹤 \_ 類型 \_ REGQUERY** (事件種類值為 13) <br/>              | 查詢索引鍵事件。 [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                                                                                                                                                                                                                                      |
| **活動 \_追蹤 \_ 類型 \_ REGQUERYMULTIPLEVALUE** (事件種類值為 19) <br/> | 查詢多個值事件。 [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                                                                                                                                                                                                                           |
| **活動 \_追蹤 \_ 類型 \_ REGQUERYVALUE** (事件種類值為 16) <br/>         | 查詢值事件。 [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                                                                                                                                                                                                                                    |
| **活動 \_追蹤 \_ 類型 \_ REGSETINFORMATION** (事件種類值為 20) <br/>     | 設定資訊事件。 [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                                                                                                                                                                                                                                |
| **活動 \_追蹤 \_ 類型 \_ REGSETVALUE** (事件種類值為 14) <br/>           | 設定值事件。 [**Registry \_ TypeGroup1**](registry-typegroup1.md) MOF 類別會定義此事件的事件資料。                                                                                                                                                                                                                                                                                                                      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**登錄**](registry.md)
</dt> <dt>

[**登錄 \_ V0**](registry-v0.md)
</dt> <dt>

[**登錄 \_ V1 \_ TypeGroup1**](registry-v1-typegroup1.md)
</dt> </dl>

 

 
