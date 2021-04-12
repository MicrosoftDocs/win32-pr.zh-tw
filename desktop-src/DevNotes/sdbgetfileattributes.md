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
ms.openlocfilehash: 651b9af34afdd2ffd767eba7ca4467ecfee081cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104109917"
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
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbFormatAttribute**](sdbformatattribute.md)
</dt> <dt>

[**SdbFreeFileAttributes**](sdbfreefileattributes.md)
</dt> </dl>

 

 




