---
title: D1106 資源類型錯誤
ms.assetid: 79a618cb-1d05-4895-b801-7663890b456a
description: 指定的資源不是預期的類型。
keywords:
- D1106 資源的類型錯誤 Direct2D
topic_type:
- apiref
api_name:
- D1106 Resource Is Wrong Type
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 5c38ef36319b8021de918a798c94a3be0683a7b7
ms.sourcegitcommit: 80ee822f6ebcbcc8f60042e0d14a39ef6989c731
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/27/2021
ms.locfileid: "106978542"
---
# <a name="d1106-resource-is-wrong-type"></a>D1106：資源類型錯誤

指定的資源 \[ *資源* \] 不是預期的類型。

## <a name="placeholders"></a>預留位置

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*資源*
</dt> <dd>

資源的位址。

</dd> </dl> 




 

## <a name="possible-causes"></a>可能的原因

介面未正確轉換，並做為方法或函數的參數使用。

## <a name="examples"></a>範例

下列範例會在預期 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)時傳遞 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 。


```C++
        m_pRenderTarget->FillGeometry(
            (ID2D1Geometry*)m_pYellowGreenBrush,
            m_pYellowGreenBrush
            );
```



此範例會產生下列 debug 訊息：

``` syntax
DEBUG ERROR - The given resource[003A2C98] is not of an expected type
```

## <a name="fixes"></a>修正

使用方法所需的型別。

 

 
