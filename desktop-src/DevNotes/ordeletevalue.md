---
description: 從離線登錄區的指定登錄機碼中移除指定的值。
ms.assetid: d2192607-34b8-4915-ac86-8ee206993071
title: 'ORDeleteValue 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteValue
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 717464b1ba44593a9b36ccf26e5df248cb95df9bfa40a7786896c87041e246d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045288"
---
# <a name="ordeletevalue-function"></a>ORDeleteValue 函式

從離線登錄區的指定登錄機碼中移除指定的值。

## <a name="syntax"></a>語法


```C++
DWORD ORDeleteValue(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpValueName
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*控制碼* \[在\]
</dt> <dd>

離線登錄 hive 中開啟登錄機碼的控制碼。

</dd> <dt>

*lpValueName* \[在中，選擇性\]
</dt> <dd>

要移除的登錄值。 如果此參數為 **Null** 或空字串，則會移除 [**ORSetValue**](orsetvalue.md) 函數所設定的預設未命名值。

值名稱不區分大小寫。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。 您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|---------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows離線登錄庫1.0 版或更新版本<br/>                      |
| 標頭<br/>          | <dl> <dt>Offreg。h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORSetValue**](orsetvalue.md)
</dt> </dl>

 

 
