---
description: 判斷 Unicode 字串是否符合指定的模式。
ms.assetid: 9b220cb8-4402-4094-8209-59a9af004b4a
title: RtlIsNameInExpression 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsNameInExpression
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ac6142b364a135b62505841963fa799ce6603dbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972126"
---
# <a name="rtlisnameinexpression-function"></a>RtlIsNameInExpression 函式

判斷 Unicode 字串是否符合指定的模式。

## <a name="syntax"></a>語法


```C++
 BOOLEAN  RtlIsNameInExpression(
  _In_     PUNICODE_STRING Expression,
  _In_     PUNICODE_STRING Name,
  _In_     BOOLEAN         IgnoreCase,
  _In_opt_ PWCH            UpcaseTable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*運算式* \[在\]
</dt> <dd>

模式字串的指標。 這個字串可以包含萬用字元。 如果 *IgnoreCase* 參數為 TRUE，則字串必須只包含大寫字元。

</dd> <dt>

*名稱* \[在\]
</dt> <dd>

要與模式比較之字串的指標。 這個字串不能包含萬用字元。

</dd> <dt>

*IgnoreCase* \[在\]
</dt> <dd>

**如果** 不區分大小寫比對，則為 TRUE，如果區分大小寫比對，則為 **FALSE** 。

</dd> <dt>

*UpcaseTable* \[在中，選擇性\]
</dt> <dd>

大寫字元資料表的選擇性指標，用於不區分大小寫比對。 如果此參數為 Null，則會使用預設系統大寫字元資料表。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果字串符合模式，則傳回 **TRUE** 。 如果字串不符合模式，則此函式會傳回 **FALSE**。

## <a name="remarks"></a>備註

此函數沒有相關聯的標頭檔。 相關聯的匯入程式庫（Ntdll.dll）可在 Microsoft Windows 驅動程式套件 (WDK) 中取得。 您也可以使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函式來呼叫這個函式，以動態連結至 Ntdll.dll。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                              |
| DLL<br/>                      | <dl> <dt>Ntdll.dll</dt> </dl> |



 

 
