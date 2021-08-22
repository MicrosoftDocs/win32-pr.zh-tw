---
description: 作業 \_ 資訊 \_ 1 結構會指定列印工作資訊，例如工作識別碼值、工作要進行多工緩衝處理的印表機名稱、建立列印工作的電腦名稱稱、擁有列印工作的使用者名稱等，依此類推。
ms.assetid: d42ada89-6bc7-4006-81d9-dbcc0347edd3
title: 'JOB_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_1
- _JOB_INFO_1A
- _JOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c6e8d5900a0f2d0a2dce5c12d2629abfc80776cdc0ada1354070005e28fbcd37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971327"
---
# <a name="job_info_1-structure"></a>作業 \_ 資訊 \_ 1 結構

**作業 \_ 資訊 \_ 1** 結構會指定列印工作資訊，例如工作識別碼值、工作要進行多工緩衝處理的印表機名稱、建立列印工作的電腦名稱稱、擁有列印工作的使用者名稱等，依此類推。

## <a name="syntax"></a>語法


```C++
typedef struct _JOB_INFO_1 {
  DWORD      JobId;
  LPTSTR     pPrinterName;
  LPTSTR     pMachineName;
  LPTSTR     pUserName;
  LPTSTR     pDocument;
  LPTSTR     pDatatype;
  LPTSTR     pStatus;
  DWORD      Status;
  DWORD      Priority;
  DWORD      Position;
  DWORD      TotalPages;
  DWORD      PagesPrinted;
  SYSTEMTIME Submitted;
} JOB_INFO_1, *PJOB_INFO_1;
```



## <a name="members"></a>成員

<dl> <dt>

**JobId**
</dt> <dd>

作業識別碼。

</dd> <dt>

**pPrinterName**
</dt> <dd>

以 null 結束的字串指標，指定工作要進行多工緩衝處理的印表機名稱。

</dd> <dt>

**pMachineName**
</dt> <dd>

以 null 結束的字串指標，指定建立列印工作的電腦名稱稱。

</dd> <dt>

**pUserName**
</dt> <dd>

以 null 結束的字串指標，指定擁有列印工作之使用者的名稱。

</dd> <dt>

**pDocument**
</dt> <dd>

以 null 結束的字串指標，指定列印工作的名稱 (例如 "MS-WORD： Review.doc" ) 。

</dd> <dt>

**pDatatype**
</dt> <dd>

以 null 結束的字串指標，指定用來記錄列印工作的資料類型。

</dd> <dt>

**pStatus**
</dt> <dd>

以 null 結束的字串指標，指定列印工作的狀態。 此成員應在 *狀態* 之前檢查，而且如果 *pStatus* 為 **Null**，則狀態會由狀態成員的內容定義。

</dd> <dt>

**狀態**
</dt> <dd>

作業狀態。 此成員的值可以是零或一或多個下列值的組合。 值為零表示列印佇列在檔完成幕後處理之後暫停。



| 值                           | 意義                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 作業 \_ 狀態已 \_ 封鎖 \_ DEVQ      | 驅動程式無法列印工作。                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 作業 \_ 狀態 \_ 完成           | **Windows XP 和更新版本：** 作業會傳送至印表機，但作業可能尚未列印。<br/> 如需詳細資訊，請參閱「備註」。<br/>                                                                                                                                                                                                                                                                                                                           |
| 作業 \_ 狀態 \_ 已刪除            | 作業已刪除。                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 作業 \_ 狀態 \_ 刪除           | 正在刪除工作。                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| 作業 \_ 狀態 \_ 錯誤              | 與作業相關聯的錯誤。                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_離線作業狀態 \_            | 印表機已離線。                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| 作業 \_ 狀態 \_ PAPEROUT           | 印表機缺紙。                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| 作業 \_ 狀態已 \_ 暫停             | 作業已暫停。                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| 作業 \_ 狀態已 \_ 列印            | 作業已列印。                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 作業 \_ 狀態 \_ 列印           | 作業正在列印。                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 作業 \_ 狀態 \_ 重新開機            | 作業已重新開機。                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| 保留的作業 \_ 狀態 \_           | **Windows Vista 和更新版本：** 作業已保留在列印佇列中，無法刪除。 這可能是由下列問題所造成：<br/> 1) 作業是透過呼叫 SetJob 來手動保留，而多工緩衝處理器正在等候作業釋放。<br/> 2) 工作尚未完成列印，必須先完成列印，才能自動將其刪除。<br/> 如需列印工作命令的詳細資訊，請參閱 [**SetJob**](setjob.md) 。<br/> |
| 作業 \_ 狀態 \_ 緩衝處理           | 作業已在幕後處理。                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| 作業 \_ 狀態 \_ 使用者 \_ 介入 | 印表機有錯誤，需要使用者進行一些動作。                                                                                                                                                                                                                                                                                                                                                                                                                |



 

</dd> <dt>

**優先順序**
</dt> <dd>

作業優先權。 這個成員可以是下列其中一個值，或介於1到99之間的範圍 (最低優先順序 \_ 到最高 \_ 優先順序) 。



| 值         | 意義           |
|---------------|-------------------|
| 最小 \_ 優先順序 | 最小優先權。 |
| 最高 \_ 優先順序 | 最高優先順序。 |
| DEF \_ 優先權 | 預設優先順序。 |



 

</dd> <dt>

**位置**
</dt> <dd>

工作在列印佇列中的位置。

</dd> <dt>

**TotalPages**
</dt> <dd>

檔包含的總頁數。 如果列印工作未包含以頁面分隔的資訊，則此值可能為零。

</dd> <dt>

**PagesPrinted**
</dt> <dd>

已列印的頁面數目。 如果列印工作未包含以頁面分隔的資訊，則此值可能為零。

</dd> <dt>

**已提交**
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構，指定此檔在多工緩衝處理的時間。

此時間值採用國際標準時間座標 (UTC) 格式。 您應該先將它轉換成當地時間值，再顯示它。 您可以使用 [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) 函數來執行轉換。

</dd> </dl>

## <a name="remarks"></a>備註

不支援 TrueEndOfJob 的埠監視器，會將工作設定為在 \_ \_ 將作業提交至印表機之後列印的工作狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 作業 \_ 資訊 \_ 1W** (Unicode) 和 **\_ 作業 \_ 資訊 \_ 1a** (ANSI) <br/>                                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

