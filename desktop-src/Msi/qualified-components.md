---
description: 限定的元件是單一層級間接取值的方法，類似于指標。
ms.assetid: b483fa7d-d31d-4855-89e5-f733541cd92d
title: 合格元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd2197aade7f3efd5d73e666c190c4447cac9fe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849155"
---
# <a name="qualified-components"></a><span data-ttu-id="5b9c5-103">合格元件</span><span class="sxs-lookup"><span data-stu-id="5b9c5-103">Qualified Components</span></span>

<span data-ttu-id="5b9c5-104">限定的元件是單一層級間接取值的方法，類似于指標。</span><span class="sxs-lookup"><span data-stu-id="5b9c5-104">A qualified component is a method of single-level indirection, similar to a pointer.</span></span> <span data-ttu-id="5b9c5-105">限定元件主要是用來將具有平行功能的元件群組成類別。</span><span class="sxs-lookup"><span data-stu-id="5b9c5-105">Qualified components are primarily used to group components with parallel functionality into categories.</span></span> <span data-ttu-id="5b9c5-106">例如，如果 [元件資料表](component-table.md) 中列出的30個元件是當地語系化為30個語言的相同 Microsoft Word 傳真範本，您可以使用 [PublishComponent 資料表](publishcomponent-table.md)，將這些元件一起分組為合格元件的類別。</span><span class="sxs-lookup"><span data-stu-id="5b9c5-106">For example, if you have 30 components listed in the [Component table](component-table.md) that are the same Microsoft Word fax template localized into 30 languages, you can group these together into a category of qualified components by using the [PublishComponent table](publishcomponent-table.md).</span></span>

<span data-ttu-id="5b9c5-107">在元件資料表中輸入限定元件的方式與一般元件相同。</span><span class="sxs-lookup"><span data-stu-id="5b9c5-107">Qualified components are entered in the Component table in the same way as ordinary components.</span></span> <span data-ttu-id="5b9c5-108">每個元件都必須有唯一的元件識別碼 GUID，以及元件資料表中指定的元件識別碼。</span><span class="sxs-lookup"><span data-stu-id="5b9c5-108">Every component must have a unique component ID GUID and component identifier specified in the Component table.</span></span> <span data-ttu-id="5b9c5-109">此外，限定的元件會與 PublishComponent 資料表中的分類 GUID 和文字字串辨識符號相關聯。</span><span class="sxs-lookup"><span data-stu-id="5b9c5-109">In addition, qualified components are associated with a category GUID and a text-string qualifier in the PublishComponent table.</span></span> <span data-ttu-id="5b9c5-110">限定的元件是由類別目錄 GUID 和辨識符號所參考，而限定詞只會指向元件資料表中的一般元件。</span><span class="sxs-lookup"><span data-stu-id="5b9c5-110">Qualified components are referenced by the category GUID and the qualifier, which just points to the ordinary component in the Component table.</span></span>

<span data-ttu-id="5b9c5-111">例如，限定的元件識別碼 GUID 可指向資源 DLL 的不同語言版本。</span><span class="sxs-lookup"><span data-stu-id="5b9c5-111">For example, a qualified component ID GUID can point to different language versions of a resource DLL.</span></span> <span data-ttu-id="5b9c5-112">在此情況下，當地語系化資源 Dll 的群組包含類別目錄和數值地區設定識別碼 (LCID) 字串通常用來作為限定詞。</span><span class="sxs-lookup"><span data-stu-id="5b9c5-112">In this case, the group of localized resource DLLs comprises the category and the numeric locale identifiers (LCID) strings are commonly used as the qualifiers.</span></span> <span data-ttu-id="5b9c5-113">開發人員可以撰寫使用這些合格元件的安裝套件，以執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="5b9c5-113">A developer could author an installation package that uses these qualified components to do the following:</span></span>

-   <span data-ttu-id="5b9c5-114">使用 [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) 或 [**MSIPROVIDEQUALIFIEDCOMPONENTEX**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) 尋找資源 DLL 特定語言版本的路徑，並安裝該資源。</span><span class="sxs-lookup"><span data-stu-id="5b9c5-114">Find the path to a particular language version of the resource DLL using [**MsiProvideQualifiedComponent**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponenta) or [**MsiProvideQualifiedComponentEx**](/windows/desktop/api/Msi/nf-msi-msiprovidequalifiedcomponentexa) and install the resource.</span></span>
-   <span data-ttu-id="5b9c5-115">藉由呼叫 [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa)，判斷所有存在的資源 DLL 語言版本。</span><span class="sxs-lookup"><span data-stu-id="5b9c5-115">Determine all of the language versions of the resource DLL that are present by calling [**MsiEnumComponentQualifiers**](/windows/desktop/api/Msi/nf-msi-msienumcomponentqualifiersa).</span></span>
-   <span data-ttu-id="5b9c5-116">準備應用程式以支援其他語言。</span><span class="sxs-lookup"><span data-stu-id="5b9c5-116">Prepare the application to support additional languages.</span></span> <span data-ttu-id="5b9c5-117">應用程式的未來語言套件可以使用限定元件來新增更多語言版本的資源 DLL。</span><span class="sxs-lookup"><span data-stu-id="5b9c5-117">A future language pack for the application can use the qualified component to add more language versions of the resource DLL.</span></span>

<span data-ttu-id="5b9c5-118">如需詳細資訊，請參閱 [使用限定的元件](using-qualified-components.md)。</span><span class="sxs-lookup"><span data-stu-id="5b9c5-118">For more information, see [Using Qualified Components](using-qualified-components.md).</span></span>

 

 



