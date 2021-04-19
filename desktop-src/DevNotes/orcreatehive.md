---
description: 建立包含單一空根金鑰的離線登錄 hive。
ms.assetid: 985cfea4-6f15-4d63-8e41-df2a490296a3
title: 'ORCreateHive 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCreateHive
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 47454169bee21012010fd7deacec6c1faf3a7d8d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987914"
---
# <a name="orcreatehive-function"></a>ORCreateHive 函式

建立包含單一空根金鑰的離線登錄 hive。

## <a name="syntax"></a>語法


```C++
DWORD ORCreateHive(
  _Out_ PORHKEY phkResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*phkResult* \[擴展\]
</dt> <dd>

指向變數，以接收新建立之離線登錄 hive 的根目錄控制碼。 如果無法建立 hive，此函式會將此參數設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。 您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。

如果記憶體不足，無法建立登錄區，則函式會傳回錯誤 \_ 的 \_ \_ 記憶體不足。

## <a name="remarks"></a>備註

**ORCreateHive** 函式會在記憶體中建立空白的離線登錄 hive。 使用 [**ORCreateKey**](orcreatekey.md) 和 [**ORSetValue**](orsetvalue.md) 函式來新增索引鍵並設定其值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|---------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows Offline Registry library 1.0 版或更新版本<br/>                      |
| 標頭<br/>          | <dl> <dt>Offreg。h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OROpenHive**](oropenhive.md)
</dt> <dt>

[**ORSaveHive**](orsavehive.md)
</dt> <dt>

[**ORSetValue**](orsetvalue.md)
</dt> </dl>

 

 
