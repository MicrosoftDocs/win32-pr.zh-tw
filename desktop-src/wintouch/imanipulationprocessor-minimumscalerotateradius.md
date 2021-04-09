---
title: IManipulationProcessor MinimumScaleRotateRadius 屬性
description: 指定縮放或旋轉手勢上的連絡人要觸發操作所需的距離。
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
keywords:
- MinimumScaleRotateRadius 屬性 Windows Touch
- MinimumScaleRotateRadius 屬性 Windows Touch，IManipulationProcessor 介面
- IManipulationProcessor 介面 Windows Touch，MinimumScaleRotateRadius 屬性
topic_type:
- apiref
api_name:
- IManipulationProcessor.MinimumScaleRotateRadius
- IManipulationProcessor.get_MinimumScaleRotateRadius
- IManipulationProcessor.put_MinimumScaleRotateRadius
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- manipulations.h
ms.openlocfilehash: 502d55e409f58127ddee94f5ba694a109c1ee1cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678612"
---
# <a name="imanipulationprocessorminimumscalerotateradius-property"></a>IManipulationProcessor：： MinimumScaleRotateRadius 屬性

指定縮放或旋轉手勢上的連絡人要觸發操作所需的距離。

這是可讀寫的屬性。

## <a name="syntax"></a>Syntax


```C++
HRESULT put_MinimumScaleRotateRadius(
  [in]  FLOAT MinimumScaleRotateRadius
);

HRESULT get_MinimumScaleRotateRadius(
  [out] FLOAT *MinimumScaleRotateRadius
);
```



## <a name="property-value"></a>屬性值

指定連絡人之間的最小距離，以觸發縮放或旋轉手勢。

## <a name="error-codes"></a>錯誤碼

## <a name="remarks"></a>備註

> [!Note]  
> 這個屬性是在圖元) 的 centipixels (100ths 中設定。

 

設定此值會讓操作處理器忽略半徑太小的手勢。 如果您想要防止使用者將物件操作成太小的半徑，這會很有用。 例如，如果您使用具有圓形的操作處理器，而且想要確保它維持大於100圖元的半徑，則會將此值設定為10000。

## <a name="examples"></a>範例


```C++
pManip->put_MinimumScaleRotateRadius(4000.0f);  
```



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IManipulationProcessor**](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




