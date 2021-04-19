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
# <a name="d1106-resource-is-wrong-type"></a><span data-ttu-id="16528-104">D1106：資源類型錯誤</span><span class="sxs-lookup"><span data-stu-id="16528-104">D1106: Resource Is Wrong Type</span></span>

<span data-ttu-id="16528-105">指定的資源 \[ *資源* \] 不是預期的類型。</span><span class="sxs-lookup"><span data-stu-id="16528-105">The given resource \[*resource*\] is not of an expected type.</span></span>

## <a name="placeholders"></a><span data-ttu-id="16528-106">預留位置</span><span class="sxs-lookup"><span data-stu-id="16528-106">Placeholders</span></span>

<dl> <dt>

<span data-ttu-id="16528-107"><span id="resource"></span><span id="RESOURCE"></span>*資源*</span><span class="sxs-lookup"><span data-stu-id="16528-107"><span id="resource"></span><span id="RESOURCE"></span>*resource*</span></span>
</dt> <dd>

<span data-ttu-id="16528-108">資源的位址。</span><span class="sxs-lookup"><span data-stu-id="16528-108">The address of the resource.</span></span>

</dd> </dl> 




 

## <a name="possible-causes"></a><span data-ttu-id="16528-109">可能的原因</span><span class="sxs-lookup"><span data-stu-id="16528-109">Possible Causes</span></span>

<span data-ttu-id="16528-110">介面未正確轉換，並做為方法或函數的參數使用。</span><span class="sxs-lookup"><span data-stu-id="16528-110">An interface was improperly cast and used as a parameter for a method or function.</span></span>

## <a name="examples"></a><span data-ttu-id="16528-111">範例</span><span class="sxs-lookup"><span data-stu-id="16528-111">Examples</span></span>

<span data-ttu-id="16528-112">下列範例會在預期 [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry)時傳遞 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) 。</span><span class="sxs-lookup"><span data-stu-id="16528-112">The following example passes an [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush) when an [**ID2D1Geometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometry) is expected.</span></span>


```C++
        m_pRenderTarget->FillGeometry(
            (ID2D1Geometry*)m_pYellowGreenBrush,
            m_pYellowGreenBrush
            );
```



<span data-ttu-id="16528-113">此範例會產生下列 debug 訊息：</span><span class="sxs-lookup"><span data-stu-id="16528-113">This example produces the following debug message:</span></span>

``` syntax
DEBUG ERROR - The given resource[003A2C98] is not of an expected type
```

## <a name="fixes"></a><span data-ttu-id="16528-114">修正</span><span class="sxs-lookup"><span data-stu-id="16528-114">Fixes</span></span>

<span data-ttu-id="16528-115">使用方法所需的型別。</span><span class="sxs-lookup"><span data-stu-id="16528-115">Use the type required by the method.</span></span>

 

 
