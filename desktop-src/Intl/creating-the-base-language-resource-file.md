---
description: 建立基礎語言資源檔
ms.assetid: 770e1f4b-5258-4b6b-afa4-5c19743daaaa
title: 建立基礎語言資源檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96d566625025c105e123e0e2edf9f4f20721274
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027362"
---
# <a name="creating-the-base-language-resource-file"></a><span data-ttu-id="b7c73-103">建立基礎語言資源檔</span><span class="sxs-lookup"><span data-stu-id="b7c73-103">Creating the Base Language Resource File</span></span>

<span data-ttu-id="b7c73-104">使用者介面專案的資源是針對應用程式所支援的基礎語言而定義，例如，英文 (美國) 。</span><span class="sxs-lookup"><span data-stu-id="b7c73-104">Resources for user interface elements are defined for the basic language that the application supports, for example, English (United States).</span></span> <span data-ttu-id="b7c73-105">Win32 PE 資源檔的範例是使用 RC 編譯器建立的 .rc 檔。</span><span class="sxs-lookup"><span data-stu-id="b7c73-105">An example of a Win32 PE resource file is an .rc file, created using RC Compiler.</span></span> <span data-ttu-id="b7c73-106">如需建立 .rc 檔的詳細資訊，請參閱 [關於資源檔](../menurc/about-resource-files.md)。</span><span class="sxs-lookup"><span data-stu-id="b7c73-106">For details of .rc file creation, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

<span data-ttu-id="b7c73-107">如果使用基礎語言資源的 .rc 檔，您可以選擇使用資源設定檔來表示資源設定資料的 XML 表示。</span><span class="sxs-lookup"><span data-stu-id="b7c73-107">If using an .rc file for the base language resources, you have the option of using a resource configuration file for an XML representation of resource configuration data.</span></span> <span data-ttu-id="b7c73-108">若要建立這個檔案，請參閱 [準備資源設定檔](preparing-a-resource-configuration-file.md)。</span><span class="sxs-lookup"><span data-stu-id="b7c73-108">To create this file, see [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>

<span data-ttu-id="b7c73-109">您也可以使用非 Win32 PE 檔案來定義基礎語言資源。</span><span class="sxs-lookup"><span data-stu-id="b7c73-109">You can also use a non-Win32 PE file to define base language resources.</span></span> <span data-ttu-id="b7c73-110">例如，您可以針對此用途使用 .xml 檔案或 .txt 檔案。</span><span class="sxs-lookup"><span data-stu-id="b7c73-110">For example, you might use an .xml file or .txt file for this purpose.</span></span>

> [!Note]  
> <span data-ttu-id="b7c73-111">當您使用非 Win32 PE 檔案來定義基礎語言資源時，不能使用 RC 編譯器進行資源定義。</span><span class="sxs-lookup"><span data-stu-id="b7c73-111">When you define base language resources using a non-Win32 PE file, you cannot use RC Compiler for resource definition.</span></span> <span data-ttu-id="b7c73-112">相反地，您會定義自己的資源格式，而您的應用程式必須提供自己的功能，以尋找並載入所需的資源。</span><span class="sxs-lookup"><span data-stu-id="b7c73-112">Instead, you define your own resource format, and your application must provide its own functionality to find and load the required resources.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="b7c73-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="b7c73-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7c73-114">準備資源</span><span class="sxs-lookup"><span data-stu-id="b7c73-114">Preparing Resources</span></span>](preparing-resources.md)
</dt> <dt>

[<span data-ttu-id="b7c73-115">準備資源設定檔</span><span class="sxs-lookup"><span data-stu-id="b7c73-115">Preparing a Resource Configuration File</span></span>](preparing-a-resource-configuration-file.md)
</dt> </dl>

 

 
