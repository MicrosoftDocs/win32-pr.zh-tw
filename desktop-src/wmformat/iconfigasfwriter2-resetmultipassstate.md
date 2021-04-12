---
title: IConfigAsfWriter2 ResetMultiPassState 方法
description: 當前置處理編碼階段在完成之前取消時，ResetMultiPassState 方法會重設篩選。
ms.assetid: b6687af7-f3cd-4e92-9c76-dddff9063fa0
keywords:
- ResetMultiPassState 方法 windows Media 格式
- ResetMultiPassState 方法 windows Media Format，IConfigAsfWriter2 介面
- IConfigAsfWriter2 介面 windows Media Format，ResetMultiPassState 方法
topic_type:
- apiref
api_name:
- IConfigAsfWriter2.ResetMultiPassState
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed61e4f0517822a602f2bb88c944bba82fa1f943
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376292"
---
# <a name="iconfigasfwriter2resetmultipassstate-method"></a>IConfigAsfWriter2：： ResetMultiPassState 方法

當前置處理編碼階段在完成之前取消時， **ResetMultiPassState** 方法會重設篩選。

## <a name="syntax"></a>語法


```C++
HRESULT ResetMultiPassState();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

方法會傳回 **HRESULT**。 可能的值包括 (但不限於) 下表中的這些值。



| 傳回碼                                                                                         | Description                                       |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                | 此方法已成功。<br/>                  |
| <dl> <dt>**VFW \_ E \_ 未 \_ 停止**</dt> </dl> | 篩選未處於已停止狀態。<br/> |



 

## <a name="remarks"></a>備註

只要在篩選器收到 EC 前置處理 **\_ \_ 完成** 事件之前取消前置處理編碼階段，就必須呼叫這個方法來重設篩選的內部狀態。 如果前置處理編碼傳遞完成而沒有錯誤，則不需要呼叫此方法。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IConfigAsfWriter2 介面**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))
</dt> </dl>

 

