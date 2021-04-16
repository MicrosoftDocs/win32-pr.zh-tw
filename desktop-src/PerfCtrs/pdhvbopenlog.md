---
description: PdhVbOpenLog 函式會開啟指定的記錄檔以供讀取和寫入。 此函數會呼叫 PdhOpenLog。
ms.assetid: d9b8d98c-64f2-4319-8ab2-67b776143cf7
title: PdhVbOpenLog 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PdhVbOpenLog
api_type:
- DllExport
api_location:
- Pdh.dll
ms.openlocfilehash: 7921585039cab285589f2cdde0f328c033069a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513404"
---
# <a name="pdhvbopenlog-function"></a>PdhVbOpenLog 函式

**PdhVbOpenLog** 函式會開啟指定的記錄檔以供讀取和寫入。 此函數會呼叫 [**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)。

> [!IMPORTANT]
> 本主題所描述的功能可能會在未來變更或無法使用。 相反地，Microsoft 建議您使用 [效能計數器](performance-counters-functions.md)函式中所述的功能。

Function PdhVbOpenLog ( \_ Byval SzLogFileName AS LPCTSTR， \_ Byval DWACCESSFLAGS as dword，Byval \_ lpdwLogType as LPDWORD，BYVAL hQuery as \_ pdh \_ hQuery，byval dwMaxSize \_ \_ \_ \_ as，byval \_ szUserCaption as，BYREF LPCSTR as，) ByRef phLog 做為 dword

## <a name="parameters"></a>參數

<dl> <dt>

*szLogFileName* \[在\]
</dt> <dd>

字串的指標，指定要開啟之記錄檔的名稱。

如果記錄檔包含 SQL 資料，則記錄檔名稱的格式為 **sql：** 資料包 *_！_*_LogFileName_。 在此情況下， *lpdwLogType* 參數的值為 PDH \_ 記錄 \_ 類型 \_ SQL。

</dd> <dt>

*dwAccessFlags* \[在\]
</dt> <dd>

開啟記錄檔時所要指定的存取類型。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                   | 意義                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="PDH_LOG_READ_ACCESS"></span><span id="pdh_log_read_access"></span><dl> <dt>**PDH \_ 記錄 \_ 讀取 \_ 許可權**</dt> </dl>       | 開啟記錄檔以進行讀取作業。<br/>            |
| <span id="PDH_LOG_WRITE_ACCESS"></span><span id="pdh_log_write_access"></span><dl> <dt>**PDH \_ 記錄 \_ 寫入 \_ 許可權**</dt> </dl>    | 針對寫入作業開啟新的記錄檔。<br/>       |
| <span id="PDH_LOG_UPDATE_ACCESS"></span><span id="pdh_log_update_access"></span><dl> <dt>**PDH \_ 記錄 \_ 更新 \_ 存取**</dt> </dl> | 針對寫入作業開啟現有的記錄檔。<br/> |



 

您可以使用 OR 運算子搭配下列其中一個 create access 旗標，來結合上表選取的值。



| 值                                                                                                                                                                                   | 意義                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_CREATE_NEW"></span><span id="pdh_log_create_new"></span><dl> <dt>**PDH \_ 記錄 \_ 建立 \_ 新的**</dt> </dl>          | 建立具有指定名稱的新記錄檔。<br/>                                                                                                    |
| <span id="PDH_LOG_CREATE_ALWAYS"></span><span id="pdh_log_create_always"></span><dl> <dt>**PDH \_ 記錄 \_ \_ 一律建立**</dt> </dl> | 將會建立具有指定名稱的新記錄檔，並且會清除具有相同名稱的任何現有記錄檔。<br/>                                             |
| <span id="PDH_LOG_OPEN_EXISTING"></span><span id="pdh_log_open_existing"></span><dl> <dt>**PDH \_ 記錄 \_ 開啟 \_ 現有的**</dt> </dl> | 開啟具有指定之名稱的現有記錄檔。 如果具有指定名稱的記錄檔不存在，這就等於 PDH \_ 記錄 \_ 新建 \_ 。<br/> |
| <span id="PDH_LOG_OPEN_ALWAYS"></span><span id="pdh_log_open_always"></span><dl> <dt>**PDH \_ 記錄 \_ \_ 一律開啟**</dt> </dl>       | 系統會開啟具有指定名稱的現有記錄檔，或建立具有指定名稱的新記錄檔。<br/>                                          |



 

