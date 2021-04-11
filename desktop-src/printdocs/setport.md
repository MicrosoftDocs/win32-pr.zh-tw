---
description: SetPort 函式會設定與印表機埠相關聯的狀態。
ms.assetid: 1b80ad93-aaa1-41ed-a668-a944fa62c3eb
title: 'SetPort 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetPort
- SetPortA
- SetPortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: ab986128c9561b7b95de668367cafb0b3e6cd636
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026700"
---
# <a name="setport-function"></a>SetPort 函式

**SetPort** 函式會設定與印表機埠相關聯的狀態。

## <a name="syntax"></a>語法


```C++
BOOL SetPort(
  _In_ LPTSTR pName,
  _In_ LPTSTR pPortName,
  _In_ DWORD  dwLevel,
  _In_ LPBYTE pPortInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以零結尾的字串指標，指定埠所連接之印表機伺服器的名稱。 如果埠是在本機電腦上，請將此參數設定為 **Null** 。

</dd> <dt>

*pPortName* \[在\]
</dt> <dd>

指定印表機埠名稱之以零結尾的字串指標。

</dd> <dt>

*dwLevel* \[在\]
</dt> <dd>

指定 *pPortInfo* 參數所指向的結構類型。

此值必須是3，其對應至 [**埠 \_ 資訊 \_ 3**](port-info-3.md) 資料結構。

</dd> <dt>

*pPortInfo* \[在\]
</dt> <dd>

[**埠 \_ 資訊 \_ 3**](port-info-3.md)結構的指標，其中包含要設定的埠狀態資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

**SetPort** 函數的呼叫者必須以系統管理員身分執行。 此外，如果呼叫端是埠監視器或語言監視器，它必須在呼叫 **SetPort** 之前呼叫 [**RevertToSelf**](/windows/desktop/api/securitybaseapi/nf-securitybaseapi-reverttoself)來停止模擬。

呼叫 **SetPort** 的所有程式都必須擁有伺服器存取權， \_ \_ 才能存取埠所連接的伺服器。

當您設定 [印表機埠狀態值] 的 [嚴重性值埠 \_ 狀態 \_ 類型] \_ 錯誤時，列印多工緩衝處理器會停止將作業傳送至埠。 當其他 **SetPort** 呼叫清除埠狀態時，列印多工緩衝處理器會繼續將作業傳送至埠。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **SetPortW** (Unicode) 和 **SetPortA** (ANSI) <br/>                                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**埠 \_ 資訊 \_ 3**](port-info-3.md)
</dt> </dl>

 

