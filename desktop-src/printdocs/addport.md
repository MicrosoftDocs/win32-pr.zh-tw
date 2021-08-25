---
description: AddPort 函式會將埠的名稱新增至支援的埠清單。 AddPort 函數是由埠監視器匯出。
ms.assetid: 9191d507-9167-4488-a4b4-286590a8a62a
title: 'AddPort 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddPort
- AddPortA
- AddPortW
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: abbb2e4b836c64ddff47c92681e32bd0d5f9f0c38224d6c710fb10bc3435ac96
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112688"
---
# <a name="addport-function"></a>AddPort 函式

**AddPort** 函式會將埠的名稱新增至支援的埠清單。 **AddPort** 函數是由埠監視器匯出。

## <a name="syntax"></a>語法


```C++
BOOL AddPort(
  _In_ LPTSTR pName,
  _In_ HWND   hWnd,
  _In_ LPTSTR pMonitorName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pName* \[在\]
</dt> <dd>

以零結束的字串指標，指定埠所連接的伺服器名稱。 如果此參數為 **Null**，則埠為本機。

</dd> <dt>

*hWnd* \[在\]
</dt> <dd>

**AddPort** 對話方塊父視窗的控制碼。

</dd> <dt>

*pMonitorName* \[在\]
</dt> <dd>

以零結束的字串指標，指定與埠相關聯的監視器。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為非零值。

如果此函式失敗，則傳回值為零。

## <a name="remarks"></a>備註

> [!Note]  
> 這是封鎖或同步函式，可能不會立即傳回。 此函式傳回的速度，取決於執行時間因素，例如網路狀態、列印伺服器設定，以及在撰寫應用程式時難以預測的印表機驅動程式執行因素。 從管理與使用者介面互動的執行緒呼叫這個函式，可能會讓應用程式看起來沒有回應。

 

**AddPort** 函式會流覽網路以尋找現有的埠，並顯示使用者的對話方塊。 **AddPort** 函式應藉由呼叫 [**EnumPorts**](enumports.md)來驗證使用者輸入的埠名稱，以確保沒有重複的名稱存在。

**AddPort** 函式的呼叫端必須具有伺服器 \_ 存取權 \_ ，才能存取埠所連接的伺服器。

若要在不顯示對話方塊的情況下新增埠，請呼叫 **XcvData** 函式，而不是 **AddPort**。 如需有關 **XcvData** 的詳細資訊，請參閱 Microsoft Windows 驅動程式開發工具組 (DDK) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Spoolss.dll</dt> </dl>                    |
| Unicode 與 ANSI 名稱<br/>   | **AddPortW** (Unicode) 和 **AddPortA** (ANSI) <br/>                                                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**DeletePort**](deleteport.md)
</dt> <dt>

[**EnumPorts**](enumports.md)
</dt> <dt>

[**SetPort**](setport.md)
</dt> </dl>

 

 




