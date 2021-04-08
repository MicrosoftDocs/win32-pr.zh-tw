---
description: 顯示對話方塊，其中包含已簽署訊息的簽署者資訊。
ms.assetid: e4552cbb-90f4-46f4-a271-3a91ccd5f806
title: CryptUIDlgViewSignerInfo 函式
ms.topic: reference
ms.date: 05/29/2020
ms.openlocfilehash: 7ae677692b9266893eabf1002039c5efbf0ca5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847887"
---
# <a name="cryptuidlgviewsignerinfo-function"></a>CryptUIDlgViewSignerInfo 函式

\[**CryptUIDlgViewSignerInfo** 函式可用於 [需求] 區段中指定的作業系統。 它在後續版本中可能會變更或無法使用。 \]

**CryptUIDlgViewSignerInfo** 函式會顯示一個對話方塊，其中包含已簽署訊息的簽署者資訊。

> [!Note]  
> 未在已發行的標頭檔中宣告此函式。 若要使用此結構，請使用所示的確切格式來宣告。

## <a name="syntax"></a>語法


```C++
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcvsi* \[在\]
</dt> <dd>

[**CRYPTUI \_ VIEWSIGNERINFO \_ 結構**](cryptui-viewsignerinfo-struct.md)結構的指標，其中包含要顯示的簽署者資訊。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式會在成功時傳回非零值，並在失敗時傳回零。 如需擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 函數。

從 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) 傳回的可能錯誤碼包括但不限於下列各項。



| 傳回碼                                                                                   | Description                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 一或多個引數無效。<br/>  |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 發生記憶體配置失敗。<br/> |

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                        |
| 結束支援<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                       |
| 程式庫<br/>                  | <dl> <dt>Cryptui .lib</dt> </dl>      |
| DLL<br/>                      | <dl> <dt>Cryptui.dll</dt> </dl>      |
| Unicode 與 ANSI 名稱<br/>   | **CryptUIDlgViewSignerInfoW** (Unicode) 和 **CryptUIDlgViewSignerInfoA** (ANSI) <br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CRYPTUI \_ VIEWSIGNERINFO \_ 結構**](cryptui-viewsignerinfo-struct.md)
</dt> </dl>
