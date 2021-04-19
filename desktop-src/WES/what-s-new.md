---
title: 'Windows 事件記錄檔 (的新功能) '
description: 此頁面摘要說明針對每個版本新增至 Windows 事件記錄檔 API 的新功能。
ms.assetid: 90adf08c-177f-46ae-82e1-f7cca5a46db8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 652d82f67292316dd7aec599955d69dd70ab39a3
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106965270"
---
# <a name="whats-new-windows-event-log"></a><span data-ttu-id="065dd-103">Windows 事件記錄檔 (的新功能) </span><span class="sxs-lookup"><span data-stu-id="065dd-103">What's New (Windows Event Log)</span></span>

<span data-ttu-id="065dd-104">此頁面摘要說明針對每個版本新增至 Windows 事件記錄檔 API 的新功能。</span><span class="sxs-lookup"><span data-stu-id="065dd-104">This page summarizes the new features that were added to the Windows Event Log API for each release.</span></span>

## <a name="windows-7-and-windows-server-2008-r2"></a><span data-ttu-id="065dd-105">Windows 7 與 Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="065dd-105">Windows 7 and Windows Server 2008 R2</span></span>

<span data-ttu-id="065dd-106">以下是對 [EventManifest](eventmanifestschema-schema.md) 架構進行的變更：</span><span class="sxs-lookup"><span data-stu-id="065dd-106">The following are the changes that were made to the [EventManifest](eventmanifestschema-schema.md) schema:</span></span>

-   <span data-ttu-id="065dd-107">已移除 [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) 複雜類型。</span><span class="sxs-lookup"><span data-stu-id="065dd-107">Removed the [**TaskEventDefinitionType**](eventmanifestschema-taskeventdefinitiontype-complextype.md) complex type.</span></span> <span data-ttu-id="065dd-108">若要提供相同的功能，請使用工作特定的作業碼 (查看 [**TaskType**](eventmanifestschema-tasktype-complextype.md)複雜 **類型的 opcode 元素。**</span><span class="sxs-lookup"><span data-stu-id="065dd-108">To provide the same functionality, use task-specific opcodes (see the **opcodes** element of the [**TaskType**](eventmanifestschema-tasktype-complextype.md) complex type.</span></span>
-   <span data-ttu-id="065dd-109">新增 [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md)、 [**filePath**](eventmanifestschema-filepath-simpletype.md)和 [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) 簡單類型，以限制指派給這些類型之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="065dd-109">Added the [**CSymbolType**](eventmanifestschema-csymboltype-simpletype.md), [**filePath**](eventmanifestschema-filepath-simpletype.md), and [**strTableRef**](eventmanifestschema-strtableref-simpletype.md) simple types to restrict values assigned to attributes of these types.</span></span>
-   <span data-ttu-id="065dd-110">將 **篩選** 屬性加入至 [**ProviderType**](eventmanifestschema-providertype-complextype.md) 複雜類型。</span><span class="sxs-lookup"><span data-stu-id="065dd-110">Added the **filters** attribute to the [**ProviderType**](eventmanifestschema-providertype-complextype.md) complex type.</span></span> <span data-ttu-id="065dd-111">提供者可以使用篩選器，就像提供者使用層級和關鍵字來判斷是否應該撰寫事件一樣。</span><span class="sxs-lookup"><span data-stu-id="065dd-111">Providers can use filters in the same way that providers use level and keywords to determine whether they should write an event.</span></span>
-   <span data-ttu-id="065dd-112">新增下列輸出類型，您可以為事件資料範本中定義的資料項目指定這些輸出類型：</span><span class="sxs-lookup"><span data-stu-id="065dd-112">Added the following output types that you can specify for data items defined in an event data template:</span></span>
    -   <span data-ttu-id="065dd-113">win： DateTimeCultureInsensitive</span><span class="sxs-lookup"><span data-stu-id="065dd-113">win:DateTimeCultureInsensitive</span></span>
    -   <span data-ttu-id="065dd-114">win： HResult</span><span class="sxs-lookup"><span data-stu-id="065dd-114">win:HResult</span></span>
    -   <span data-ttu-id="065dd-115">win： NTSTATUS</span><span class="sxs-lookup"><span data-stu-id="065dd-115">win:NTSTATUS</span></span>
-   <span data-ttu-id="065dd-116">輸出類型現在已被接受，但在忽略之前。</span><span class="sxs-lookup"><span data-stu-id="065dd-116">The output types are now honored whereas before they were ignored.</span></span>

<span data-ttu-id="065dd-117">Windows 7 版 Windows SDK 隨附的 [**訊息編譯器**](message-compiler--mc-exe-.md) 版本已進行下列變更：</span><span class="sxs-lookup"><span data-stu-id="065dd-117">The following changes were made to the version of the [**Message Compiler**](message-compiler--mc-exe-.md) that ships with the Windows 7 version of the Windows SDK:</span></span>

-   <span data-ttu-id="065dd-118">已新增引數，讓編譯器根據您的資訊清單產生記錄程式碼。</span><span class="sxs-lookup"><span data-stu-id="065dd-118">Added arguments to have the compiler generate logging code based on your manifest.</span></span> <span data-ttu-id="065dd-119">您也可以要求編譯器產生程式碼，以在 Windows Vista 之前的作業系統上記錄事件。</span><span class="sxs-lookup"><span data-stu-id="065dd-119">You can also request that the compiler generate code to log events on operating systems prior to Windows Vista.</span></span> <span data-ttu-id="065dd-120">如需引數的清單，請參閱 [**訊息編譯器**](message-compiler--mc-exe-.md) 主題的「產生用來記錄事件的程式碼特定的引數」一節。</span><span class="sxs-lookup"><span data-stu-id="065dd-120">For a list of the arguments, see the "Arguments specific to generating code used to log events" section of the [**Message Compiler**](message-compiler--mc-exe-.md) topic.</span></span>
-   <span data-ttu-id="065dd-121">編譯器現在會在資訊清單上強制執行更嚴格的語法和語意驗證。</span><span class="sxs-lookup"><span data-stu-id="065dd-121">The compiler now enforces stricter syntactic and semantic validation on the manifest.</span></span> <span data-ttu-id="065dd-122">這可能會導致在舊版訊息編譯器上成功編譯的一些資訊清單需要變更，才能使用最新版本順利進行編譯。</span><span class="sxs-lookup"><span data-stu-id="065dd-122">This may cause some manifests that successfully compiled on previous versions of the message compiler to require changes in order to successfully compile using the latest version.</span></span>
