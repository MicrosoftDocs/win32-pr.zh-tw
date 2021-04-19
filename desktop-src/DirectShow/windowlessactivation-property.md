---
description: WindowlessActivation 屬性會在設計階段為視窗化或無視窗模式初始化 MSWebDVD 物件。
ms.assetid: 290a9459-154a-4ec7-a013-d696e6b27341
title: WindowlessActivation 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 427fdcb265d60200bfe8716cd1ece384861fbdf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106999936"
---
# <a name="windowlessactivation-property"></a><span data-ttu-id="263c8-103">WindowlessActivation 屬性</span><span class="sxs-lookup"><span data-stu-id="263c8-103">WindowlessActivation Property</span></span>

> [!Note]  
> <span data-ttu-id="263c8-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="263c8-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="263c8-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="263c8-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="263c8-106">`WindowlessActivation`屬性會在設計階段為視窗化或無視窗模式初始化 **MSWebDVD** 物件。</span><span class="sxs-lookup"><span data-stu-id="263c8-106">The `WindowlessActivation` property initializes the **MSWebDVD** object at design time for either windowed or windowless mode.</span></span>

``` syntax
[ bWindowless = ] MSWebDVD.WindowlessActivation
```

## <a name="return-value"></a><span data-ttu-id="263c8-107">傳回值</span><span class="sxs-lookup"><span data-stu-id="263c8-107">Return Value</span></span>

<span data-ttu-id="263c8-108">傳回物件是否為視窗模式的布林值。</span><span class="sxs-lookup"><span data-stu-id="263c8-108">Returns whether the object is in windowed mode as a Boolean.</span></span>

## <a name="remarks"></a><span data-ttu-id="263c8-109">備註</span><span class="sxs-lookup"><span data-stu-id="263c8-109">Remarks</span></span>

<span data-ttu-id="263c8-110">此屬性是讀取/寫入，預設值為 true。</span><span class="sxs-lookup"><span data-stu-id="263c8-110">This property is read/write with a default value of true.</span></span> <span data-ttu-id="263c8-111">因此，如果您在視窗化的容器中執行 **MSWebDVD** 物件，則只需要設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="263c8-111">Therefore, you only need to set this property if you are running the **MSWebDVD** object in a windowed container.</span></span> <span data-ttu-id="263c8-112">當包含在 Microsoft® Internet Explorer 的網頁時， **MSWebDVD** 一律會處於無視窗模式，而您不需要設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="263c8-112">When contained in a Web page in Microsoft® Internet Explorer, **MSWebDVD** is always in windowless mode, and you don't need to set this property.</span></span>

 

 



