---
description: 抓取指定檔案的屬性資料。
ms.assetid: 899b4af3-8185-4ce5-8e81-05ec3a446e42
title: SdbGetFileAttributes 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetFileAttributes
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: a75dd64bfbeaf027839c63227c594ada7602101d059cbbd9d10deb085152918d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120103648"
---
# <a name="sdbgetfileattributes-function"></a>SdbGetFileAttributes 函式

抓取指定檔案的屬性資料。

## <a name="syntax"></a>語法


```C++
BOOL WINAPI SdbGetFileAttributes(
  _In_  LPCTSTR   lpwszFileName,
  _Out_ PATTRINFO *ppAttrInfo,
  _Out_ LPDWORD   lpdwAttrCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lpwszFileName* \[在\]
</dt> <dd>

檔案的路徑。

</dd> <dt>

*ppAttrInfo* \[擴展\]
</dt> <dd>

[**ATTRINFO**](attrinfo.md)結構的陣列，其中包含屬性資料。

</dd> <dt>

*lpdwAttrCount* \[擴展\]
</dt> <dd>

屬性的數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。

## <a name="remarks"></a>備註

當您完成資料時，請使用 [**SdbFreeFileAttributes**](sdbfreefileattributes.md) 函數釋出資料。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> </dl>

 

 




