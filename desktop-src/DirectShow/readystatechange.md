---
description: 當 MSWebDVD 控制項的 ReadyState 屬性變更時，就會傳送 ReadyStateChange 事件。
ms.assetid: 814a09e1-2e85-4ea3-9135-8377dc2acf64
title: ReadyStateChange
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46cc8d7ffdee650aac48839d49ed8162e10bb955
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510173"
---
# <a name="readystatechange"></a><span data-ttu-id="fbecf-103">ReadyStateChange</span><span class="sxs-lookup"><span data-stu-id="fbecf-103">ReadyStateChange</span></span>

> [!Note]  
> <span data-ttu-id="fbecf-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="fbecf-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="fbecf-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="fbecf-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="fbecf-106">`ReadyStateChange`當 MSWebDVD 控制項的 **ReadyState** 屬性變更時，就會傳送事件。</span><span class="sxs-lookup"><span data-stu-id="fbecf-106">The `ReadyStateChange` event is sent when the **ReadyState** property of the MSWebDVD control has changed.</span></span>

``` syntax
ReadyStateChange(ReadyState)
```

## <a name="parameters"></a><span data-ttu-id="fbecf-107">參數</span><span class="sxs-lookup"><span data-stu-id="fbecf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fbecf-108"><span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*</span><span class="sxs-lookup"><span data-stu-id="fbecf-108"><span id="ReadyState"></span><span id="readystate"></span><span id="READYSTATE"></span>*ReadyState*</span></span>
</dt> <dd>

<span data-ttu-id="fbecf-109">指定 [**ReadyState**](readystate-property.md) 屬性的新值。</span><span class="sxs-lookup"><span data-stu-id="fbecf-109">Specifies the new value of the [**ReadyState**](readystate-property.md) property.</span></span>



| <span data-ttu-id="fbecf-110">值</span><span class="sxs-lookup"><span data-stu-id="fbecf-110">Value</span></span> | <span data-ttu-id="fbecf-111">描述</span><span class="sxs-lookup"><span data-stu-id="fbecf-111">Description</span></span>               |
|-------|---------------------------|
| <span data-ttu-id="fbecf-112">0</span><span class="sxs-lookup"><span data-stu-id="fbecf-112">0</span></span>     | <span data-ttu-id="fbecf-113">READYSTATE \_ 未初始化</span><span class="sxs-lookup"><span data-stu-id="fbecf-113">READYSTATE\_UNINITIALIZED</span></span> |
| <span data-ttu-id="fbecf-114">1</span><span class="sxs-lookup"><span data-stu-id="fbecf-114">1</span></span>     | <span data-ttu-id="fbecf-115">READYSTATE \_ 載入</span><span class="sxs-lookup"><span data-stu-id="fbecf-115">READYSTATE\_LOADING</span></span>       |
| <span data-ttu-id="fbecf-116">2</span><span class="sxs-lookup"><span data-stu-id="fbecf-116">2</span></span>     | <span data-ttu-id="fbecf-117">READYSTATE 已 \_ 載入</span><span class="sxs-lookup"><span data-stu-id="fbecf-117">READYSTATE\_LOADED</span></span>        |
| <span data-ttu-id="fbecf-118">3</span><span class="sxs-lookup"><span data-stu-id="fbecf-118">3</span></span>     | <span data-ttu-id="fbecf-119">READYSTATE \_ 互動</span><span class="sxs-lookup"><span data-stu-id="fbecf-119">READYSTATE\_INTERACTIVE</span></span>   |
| <span data-ttu-id="fbecf-120">4</span><span class="sxs-lookup"><span data-stu-id="fbecf-120">4</span></span>     | <span data-ttu-id="fbecf-121">READYSTATE \_ 完成</span><span class="sxs-lookup"><span data-stu-id="fbecf-121">READYSTATE\_COMPLETE</span></span>      |



 

</dd> </dl>

 

 



