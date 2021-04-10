---
title: 架構延伸模組
description: ADSI 架構的架構可讓您將新的架構類別加入至架構類別容器，並在執行時間將新的屬性加入至現有的架構類別物件。
ms.assetid: 935d39ca-cfb9-4aa3-aa0e-b614f7b359f2
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b86491966e2bfddbef72d68d7a96869448c38188
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092191"
---
# <a name="schema-extensions"></a><span data-ttu-id="82c2e-103">架構延伸模組</span><span class="sxs-lookup"><span data-stu-id="82c2e-103">Schema Extensions</span></span>

<span data-ttu-id="82c2e-104">ADSI 架構的架構可讓您將新的架構類別加入至架構類別容器，並在執行時間將新的屬性加入至現有的架構類別物件。</span><span class="sxs-lookup"><span data-stu-id="82c2e-104">The architecture of the ADSI schema provides that new schema classes can be added to the schema class container and new properties to an existing schema class object at run time.</span></span> <span data-ttu-id="82c2e-105">後者的功能不需要新的程式碼。</span><span class="sxs-lookup"><span data-stu-id="82c2e-105">The latter ability requires no new code.</span></span> <span data-ttu-id="82c2e-106">對於允許可延伸目錄服務的命名空間，這是一項重要的功能。</span><span class="sxs-lookup"><span data-stu-id="82c2e-106">This is an important feature for namespaces that allow extensible directory services.</span></span> <span data-ttu-id="82c2e-107">提供者元件必須允許此擴充性，並知道要存取和儲存類別實例和其屬性值的位置。</span><span class="sxs-lookup"><span data-stu-id="82c2e-107">The provider component must allow for this extensibility and know where to access and store the class instance and the values of its properties.</span></span> <span data-ttu-id="82c2e-108">在典型的可延伸目錄服務中，這項資訊會以與任何其他架構類別和屬性定義相同的方式儲存在目錄服務資料庫中。</span><span class="sxs-lookup"><span data-stu-id="82c2e-108">In a typical extensible directory service, this information is stored in the directory service database in the same manner as any other schema class and property definitions.</span></span>

> [!Note]  
> <span data-ttu-id="82c2e-109">在 COM 介面詞彙中，只有屬性可以加入至現有的架構類別，而不是方法。</span><span class="sxs-lookup"><span data-stu-id="82c2e-109">In COM interface terminology, only properties can be added to an existing schema class, not methods.</span></span> <span data-ttu-id="82c2e-110">加入新的方法需要加入該方法的新實，因此需要額外的程式碼。</span><span class="sxs-lookup"><span data-stu-id="82c2e-110">Adding a new method would require adding a new implementation of that method and thus require additional code.</span></span>

 

<span data-ttu-id="82c2e-111">如需特定提供者架構的範例，請參閱 [架構管理](schema-management.md)。</span><span class="sxs-lookup"><span data-stu-id="82c2e-111">For an example of a specific provider schema, see [Schema Management](schema-management.md).</span></span>

 

 




