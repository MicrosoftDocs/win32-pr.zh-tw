---
title: 使用 ADSI 架構
description: 架構會定義儲存在目錄中的物件 universe。
ms.assetid: 140a5dd0-6f50-4f84-8708-45c0f1c6bdc4
ms.tgt_platform: multiple
keywords:
- 使用 ADSI 架構
- Adsi ADSI，使用 ADSI 架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 478104a24d850f79cc52473f3d9e546936c56650
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842735"
---
# <a name="using-the-adsi-schema"></a><span data-ttu-id="786f6-105">使用 ADSI 架構</span><span class="sxs-lookup"><span data-stu-id="786f6-105">Using the ADSI Schema</span></span>

<span data-ttu-id="786f6-106">架構會定義儲存在目錄中的物件 universe。</span><span class="sxs-lookup"><span data-stu-id="786f6-106">A schema defines the universe of objects stored in a directory.</span></span> <span data-ttu-id="786f6-107">在 Active Directory 中，架構會指定目錄服務物件可以或必須擁有的屬性。</span><span class="sxs-lookup"><span data-stu-id="786f6-107">In Active Directory, the schema specifies what attributes a directory service object can, or must, have.</span></span> <span data-ttu-id="786f6-108">它也會指定屬性的值範圍和語法，以及它們是否支援單一或多個值。</span><span class="sxs-lookup"><span data-stu-id="786f6-108">It also specifies the value range and the syntax of the attributes and whether they support single or multiple values.</span></span> <span data-ttu-id="786f6-109">簡單地說，架構是依類別定義、屬性定義和屬性語法來組織。</span><span class="sxs-lookup"><span data-stu-id="786f6-109">In short, the schema is organized by class definitions, attribute definitions, and attribute syntax.</span></span> <span data-ttu-id="786f6-110">ADSI 提供三個介面，可讓您從架構讀取屬性、類別和語法資料： [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass)、 [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)和 [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)。</span><span class="sxs-lookup"><span data-stu-id="786f6-110">ADSI provides three interfaces for reading attribute, class, and syntax data from a schema: [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass), [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty), and [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax).</span></span>

<span data-ttu-id="786f6-111">Active Directory 會使用一組架構物件來提供可動態擴充的架構管理。</span><span class="sxs-lookup"><span data-stu-id="786f6-111">Active Directory uses a set of schema objects to provide dynamically extensible schema management.</span></span> <span data-ttu-id="786f6-112">如需未知物件的詳細資訊，請查閱其相關聯的架構物件。</span><span class="sxs-lookup"><span data-stu-id="786f6-112">For more information about an unknown object, look up its associated schema objects.</span></span> <span data-ttu-id="786f6-113">若要建立新的類別定義或擴充現有的類別定義，您可以建立或擴充適當的架構物件。</span><span class="sxs-lookup"><span data-stu-id="786f6-113">To create a new class definition or extend an existing class definition, you can create or extend the appropriate schema objects.</span></span> <span data-ttu-id="786f6-114">架構物件會組織在指定目錄的架構容器中。</span><span class="sxs-lookup"><span data-stu-id="786f6-114">Schema objects are organized in the schema container of a given directory.</span></span> <span data-ttu-id="786f6-115">若要存取物件架構類別，請使用物件的 [**IADs**](iads-property-methods.md) 屬性來取得 ADsPath 字串，然後使用該字串來系結至物件架構類別上的 [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) 介面。</span><span class="sxs-lookup"><span data-stu-id="786f6-115">To access an object schema class, use the [**IADs.Schema**](iads-property-methods.md) property of the object to obtain the ADsPath string and use that string to bind to an [**IADsClass**](/windows/desktop/api/Iads/nn-iads-iadsclass) interface on the object schema class.</span></span>

<span data-ttu-id="786f6-116">若要判斷屬性定義（也就是值的範圍、語法等等），請檢查目錄服務物件所支援之每個屬性的架構屬性物件。</span><span class="sxs-lookup"><span data-stu-id="786f6-116">To determine attribute definitions, that is, the range of values, the syntax, and so on, inspect the schema attribute objects for each property supported by the directory service object.</span></span> <span data-ttu-id="786f6-117">如需有關如何存取架構屬性物件的詳細資訊，請參閱 [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)。</span><span class="sxs-lookup"><span data-stu-id="786f6-117">For more information about how to access the schema attribute objects, see [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty).</span></span>

<span data-ttu-id="786f6-118">ADSI 會視需要將語法資料抽象化，並可讓您使用 [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) 來識別表示物件資料所需的語法。</span><span class="sxs-lookup"><span data-stu-id="786f6-118">ADSI abstracts the syntax data as necessary and enables you to use [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax) to identify the syntax required to represent object data.</span></span>

<span data-ttu-id="786f6-119">如需 Active Directory 架構的詳細資訊，請參閱 [Active Directory 架構](/windows/desktop/AD/active-directory-schema)。</span><span class="sxs-lookup"><span data-stu-id="786f6-119">For more information about the Active Directory schema, see [Active Directory Schema](/windows/desktop/AD/active-directory-schema).</span></span> <span data-ttu-id="786f6-120">如需用來讀取架構容器的程式碼範例，請參閱 [讀取架構](reading-the-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="786f6-120">For code examples to use to read the schema container, see [Reading the Schema](reading-the-schema.md).</span></span>

 

 