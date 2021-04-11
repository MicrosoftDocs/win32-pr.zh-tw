---
description: 本主題摘要說明在您的應用程式中加入 MUI 功能時，要牢記在心的主要程式設計考慮。
ms.assetid: 10064f5c-5563-44f8-afb5-c6c77991e13c
title: 開發 MUI 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb4a3278b4cc70969c1aa968de895d99fd3363a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851816"
---
# <a name="development-of-mui-applications"></a><span data-ttu-id="c616c-103">開發 MUI 應用程式</span><span class="sxs-lookup"><span data-stu-id="c616c-103">Development of MUI Applications</span></span>

<span data-ttu-id="c616c-104">本主題摘要說明在您的應用程式中加入 MUI 功能時，要牢記在心的主要程式設計考慮。</span><span class="sxs-lookup"><span data-stu-id="c616c-104">This topic summarizes the main programming considerations to keep in mind when adding MUI functionality to your applications.</span></span>

## <a name="requirements-for-a-mui-application"></a><span data-ttu-id="c616c-105">MUI 應用程式的需求</span><span class="sxs-lookup"><span data-stu-id="c616c-105">Requirements for a MUI Application</span></span>

<span data-ttu-id="c616c-106">MUI 功能只適用于完整全球化應用程式的當地語系化，使用稱為軟體國際化的程式建立。</span><span class="sxs-lookup"><span data-stu-id="c616c-106">MUI functionality is applied only to the localization of a fully globalized application, created using a process called software internationalization.</span></span> <span data-ttu-id="c616c-107">Microsoft [Go 全球開發人員中心](https://msdn.microsoft.com/goglobal) 提供廣泛的相關檔，可協助您設計、建立及部署可供使用的全球應用程式。</span><span class="sxs-lookup"><span data-stu-id="c616c-107">The Microsoft [Go Global Developer Center](https://msdn.microsoft.com/goglobal) provides a wide selection of related documentation that helps you design, build, and deploy world-ready applications.</span></span> <span data-ttu-id="c616c-108">這些檔可協助您考慮不同人類語言的特性如何影響您的軟體設計。</span><span class="sxs-lookup"><span data-stu-id="c616c-108">These documents help you consider how the characteristics of different human languages can affect the design of your software.</span></span> <span data-ttu-id="c616c-109">請注意，入口網站也會提供 Dr. 國際資料行的完整保存。</span><span class="sxs-lookup"><span data-stu-id="c616c-109">Note that the portal also provides a complete archive of Dr. International columns.</span></span>

<span data-ttu-id="c616c-110">您的 MUI 應用程式可以在任何語言或地區設定下執行，而且使用者可以要求應用程式包含支援的任何語言。</span><span class="sxs-lookup"><span data-stu-id="c616c-110">Your MUI application can run under any language or locale setting, and the user can request any language for which the application includes support.</span></span> <span data-ttu-id="c616c-111">因此，應用程式必須將使用者介面文字編碼，以支援最廣泛的可能各種語言。</span><span class="sxs-lookup"><span data-stu-id="c616c-111">Therefore, the application must encode user interface text to support the widest possible variety of languages.</span></span> <span data-ttu-id="c616c-112">最重要的一點是使用 [Unicode](unicode.md) 來處理所有文字處理。</span><span class="sxs-lookup"><span data-stu-id="c616c-112">The most important thing to remember is to use [Unicode](unicode.md) to handle all text processing.</span></span> <span data-ttu-id="c616c-113">如需使用 Unicode 進行全球化的詳細資訊，請參閱 Microsoft [Go 全球開發人員中心](https://msdn.microsoft.com/goglobal)。</span><span class="sxs-lookup"><span data-stu-id="c616c-113">For more information about globalization using Unicode, see the Microsoft [Go Global Developer Center](https://msdn.microsoft.com/goglobal).</span></span>

## <a name="supported-programming-environments"></a><span data-ttu-id="c616c-114">支援的程式設計環境</span><span class="sxs-lookup"><span data-stu-id="c616c-114">Supported Programming Environments</span></span>

<span data-ttu-id="c616c-115">您可以依照此 SDK 所述，將 MUI 功能新增至全球化的 Win32 forms 應用程式或主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="c616c-115">You can add MUI functionality to a globalized Win32 forms application or console application as described in this SDK.</span></span> <span data-ttu-id="c616c-116">此外，您可以使用與 MUI 相容的 .NET Framework 來建立受控應用程式。</span><span class="sxs-lookup"><span data-stu-id="c616c-116">In addition, you can create managed applications using .NET Framework, which is compatible with MUI.</span></span> <span data-ttu-id="c616c-117">如需詳細資訊，請參閱 [.Net 開發](/previous-versions/ff361664(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="c616c-117">For more information, see [.NET Development](/previous-versions/ff361664(v=vs.100)).</span></span>

## <a name="user-interface-language-settings"></a><span data-ttu-id="c616c-118">消費者介面語言設定</span><span class="sxs-lookup"><span data-stu-id="c616c-118">User Interface Language Settings</span></span>

<span data-ttu-id="c616c-119">在規劃 MUI 應用程式時，您必須先決定使用者介面的語言，以及將它們呈現給使用者的方式。</span><span class="sxs-lookup"><span data-stu-id="c616c-119">When planning your MUI application, you must first decide on the languages for the user interface and the way to present them to the user.</span></span> <span data-ttu-id="c616c-120">應用程式可透過下列其中一種方式支援語言：</span><span class="sxs-lookup"><span data-stu-id="c616c-120">The application can support languages in one of these ways:</span></span>

-   <span data-ttu-id="c616c-121">遵循系統語言設定。</span><span class="sxs-lookup"><span data-stu-id="c616c-121">Follow system language settings.</span></span> <span data-ttu-id="c616c-122">假設使用者慣用的 UI 語言和系統慣用的 UI 語言（結合在一起）表示使用者可用的語言。</span><span class="sxs-lookup"><span data-stu-id="c616c-122">Assume that the user preferred UI languages and the system preferred UI languages, taken together, represent the languages available to the user.</span></span> <span data-ttu-id="c616c-123">使用資源載入器的回溯機制來選擇語言。</span><span class="sxs-lookup"><span data-stu-id="c616c-123">Use the fallback mechanism of the resource loader for language selection.</span></span>
-   <span data-ttu-id="c616c-124">建立應用程式特定的語言設定。</span><span class="sxs-lookup"><span data-stu-id="c616c-124">Make application-specific language settings.</span></span> <span data-ttu-id="c616c-125">支援特定語言，並向使用者呈現選取機制。</span><span class="sxs-lookup"><span data-stu-id="c616c-125">Support specific languages and present a selection mechanism to the user.</span></span>

## <a name="resource-creation"></a><span data-ttu-id="c616c-126">資源建立</span><span class="sxs-lookup"><span data-stu-id="c616c-126">Resource Creation</span></span>

<span data-ttu-id="c616c-127">本節說明為應用程式建立使用者介面語言資源的可能性。</span><span class="sxs-lookup"><span data-stu-id="c616c-127">This section describes the possibilities for creating the user interface language resources for the application.</span></span> <span data-ttu-id="c616c-128">如需詳細資訊，請參閱 [準備資源](preparing-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="c616c-128">For more information, see [Preparing Resources](preparing-resources.md).</span></span>

> [!Note]  
> <span data-ttu-id="c616c-129">在 Windows Vista 之前版本的作業系統上，您通常會以可執行檔中包含的資源區段所支援的語言，建立靜態和個別封裝的單一語言當地語系化應用程式。</span><span class="sxs-lookup"><span data-stu-id="c616c-129">On pre-Windows Vista operating systems, you generally create static and separately packaged single-language localized applications with the languages supported by resource sections included in the executable files.</span></span> <span data-ttu-id="c616c-130">這種類型的實大部分已淘汰，建議您選擇本節中所述的其他資源建立技巧，以支援 Windows Vista 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="c616c-130">This type of implementation is largely obsolete, and you are recommended to choose one of the other resource creation techniques described in this section, supported for Windows Vista and later.</span></span> <span data-ttu-id="c616c-131">然後，您可以使用 [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)，在 Windows Vista 之前的作業系統上執行此應用程式。</span><span class="sxs-lookup"><span data-stu-id="c616c-131">The application can then be made to run on pre-Windows Vista operating systems by the use of [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya).</span></span>

 

### <a name="use-of-a-single-language-in-a-resource-dll-mui-resource-technology"></a><span data-ttu-id="c616c-132">使用資源 DLL 中的單一語言 (MUI 資源技術) </span><span class="sxs-lookup"><span data-stu-id="c616c-132">Use of a Single Language in a Resource DLL (MUI Resource Technology)</span></span>

<span data-ttu-id="c616c-133">許多 Microsoft 應用程式都會使用標準的附屬 DLL 資源實作為。</span><span class="sxs-lookup"><span data-stu-id="c616c-133">A standard satellite DLL resource implementation is used by many Microsoft applications.</span></span> <span data-ttu-id="c616c-134">在此情況下，會針對 MUI 應用程式使用核心可執行檔，並為每個支援的語言建立一個資源 DLL。</span><span class="sxs-lookup"><span data-stu-id="c616c-134">In this case, a core executable file is used for the MUI application and one resource DLL is created for each supported language.</span></span> <span data-ttu-id="c616c-135">使用附屬 DLL 適用于在任何 Windows 作業系統上執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="c616c-135">Use of a satellite DLL applies to applications that run on any Windows operating system.</span></span> <span data-ttu-id="c616c-136">如 [Mui 資源管理](mui-resource-management.md)中所述，mui 資源技術支援標準附屬 DLL 執行的變化。</span><span class="sxs-lookup"><span data-stu-id="c616c-136">As described in [MUI Resource Management](mui-resource-management.md), the MUI resource technology supports a variation on the standard satellite DLL implementation.</span></span>

### <a name="use-of-multiple-languages-in-a-resource-dll"></a><span data-ttu-id="c616c-137">在資源 DLL 中使用多種語言</span><span class="sxs-lookup"><span data-stu-id="c616c-137">Use of Multiple Languages in a Resource DLL</span></span>

<span data-ttu-id="c616c-138">您可以選擇為您的 MUI 應用程式建立一個核心可執行檔，並為與支援語言相關聯的資源建立一個資源 DLL。</span><span class="sxs-lookup"><span data-stu-id="c616c-138">You can choose to create one core executable file for your MUI application and one resource DLL for the resources associated with supported languages.</span></span> <span data-ttu-id="c616c-139">相同資源識別碼的複本會在基礎語言資源檔中定義 ( .rc 延伸模組) 在所有支援語言的不同語言標記下。</span><span class="sxs-lookup"><span data-stu-id="c616c-139">Copies of the same resource identifier are defined in the base language resource file (.rc extension) under different language tags for all supported languages.</span></span>

### <a name="use-of-an-application-specific-resource-mechanism"></a><span data-ttu-id="c616c-140">使用 Application-Specific 資源機制</span><span class="sxs-lookup"><span data-stu-id="c616c-140">Use of an Application-Specific Resource Mechanism</span></span>

<span data-ttu-id="c616c-141">您可以規劃 MUI 應用程式以使用自訂的資源機制。</span><span class="sxs-lookup"><span data-stu-id="c616c-141">You can plan your MUI application to use a customized resource mechanism.</span></span> <span data-ttu-id="c616c-142">在此情況下，應用程式會以特殊方式處理其資源載入。</span><span class="sxs-lookup"><span data-stu-id="c616c-142">In this case, the application handles its resource loading in a specialized way.</span></span>

## <a name="resource-localization"></a><span data-ttu-id="c616c-143">資源當地語系化</span><span class="sxs-lookup"><span data-stu-id="c616c-143">Resource Localization</span></span>

<span data-ttu-id="c616c-144">若要支援 MUI 應用程式的使用者介面語言，您必須將語言資源當地語系化。</span><span class="sxs-lookup"><span data-stu-id="c616c-144">To support the user interface languages for your MUI application, you must have the language resources localized.</span></span> <span data-ttu-id="c616c-145">MUI 支援兩種類型的當地語系化，如下表所述。</span><span class="sxs-lookup"><span data-stu-id="c616c-145">MUI supports two types of localization, as described in the following table.</span></span>



| <span data-ttu-id="c616c-146">當地語系化類型</span><span class="sxs-lookup"><span data-stu-id="c616c-146">Localization type</span></span>       | <span data-ttu-id="c616c-147">Description</span><span class="sxs-lookup"><span data-stu-id="c616c-147">Description</span></span>                                                                                                                                                                                                                                                                |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c616c-148">預先建立當地語系化</span><span class="sxs-lookup"><span data-stu-id="c616c-148">Pre-build localization</span></span>  | <span data-ttu-id="c616c-149">在建立應用程式和特定語言的資源之前，先要求當地語系化。</span><span class="sxs-lookup"><span data-stu-id="c616c-149">Request localization before building the application and language-specific resources.</span></span> <span data-ttu-id="c616c-150">針對每個支援的語言，會針對支援的使用者介面語言複製並重新命名基底語言資源檔，並視需要將這些複本提供給當地語系化人員。</span><span class="sxs-lookup"><span data-stu-id="c616c-150">The base language resource file for the supported user interface languages is copied and renamed for each supported language, and the copies are provided to localizers as required.</span></span> |
| <span data-ttu-id="c616c-151">組建後當地語系化</span><span class="sxs-lookup"><span data-stu-id="c616c-151">Post-build localization</span></span> | <span data-ttu-id="c616c-152">建立應用程式的可執行檔和資源 DLL 之後，要求當地語系化。</span><span class="sxs-lookup"><span data-stu-id="c616c-152">Request localization after building the executable file and resource DLL for your application.</span></span> <span data-ttu-id="c616c-153">在此情況下，會將資源 DLL 的複本提供給每個當地語系化人員。</span><span class="sxs-lookup"><span data-stu-id="c616c-153">In this case, a copy of the resource DLL is provided to each localizer.</span></span>                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="c616c-154">相關主題</span><span class="sxs-lookup"><span data-stu-id="c616c-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c616c-155">關於多語系消費者介面</span><span class="sxs-lookup"><span data-stu-id="c616c-155">About Multilingual User Interface</span></span>](about-multilingual-user-interface.md)
</dt> </dl>

 

 
