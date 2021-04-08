---
description: GetPrintProcessorDirectory 函式會在指定的伺服器上，捕獲列印處理器目錄的路徑。
ms.assetid: a2443cfd-e5ba-41c6-aaf4-45051a3d0e26
title: 'GetPrintProcessorDirectory 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintProcessorDirectory
- GetPrintProcessorDirectoryA
- GetPrintProcessorDirectoryW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: a105025ba22c7e188b8dd20df67f5e8ad28fce01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852420"
---
# <a name="getprintprocessordirectory-function"></a>GetPrintProcessorDirectory 函式

**GetPrintProcessorDirectory** 函式會在指定的伺服器上，捕獲列印處理器目錄的路徑。

## <a name="syntax"></a>語法


```C++
BOOL GetPrintProcessorDirectory(
  _In_  LPTSTR  pName,
  _In_  LPTSTR  pEnvironment,
  _In_  DWORD   Level,
  _Out_ LPBYTE  pPrintProcessorInfo,
  _In_  DWORD   cbBuf,
  _Out_ LPDWORD pcbNeeded
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

指定伺服器名稱之以 null 結束的字串指標。 如果此參數為 **Null**，則會傳回本機路徑。

</dd> <dt>

*pEnvironment* \[在\]
</dt> <dd>

以 null 結束的字串指標，指定環境 (例如，Windows x86、Windows IA64 或 Windows x64) 。 如果此參數為 **Null**，則會使用目前的呼叫應用程式和用戶端電腦的環境 (不是目的地應用程式，而列印伺服器) 。

</dd> <dt>

*層級* \[在\]
</dt> <dd>

結構層級。 此值必須是1。

</dd> <dt>

*pPrintProcessorInfo* \[擴展\]
</dt> <dd>

接收路徑之緩衝區的指標。 請注意，如果是 Windows Server 2003 SP 1 之前的作業系統，則路徑是伺服器的本機格式，而不是真正的遠端格式。 例如，路徑會被指定為「% Windir% System32 多工 \\ \\ 緩衝處理 \\ Prtprocs \\ % 環境%」，而不是「 \\ \\ ServerName \\ Print $ \\ Prtprocs \\ % 環境%」，即使是針對遠端伺服器呼叫也是一樣。 若是 Windows Server 2003 SP 1 和更新版本的作業系統，則會傳回真正的遠端路徑。

</dd> <dt>

*cbBuf* \[在\]
</dt> <dd>

*PPrintProcessorInfo* 所指向的緩衝區大小。

</dd> <dt>

*pcbNeeded* \[擴展\]
</dt> <dd>

值的指標，指定函式成功時所複製的位元組數目，或者，如果 *cbBuf* 太小，則為所需的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **GetPrintProcessorDirectoryW** (Unicode) 和 **GetPrintProcessorDirectoryA** (ANSI) <br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPrintProcessor**](addprintprocessor.md)
</dt> </dl>

 

 




