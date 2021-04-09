---
title: JAVATLB Command-Line 工具
description: JAVATLB Command-Line 工具
ms.assetid: b46d7bcc-ccd9-4242-9b19-f398d2cb8f91
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7a0214648f7ad86613d6b35e3084021e2be24aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675819"
---
# <a name="javatlb-command-line-tool"></a><span data-ttu-id="ca44a-103">JAVATLB Command-Line 工具</span><span class="sxs-lookup"><span data-stu-id="ca44a-103">JavaTLB Command-Line Tool</span></span>

<span data-ttu-id="ca44a-104">JAVATLB 是 Visual j + + 5.0 的元件。</span><span class="sxs-lookup"><span data-stu-id="ca44a-104">JavaTLB is a component of Visual J++ 5.0.</span></span> <span data-ttu-id="ca44a-105">JAVATLB 是一種命令列應用程式，可產生 COM 物件的類別檔案。</span><span class="sxs-lookup"><span data-stu-id="ca44a-105">JavaTLB is a command-line application that generates class files for a COM object.</span></span> <span data-ttu-id="ca44a-106">包含無法準確且安全地在 JAVA 中表示之資料類型的方法，不會轉換。</span><span class="sxs-lookup"><span data-stu-id="ca44a-106">Methods that contain data types that cannot be accurately and safely represented in Java are not converted.</span></span>

<span data-ttu-id="ca44a-107">與 [JAVA 類型程式庫 Wizard](java-type-library-wizard.md)不同的是，JAVATLB 不會產生包含 JAVA 類型程式庫資訊的摘要檔案。</span><span class="sxs-lookup"><span data-stu-id="ca44a-107">Unlike the [Java Type Library Wizard](java-type-library-wizard.md), JavaTLB does not generate a summary file containing the Java type library information.</span></span>

<span data-ttu-id="ca44a-108">若要產生單一 COM 物件的 JAVA 類別檔案，請從命令提示字元執行：</span><span class="sxs-lookup"><span data-stu-id="ca44a-108">To generate Java class files for a single COM object, from the command prompt run:</span></span>

<span data-ttu-id="ca44a-109">**javatlb** *檔案名*</span><span class="sxs-lookup"><span data-stu-id="ca44a-109">**javatlb** *filename*</span></span>

<span data-ttu-id="ca44a-110">其中 *filename* 是包含類型程式庫之檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="ca44a-110">where *filename* is the name of the file that contains the type library.</span></span> <span data-ttu-id="ca44a-111">這個檔案可能會有下列任何副檔名： .tlb、. .olb、.ocx、.dll 或 .exe。</span><span class="sxs-lookup"><span data-stu-id="ca44a-111">This file may have any of the following file name extensions: .tlb, .olb, .ocx, .dll, or .exe.</span></span>

<span data-ttu-id="ca44a-112">若要產生多個 COM 物件的 JAVA 類別檔案，請從命令提示字元執行：</span><span class="sxs-lookup"><span data-stu-id="ca44a-112">To generate Java class files for multiple COM objects, from the command prompt run:</span></span>

<span data-ttu-id="ca44a-113">\**javatlb @ \* \* \* TextFile*</span><span class="sxs-lookup"><span data-stu-id="ca44a-113">\**javatlb @\*\*\*TextFile*</span></span>

<span data-ttu-id="ca44a-114">其中 *TextFile* 是文字檔的名稱，其中包含包含 COM 物件類型程式庫的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="ca44a-114">where *TextFile* is the name of a text file that contains a list of the files containing the COM object's type libraries.</span></span>

> [!Note]  
> <span data-ttu-id="ca44a-115">在 Visual c + + 6.0 中，JAVATLB 命令列工具是由 [JActiveX 工具](jactivex-command-line-tool.md)所取代。</span><span class="sxs-lookup"><span data-stu-id="ca44a-115">In Visual J++ 6.0, the JavaTLB command-line tool is replaced by the [JActiveX tool](jactivex-command-line-tool.md).</span></span> <span data-ttu-id="ca44a-116">如需詳細資訊，請參閱 Visual c + + 6.0 檔。</span><span class="sxs-lookup"><span data-stu-id="ca44a-116">For more information, see the Visual J++ 6.0 documentation.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="ca44a-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="ca44a-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca44a-118">轉換成 JAVA</span><span class="sxs-lookup"><span data-stu-id="ca44a-118">Translating to Java</span></span>](translating-to-java.md)
</dt> </dl>

 

 




