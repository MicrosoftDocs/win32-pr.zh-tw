---
title: IDWriteColorGlyphRunEnumerator MoveNext 方法
description: 移至列舉值中的下一個圖像執行。
ms.assetid: E6336C0E-F880-485C-9111-A102298257C1
keywords:
- MoveNext 方法直接寫入
- MoveNext 方法 Direct Write，IDWriteColorGlyphRunEnumerator 介面
- IDWriteColorGlyphRunEnumerator 介面直接寫入，MoveNext 方法
topic_type:
- apiref
api_name:
- IDWriteColorGlyphRunEnumerator.MoveNext
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 15c9963916c07f1df8cf3cfedb49b9e3fd66d0df
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508799"
---
# <a name="idwritecolorglyphrunenumeratormovenext-method"></a>IDWriteColorGlyphRunEnumerator：： MoveNext 方法

移至列舉值中的下一個圖像執行。

## <a name="syntax"></a>語法


```C++
HRESULT MoveNext(
  [out] BOOL *haveRun
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*haveRun* \[擴展\]
</dt> <dd>

類型： **BOOL \** _

如果有下一個圖像執行，則傳回 _ *TRUE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **HRESULT**

如果這個方法成功，它會傳回 **S \_ OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                                     |
| 最低支援的伺服器<br/> | Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]<br/>                          |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/> |
| 程式庫<br/>                  | <dl> <dt>Dwrite .lib</dt> </dl>   |
| DLL<br/>                      | <dl> <dt>Dwrite.dll</dt> </dl>   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md)
</dt> </dl>

 

 





