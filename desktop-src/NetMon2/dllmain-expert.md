---
description: 專家會實作為 DllMain 函數。 作業系統會呼叫 DllMain 來取得專家實例的控制碼。
ms.assetid: 38593ba0-dc37-4620-bb49-2e50c3d9ea3c
title: 'DllMain 專家回呼函數 (Process .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DllMain
api_type:
- UserDefined
api_location:
- process.h
ms.openlocfilehash: 914f50b75e83fdc67448770b32ac8d0f8e8ab656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850155"
---
# <a name="dllmain-expert-callback-function"></a>DllMain 專家回呼函數

專家會實作為 [**DllMain**](/windows/desktop/Dlls/dllmain) 函數。 作業系統會呼叫 **DllMain** 來取得專家實例的控制碼。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI DllMain(
  _Out_ HINSTANCE hInstance,
  _In_  ULONG     ulReason,
        LPVOID    Reserved
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hInstance* \[擴展\]
</dt> <dd>

專家實例的控制碼。

如果專家使用網路監視器的使用者介面， *hInstance* 值就必須儲存在全域變數中。 只有當 *ulReason* 參數的值設定為 DLL 進程附加時，才需要這個 \_ 方法 \_ 。

</dd> <dt>

*ulReason* \[在\]
</dt> <dd>

呼叫函數的原因指標。 DLL \_ 進程附加的值 \_ ， (在第一次載入 dll 時套用) 指出專家應該將 *hInstance* 值儲存在全域變數中。

使用任何其他值，就可以忽略 [**DllMain**](/windows/desktop/Dlls/dllmain) 函數的所有呼叫。 如需作業系統所設定之所有可能旗標的清單，請參閱 **DLLMain**。

</dd> <dt>

*已保留* 
</dt> <dd>

參數未使用中。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為 **TRUE**。

如果函式不成功，則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

當進程載入或卸載專家 DLL 時，作業系統會呼叫 **DllMain** 專家功能。 只有當專家的使用者介面可以用來查看設定或結果，然後只傳回適當的 *hInstance* 值時，才必須匯出 **DllMain** 專家函式。

**DllMain** 專家函式是以動態連結程式庫 [**DllMain**](/windows/desktop/Dlls/dllmain)函數為基礎。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>處理。h</dt> </dl> |



 

