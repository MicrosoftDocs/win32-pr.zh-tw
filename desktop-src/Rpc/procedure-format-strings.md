---
title: 程式格式字串
description: 以下是完整的格式字串描述。 它會組合與解譯器演進的不同階段相關的所有層級。
ms.assetid: fab603ed-1f68-4e0b-9c8d-b9730b8cd389
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e58a9acf10caad23063bdba117dc402e411638
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933474"
---
# <a name="procedure-format-strings"></a><span data-ttu-id="8d528-104">程式格式字串</span><span class="sxs-lookup"><span data-stu-id="8d528-104">Procedure Format Strings</span></span>

<span data-ttu-id="8d528-105">以下是完整的格式字串描述。</span><span class="sxs-lookup"><span data-stu-id="8d528-105">The following is a complete format string description.</span></span> <span data-ttu-id="8d528-106">它會組合與解譯器演進的不同階段相關的所有層級。</span><span class="sxs-lookup"><span data-stu-id="8d528-106">It assembles all layers related to different stages of the interpreter evolution.</span></span>

## <a name="procedure-descriptor-overview"></a><span data-ttu-id="8d528-107">程式描述項總覽</span><span class="sxs-lookup"><span data-stu-id="8d528-107">Procedure Descriptor Overview</span></span>

<span data-ttu-id="8d528-108">程式描述項是由標頭描述元和參數描述元所組成。</span><span class="sxs-lookup"><span data-stu-id="8d528-108">A procedure descriptor consists of the header descriptors and the parameter descriptors.</span></span> <span data-ttu-id="8d528-109">在目前的 RPC 程式設計中， [**-Oi**](/windows/desktop/Midl/-oi) 樣式描述會視為過時。</span><span class="sxs-lookup"><span data-stu-id="8d528-109">The [**–Oi**](/windows/desktop/Midl/-oi) style description is considered outdated, in terms of common usage in current RPC programming.</span></span> <span data-ttu-id="8d528-110">**– Oif** 被視為較新的。</span><span class="sxs-lookup"><span data-stu-id="8d528-110">The **–Oif** is considered more current.</span></span>

## <a name="the-oi-style-description"></a><span data-ttu-id="8d528-111">– Oi 樣式描述</span><span class="sxs-lookup"><span data-stu-id="8d528-111">The –Oi Style Description</span></span>

<span data-ttu-id="8d528-112">此描述包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="8d528-112">This description consists of the following:</span></span>

``` syntax
-Oi_style_header_descriptor<>
{-Oi_style_parameter_descriptor<>}*
```

<span data-ttu-id="8d528-113">標頭的大小為6到16個位元組。</span><span class="sxs-lookup"><span data-stu-id="8d528-113">The header would have from 6 to 16 bytes.</span></span>

<span data-ttu-id="8d528-114">在 [**– Oi**](/windows/desktop/Midl/-oi) 模式下編譯時，會產生完整的描述。</span><span class="sxs-lookup"><span data-stu-id="8d528-114">The complete description is generated when compiling in [**–Oi**](/windows/desktop/Midl/-oi) mode.</span></span> <span data-ttu-id="8d528-115">在 [**–作業系統**](/windows/desktop/Midl/-os) 模式中，只會產生參數描述項，以用於轉換。</span><span class="sxs-lookup"><span data-stu-id="8d528-115">In [**–Os**](/windows/desktop/Midl/-os) mode, only the parameter descriptors are generated, which are used for conversion.</span></span> <span data-ttu-id="8d528-116">Pickling 解譯器會使用舊的樣式參數描述元。</span><span class="sxs-lookup"><span data-stu-id="8d528-116">The pickling interpreter uses old style parameter descriptors.</span></span>

## <a name="the-oif-style-description"></a><span data-ttu-id="8d528-117">– Oif 樣式描述</span><span class="sxs-lookup"><span data-stu-id="8d528-117">The –Oif Style Description</span></span>

<span data-ttu-id="8d528-118">描述包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="8d528-118">The description consists of the following:</span></span>

``` syntax
-Oif_style_header_descriptor<>
{-Oif_style_parameter_descriptor<6>}*
```

<span data-ttu-id="8d528-119">[**– Oif**](/windows/desktop/Midl/-oi)樣式標頭描述項包含</span><span class="sxs-lookup"><span data-stu-id="8d528-119">The [**–Oif**](/windows/desktop/Midl/-oi) style header descriptor consists of</span></span>

<span data-ttu-id="8d528-120">在編譯器的 [**Oif**](/windows/desktop/Midl/-oi) 或 **-Oicf** 模式中進行編譯時，會產生– Oif 樣式描述。</span><span class="sxs-lookup"><span data-stu-id="8d528-120">The –Oif style description is generated when compiling in [**–Oif**](/windows/desktop/Midl/-oi) or **–Oicf** mode of the compiler.</span></span>

``` syntax
-Oi_style_header_descriptor<>
-Oif_extensions_to_the_old_header<6>
```

<span data-ttu-id="8d528-121">某些較新的功能（例如管道、非同步和 [**/robust**](/windows/desktop/Midl/-robust) ）會在使用時強制執行編譯器的 [**– Oicf**](/windows/desktop/Midl/-oi) 模式。</span><span class="sxs-lookup"><span data-stu-id="8d528-121">Some more recent features like pipe, async, and [**/robust**](/windows/desktop/Midl/-robust) force the [**–Oicf**](/windows/desktop/Midl/-oi) mode of the compiler, when used.</span></span>

## <a name="the-extended-oif-description"></a><span data-ttu-id="8d528-122">外延– Oif 描述</span><span class="sxs-lookup"><span data-stu-id="8d528-122">The Extended –Oif Description</span></span>

<span data-ttu-id="8d528-123">描述包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="8d528-123">The description consists of the following:</span></span>

``` syntax
-Oif_style_header_descriptor<>
extensions_to_the_-Oif_header<8>
{-Oif style parameter descriptors<6>}*
```

 

 