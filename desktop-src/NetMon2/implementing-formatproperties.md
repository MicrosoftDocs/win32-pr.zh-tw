---
description: 網路監視器會呼叫 FormatProperties 函式來格式化網路監視器 UI 的詳細資料窗格中所顯示的資料。
ms.assetid: d0a58e1d-c867-4277-916e-f408627b5269
title: 執行 FormatProperties
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 660b581bf29fd8e5d40af65f5ff90e1e9223ad2e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112797"
---
# <a name="implementing-formatproperties"></a><span data-ttu-id="4cda8-103">執行 FormatProperties</span><span class="sxs-lookup"><span data-stu-id="4cda8-103">Implementing FormatProperties</span></span>

<span data-ttu-id="4cda8-104">網路監視器會呼叫 [**FormatProperties**](formatproperties.md) 函式來格式化網路監視器 UI 的詳細資料窗格中所顯示的資料。</span><span class="sxs-lookup"><span data-stu-id="4cda8-104">Network Monitor calls the [**FormatProperties**](formatproperties.md) function to format the data that is displayed in the details pane of the Network Monitor UI.</span></span> <span data-ttu-id="4cda8-105">一般來說，會呼叫 **FormatProperties** 來格式化通訊協定的摘要行，然後格式化框架內的所有通訊協定屬性實例。</span><span class="sxs-lookup"><span data-stu-id="4cda8-105">Typically, **FormatProperties** is called to format the summary line for a protocol, and then to format all the property instances of the protocol within a frame.</span></span> <span data-ttu-id="4cda8-106">不過，網路監視器不會識別針對特定剖析器呼叫 **FormatProperties** 的次數。</span><span class="sxs-lookup"><span data-stu-id="4cda8-106">However, Network Monitor does not identify the number of times that **FormatProperties** is called for a specific parser.</span></span>

<span data-ttu-id="4cda8-107">呼叫 [**FormatProperties**](formatproperties.md)時，網路監視器為其顯示的每個屬性提供 [**PROPERTYINST**](propertyinst.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="4cda8-107">When calling [**FormatProperties**](formatproperties.md), Network Monitor provides a [**PROPERTYINST**](propertyinst.md) structure for each property that it displays.</span></span> <span data-ttu-id="4cda8-108">**PROPERTYINST** 結構提供要顯示之資料的相關資訊，包括 [**PROPERTYINFO**](propertyinfo.md)結構的指標，此結構會指定用來格式化顯示的資料屬性的函式。</span><span class="sxs-lookup"><span data-stu-id="4cda8-108">The **PROPERTYINST** structure provides information about the data to be displayed, including a pointer to the [**PROPERTYINFO**](propertyinfo.md) structure that specifies the function to use to format the displayed data property.</span></span>

> [!Note]  
> <span data-ttu-id="4cda8-109">將屬性加入至剖析器的 [*屬性資料庫*](p.md)時，會指定 [**PROPERTYINFO**](propertyinfo.md)結構。</span><span class="sxs-lookup"><span data-stu-id="4cda8-109">A [**PROPERTYINFO**](propertyinfo.md) structure is specified when adding a property to the [*property database*](p.md) of the parser.</span></span>

 

<span data-ttu-id="4cda8-110">網路監視器識別要針對每個屬性實例呼叫的格式函數。</span><span class="sxs-lookup"><span data-stu-id="4cda8-110">Network Monitor identifies the format function to call for each property instance.</span></span> <span data-ttu-id="4cda8-111">[**PROPERTYINFO**](propertyinfo.md)結構的 **InstanceData** 成員可以指定下列各項：</span><span class="sxs-lookup"><span data-stu-id="4cda8-111">The **InstanceData** member of the [**PROPERTYINFO**](propertyinfo.md) structure can specify the following:</span></span>

-   <span data-ttu-id="4cda8-112">[**FormatPropertyInstance**](formatpropertyinstance.md)函式，使用網路監視器提供的 [*一般格式*](g.md)器。</span><span class="sxs-lookup"><span data-stu-id="4cda8-112">The [**FormatPropertyInstance**](formatpropertyinstance.md) function to use the [*generic formatter*](g.md) that Network Monitor provides.</span></span>

    <span data-ttu-id="4cda8-113">-或-</span><span class="sxs-lookup"><span data-stu-id="4cda8-113">– or –</span></span>

-   <span data-ttu-id="4cda8-114">剖析器所提供的自訂格式函數名稱。</span><span class="sxs-lookup"><span data-stu-id="4cda8-114">The name of a custom format function that the parser provides.</span></span>

<span data-ttu-id="4cda8-115">[**FormatPropertyInstance**](formatpropertyinstance.md)和自訂格式函數會傳回在網路監視器 UI 的詳細資料窗格中所顯示的格式化資料。</span><span class="sxs-lookup"><span data-stu-id="4cda8-115">The [**FormatPropertyInstance**](formatpropertyinstance.md) and the custom format functions return the formatted data that is displayed in the details pane of the Network Monitor UI.</span></span>

<span data-ttu-id="4cda8-116">下圖顯示網路監視器如何識別要針對每個屬性實例呼叫的函數。</span><span class="sxs-lookup"><span data-stu-id="4cda8-116">The following illustration shows how Network Monitor identifies the function to call for each property instance.</span></span>

![網路監視器如何識別要呼叫的函式](images/formatprop1.png)

<span data-ttu-id="4cda8-118">下列程式識別執行 [**FormatProperties**](formatproperties.md)所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="4cda8-118">The following procedure identifies the steps necessary to implement [**FormatProperties**](formatproperties.md).</span></span>

<span data-ttu-id="4cda8-119">**若要執行 FormatProperties**</span><span class="sxs-lookup"><span data-stu-id="4cda8-119">**To implement FormatProperties**</span></span>

-   <span data-ttu-id="4cda8-120">使用迴圈結構，針對傳遞給 [**FormatProperties**](formatproperties.md)函式之 *lpPropInst* 參數中的剖析器，呼叫每個 [**PROPERTYINST**](propertyinst.md)結構的格式函數。</span><span class="sxs-lookup"><span data-stu-id="4cda8-120">Using a loop structure, call the format function for each [**PROPERTYINST**](propertyinst.md) structure that is passed to the parser in the *lpPropInst* parameter of the [**FormatProperties**](formatproperties.md) function.</span></span>

<span data-ttu-id="4cda8-121">以下是 [**FormatProperties**](formatproperties.md)的基本執行。</span><span class="sxs-lookup"><span data-stu-id="4cda8-121">The following is a basic implementation of [**FormatProperties**](formatproperties.md).</span></span>

``` syntax
#include <windows.h>

DWORD BHAPI MyProtocolFormatProperties( HFRAME hFrame,
                                        LPBYTE         pMacFrame,
                                        LPBYTE         pBLRPLATEFrame,
                                        DWORD          nPropertyInsts
                                        LPPROPERTYINST  p)
  {
    while( nPropertyInsts-- > 0)
      {
         ( (FORMAT) p->lpPropertyInfo->InstanceData) ) (p);
         p++;
      }
  return BHERR_SUCCESS;
  }
```

 

 



