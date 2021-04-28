---
description: FileIo 類別-這個類別是檔案 i/o 事件的父類別。 以下是從 MOF 程式碼簡化的語法。
ms.assetid: 8e006a63-a061-4b62-8f90-b8c8823bb047
title: FileIo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FileIo
api_type:
- NA
api_location: ''
ms.openlocfilehash: 716528902a115e23eae5b49ef572b87a71d11e25
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108106526"
---
# <a name="fileio-class"></a>FileIo 類別

這個類別是檔案 i/o 事件的父類別。

以下是從 MOF 程式碼簡化的語法。

## <a name="syntax"></a>語法

``` syntax
[Guid("{90cbdc39-4a3e-11d1-84f4-0000f80464e3}"), EventVersion(2)]
class FileIo : MSNT_SystemTrace
{
};
```

## <a name="members"></a>成員

**FileIo** 類別不會定義任何成員。

## <a name="remarks"></a>備註

若要在 NT 核心記錄會話中啟用檔案 IO 事件，請在呼叫 [**StartTrace**](/windows/win32/api/evntrace/nf-evntrace-starttracea)函數時，于 [**事件 \_ 追蹤 \_ 屬性**](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)結構的 **EnableFlags** 成員中指定 **事件 \_ 追蹤 \_ 旗標磁片檔案 \_ \_ \_ IO** 旗標。 您也可以指定下列一或多個旗標：

-   **事件 \_ 追蹤 \_ 旗標檔案 \_ \_ IO**
-   **事件 \_ 追蹤 \_ 旗標檔案 \_ \_ IO \_ 初始化**

事件追蹤取用者可以藉由呼叫 [**SetTraceCallback**](/windows/win32/api/evntrace/nf-evntrace-settracecallback) 函式並將 [**FileIoGuid**](nt-kernel-logger-constants.md) 指定為 *pGuid* 參數，來執行檔案 i/o 事件的特殊處理。 使用下列事件種類來識別使用事件時的實際事件。



| 事件類型             | 描述                                                                                                                                                                             |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 事件種類值為0  | 檔案名事件。 [**FileIo \_ 名稱**](fileio-name.md)MOF 類別會定義此事件的事件資料。                                                                               |
| 事件種類值為32 | File create 事件。 [**FileIo \_ 名稱**](fileio-name.md)MOF 類別會定義此事件的事件資料。                                                                             |
| 事件種類值為35 | 檔案刪除事件。 [**FileIo \_ 名稱**](fileio-name.md)MOF 類別會定義此事件的事件資料。                                                                             |
| 事件種類值為36 | File 取消事件。 列舉在追蹤會話結束時，電腦上所有開啟的檔案。 [**FileIo \_ 名稱**](fileio-name.md)MOF 類別會定義此事件的事件資料。 |
| 事件種類值為64 | File create 事件。 [**FileIo \_ Create**](fileio-create.md) MOF 類別會定義此事件的事件資料。                                                                         |
| 事件種類值為72 | 目錄列舉事件。 [**FileIo \_ DirEnum**](fileio-direnum.md) MOF 類別會定義此事件的事件資料。                                                             |
| 事件種類值為77 | 目錄通知事件。 [**FileIo \_ DirEnum**](fileio-direnum.md) MOF 類別會定義此事件的事件資料。                                                            |
| 事件種類值為69 | 設定資訊事件。 [**FileIo \_ 資訊**](fileio-info.md)MOF 類別會定義此事件的事件資料。                                                                         |
| 事件種類值為70 | 刪除檔案事件。 [**FileIo \_ 資訊**](fileio-info.md)MOF 類別會定義此事件的事件資料。                                                                             |
| 事件種類值為71 | 重新命名檔案事件。 [**FileIo \_ 資訊**](fileio-info.md)MOF 類別會定義此事件的事件資料。                                                                             |
| 事件種類值為74 | 查詢檔案資訊事件。 [**FileIo \_ 資訊**](fileio-info.md)MOF 類別會定義此事件的事件資料。                                                                  |
| 事件種類值為75 | 檔案系統控制事件。 [**FileIo \_ 資訊**](fileio-info.md)MOF 類別會定義此事件的事件資料。                                                                     |
| 事件種類值為76 | 作業結束事件。 [**FileIo \_ OpEnd**](fileio-opend.md) MOF 類別會定義此事件的事件資料。                                                                      |
| 事件種類值為67 | File read 事件。 [**FileIo \_ ReadWrite**](fileio-readwrite.md) MOF 類別會定義此事件的事件資料。                                                                     |
| 事件種類值為68 | 檔案寫入事件。 [**FileIo \_ ReadWrite**](fileio-readwrite.md) MOF 類別會定義此事件的事件資料。                                                                    |
| 事件種類值為65 | 清除事件。 釋放檔案的最後一個控制碼時，就會產生此事件。 [**FileIo \_ SimpleOp**](fileio-simpleop.md) MOF 類別會定義此事件的事件資料。   |
| 事件種類值為66 | 關閉事件。 釋放檔案物件時，就會產生此事件。 [**FileIo \_ SimpleOp**](fileio-simpleop.md) MOF 類別會定義此事件的事件資料。                     |
| 事件種類值為73 | Flush 事件。 當檔案緩衝區完全排清到磁片時，就會產生此事件。 [**FileIo \_ SimpleOp**](fileio-simpleop.md) MOF 類別會定義此事件的事件資料。  |



 

檔案 IO 事件是在作業開始時記錄。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>       |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**MSNT \_ SystemTrace**](msnt-systemtrace.md)
</dt> <dt>

[**FileIo \_ V0**](fileio-v0.md)
</dt> <dt>

[**FileIo \_ V1**](fileio-v1.md)
</dt> </dl>

 

 
