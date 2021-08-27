---
description: 描述與作業相關聯的一組完整值，並支援大小以64位表示的大型多工緩衝處理檔案。
ms.assetid: 90932ae2-ea9e-43bc-9a1d-c68223f6d0ee
title: 'JOB_INFO_4 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_4
- _JOB_INFO_4A
- _JOB_INFO_4W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: dd338b4e6e486c59bfdac705b68c72c56eafb96c9f4e1899e9b4cb3b294791de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120091918"
---
# <a name="job_info_4-structure"></a>作業 \_ 資訊 \_ 4 結構

描述與作業相關聯的一組完整值，並支援大小以64位表示的大型多工緩衝處理檔案。

## <a name="syntax"></a>語法


```C++
typedef struct _JOB_INFO_4 {
  DWORD                JobId;
  LPTSTR               pPrinterName;
  LPTSTR               pMachineName;
  LPTSTR               pUserName;
  LPTSTR               pDocument;
  LPTSTR               pNotifyName;
  LPTSTR               pDatatype;
  LPTSTR               pPrintProcessor;
  LPTSTR               pParameters;
  LPTSTR               pDriverName;
  LPDEVMODE            pDevMode;
  LPTSTR               pStatus;
  PSECURITY_DESCRIPTOR pSecurityDescriptor;
  DWORD                Status;
  DWORD                Priority;
  DWORD                Position;
  DWORD                StartTime;
  DWORD                UntilTime;
  DWORD                TotalPages;
  DWORD                Size;
  SYSTEMTIME           Submitted;
  DWORD                Time;
  DWORD                PagesPrinted;
  LONG                 SizeHigh;
} JOB_INFO_4, *PJOB_INFO_4;
```



## <a name="members"></a>成員

<dl> <dt>

**JobId**
</dt> <dd>

作業識別碼值。

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

**pNotifyName**
</dt> <dd>

以 null 結束的字串指標，指定當工作已列印時，或列印工作時發生錯誤時，應通知的使用者名稱。

</dd> <dt>

**pDatatype**
</dt> <dd>

以 null 結束的字串指標，指定用來記錄列印工作的資料類型。

</dd> <dt>

**pPrintProcessor**
</dt> <dd>

以 null 結束的字串指標，指定應該用來列印工作的列印處理器名稱。

</dd> <dt>

**pParameters**
</dt> <dd>

指定列印處理器參數之以 null 結束的字串指標。

</dd> <dt>

**pDriverName**
</dt> <dd>

以 null 結束的字串指標，指定應該用來處理列印工作的印表機驅動程式名稱。

</dd> <dt>

**pDevMode**
</dt> <dd>

[**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)結構的指標，其中包含印表機驅動程式的裝置初始化和環境資料。

</dd> <dt>

**pStatus**
</dt> <dd>

以 null 結束的字串指標，指定列印工作的狀態。 此成員應在 **狀態** 之前檢查，而且如果 **pStatus** 為 **Null**，則狀態會由狀態成員的內容定義。

</dd> <dt>

**pSecurityDescriptor**
</dt> <dd>

此成員的值為 **Null**。 此版本不支援檔安全描述項的抓取和設定。

</dd> <dt>

**狀態**
</dt> <dd>

作業狀態。 這個成員可以是下列其中一個或多個值：

| 值                           | 意義                                                      |
|---------------------------------|--------------------------------------------------------------|
| 作業 \_ 狀態已 \_ 封鎖 \_ DEVQ      | 驅動程式無法列印工作。                             |
| 作業 \_ 狀態 \_ 已刪除            | 作業已刪除。                                        |
| 作業 \_ 狀態 \_ 刪除           | 正在刪除工作。                                        |
| 作業 \_ 狀態 \_ 錯誤              | 與作業相關聯的錯誤。                         |
| \_離線作業狀態 \_            | 印表機已離線。                                          |
| 作業 \_ 狀態 \_ PAPEROUT           | 印表機缺紙。                                     |
| 作業 \_ 狀態已 \_ 暫停             | 作業已暫停。                                               |
| 作業 \_ 狀態已 \_ 列印            | 作業已列印。                                             |
| 作業 \_ 狀態 \_ 列印           | 作業正在列印。                                             |
| 作業 \_ 狀態 \_ 重新開機            | 作業已重新開機。                                      |
| 作業 \_ 狀態 \_ 緩衝處理           | 作業已在幕後處理。                                             |
| 作業 \_ 狀態 \_ 使用者 \_ 介入 | 印表機有錯誤，需要使用者進行一些動作。 |



 

在 Windows XP 和更新版本的 Windows 中，也可以使用下列值：

| 值                 | 意義                                                                                       |
|-----------------------|-----------------------------------------------------------------------------------------------|
| 作業 \_ 狀態 \_ 完成 | 作業會傳送至印表機，但可能尚未列印。 如需詳細資訊，請參閱「備註」。 |
| 保留的作業 \_ 狀態 \_ | 作業已在列印後保留在列印佇列中。                              |



 

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

**StartTime**
</dt> <dd>

作業可以列印的最早時間。

</dd> <dt>

**UntilTime**
</dt> <dd>

作業可以列印的最晚時間。

</dd> <dt>

**TotalPages**
</dt> <dd>

作業所需的頁面數目。 如果列印工作未包含以頁面分隔的資訊，則此值可能為零。

</dd> <dt>

**大小**
</dt> <dd>

作業大小的低四個位元組，以位元組為單位。 另請參閱下方的 **SizeHigh** 成員。

</dd> <dt>

**已提交**
</dt> <dd>

[**SYSTEMTIME**](/windows/desktop/api/minwinbase/ns-minwinbase-systemtime)結構，指定提交作業的時間。

此時間值採用國際標準時間座標 (UTC) 格式。 您應該先將它轉換成當地時間值，再顯示它。 您可以使用 [**FileTimeToLocalFileTime**](/windows/desktop/api/fileapi/nf-fileapi-filetimetolocalfiletime) 函數來執行轉換。

</dd> <dt>

**Time**
</dt> <dd>

自從作業開始列印以來經過的總時間（以毫秒為單位）。

</dd> <dt>

**PagesPrinted**
</dt> <dd>

已列印的頁面數目。 如果列印工作未包含以頁面分隔的資訊，則此值可能為零。

</dd> <dt>

**SizeHigh**
</dt> <dd>

作業的大小上限（以位元組為單位）。 另請參閱上方的 **大小** 成員。

</dd> </dl>

## <a name="remarks"></a>備註

不支援 TrueEndOfJob 的埠監視器，會將工作設定為在 \_ \_ 將作業提交至印表機後立即列印的工作狀態。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Winspool.drv。h</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ 作業 \_ 資訊 \_ 4W** (Unicode) 和 **\_ 工作 \_ 資訊 \_ 4a** (ANSI) <br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**版**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

