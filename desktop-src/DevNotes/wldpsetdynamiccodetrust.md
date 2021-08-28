---
description: 為 .NET 設定磁片上的 .NET CRL 動態程式碼信任。
ms.assetid: 4C8C3EF5-5C3C-4710-8223-D7B5BA86EF47
title: 'WldpSetDynamicCodeTrust 函式 (Wldp) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WldpSetDynamicCodeTrust
api_type:
- DllExport
api_location:
- wldp.dll
ms.openlocfilehash: 5a7277f13596ff3d397c97c8e8260e57e0e444e6943ba68f073f90c90cf3583d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119075638"
---
# <a name="wldpsetdynamiccodetrust-function"></a>WldpSetDynamicCodeTrust 函式

為 .NET 設定磁片上的 .NET CRL 動態程式碼信任。

## <a name="syntax"></a>語法


```C++
HRESULT WINAPI WldpSetDynamicCodeTrust(
   HANDLE FileHandle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*FileHandle* 
</dt> <dd>

磁片上動態程式碼檔案的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

**如果成功，則 \_ 此** 方法會傳回，否則會傳回失敗碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1803版桌面應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Wldp。h</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Wldp.dll</dt> </dl> |



 

 




