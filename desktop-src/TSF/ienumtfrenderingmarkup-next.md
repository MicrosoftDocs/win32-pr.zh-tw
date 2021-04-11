---
title: IEnumTfRenderingMarkup Next 方法
description: IEnumTfRenderingMarkup Next 方法會從目前位置取得列舉順序中指定的專案數。
ms.assetid: a3aec919-2c65-4e65-9430-d73fdaf5d28e
keywords:
- Next 方法文字服務架構
- Next 方法文字服務架構，IEnumTfRenderingMarkup 介面
- IEnumTfRenderingMarkup 介面文字服務架構、Next 方法
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Next
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0989d35a2fa7c521d5ea103fbe40a73d012a3997
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023725"
---
# <a name="ienumtfrenderingmarkupnext-method"></a>IEnumTfRenderingMarkup：： Next 方法

**IEnumTfRenderingMarkup：： Next** 方法會從目前位置取得列舉順序中指定的元素數目。

## <a name="syntax"></a>語法


```C++
HRESULT Next(
  [out] ULONG ulCount,
  [out]       ppElement,
  [out] ULONG *pcFetched
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ulCount* \[擴展\]
</dt> <dd>

\[out \] 指定要取得的元素數目。

</dd> <dt>

*ppElement* \[擴展\]
</dt> <dd>

\[\] [TF \_ RENDERINGMARKUP](/windows/desktop/TSF/tf-renderingmarkup)結構陣列的指標。 此陣列的大小必須至少為 *ulCount* 元素。

</dd> <dt>

*pcFetched* \[擴展\]
</dt> <dd>

\[指向 \] ULONG 值的指標，此值會接收實際取得的元素數目。 這個值可能小於所要求的專案數。 此參數可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                        | 描述                                                                                                         |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 此方法成功。<br/>                                                                               |
| <dl> <dt>**S \_ FALSE**</dt> </dl>      | 方法在取得指定數目的元素之前，已到達列舉的結尾。<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 一或多個參數無效。<br/>                                                                      |



 

## <a name="remarks"></a>備註

> [!Note]  
> 這個方法目前不在公用標頭檔中。 若要使用此 API，您必須 MIDL 編譯 [原型](prototypes.md)。

 

 

