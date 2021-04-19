---
title: '應用程式佈建檔 (ACF) '
description: 您的分散式應用程式可能會影響某個元件，但與另一個元件無關。
ms.assetid: 017d93fd-1701-4713-a786-752a7695b5a6
keywords:
- ACF MIDL
- Microsoft 介面定義語言 MIDL，描述，應用程式佈建檔案
- 應用程式佈建檔 MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9066e5641d6b71e68ba670984765661f1b9f6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967436"
---
# <a name="application-configuration-file-acf"></a><span data-ttu-id="ff87d-106">應用程式佈建檔 (ACF) </span><span class="sxs-lookup"><span data-stu-id="ff87d-106">Application Configuration File (ACF)</span></span>

<span data-ttu-id="ff87d-107">您的分散式應用程式可能會影響某個元件，但與另一個元件無關。</span><span class="sxs-lookup"><span data-stu-id="ff87d-107">There may be aspects of your distributed application that affect one component, but have nothing to do with another.</span></span> <span data-ttu-id="ff87d-108">例如，物件可能包含大型的複雜資料結構，並將此資料結構的內容傳遞至另一個物件。</span><span class="sxs-lookup"><span data-stu-id="ff87d-108">For example, an object may contain a large, complex data structure and pass the contents of this data structure to another object.</span></span> <span data-ttu-id="ff87d-109">對接收應用程式而言，此資料結構的確切版面配置可能沒有意義。</span><span class="sxs-lookup"><span data-stu-id="ff87d-109">The exact layout of this data structure may be meaningless to the receiving application.</span></span> <span data-ttu-id="ff87d-110">此外，此結構可能包含 MIDL 編譯器無法辨識的資料類型，而且無法產生封送處理和封送處理常式代碼。</span><span class="sxs-lookup"><span data-stu-id="ff87d-110">Also, the structure may contain data types that the MIDL compiler does not recognize and cannot generate marshaling and unmarshaling code.</span></span>

<span data-ttu-id="ff87d-111">用戶端應用程式可以共用相同的介面，但在不同的平臺上執行;它們可能每一個都需要自己的封送處理常式集。</span><span class="sxs-lookup"><span data-stu-id="ff87d-111">Client applications may share the same interface but run on different platforms; they may each need their own set of marshaling routines.</span></span> <span data-ttu-id="ff87d-112">最後，個別用戶端不一定需要相同的函式集合。</span><span class="sxs-lookup"><span data-stu-id="ff87d-112">Finally, individual clients may not always need the same set of functions.</span></span> <span data-ttu-id="ff87d-113">針對將永遠不會在特定用戶端應用程式中執行的函式產生 stub 程式碼，會產生效率不佳的情況。</span><span class="sxs-lookup"><span data-stu-id="ff87d-113">It is inefficient to generate stub code for functions that will never be implemented in a particular client application.</span></span>

<span data-ttu-id="ff87d-114">藉由在應用程式佈建檔中定義介面的這些本機層面 (ACF) ，您可以將用戶端介面的差異與其網路表示分開，讓伺服器以一致的格式來傳送和接收資料，並讓您的存根程式碼更簡潔且更有效率。</span><span class="sxs-lookup"><span data-stu-id="ff87d-114">By defining these local aspects of your interface in an application configuration file (ACF), you can separate the differences between the client interfaces from their network representation, allowing the server to send and receive data in a consistent format, and making your stub code more compact and efficient.</span></span>

<span data-ttu-id="ff87d-115">ACF 介面定義的結構和語法與 IDL 定義相同：</span><span class="sxs-lookup"><span data-stu-id="ff87d-115">The structure and syntax of an ACF interface definition are identical to the IDL definition:</span></span>

``` syntax
[ interface-attribute-list] interface interface-name {. . .}
```

<span data-ttu-id="ff87d-116">根據預設，ACF 介面名稱必須與 IDL 定義中的名稱相符。</span><span class="sxs-lookup"><span data-stu-id="ff87d-116">By default, the ACF interface name must match its name in the IDL definition.</span></span> <span data-ttu-id="ff87d-117">但是，當您使用 MIDL 編譯器選項/ [**acf**](-acf.md) 明確指定 acf 檔案名時，介面名稱不一定要相符。</span><span class="sxs-lookup"><span data-stu-id="ff87d-117">However, when you use the MIDL compiler option / [**acf**](-acf.md) to explicitly specify an ACF file name, the interface names do not have to match.</span></span> <span data-ttu-id="ff87d-118">這項功能可讓數個介面共用單一 ACF 規格。</span><span class="sxs-lookup"><span data-stu-id="ff87d-118">This feature allows several interfaces to share a single ACF specification.</span></span>

 

 




