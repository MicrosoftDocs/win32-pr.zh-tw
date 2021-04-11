---
description: 檢查是否已載入線上使用者設定檔。
ms.assetid: 4391664E-44D0-461D-84FF-E2B2410511BC
title: 'OnProfileLoaded 函式 (Lsaidprov) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnProfileLoaded
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: cff9056ab5ea5437bb37da9b3c01368127db11cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692931"
---
# <a name="onprofileloaded-function"></a>OnProfileLoaded 函式

檢查是否已載入線上使用者設定檔。

## <a name="syntax"></a>語法


```C++
SEC_ENTRY OnProfileLoaded(
  _In_ PVOID   ProviderHandle,
  _In_ HANDLE  UserToken,
  _In_ BOOLEAN Loaded
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ProviderHandle* \[在\]
</dt> <dd>

提供者控制碼。

</dd> <dt>

*UserToken* \[在\]
</dt> <dd>

正在載入或卸載其設定檔的使用者 Token。

</dd> <dt>

已 *載入* \[在\]
</dt> <dd>

如果已載入設定檔，**則為 TRUE** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，函數會傳回狀態 \_ SUCCESS。

如果函式失敗，函式會傳回非零的錯誤碼，此錯誤碼為診斷目的提供者特有的錯誤。

## <a name="remarks"></a>備註

每次呼叫 [**LoadUserProfile**](/windows/win32/api/userenv/nf-userenv-loaduserprofilea) 函數時，就會呼叫此函式。 它不會與 **LoadUserProfile** 同步;也就是說， **LoadUserProfile** 可能已傳回，而且設定檔可能會在呼叫函式時卸載。 即使已載入設定檔，也可以多次呼叫這個函數。 身分識別提供者不能假設 *載入* 等於 TRUE 的這個函式的呼叫，後面會接著 *載入* 等於 FALSE 的呼叫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                   |
| 標頭<br/>                   | <dl> <dt>Lsaidprov。h</dt> </dl> |



 

 
