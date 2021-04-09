---
title: IEnumTfRenderingMarkup Skip 方法
description: IEnumTfRenderingMarkup Skip 方法會從目前位置取得列舉順序中指定的元素數目。
ms.assetid: d328dfe3-36ab-4daf-8809-ad6686ca5dae
keywords:
- Skip 方法文字服務架構
- Skip 方法文字服務架構，IEnumTfRenderingMarkup 介面
- IEnumTfRenderingMarkup 介面文字服務架構，Skip 方法
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup.Skip
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3542893c739e6cfa2933d95bfed31f16957a0841
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678315"
---
# <a name="ienumtfrenderingmarkupskip-method"></a>IEnumTfRenderingMarkup：： Skip 方法

**IEnumTfRenderingMarkup：： Skip** 方法會從目前位置取得列舉順序中指定的元素數目。

## <a name="syntax"></a>語法


```C++
HRESULT Skip(
  [in] ULONG ulCount
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ulCount* \[在\]
</dt> <dd>

\[中的 \] 指定要略過的元素數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                   | 描述                                                                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>    | 此方法成功。<br/>                                                                              |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | 方法在可以略過指定的元素數目之前，已到達列舉的結尾。<br/> |



 

## <a name="remarks"></a>備註

> [!Note]  
> 這個方法目前不在公用標頭檔中。 若要使用此 API，您必須 MIDL 編譯 [原型](prototypes.md)。

 

 

 





