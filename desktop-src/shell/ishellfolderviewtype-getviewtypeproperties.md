---
description: 取得視圖的屬性。
title: IShellFolderViewType：： GetViewTypeProperties 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType.GetViewTypeProperties
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 82be6bd5-a46c-48b3-a1f0-a92b9454c35e
ms.openlocfilehash: f5c7c6b75c89711a69ac578b3d04a72362b1eac9
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842699"
---
# <a name="ishellfolderviewtypegetviewtypeproperties-method"></a>IShellFolderViewType：： GetViewTypeProperties 方法

取得視圖的屬性。

## <a name="syntax"></a>語法


```C++
HRESULT GetViewTypeProperties(
  [in]  PCUITEMID_CHILD pidl,
  [out] DWORD           *pdwFlags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pidl* \[在\]
</dt> <dd>

類型： **PCUITEMID \_ 子** 系

PIDL。

</dd> <dt>

*pdwFlags* \[擴展\]
</dt> <dd>

類型： **DWORD \***

不帶正負號整數變數的指標，此變數會接收 view 屬性，表示選取視圖時該怎麼辦。 旗標可以是下列值的任何組合。

<dt>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>

<span id="SFVTFLAG_NOTIFY_CREATE"></span><span id="sfvtflag_notify_create"></span>**SFVTFLAG \_通知 \_ CREATE** (0x00000001) 


</dt> <dd>

建立視圖專案（如果沒有的話）。

</dd> <dt>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>

<span id="SFVTFLAG_NOTIFY_RESORT"></span><span id="sfvtflag_notify_resort"></span>**SFVTFLAG \_通知 \_ 手段** (0x00000002) 


</dt> <dd>

重新插入 PIDL 並重新排序。

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Shell32.dll</dt> </dl> |



 

 




