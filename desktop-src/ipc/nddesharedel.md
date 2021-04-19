---
description: 從 DDE 共用資料庫管理員刪除 DDE 共用 (DSDM) 。
ms.assetid: 3240f4b1-2625-46bc-9bbe-27737c59df81
title: 'NDdeShareDel 函式 (Nddeapi) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDdeShareDel
- NDdeShareDelA
- NDdeShareDelW
api_type:
- DllExport
api_location:
- Nddeapi.dll
ms.openlocfilehash: 2d57307c157c532e124699b6bfb2ed666f374722
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967078"
---
# <a name="nddesharedel-function"></a>NDdeShareDel 函式

\[不再支援網路 DDE。 Windows Vista 上有 Nddeapi.dll，但是所有的函式呼叫都會傳回 NDDE \_ 未 \_ 執行。\]

從 DDE 共用資料庫管理員刪除 DDE 共用 (DSDM) 。

## <a name="syntax"></a>語法


```C++
UINT NDdeShareDel(
  _In_ LPTSTR lpszServer,
  _In_ LPTSTR lpszShareName,
  _In_ UINT   wReserved
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpszServer* \[在\]
</dt> <dd>

要修改其 DSDM 的伺服器名稱。

</dd> <dt>

*lpszShareName* \[在\]
</dt> <dd>

要從 DSDM 中刪除的共用名稱。 此參數不可以是 **Null**。

</dd> <dt>

*wReserved* \[在\]
</dt> <dd>

保留的。 此參數必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 NDDE \_ NO \_ ERROR。

如果函式失敗，則傳回值是可透過呼叫 [**NDdeGetErrorString**](nddegeterrorstring.md)轉譯成文字錯誤訊息的錯誤碼。

## <a name="remarks"></a>備註

若要從 DSDM 中刪除 DDE 共用，您必須具有適當的許可權。 共用建立者具有刪除許可權。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Nddeapi。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Nddeapi .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Nddeapi.dll</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **NDdeShareDelW** (Unicode) 和 **NDdeShareDelA** (ANSI) <br/>                    |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[網路動態資料交換總覽](network-dynamic-data-exchange.md)
</dt> <dt>

[網路 DDE 函數](network-dde-functions.md)
</dt> </dl>

 

 




