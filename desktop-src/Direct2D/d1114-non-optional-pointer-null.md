---
title: D1114 非選擇性指標 Null
ms.assetid: 62f0f247-8359-4f75-b3ce-195202d491d5
description: Interface：：方法的參數不是選擇性的。 傳遞了 Null 指標。 這會導致 Direct2D 損毀。
keywords:
- D1114 非選擇性指標 Null Direct2D
topic_type:
- apiref
api_name:
- D1114 Non Optional Pointer NULL
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: abf8f070e339f2dcda5f818f5ffd5386c33d0e29
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/27/2021
ms.locfileid: "107001636"
---
# <a name="d1114-non-optional-pointer-null"></a>D1114：非選擇性指標 Null

\[  \] *Interface*：：*方法* 的參數參數不是選擇性的。 傳遞了 **Null** 指標。 這會導致 Direct2D 損毀。

### <a name="placeholders"></a>預留位置

<dl> <dt>

<span id="parameter"></span><span id="PARAMETER"></span>*參數*
</dt> <dd>

包含 **Null** 指標的參數名稱。

</dd> <dt>

<span id="interface"></span><span id="INTERFACE"></span>*介面*
</dt> <dd>

*方法* 所屬的介面名稱。

</dd> <dt>

<span id="method"></span><span id="METHOD"></span>*方法*
</dt> <dd>

收到無效參數之方法的名稱。

</dd> </dl> 




 

### <a name="examples"></a>範例

下列範例顯示 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry) 方法收到非選擇性 *GEOMETRY* 參數的 Null 指標。


```C++
        m_pRenderTarget->FillGeometry(NULL, m_pYellowGreenBrush);
```



此範例會產生下列 debug 訊息：

``` syntax
D2D DEBUG ERROR - The parameter [geometry] for ID2D1RenderTarget::FillGeometry is not optional. 
A NULL pointer was passed. This will cause Direct2D to crash.
```

## <a name="possible-causes"></a>可能的原因

傳遞非選擇性參數的 Null 指標。

## <a name="fixes"></a>修正

確定非選擇性參數沒有 Null 指標。

 

 
