---
description: GetPrintExecutionData 會捕獲目前的列印內容。
ms.assetid: bb9506aa-a0da-46bc-a86a-84a79587cd50
title: 'GetPrintExecutionData 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetPrintExecutionData
api_type:
- DllExport
api_location:
- winspool.drv
ms.openlocfilehash: 0bbe08e82fb8f753d6e4fd23776618cb5f555b390434fdd0feddd231aaebc635
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971347"
---
# <a name="getprintexecutiondata-function"></a>GetPrintExecutionData 函式

**GetPrintExecutionData** 會捕獲目前的列印內容。

> [!Note]  
> 這項功能的目的是要供在列印多工緩衝處理器內容中執行的印表機驅動程式使用。

 

## <a name="syntax"></a>語法


```C++
BOOL WINAPI GetPrintExecutionData(
  _Out_ PRINT_EXECUTION_DATA *pData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*.pdata* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收 [**列印 \_ 執行 \_ 資料**](print-execution-data.md) 結構的位址。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回 **TRUE** ;否則 **為 FALSE**。 如果傳回值為 **FALSE**，則呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) 以取得錯誤狀態。

## <a name="remarks"></a>備註

印表機驅動程式應該呼叫 winspool.drv. winspool.drv 模組上的 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)來取得 **GetPrintExecutionData** 函式的位址，因為 Windows Vista 或舊版的 Windows 不支援 **GetPrintExecutionData** 。

只有當 *.pdata* 的值為 **Null** 時， **GetPrintExecutionData** 才會失敗。

只有當 **coNtext** 的值是 **列印 \_ 執行 \_ 內容 \_ WOW64** 時，[**列印 \_ 執行 \_ 資料**](print-execution-data.md)的 **clientAppPID** 成員值才有意義。 如果 **內容** 的值不是 **列印 \_ 執行 \_ 內容 \_ WOW64**，則 **clientAppPID** 的值為0。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                                |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**3]。Getlasterror**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)
</dt> <dt>

[**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[**列印 \_ 執行 \_ 內容**](print-execution-context.md)
</dt> <dt>

[**列印 \_ 執行 \_ 資料**](print-execution-data.md)
</dt> </dl>

 

