---
description: 在指定的索引中尋找符合指定準則的第一個 DWORD 記錄。
ms.assetid: 81302f84-497d-4fef-b348-eee2a53284c7
title: SdbFindFirstDWORDIndexedTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbFindFirstDWORDIndexedTag
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 4f3c9290f98fb24d856561114bc654da0315c5a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510365"
---
# <a name="sdbfindfirstdwordindexedtag-function"></a>SdbFindFirstDWORDIndexedTag 函式

在指定的索引中尋找符合指定準則的第一個 **DWORD** 記錄。

## <a name="syntax"></a>語法


```C++
TAGID WINAPI SdbFindFirstDWORDIndexedTag(
  _In_  PDB       pdb,
  _In_  TAG       tWhich,
  _In_  TAG       tKey,
  _In_  DWORD     dwName,
  _Out_ FIND_INFO *pFindInfo
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pdb* \[在\]
</dt> <dd>

填充碼資料庫的控制碼。

</dd> <dt>

*tWhich* \[在\]
</dt> <dd>

索引類型。 如需值清單，請參閱 [**標記**](tag.md) 。

</dd> <dt>

*tKey* \[在\]
</dt> <dd>

索引鍵類型。

</dd> <dt>

*dwName* \[在\]
</dt> <dd>

要尋找的資料名稱。 此值將會轉換為索引鍵。

</dd> <dt>

*pFindInfo* \[擴展\]
</dt> <dd>

接收記錄的 [**尋找 \_ 資訊**](find-info.md) 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

第一個相符項的 **TAGID** ，如果找不到相符的標記，則 **\_ 為 Null** 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**SdbFindFirstTag**](sdbfindfirsttag.md)
</dt> </dl>

 

 




