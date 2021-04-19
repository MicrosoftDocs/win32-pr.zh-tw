---
title: 開發人員工具如何使用類型程式庫
description: 開發人員工具如何使用類型程式庫
ms.assetid: 260aa694-1055-4a43-93aa-69a9d7359881
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0cc0f5249075aa861a1301466f86a0f769b8bf3
ms.sourcegitcommit: d39e82e232f6510f843fdb8d55d25b4e9e02e880
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "106976617"
---
# <a name="how-developer-tools-use-type-libraries"></a><span data-ttu-id="9dd69-103">開發人員工具如何使用類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9dd69-103">How Developer Tools Use Type Libraries</span></span>

<span data-ttu-id="9dd69-104">下圖說明各種開發工具如何與 COM 物件的類型程式庫互動。</span><span class="sxs-lookup"><span data-stu-id="9dd69-104">The following diagram illustrates how the various development tools interact with a COM object's type library.</span></span> <span data-ttu-id="9dd69-105">每個類型程式庫會公開標準的程式設計介面，工具可以呼叫這些介面來取得該類型程式庫中所述專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="9dd69-105">Each type library exposes standard programmatic interfaces that tools can call to get information about the elements described in that type library.</span></span> <span data-ttu-id="9dd69-106">在此圖中，GUID 代表遠端程序呼叫的全域唯一識別碼和 RPC。</span><span class="sxs-lookup"><span data-stu-id="9dd69-106">In this diagram, GUID stands for globally unique identifier and RPC for remote procedure call.</span></span>

![顯示開發只有才如何與 C O M 物件的類型程式庫互動的圖表。](images/09983c96-3f01-4ad5-8d3e-12b8ed28c35d.png)

<span data-ttu-id="9dd69-108">在上圖中，c + + 轉換工具，例如 MIDL 編譯器和 Microsoft Visual C++ 開發系統提供的嚮導，會產生標頭和存根檔案。</span><span class="sxs-lookup"><span data-stu-id="9dd69-108">In the preceding diagram, the C++ conversion tools, such as the MIDL compiler and the wizards provided by the Microsoft Visual C++ development system, generate header and stub files.</span></span> <span data-ttu-id="9dd69-109">您可以將這些檔案新增至您的專案，以便使用類型程式庫所描述的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="9dd69-109">You can add these files to your project in order to use the COM object described by the type library.</span></span>

<span data-ttu-id="9dd69-110">同樣地，在 JAVA 中，開發人員工具會產生 JAVA 類別和原始程式檔，然後您就可以將其匯入至應用程式。</span><span class="sxs-lookup"><span data-stu-id="9dd69-110">Similarly, in Java the developer tools generate Java class and source files, which you can then import into your application.</span></span>

<span data-ttu-id="9dd69-111">在 Visual Basic 中，此案例稍微簡單許多。</span><span class="sxs-lookup"><span data-stu-id="9dd69-111">In Visual Basic, the scenario is somewhat simpler.</span></span> <span data-ttu-id="9dd69-112">您不需要產生其他檔案。</span><span class="sxs-lookup"><span data-stu-id="9dd69-112">You do not need to generate additional files.</span></span> <span data-ttu-id="9dd69-113">Visual Basic 環境會提供對話方塊，列出目前安裝在電腦上的 COM 物件。</span><span class="sxs-lookup"><span data-stu-id="9dd69-113">The Visual Basic environment provides dialog boxes listing the COM objects currently installed on your computer.</span></span> <span data-ttu-id="9dd69-114">您可以從應用程式中選取要呼叫的元件，並將它新增至您的專案，以做為元件或參考。</span><span class="sxs-lookup"><span data-stu-id="9dd69-114">You select the component you want to call from your application, and it is added to your project, either as a component or a reference.</span></span>

<span data-ttu-id="9dd69-115">OLE COM 檢視器會讀取類型程式庫、根據類型程式庫產生暫時性的 IDL 檔案，然後將它顯示給使用者。</span><span class="sxs-lookup"><span data-stu-id="9dd69-115">The OLE-COM viewer reads a type library, generates a temporary IDL file based on the type library, and displays it to users.</span></span> <span data-ttu-id="9dd69-116">OLE COM 檢視器也會顯示類型程式庫中所列 COM 元素的 c + + 語法。</span><span class="sxs-lookup"><span data-stu-id="9dd69-116">The OLE-COM viewer also displays the C++ syntax for the COM elements listed in the type library.</span></span>

<span data-ttu-id="9dd69-117">如需型別程式庫的詳細資訊，請參閱 [類型程式庫和物件描述語言](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language)。</span><span class="sxs-lookup"><span data-stu-id="9dd69-117">For more information about type libraries, see [Type Libraries and the Object Description Language](/previous-versions/windows/desktop/automat/type-libraries-and-the-object-description-language).</span></span>

 

 