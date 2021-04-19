---
description: 說明如何針對 Tablet PC 的功能來識別視窗。
ms.assetid: 513e0c9d-4c9e-4e7c-8314-bd7603489e89
title: 依函數的函式來識別視窗
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 497f660d6690bd4dc37c252f82f2408da3e3655d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972868"
---
# <a name="identifying-a-window-by-its-function"></a><span data-ttu-id="8e496-103">依函數的函式來識別視窗</span><span class="sxs-lookup"><span data-stu-id="8e496-103">Identifying a Window by Its Function</span></span>

<span data-ttu-id="8e496-104">藉由指派唯一的視窗類別來識別每種類型的視窗。</span><span class="sxs-lookup"><span data-stu-id="8e496-104">Identify each type of window by assigning it a unique window class.</span></span> <span data-ttu-id="8e496-105">避免使用適用于各種函式的單一視窗類別。</span><span class="sxs-lookup"><span data-stu-id="8e496-105">Avoid having a single window class that is used for a wide variety of functions.</span></span>

<span data-ttu-id="8e496-106">協助工具輔助必須有此識別，才能在相同的應用程式中處理不同的視窗。</span><span class="sxs-lookup"><span data-stu-id="8e496-106">Accessibility aids must have this identification in order to handle different windows within the same application.</span></span> <span data-ttu-id="8e496-107">您可能會有個別的指示來處理這些視窗，例如在內容變更時宣佈特定的領域。</span><span class="sxs-lookup"><span data-stu-id="8e496-107">There may be separate instructions for handling these windows, such as announcing specific areas when the content changes.</span></span>

<span data-ttu-id="8e496-108">如果您無法使用不同的視窗類別，您可以透過 Microsoft <entity type="reg"/> Active Accessibility <entity type="reg"/> 或必要時，透過您在網站上記載的私用視窗訊息來公開差異。</span><span class="sxs-lookup"><span data-stu-id="8e496-108">If you cannot use separate window classes, you can expose the differences through Microsoft<entity type="reg"/> Active Accessibility<entity type="reg"/>, or if necessary, by a private window message that you document on your website.</span></span>

<span data-ttu-id="8e496-109">如需使用 Active Accessibility 公開視窗類別的詳細資訊，請參閱 [協助工具](/windows/desktop/accessibility) 一節。</span><span class="sxs-lookup"><span data-stu-id="8e496-109">For more information about exposing window classes by using Active Accessibility, see the [Accessibility](/windows/desktop/accessibility) section.</span></span>

 

 
