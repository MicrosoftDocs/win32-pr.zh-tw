---
description: CommitSpoolData 函式會通知列印多工緩衝處理器，指定的資料量已寫入指定的多工緩衝處理檔案，而且已準備好可供轉譯。
ms.assetid: cb8899e0-2fdf-4928-adff-17ef5af39f63
title: 'CommitSpoolData 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CommitSpoolData
api_type:
- DllExport
api_location:
- WinSpool.drv
ms.openlocfilehash: fa90cb1344e7c087a601a74991598e509daed226
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849112"
---
# <a name="commitspooldata-function"></a>CommitSpoolData 函式

**CommitSpoolData** 函式會通知列印多工緩衝處理器，指定的資料量已寫入指定的多工緩衝處理檔案，而且已準備好可供轉譯。

## <a name="syntax"></a>語法


```C++
HANDLE CommitSpoolData(
  _In_ HANDLE hPrinter,
  _In_ HANDLE hSpoolFile,
       DWORD  cbCommit
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hPrinter* \[在\]
</dt> <dd>

提交工作之印表機的控制碼。 這應該是用來取得 *hSpoolFile* with [**GetSpoolFileHandle**](getspoolfilehandle.md)的相同控制碼。

</dd> <dt>

*hSpoolFile* \[在\]
</dt> <dd>

要變更之多工緩衝處理檔案的控制碼。 在第一次呼叫 **CommitSpoolData** 時，這應該與 [**GetSpoolFileHandle**](getspoolfilehandle.md)所傳回的控制碼相同。 對 **CommitSpoolData** 的後續呼叫應該傳遞先前呼叫所傳回的控制碼。 請參閱＜備註＞。

</dd> <dt>

*cbCommit* 
</dt> <dd>

認可至列印多工緩衝處理器的位元組數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，它會將控制碼傳回至多工緩衝處理檔案。

如果函式失敗，則會傳回不正確 \_ 控制碼 \_ 值。

## <a name="remarks"></a>備註

提交多工緩衝處理器列印工作的應用程式可以呼叫 [**GetSpoolFileHandle**](getspoolfilehandle.md) ，然後藉由呼叫 [**WriteFile**](/windows/desktop/api/fileapi/nf-fileapi-writefile)，直接將資料寫入多工緩衝處理檔案控制代碼。 若要通知「列印多工緩衝處理器」檔案包含可供轉譯的資料，應用程式必須呼叫 **CommitSpoolData** 並提供可用的位元組數目。

如果呼叫 **CommitSpoolData** 多次，則每次呼叫都必須使用先前呼叫所傳回的多工緩衝處理檔案控制代碼。 如果不再將任何資料寫入多工緩衝處理檔案，則應該針對上次呼叫 **CommitSpoolData** 所傳回的檔案控制代碼呼叫 [**CloseSpoolFileHandle**](closespoolfilehandle.md) 。

在呼叫 **CommitSpoolData** 之前，應用程式必須將檔案指標設定為將資料寫入檔案之前的位置。 在以多工緩衝處理器檔案轉譯資料的過程中，列印多工緩衝處理器會將多工緩衝處理檔案指標從目前的檔案指標值移至 *cbCommit* 位元組。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**GetSpoolFileHandle**](getspoolfilehandle.md)
</dt> <dt>

[**CloseSpoolFileHandle**](closespoolfilehandle.md)
</dt> </dl>

 