</dd> <dt>

*lpdwLogType* \[在\]
</dt> <dd>

變數的指標，指出要開啟的記錄檔類型。 此參數可以是下列其中一個值。



| 值                                                                                                                                                                                      | 意義                                                                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="PDH_LOG_TYPE_UNDEFINED"></span><span id="pdh_log_type_undefined"></span><dl> <dt>**PDH \_ 記錄 \_ 類型 \_ 未定義**</dt> </dl> | 未定義的記錄檔格式。<br/>                                                                                   |
| <span id="PDH_LOG_TYPE_CSV"></span><span id="pdh_log_type_csv"></span><dl> <dt>**PDH \_ 記錄 \_ 類型 \_ CSV**</dt> </dl>                   | 在第一行包含資料行標頭的文字檔，以及每個後續行中的個別資料範例。<br/> |
| <span id="PDH_LOG_TYPE_SQL"></span><span id="pdh_log_type_sql"></span><dl> <dt>**PDH \_ 記錄 \_ 類型 \_ SQL**</dt> </dl>                   | 記錄檔中的資料是在 SQL 中。<br/>                                                                          |
| <span id="PDH_LOG_TYPE_TSV"></span><span id="pdh_log_type_tsv"></span><dl> <dt>**PDH \_ 記錄 \_ 類型 \_ TSV**</dt> </dl>                   | 與 PDH \_ 記錄檔 \_ 類型 \_ CSV 相同。<br/>                                                                                 |
| <span id="PDH_LOG_TYPE_BINARY"></span><span id="pdh_log_type_binary"></span><dl> <dt>**PDH \_ 記錄 \_ 類型 \_ 二進位**</dt> </dl>          | 二進位記錄檔格式。 包含迴圈記錄檔。<br/>                                                         |
| <span id="PDH_LOG_TYPE_PERFMON"></span><span id="pdh_log_type_perfmon"></span><dl> <dt>**PDH \_ 記錄 \_ 類型 \_ PERFMON**</dt> </dl>       | Perfmon 記錄檔格式。<br/>                                                                                     |



 

</dd> <dt>

*hQuery* \[在\]
</dt> <dd>

查詢控制碼。 [**PdhVbOpenQuery**](pdhvbopenquery.md)函數會傳回這個控制碼。

如果要開啟記錄檔以供讀取，這個參數可以是 **Null** 。

</dd> <dt>

*dwMaxSize* \[在\]
</dt> <dd>

記錄檔的大小上限（以位元組為單位）。 只有當記錄檔是有限大小或迴圈的記錄檔時，才會使用這個值。

</dd> <dt>

*szUserCaption* \[在\]
</dt> <dd>

字串的指標，指定記錄檔的使用者定義標題。 記錄檔標題通常會描述記錄檔的內容。 開啟現有的記錄檔時，會忽略這個參數的值。

</dd> <dt>

*phLog* \[在中，ref\]
</dt> <dd>

接收已開啟記錄檔之控制碼的緩衝區指標。

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



 

## <a name="remarks"></a>備註

使用這個函數將效能資料寫入記錄檔時，必須先使用 [**PdhVbOpenQuery**](pdhvbopenquery.md)開啟查詢。

在呼叫此函式之前，必須要有目前開啟的查詢，而且必須將所需的計數器新增至其中。

請注意，Perfmon 格式的記錄檔只能開啟以供讀取。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                               |
| 程式庫<br/>                  | <dl> <dt>Pdh. .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Pdh.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PdhOpenLog**](/windows/desktop/api/Pdh/nf-pdh-pdhopenloga)
</dt> <dt>

[**PdhVbGetLogFileSize**](pdhvbgetlogfilesize.md)
</dt> <dt>

[**PdhVbUpdateLog**](pdhvbupdatelog.md)
</dt> </dl>

 

