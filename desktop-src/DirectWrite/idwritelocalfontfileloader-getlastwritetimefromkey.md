---
title: IDWriteLocalFontFileLoader GetLastWriteTimeFromKey 方法
description: 從字型檔案參考索引鍵取得檔案的上次寫入時間。
ms.assetid: ce7f5321-8ad8-4412-a54c-7102790e99c0
keywords:
- GetLastWriteTimeFromKey 方法直接寫入
- GetLastWriteTimeFromKey 方法 Direct Write，IDWriteLocalFontFileLoader 介面
- IDWriteLocalFontFileLoader 介面 Direct Write，GetLastWriteTimeFromKey 方法
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader.GetLastWriteTimeFromKey
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea9817917a59761278a961a6fcafcdeaea5fda32
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001910"
---
# <a name="idwritelocalfontfileloadergetlastwritetimefromkey-method"></a>IDWriteLocalFontFileLoader：： GetLastWriteTimeFromKey 方法

從字型檔案參考索引鍵取得檔案的上次寫入時間。

## <a name="syntax"></a>語法


```C++
virtual HRESULT GetLastWriteTimeFromKey(
  [in]  const void     *fontFileReferenceKey,
              UINT32   fontFileReferenceKeySize,
  [out]       FILETIME *lastWriteTime
) = 0;
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

*lastWriteTime* \[擴展\]
</dt> <dd>

類型： **FILETIME \***

上次修改字型檔案的時間。

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

 

 





