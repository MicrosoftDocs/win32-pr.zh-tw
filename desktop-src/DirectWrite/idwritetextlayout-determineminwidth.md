---
title: IDWriteTextLayout DetermineMinWidth 方法
description: 判斷配置可設定的最小可能寬度，而不會在整個單字的字元之間進行緊急中斷。
ms.assetid: 8efa1471-1b74-46d4-ac6d-fb1839ce2e74
keywords:
- DetermineMinWidth 方法直接寫入
- DetermineMinWidth 方法 Direct Write，IDWriteTextLayout 介面
- IDWriteTextLayout 介面 Direct Write，DetermineMinWidth 方法
topic_type:
- apiref
api_name:
- IDWriteTextLayout.DetermineMinWidth
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41123f2a5d584341c344248d0af936f34fc04e49c9aabc1cb73ecea0eacc84ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120075528"
---
# <a name="idwritetextlayoutdetermineminwidth-method"></a>IDWriteTextLayout：:D etermineMinWidth 方法

判斷配置可設定的最小可能寬度，而不會在整個單字的字元之間進行緊急中斷。

## <a name="syntax"></a>語法


```C++
virtual HRESULT DetermineMinWidth(
  [out] FLOAT *minWidth
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*minWidth* \[擴展\]
</dt> <dd>

類型： **FLOAT \***

寬度下限。

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

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> <dt>

[**IDWriteTextLayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout)
</dt> </dl>

 

