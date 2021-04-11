---
description: DeletePort 函式會顯示一個對話方塊，可讓使用者刪除埠名稱。
ms.assetid: 5f5788c2-c781-4106-abd2-98556d0a22de
title: 'DeletePort 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeletePort
- DeletePortA
- DeletePortW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: fa0e3d4b0b5fd43d946d0b6a96b96d0494997a3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193617"
---
# <a name="deleteport-function"></a>DeletePort 函式

**DeletePort** 函式會顯示一個對話方塊，可讓使用者刪除埠名稱。

## <a name="syntax"></a>語法


```C++
BOOL DeletePort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pPortName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以零結束的字串指標，指定應刪除其埠之伺服器的名稱。 如果此參數為 **Null**，則會刪除本機埠。

</dd> <dt>

*hWnd* \[在\]
</dt> <dd>

埠刪除對話方塊之父視窗的控制碼。

</dd> <dt>

*pPortName* \[在\]
</dt> <dd>

以零結束的字串指標，指定應該刪除的埠名稱。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

應用程式可以藉由呼叫 [**EnumPorts**](enumports.md) 函式來取得有效埠的名稱。

如果印表機目前連接到指定的埠， **DeletePort** 函數會傳回錯誤。

**DeletePort** 函式的呼叫端必須具有伺服器 \_ 存取權 \_ ，才能存取埠所連接的伺服器。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl>                   |
| Unicode 與 ANSI 名稱<br/>   | **DeletePortW** (Unicode) 和 **DeletePortA** (ANSI) <br/>                                           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**AddPort**](addport.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> </dl>

 

 




