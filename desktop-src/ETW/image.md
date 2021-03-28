---
description: 這個類別是影像事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: a719a34c-7e32-4758-9031-6ca2b2873e3e
title: Image 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Image
api_type:
- NA
api_location: ''
ms.openlocfilehash: 47280a81b882f91ad71c6cd91004d1c0885afddf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973308"
---
# <a name="image-class"></a>Image 類別

這個類別是影像事件的父類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[Guid("{2cb15d1d-5fc1-11d2-abe1-00a0c911f518}"), EventVersion(2)]
class Image : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

**Image** 類別未定義任何成員。

## <a name="remarks"></a>備註

若要在 NT 核心記錄會話中啟用影像事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函式時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標 \_ 影像 \_ 載入** 旗標。

事件追蹤取用者可以藉由呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式並將 [**ImageLoadGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，來為影像載入事件執行特殊處理。 使用下列事件種類來識別使用事件時的影像載入事件。



| 事件類型                                                          | 描述                                                                                                                                                                                                                                      |
|---------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **活動 \_追蹤 \_ 類型 \_ 載入** (事件種類值為 10) <br/>     | 映射載入事件。 當 DLL 或可執行檔載入時產生。 在第一次載入指定的 DLL 時，提供者只會產生一個事件。 [**影像 \_ 載入**](image-load.md)MOF 類別會定義此事件的事件資料。      |
| **活動 \_追蹤 \_ 類型 \_ END** (事件種類值為 2) <br/>       | 影像卸載事件。 當 DLL 或可執行檔卸載時產生。 在最後一次卸載指定的 DLL 時，提供者只會產生一個事件。 [**影像 \_ 載入**](image-load.md)MOF 類別會定義此事件的事件資料。 |
| **活動 \_追蹤 \_ 類型 \_ DC \_ 開始** (事件種類值為 3) <br/> | 資料收集開始事件。 列舉追蹤開頭的所有載入的影像。 [**影像 \_ 載入**](image-load.md)MOF 類別會定義此事件的事件資料。                                                                  |
| **活動 \_追蹤 \_ 類型 \_ DC \_ END** (事件種類值為 4) <br/>   | 資料收集結束事件。 列舉追蹤結尾的所有載入的影像。 [**影像 \_ 載入**](image-load.md)MOF 類別會定義此事件的事件資料。                                                                          |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**映射 \_ 載入**](image-load.md)
</dt> <dt>

[**影像 \_ V0**](image-v0.md)
</dt> <dt>

[**映射 \_ V1**](image-v1.md)
</dt> </dl>

 

 
