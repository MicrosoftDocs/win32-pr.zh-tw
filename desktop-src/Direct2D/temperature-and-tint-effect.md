---
title: 溫度和色調效果
description: .
ms.assetid: 8df72105-26ea-2dea-a4de-ef06902b7e0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a8a483b926b26c115002b2bb352d8e3120e7479
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843588"
---
# <a name="temperature-and-tint-effect"></a><span data-ttu-id="48d1d-103">溫度和色調效果</span><span class="sxs-lookup"><span data-stu-id="48d1d-103">Temperature and tint effect</span></span>

<span data-ttu-id="48d1d-104">這項效果的 CLSID 是 CLSID \_ D2D1TemperatureTint。</span><span class="sxs-lookup"><span data-stu-id="48d1d-104">The CLSID for this effect is CLSID\_D2D1TemperatureTint.</span></span>

## <a name="sample-code"></a><span data-ttu-id="48d1d-105">範例程式碼</span><span class="sxs-lookup"><span data-stu-id="48d1d-105">Sample code</span></span>

```cpp
ComPtr<ID2D1Effect> temperatureTintEffect;
m_d2dContext->CreateEffect(CLSID_D2D1TemperatureTint, &temperatureTintEffect);
 
temperatureTintEffect->SetInput(0, bitmap);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TEMPERATURE, 0.5f);
temperatureTintEffect->SetValue(D2D1_TEMPERATUREANDTINT_PROP_TINT, 0.5f);
 
m_d2dContext->BeginDraw();
m_d2dContext->DrawImage(temperatureTintEffect.Get());
m_d2dContext->EndDraw();
```

## <a name="effect-properties"></a><span data-ttu-id="48d1d-106">效果屬性</span><span class="sxs-lookup"><span data-stu-id="48d1d-106">Effect properties</span></span>

<span data-ttu-id="48d1d-107">溫度和色調效果的屬性是由 [**D2D1 \_ TEMPERATUREANDTINT \_**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop) 屬性列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="48d1d-107">The properties for the temperature and tint effect are defined by the [**D2D1\_TEMPERATUREANDTINT\_PROP**](/windows/desktop/api/d2d1effects_2/ne-d2d1effects_2-d2d1_temperatureandtint_prop) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="48d1d-108">規格需求</span><span class="sxs-lookup"><span data-stu-id="48d1d-108">Requirements</span></span>



| <span data-ttu-id="48d1d-109">需求</span><span class="sxs-lookup"><span data-stu-id="48d1d-109">Requirement</span></span> | <span data-ttu-id="48d1d-110">值</span><span class="sxs-lookup"><span data-stu-id="48d1d-110">Value</span></span> |
|--------------------------|---------------------------------------------------|
| <span data-ttu-id="48d1d-111">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48d1d-111">Minimum supported client</span></span> | <span data-ttu-id="48d1d-112">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48d1d-112">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="48d1d-113">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48d1d-113">Minimum supported server</span></span> | <span data-ttu-id="48d1d-114">Windows 10 \[ 桌面應用程式 \| Windows Store 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48d1d-114">Windows 10 \[desktop apps \| Windows Store apps\]</span></span> |
| <span data-ttu-id="48d1d-115">標頭</span><span class="sxs-lookup"><span data-stu-id="48d1d-115">Header</span></span>                   | <span data-ttu-id="48d1d-116">d2d1effects \_ 2。h</span><span class="sxs-lookup"><span data-stu-id="48d1d-116">d2d1effects\_2.h</span></span>                                  |
| <span data-ttu-id="48d1d-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="48d1d-117">Library</span></span>                  | <span data-ttu-id="48d1d-118">d2d1 .lib，dxguid .lib</span><span class="sxs-lookup"><span data-stu-id="48d1d-118">d2d1.lib, dxguid.lib</span></span>                              |



 

## <a name="related-topics"></a><span data-ttu-id="48d1d-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="48d1d-119">Related topics</span></span>

* [<span data-ttu-id="48d1d-120">ID2D1Effect 介面</span><span class="sxs-lookup"><span data-stu-id="48d1d-120">ID2D1Effect interface</span></span>](/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect)
