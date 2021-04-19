---
description: IsValidDevmode 函數會驗證 DEVMODE 結構的內容是否有效。
ms.assetid: 8b4e32cc-5eeb-4a0d-a1b7-f6edb99ed8d8
title: 'IsValidDevmode 函式 (Winspool.drv) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IsValidDevmode
- IsValidDevmodeA
- IsValidDevmodeW
api_type:
- DllExport
api_location:
- Winspool.drv
ms.openlocfilehash: 0b8a940fd08e1ab19b18969a763448b65fffd9d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975300"
---
# <a name="isvaliddevmode-function"></a>IsValidDevmode 函式

**IsValidDevmode** 函數會驗證 DEVMODE 結構的內容是否有效。

## <a name="syntax"></a>語法


```C++
BOOL IsValidDevmode(
  _In_ PDEVMODE pDevmode,
       size_t   DevmodeSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDevmode* \[在\]
</dt> <dd>

要驗證的 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 指標。

</dd> <dt>

*DevmodeSize* 
</dt> <dd>

輸入位元組緩衝區的大小（以位元組為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)在結構上有效，**則為 TRUE**。 如果發現次要錯誤，函數會修正這些錯誤並傳回 **TRUE**。

如果 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)有一或多個明顯的結構化問題，則 **為 FALSE**。 例如，其 **dmSize** 成員未對齊，或指定的緩衝區太小。 此外，如果 **pDevmode** 為 **Null**，則 **為 FALSE** 。

## <a name="remarks"></a>備註

不會檢查 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 的私用印表機驅動程式欄位，只會檢查公用欄位。

 + 只有當呼叫者可以保證輸入緩衝區大小至少為該大小時，才應該使用 dmSize **dmDriverExtra** 進行 **DevmodeSize** 。 由於 [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) 通常是不受信任的資料，因此 **dmSize** 和 **dmDriverExtra** 位移之輸入緩衝區中的值也不受信任。

此函式可在 Least-Privileged 使用者帳戶 (LUA) 內容中執行。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Winspool.drv。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Winspool.drv .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Winspool.drv. winspool.drv</dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **IsValidDevmodeW** (Unicode) 和 **IsValidDevmodeA** (ANSI) <br/>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 函式](printing-and-print-spooler-functions.md)
</dt> <dt>

[**版**](/windows/win32/api/wingdi/ns-wingdi-devmodea)
</dt> </dl>

 

 




