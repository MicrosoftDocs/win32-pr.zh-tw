---
description: 網路監視器提供 PROPERTYINFO 結構來定義通訊協定的屬性，以及 PROPERTYINST 和 PROPERTYINSTEX 結構來定義屬性的實例。
ms.assetid: d1e29bd6-c04a-48f1-9727-96b9450e256f
title: 屬性定義和屬性實例結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55aa67efb5054d93184b56c53f84f9fac0893abf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692783"
---
# <a name="property-definition-and-property-instance-structures"></a><span data-ttu-id="49924-103">屬性定義和屬性實例結構</span><span class="sxs-lookup"><span data-stu-id="49924-103">Property Definition and Property Instance Structures</span></span>

<span data-ttu-id="49924-104">網路監視器提供 [**PROPERTYINFO**](propertyinfo.md) 結構來定義通訊協定的屬性，以及 [**PROPERTYINST**](propertyinst.md)和 [**PROPERTYINSTEX**](propertyinstex.md) 結構來定義屬性的實例。</span><span class="sxs-lookup"><span data-stu-id="49924-104">Network Monitor provides a [**PROPERTYINFO**](propertyinfo.md) structure to define the properties of a protocol, and a [**PROPERTYINST**](propertyinst.md), and [**PROPERTYINSTEX**](propertyinstex.md) structure to define an instance of a property.</span></span>

![網路監視器結構](images/property1.png)

<span data-ttu-id="49924-106">剖析器會為通訊協定支援的所有屬性配置和填入 [**PROPERTYINFO**](propertyinfo.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="49924-106">The parser allocates and fills-in the [**PROPERTYINFO**](propertyinfo.md) structure for all the properties that a protocol supports.</span></span> <span data-ttu-id="49924-107">剖析器會將結構傳遞給網路監視器，其中結構會新增至通訊協定 [*屬性資料庫*](p.md)。</span><span class="sxs-lookup"><span data-stu-id="49924-107">The parser passes the structure to Network Monitor where the structure is added to the protocol [*property database*](p.md).</span></span> <span data-ttu-id="49924-108">當剖析屬性的實例，以及將網路監視器 UI 中顯示的資料格式化時，會使用 **PROPERTYINFO** 結構中的資訊。</span><span class="sxs-lookup"><span data-stu-id="49924-108">The information in the **PROPERTYINFO** structure is used when parsing an instance of a property, and when formatting the data that is displayed in the Network Monitor UI.</span></span>

<span data-ttu-id="49924-109">當剖析器將屬性定義附加至屬性的實例時，網路監視器會配置 [**PROPERTYINST**](propertyinst.md) 和 [**PROPERTYINSTEX**](propertyinstex.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="49924-109">Network Monitor allocates the [**PROPERTYINST**](propertyinst.md) and [**PROPERTYINSTEX**](propertyinstex.md) structures when the parser attaches a property definition to an instance of a property.</span></span>

<span data-ttu-id="49924-110">下列程式識別附加屬性定義所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="49924-110">The following procedure identifies the steps necessary to attach a property definition.</span></span>

<span data-ttu-id="49924-111">**附加屬性定義**</span><span class="sxs-lookup"><span data-stu-id="49924-111">**To attach a property definition**</span></span>

1.  <span data-ttu-id="49924-112">識別存在於通訊協定實例中的每個屬性。</span><span class="sxs-lookup"><span data-stu-id="49924-112">Identify each property that exists in an instance of the protocol.</span></span> <span data-ttu-id="49924-113">附加定義時，網路監視器會將捕獲的資料傳遞給剖析器。</span><span class="sxs-lookup"><span data-stu-id="49924-113">When attaching a definition, Network Monitor passes the captured data to the parser.</span></span> <span data-ttu-id="49924-114">資料會根據通訊協定實例來傳遞。</span><span class="sxs-lookup"><span data-stu-id="49924-114">The data is passed on a protocol instance basis.</span></span>
2.  <span data-ttu-id="49924-115">判斷通訊協定實例中屬性的位置。</span><span class="sxs-lookup"><span data-stu-id="49924-115">Determine the location of the property in the protocol instance.</span></span>
3.  <span data-ttu-id="49924-116">將屬性定義附加至屬性位置。</span><span class="sxs-lookup"><span data-stu-id="49924-116">Attach a property definition to the property location.</span></span>

<span data-ttu-id="49924-117">當剖析器使用存在於捕捉中的屬性資料時，網路監視器會執行 [**PROPERTYINST**](propertyinst.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="49924-117">Network Monitor implements a [**PROPERTYINST**](propertyinst.md) structure when the parser uses the property data as it exists in the capture.</span></span> <span data-ttu-id="49924-118">當剖析器必須修改 capture 中的屬性資料時，網路監視器會執行 [**PROPERTYINSTEX**](propertyinstex.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="49924-118">Network Monitor implements a [**PROPERTYINSTEX**](propertyinstex.md) structure when the parser must modify the property data in the capture.</span></span>

 

 



