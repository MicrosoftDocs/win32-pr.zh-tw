---
title: 'UtilLoadStringWithAlloc 函式 (Ndattributils) '
description: 從資源資料表配置和載入字串。
ms.assetid: 34bf0b93-2bec-49c3-9441-c83686c4abdb
keywords:
- UtilLoadStringWithAlloc 函式 NDF
topic_type:
- apiref
api_name:
- UtilLoadStringWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ca649599e2a8a29ecdab2dbbfe2c188947b40487ceb82ab4937622ce82c701a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119685608"
---
# <a name="utilloadstringwithalloc-function"></a>UtilLoadStringWithAlloc 函式

**UtilLoadStringWithAlloc** 函式會從資源資料表配置和載入字串。

## <a name="syntax"></a>語法


```C++
HRESULT UtilLoadStringWithAlloc(
  _In_  UINT   uID,
  _Out_ LPWSTR *ppwzBuffer,
  _In_  UINT   cchBufferMax
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*uID* \[在\]
</dt> <dd>

類型： **UINT**

要載入之字串的識別碼。

</dd> <dt>

*ppwzBuffer* \[擴展\]
</dt> <dd>

類型： **LPWSTR \***

將放置新配置之字串的位置。 當您不再需要字串時，必須使用 [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) 釋出字串。

</dd> <dt>

*cchBufferMax* \[在\]
</dt> <dd>

類型： **UINT**

要從資源資料表載入的最大字元數。 如果資源字串的長度超過指定的字元數，則會被截斷並以 null 結束。

> [!Note]  
> 此參數不可以設定為零。

 

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

可能的傳回值包括（但不限於）下列各項。



| 傳回碼                                                                                  | 描述                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 作業成功。<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 未正確提供一或多個參數。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>Ndattributils。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**UtilStringCopyWithAlloc**](utilstringcopywithalloc.md)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> </dl>

 

