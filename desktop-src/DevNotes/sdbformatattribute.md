---
description: 將指定的屬性資料轉換為 XML 格式。
ms.assetid: 7a75726d-f1ec-4137-89c1-eccb4a78fc22
title: SdbFormatAttribute 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFormatAttribute
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 44303a568a9f7775893033edc512e8a916004c43207277e308e1d4826d9f9537
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161551"
---
# <a name="sdbformatattribute-function"></a>SdbFormatAttribute 函式

將指定的屬性資料轉換為 XML 格式。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI SdbFormatAttribute(
  _In_  PATTRINFO pAttrInfo,
  _Out_ LPTSTR    pchBuffer,
  _In_  DWORD     dwBufferSize
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAttrInfo* \[在\]
</dt> <dd>

[**ATTRINFO**](attrinfo.md)結構。

</dd> <dt>

*pchBuffer* \[擴展\]
</dt> <dd>

輸出緩衝區。

</dd> <dt>

*dwBufferSize* \[在\]
</dt> <dd>

*PchBuffer* 緩衝區的大小（以字元為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果緩衝區太小，或找不到屬性，則函式會在成功時傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbGetFileAttributes**](sdbgetfileattributes.md)
</dt> </dl>

 

 




