---
title: EventManifest 架構
ms.assetid: 89acbc43-739b-4e89-a96a-cc3438ec8ecc
description: 深入瞭解： EventManifest 架構
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 67e1c2e9b769cd26e81a71853037655220a27d1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001709"
---
# <a name="eventmanifest-schema"></a><span data-ttu-id="37594-103">EventManifest 架構</span><span class="sxs-lookup"><span data-stu-id="37594-103">EventManifest Schema</span></span>

<span data-ttu-id="37594-104">EventManifest 架構會定義您用來撰寫檢測資訊清單的下列元素和類型：</span><span class="sxs-lookup"><span data-stu-id="37594-104">The EventManifest schema defines the following elements and types that you use to write an instrumentation manifest:</span></span>

-   [<span data-ttu-id="37594-105">EventManifestSchema 元素</span><span class="sxs-lookup"><span data-stu-id="37594-105">EventManifestSchema Elements</span></span>](eventmanifestschema-elements.md)
-   [<span data-ttu-id="37594-106">EventManifestSchema 簡單類型</span><span class="sxs-lookup"><span data-stu-id="37594-106">EventManifestSchema Simple Types</span></span>](eventmanifestschema-simple-types.md)
-   [<span data-ttu-id="37594-107">EventManifestSchema 複雜類型</span><span class="sxs-lookup"><span data-stu-id="37594-107">EventManifestSchema Complex Types</span></span>](eventmanifestschema-complex-types.md)

<span data-ttu-id="37594-108">Elements 區段包含您在資訊清單中使用的元素名稱;不過，若要取得每個專案的詳細資料，請參閱包含元素的複雜類型。</span><span class="sxs-lookup"><span data-stu-id="37594-108">The elements section contains the names of the elements that you use in your manifest; however, to get the details for each element, see the complex type that contains the element.</span></span>

<span data-ttu-id="37594-109">檢測資訊清單是一種 XML 檔案，可定義事件提供者、寫入事件的通道、事件本身、事件篩選準則（例如層級、工作和 opcode），以及轉譯事件時使用的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="37594-109">An instrumentation manifest is an XML file that defines an event provider, the channels to which the events are written, the events themselves, the event filtering criteria such as levels, tasks, and opcodes, and the localized strings used when rendering the events.</span></span> <span data-ttu-id="37594-110">慣例是使用. man 做為資訊清單檔的副檔名。</span><span class="sxs-lookup"><span data-stu-id="37594-110">The convention is to use .man as the extension for manifest files.</span></span> <span data-ttu-id="37594-111">如需寫入資訊清單的詳細資訊，請參閱 [撰寫檢測資訊清單](writing-an-instrumentation-manifest.md)。</span><span class="sxs-lookup"><span data-stu-id="37594-111">For details on writing a manifest, see [Writing an Instrumentation Manifest](writing-an-instrumentation-manifest.md).</span></span>

<span data-ttu-id="37594-112">Windows SDK 包含 \\ 包含 Eventman .xsd 檔案中的架構。 \\</span><span class="sxs-lookup"><span data-stu-id="37594-112">The Windows SDK includes the schema in the \\Include\\Eventman.xsd file.</span></span> <span data-ttu-id="37594-113">您可以使用 XSD 來驗證您的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="37594-113">You can use the XSD to validate your manifest.</span></span>

<span data-ttu-id="37594-114">除了 EventManifest 架構之外，Windows 事件記錄檔也會定義下列架構：</span><span class="sxs-lookup"><span data-stu-id="37594-114">In addition to the EventManifest schema, Windows Event Log also defines the following schemas:</span></span>

-   <span data-ttu-id="37594-115">[事件架構](eventschema-schema.md)：定義用來呈現事件的元素和類型。</span><span class="sxs-lookup"><span data-stu-id="37594-115">[Event Schema](eventschema-schema.md)—defines the elements and types used to render an event.</span></span>
-   <span data-ttu-id="37594-116">[查詢架構](queryschema-schema.md)：定義用來撰寫查詢以從一或多個通道取出事件的元素和類型。</span><span class="sxs-lookup"><span data-stu-id="37594-116">[Query Schema](queryschema-schema.md)—defines the elements and types used to write a query to retrieve events from one or more channels.</span></span>

 

 




