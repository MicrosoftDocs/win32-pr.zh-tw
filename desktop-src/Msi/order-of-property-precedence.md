---
description: 安裝程式會使用下列優先順序來設定屬性。 此清單中的屬性值可以覆寫在其後面的值，並由在清單中之前的值覆寫。
ms.assetid: ba9240fe-2e5a-43f5-8cdf-59dd6348092b
title: 屬性優先順序的順序
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90c114594b9a825a3847db37f5b98dc990211d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980064"
---
# <a name="order-of-property-precedence"></a><span data-ttu-id="90e0b-104">屬性優先順序的順序</span><span class="sxs-lookup"><span data-stu-id="90e0b-104">Order of Property Precedence</span></span>

<span data-ttu-id="90e0b-105">安裝程式會使用下列優先順序來設定屬性。</span><span class="sxs-lookup"><span data-stu-id="90e0b-105">The installer sets properties using the following order of precedence.</span></span> <span data-ttu-id="90e0b-106">此清單中的屬性值可以覆寫在其後面的值，並由在清單中之前的值覆寫。</span><span class="sxs-lookup"><span data-stu-id="90e0b-106">A property value in this list can override a value that comes after it and be overridden by a value coming before it in the list.</span></span>

1.  <span data-ttu-id="90e0b-107">作業環境所指定的屬性。</span><span class="sxs-lookup"><span data-stu-id="90e0b-107">Properties specified by the operating environment.</span></span>
2.  <span data-ttu-id="90e0b-108">在命令列上設定的[公用屬性](public-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="90e0b-108">[Public properties](public-properties.md) set on the command line.</span></span>
3.  <span data-ttu-id="90e0b-109">[**AdminProperties**](adminproperties.md) propertyset 在 [系統管理安裝](administrative-installation.md)期間列出的公用屬性。</span><span class="sxs-lookup"><span data-stu-id="90e0b-109">Public properties listed by the [**AdminProperties**](adminproperties.md) propertyset during an [administrative installation](administrative-installation.md) .</span></span>
4.  <span data-ttu-id="90e0b-110">在應用程式 [*轉換*](t-gly.md)期間設定的公用或私用屬性。</span><span class="sxs-lookup"><span data-stu-id="90e0b-110">Public or private properties set during the application of a [*transform*](t-gly.md).</span></span>
5.  <span data-ttu-id="90e0b-111">藉由撰寫 .msi 檔案的 [屬性工作表](property-table.md) 所設定的公用或私用屬性。</span><span class="sxs-lookup"><span data-stu-id="90e0b-111">Public or private property that set by authoring the [Property table](property-table.md) of the .msi file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90e0b-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="90e0b-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90e0b-113">關於屬性</span><span class="sxs-lookup"><span data-stu-id="90e0b-113">About Properties</span></span>](about-properties.md)
</dt> </dl>

 

 



