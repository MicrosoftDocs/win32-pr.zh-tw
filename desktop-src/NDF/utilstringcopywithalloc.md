---
title: 'UtilStringCopyWithAlloc 函式 (Ndattributils) '
description: 配置和複製來源字串。
ms.assetid: e1400ae1-0edd-4b59-af03-3da1b9d7073b
keywords:
- UtilStringCopyWithAlloc 函式 NDF
topic_type:
- apiref
api_name:
- UtilStringCopyWithAlloc
api_location:
- ndattributils.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b68bd1815ff09473f0431dde19a12a87603a9dec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965706"
---
# <a name="utilstringcopywithalloc-function"></a>UtilStringCopyWithAlloc 函式

**UtilStringCopyWithAlloc** 函數會配置和複製來源字串。

## <a name="syntax"></a>語法


```C++
HRESULT UtilStringCopyWithAlloc(
  _Out_ LPWSTR  *Buffer,
  _In_  UINT    BufferMax,
  _In_  LPCWSTR Source
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*緩衝區* \[擴展\]
</dt> <dd>

類型： **LPWSTR \** _

儲存配置記憶體指標的位置。 當不再需要時，必須使用 [_ *CoTaskMemFree* *](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)來發行。 這個緩衝區一律會以 null 結束。

</dd> <dt>

*BufferMax* \[在\]
</dt> <dd>

類型： **UINT**

要從 *來源* 讀取的最大字元數。

</dd> <dt>

*來源* \[在\]
</dt> <dd>

類型： **LPCWSTR**

要複製的字串。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

可能的傳回值包括（但不限於）下列各項。



| 傳回碼                                                                                  | Description                                                        |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 作業成功。<br/>                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 未正確提供一或多個參數。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>Ndattributils。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree)
</dt> <dt>

[**UtilAssembleStringsWithAlloc**](utilassemblestringswithalloc.md)
</dt> <dt>

[**UtilLoadStringWithAlloc**](utilloadstringwithalloc.md)
</dt> </dl>

 

