---
description: ActivateButton 方法會啟用選取的功能表按鈕。
ms.assetid: 1da486a0-dadc-4c92-b3d3-83aeace01e39
title: ActivateButton 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8a463a3aad1ee0dcabc0e5daaa4a4969efa37aa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106997468"
---
# <a name="activatebutton-method"></a><span data-ttu-id="e8f36-103">ActivateButton 方法</span><span class="sxs-lookup"><span data-stu-id="e8f36-103">ActivateButton Method</span></span>

> [!Note]  
> <span data-ttu-id="e8f36-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="e8f36-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="e8f36-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="e8f36-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="e8f36-106">ActivateButton 方法會啟用選取的功能表按鈕。</span><span class="sxs-lookup"><span data-stu-id="e8f36-106">The ActivateButton method activates the selected menu button.</span></span>

``` syntax
        MSWebDVD.ActivateButton()
```

## <a name="return-value"></a><span data-ttu-id="e8f36-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="e8f36-107">Return Value</span></span>

<span data-ttu-id="e8f36-108">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="e8f36-108">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e8f36-109">備註</span><span class="sxs-lookup"><span data-stu-id="e8f36-109">Remarks</span></span>

<span data-ttu-id="e8f36-110">將 [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) 設為 **true** 之後，執行自訂滑鼠處理時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="e8f36-110">Use this method when implementing custom mouse handling after setting [**DisableAutoMouseProcessing**](disableautomouseprocessing-property.md) to **true**.</span></span>

<span data-ttu-id="e8f36-111">您可以使用這個方法來啟動透過 [**SelectLeftButton**](selectleftbutton-method.md)、 [**SelectLowerButton**](selectlowerbutton-method.md)、 [**SelectUpperButton**](selectupperbutton-method.md)或 [**SelectRightButton**](selectrightbutton-method.md) 方法選取的按鈕。</span><span class="sxs-lookup"><span data-stu-id="e8f36-111">Use this method to activate a button that has been selected through the [**SelectLeftButton**](selectleftbutton-method.md), [**SelectLowerButton**](selectlowerbutton-method.md), [**SelectUpperButton**](selectupperbutton-method.md), or [**SelectRightButton**](selectrightbutton-method.md) method.</span></span>

 

 



