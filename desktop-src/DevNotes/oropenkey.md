---
description: 在離線登錄 hive 中開啟指定的登錄機碼。
ms.assetid: 4a4afbef-5107-4006-bd67-aecb5d3b5112
title: 'OROpenKey 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 4c0f641925fbc35fba6072ee395f67fad540dcd2ec5198b945ad658a723238b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667091"
---
# <a name="oropenkey-function"></a>OROpenKey 函式

在離線登錄 hive 中開啟指定的登錄機碼。

## <a name="syntax"></a>語法


```C++
DWORD OROpenKey(
  _In_     ORHKEY  Handle,
  _In_opt_ PCWSTR  lpSubKeyName,
  _Out_    PORHKEY phkResult
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*控制碼* \[在\]
</dt> <dd>

離線登錄 hive 中開啟登錄機碼的控制碼。

</dd> <dt>

*lpSubKeyName* \[在中，選擇性\]
</dt> <dd>

UNICODE 字串的指標，其中包含要開啟的登錄機碼名稱。 此索引鍵必須是 *控制碼* 參數所識別之機碼的子機碼。

索引鍵名稱不區分大小寫。

如果此參數為 **Null** 或空字串的指標，則函數會傳回傳入的相同控制碼。 如果 *Handle* 參數所指定的索引鍵是 hive 的根金鑰，則函式會傳回錯誤 \_ 不正確 \_ 參數。

如需詳細資訊，請參閱登錄 [元素大小限制](../sysinfo/registry-element-size-limits.md)。

</dd> <dt>

*phkResult* \[擴展\]
</dt> <dd>

變數的指標，此變數會接收開啟之索引鍵的控制碼。 當您完成使用控制碼之後，請使用 [**ORCloseKey**](orclosekey.md) 函數來關閉金鑰。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果函式成功，則傳回值為「錯誤 \_ 成功」。

如果函式失敗，則傳回值為 Winerror.h 中定義的非零錯誤碼。 您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。

如果要傳回的控制碼會是 hive 根金鑰的控制碼，則函式會傳回錯誤不正確 \_ \_ 參數。

如果指定的索引鍵已標示為已刪除，則此函式會傳回已刪除的錯誤索引 \_ 鍵 \_ 。

## <a name="remarks"></a>備註

**OROpenKey** 函式不能用來開啟離線登錄區中的根機碼。 若要取得 hive 根金鑰的控制碼，請使用 [**OROpenHive**](oropenhive.md) 函式將 hive 載入記憶體中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------------|---------------------------------------------------------------------------------------|
| 可轉散發套件<br/> | Windows離線登錄庫1.0 版或更新版本<br/>                      |
| 標頭<br/>          | <dl> <dt>Offreg。h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenHive**](oropenhive.md)
</dt> </dl>

 

 
