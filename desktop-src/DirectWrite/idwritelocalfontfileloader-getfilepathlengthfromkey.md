---
title: IDWriteLocalFontFileLoader GetFilePathLengthFromKey 方法
description: 從字型檔案參考索引鍵取得絕對檔案路徑的長度。
ms.assetid: bdd84d75-5a7a-448a-a52c-0f5997ab07b9
keywords:
- GetFilePathLengthFromKey 方法直接寫入
- GetFilePathLengthFromKey 方法 Direct Write，IDWriteLocalFontFileLoader 介面
- IDWriteLocalFontFileLoader 介面 Direct Write，GetFilePathLengthFromKey 方法
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetFilePathLengthFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587f432f006493097ec8262fcc2201e2c3b67abe7115c395332671ec35efeba9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117816349"
---
# <a name="idwritelocalfontfileloadergetfilepathlengthfromkey-method"></a>IDWriteLocalFontFileLoader：： GetFilePathLengthFromKey 方法

從字型檔案參考索引鍵取得絕對檔案路徑的長度。

## <a name="syntax"></a>語法


```C++
HRESULT GetFilePathLengthFromKey(
  [in]  const void   *fontFileReferenceKey,
              UINT32 fontFileReferenceKeySize,
  [out]       UINT32 *filePathLength
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*fontFileReferenceKey* \[在\]
</dt> <dd>

類型： **const void \***

字型檔案參考索引鍵，可在使用的字型載入器範圍內唯一識別本機字型檔案。

</dd> <dt>

*fontFileReferenceKeySize* 
</dt> <dd>

類型： **UINT32**

字型檔案參考索引鍵的大小（以位元組為單位）。

</dd> <dt>

*filePathLength* \[擴展\]
</dt> <dd>

類型： **UINT32 \***

檔案路徑字串的長度，不包含終止的 **Null** 字元。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>Dwrite .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>Dwrite.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md)
</dt> </dl>

 

 





