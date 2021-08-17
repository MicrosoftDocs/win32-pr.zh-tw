---
description: 啟用或停用磁片磁區的讀取和寫入。
ms.assetid: 885e4db1-a131-4727-80ab-3be8c591b766
title: FveEnableRawAccessW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FveEnableRawAccessW
api_type:
- DllExport
api_location:
- Fveapi.dll
ms.openlocfilehash: 050983663b782d40c330092919b8fc29060cbba057a16d147b80c6ea477cbf54
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956087"
---
# <a name="fveenablerawaccessw-function"></a>FveEnableRawAccessW 函式

啟用或停用磁片磁區的讀取和寫入。

## <a name="syntax"></a>語法


```C++
HRESULT FveEnableRawAccessW(
  _In_ PCWSTR VolumeName,
  _In_ BOOL   Enabled
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*VolumeName* \[在\]
</dt> <dd>

磁片區的唯一識別碼。

</dd> <dt>

*已啟用* \[在\]
</dt> <dd>

若 **為 TRUE**，則允許存取原始磁片區。 如果 **為 FALSE**，則不允許對未經處理的磁片區進行存取。 如果已啟用原始存取，但此值為 **FALSE**，則磁片區會重新掛接和重新驗證。

</dd> </dl>

## <a name="return-value"></a>傳回值

此函式會傳回下列其中一個程式碼，如果失敗，則傳回另一個錯誤碼。



| 傳回碼/值                                                                                                                                                           | 描述                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> <dt>0 (0x0)</dt> </dl>                           | 函數成功。<br/>                                            |
| <dl> <dt>**S \_FALSE**</dt> <dt>1 (0x1)</dt> </dl>                        | Enabled 為 **FALSE** ，且磁片區尚未處於原始存取模式。<br/> |
| <dl> <dt>**E \_ACCESSDENIED**</dt> <dt>2147942405 (0x80070005)</dt> </dl> | 無法鎖定磁片區。<br/>                                            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                  |
| DLL<br/>                      | <dl> <dt>Fveapi.dll</dt> </dl> |



 

 




