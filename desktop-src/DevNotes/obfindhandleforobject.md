---
description: 抓取與指定進程相關聯之指定物件的物件控制碼。
ms.assetid: c7b371c3-02c0-4137-ad9d-dd07a74fe2a5
title: 'ObFindHandleForObject 函式 (Ntosp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ObFindHandleForObject
api_type:
- LibDef
api_location:
- Ntoskrnl.lib
- Ntoskrnl.dll
ms.openlocfilehash: 7ba87d05d4264f3bb160bae16053a338e38e2145
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847126"
---
# <a name="obfindhandleforobject-function"></a>ObFindHandleForObject 函式

\[此函式已過時，可能會在未來的 Windows 版本中變更或無法使用。 請避免使用此函數。\]

抓取與指定進程相關聯之指定物件的物件控制碼。

## <a name="syntax"></a>語法


```C++
BOOLEAN WINAPI ObFindHandleForObject(
  _In_     PEPROCESS Process,
  _In_     PVOID     Object,
  _In_opt_ PVOID     Reserved1,
  _In_opt_ PVOID     Reserved2,
  _Out_    PHANDLE   Handle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*進程* \[在\]
</dt> <dd>

處理序。 **IoGetCurrentProcess** 或 **PsGetCurrentProcess** 函數會傳回此控制碼。

</dd> <dt>

*物件* \[在\]
</dt> <dd>

物件的指標。

</dd> <dt>

*Reserved1* \[在中，選擇性\]
</dt> <dd>

保留的。

</dd> <dt>

*Reserved2* \[在中，選擇性\]
</dt> <dd>

保留的。

</dd> <dt>

*控制碼* \[擴展\]
</dt> <dd>

物件控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果找到相符的函式，則函式會傳回 **TRUE** ，否則會傳回 **FALSE** 。

## <a name="remarks"></a>備註

此函式可在 Ntoskrnl.exe 中取得，而且只能從核心模式中呼叫。 對應的匯入程式庫可透過 Windows 驅動程式套件 (WDK) 取得。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Ntosp。h</dt> </dl>      |
| 程式庫<br/>                  | <dl> <dt>Ntoskrnl.exe .lib</dt> </dl> |



 

 




