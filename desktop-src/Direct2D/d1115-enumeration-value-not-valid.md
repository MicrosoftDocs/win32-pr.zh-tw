---
title: D1115 列舉值無效
description: D1115 列舉值無效
ms.assetid: cfffd2b8-a7d3-4a60-8586-81d8435936a6
keywords:
- D1115 列舉值無效 Direct2D
topic_type:
- apiref
api_name:
- D1115 Enumeration Value Not Valid
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11800acaae350b5289b339738448300c91db32a16c0d3f3d9224f08b6079fba2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758118"
---
# <a name="d1115-enumeration-value-not-valid"></a>D1115：列舉值無效

\[  \] \[  \] *Interface*：：*method* 值為 value 的參數參數不是有效的列舉值。

## <a name="placeholders"></a>預留位置

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*參數*
</dt> <dd>

收到未預期之類型的參數名稱。

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*價值*
</dt> <dd>

不正確列舉值。

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*介面*
</dt> <dd>

*方法* 所屬的介面名稱。

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*方法*
</dt> <dd>

收到無效列舉值之方法的名稱。

</dd> </dl> 




 

## <a name="examples"></a>範例

下列範例會指定 [**D2D1 轉譯 \_ \_ 目標 \_ 型**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type) 別列舉值30（超出預期的範圍）。


```C++
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties((D2D1_RENDER_TARGET_TYPE)(30)),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );
```



此範例會產生下列 debug 訊息：

``` syntax
D2D DEBUG ERROR - The parameter [renderTargetProperties->type] with value [30] 
for ID2D1Factory::CreateHwndRenderTarget is not a valid enumeration value.
```

## <a name="possible-causes"></a>可能的原因

參數使用了不正確列舉值。

## <a name="fixes"></a>修正

請使用有效的列舉值。

> [!Note]  
> Debug 層目前只會檢查個別的列舉值;它不會檢查位組合是否有效。

 

 

 
