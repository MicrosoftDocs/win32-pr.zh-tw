---
description: 載入 Apphelp 資源檔。
ms.assetid: fca50e00-9324-410a-a572-69441f332593
title: SdbOpenApphelpResourceFile 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpResourceFile
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: ab865a29e0879119ca50cf4177aa7649bd82a83e70c07e1b7068a5d8fcd2cc30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120044988"
---
# <a name="sdbopenapphelpresourcefile-function"></a>SdbOpenApphelpResourceFile 函式

載入 Apphelp 資源檔。

## <a name="syntax"></a>語法


```C++
HMODULE WINAPI SdbOpenApphelpResourceFile(
  _In_opt_ LPCWSTR pwszACResourceFile
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pwszACResourceFile* \[在中，選擇性\]
</dt> <dd>

資源檔的路徑。 如果此參數為 **Null**，則會開啟本機資源 DLL。

</dd> </dl>

## <a name="return-value"></a>傳回值

函式會將控制碼傳回至已開啟的資源檔。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




