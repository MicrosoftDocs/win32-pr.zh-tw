---
title: IEnumTfRenderingMarkup Clone 方法
description: IEnumTfRenderingMarkup Clone 方法會建立枚舉器物件的複本。
ms.assetid: f1b0ccf9-36d1-4eff-af7c-d7fb4f0e9104
keywords:
- Clone 方法文字服務架構
- Clone 方法文字服務架構，IEnumTfRenderingMarkup 介面
- IEnumTfRenderingMarkup 介面文字服務架構，Clone 方法
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Clone
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7f15d1bda18d2371f6518da4fa2884fac4df91b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106979669"
---
# <a name="ienumtfrenderingmarkupclone-method"></a>IEnumTfRenderingMarkup：： Clone 方法

**IEnumTfRenderingMarkup：： Clone** 方法會建立枚舉器物件的複本。

## <a name="syntax"></a>語法


```C++
HRESULT Clone(
  [out] IEnumTfRenderingMarkup **ppEnum
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppEnum* \[擴展\]
</dt> <dd>

\[\] [IEnumTfRenderingMarkup](/windows/desktop/TSF/ienumtfrenderingmarkup)介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                        | 描述                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法成功。<br/>          |
| <dl> <dt>**E \_ 失敗**</dt> </dl>       | 發生未指定的錯誤。<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 一或多個參數無效。<br/> |



 

## <a name="remarks"></a>備註

> [!Note]  
> 這個方法目前不在公用標頭檔中。 若要使用此 API，您必須 MIDL 編譯 [原型](prototypes.md)。

 

 

