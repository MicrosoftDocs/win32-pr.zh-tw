---
description: 使用主動存取範圍來公開文字的總覽。
ms.assetid: c04ade90-5f17-4e16-b82b-c99230000954
title: 使用 Active Accessibility 來公開文字
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52d475a8c576e109f47be7b5a3d61cddf543038d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973633"
---
# <a name="using-active-accessibility-to-expose-text"></a><span data-ttu-id="0ee60-103">使用 Active Accessibility 來公開文字</span><span class="sxs-lookup"><span data-stu-id="0ee60-103">Using Active Accessibility to Expose Text</span></span>

<span data-ttu-id="0ee60-104">應用程式可以使用 Microsoft Active Accessibility 來公開文字。</span><span class="sxs-lookup"><span data-stu-id="0ee60-104">Applications can use Microsoft Active Accessibility to expose text.</span></span> <span data-ttu-id="0ee60-105">不過，舊版 Active Accessibility 所定義的 [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) 介面未針對公開大量 rtf 文字進行優化。</span><span class="sxs-lookup"><span data-stu-id="0ee60-105">However, the [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible) interface defined by earlier versions of Active Accessibility is not optimized for exposing large amounts of rich text.</span></span> <span data-ttu-id="0ee60-106">較新的版本會定義已針對公開大量文字和文字屬性優化的介面。</span><span class="sxs-lookup"><span data-stu-id="0ee60-106">Later versions define interfaces that are optimized for exposing large amounts of text and textual attributes.</span></span>

<span data-ttu-id="0ee60-107">若要公開大量文字，請建立個別的元件物件模型 (COM) 物件，這些物件支援 [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible)或子項目，以代表每個文字執行。</span><span class="sxs-lookup"><span data-stu-id="0ee60-107">To expose large amounts text, create separate Component Object Model (COM) objects that support [**IAccessible**](/windows/win32/api/oleacc/nn-oleacc-iaccessible), or child elements, to represent each run of text.</span></span> <span data-ttu-id="0ee60-108">執行是共用相同格式的一行或一行部分。</span><span class="sxs-lookup"><span data-stu-id="0ee60-108">A run is a line, or portion of a line, that shares the same formatting.</span></span>

<span data-ttu-id="0ee60-109">Active Accessibility 只會公開文字及其位置，但沒有公開文字格式的機制。</span><span class="sxs-lookup"><span data-stu-id="0ee60-109">Active Accessibility exposes only the text and its location, but has no mechanism for exposing the formatting of the text.</span></span> <span data-ttu-id="0ee60-110">儘管有這些限制，某些程式還是會使用 Active Accessibility 來公開文字。</span><span class="sxs-lookup"><span data-stu-id="0ee60-110">Despite these limitations, some programs use Active Accessibility to expose text.</span></span> <span data-ttu-id="0ee60-111">例如，Microsoft Internet Explorer 和 Microsoft Visual Studio 都會使用 Active Accessibility 來公開大量的文字。</span><span class="sxs-lookup"><span data-stu-id="0ee60-111">For example, Microsoft Internet Explorer and Microsoft Visual Studio both use Active Accessibility to expose large amounts of text.</span></span>

<span data-ttu-id="0ee60-112">如需使用 Active Accessibility 公開文字的詳細資訊，請參閱 [協助工具](../accessibility/accessibility.md)。</span><span class="sxs-lookup"><span data-stu-id="0ee60-112">For more information about exposing text by using Active Accessibility, see [Accessibility](../accessibility/accessibility.md).</span></span>

 

 
