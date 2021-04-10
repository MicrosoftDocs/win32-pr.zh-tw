---
title: 使用 MIDL
description: 建立和編譯 Microsoft 介面定義語言 (MIDL) 介面和遠端程序呼叫 (RPC) 。
ms.assetid: 2594e3d6-d44a-4e12-8286-b9700e67702e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22da60f20cba6c558c7f1a67478adef7b407d591
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103683036"
---
# <a name="using-midl"></a><span data-ttu-id="76e51-103">使用 MIDL</span><span class="sxs-lookup"><span data-stu-id="76e51-103">Using MIDL</span></span>

<span data-ttu-id="76e51-104">使用 RPC 的程式的所有介面都必須在 Microsoft 介面定義語言 (MIDL) 中定義，並使用 MIDL 編譯器進行編譯。</span><span class="sxs-lookup"><span data-stu-id="76e51-104">All interfaces for programs using RPC must be defined in Microsoft Interface Definition Language (MIDL) and compiled with the MIDL compiler.</span></span> <span data-ttu-id="76e51-105">下列主題提供建立和編譯 MIDL 介面的簡短總覽：</span><span class="sxs-lookup"><span data-stu-id="76e51-105">The following topics present a brief overview of creating and compiling a MIDL interface:</span></span>

-   [<span data-ttu-id="76e51-106">使用 MIDL 定義介面</span><span class="sxs-lookup"><span data-stu-id="76e51-106">Defining an Interface with MIDL</span></span>](#defining-an-interface-with-midl)
-   [<span data-ttu-id="76e51-107">編譯 MIDL 檔案</span><span class="sxs-lookup"><span data-stu-id="76e51-107">Compiling a MIDL File</span></span>](#compiling-a-midl-file)

<span data-ttu-id="76e51-108">如需這些主題的詳細討論，請參閱 [IDL 和 ACF](the-idl-and-acf-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="76e51-108">For a detailed discussion of these topics, see [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

## <a name="defining-an-interface-with-midl"></a><span data-ttu-id="76e51-109">使用 MIDL 定義介面</span><span class="sxs-lookup"><span data-stu-id="76e51-109">Defining an Interface with MIDL</span></span>

<span data-ttu-id="76e51-110">MIDL 檔案是您可以使用文字編輯器來建立和編輯的文字檔。</span><span class="sxs-lookup"><span data-stu-id="76e51-110">MIDL files are text files that you can create and edit with a text editor.</span></span> <span data-ttu-id="76e51-111">如果您為介面產生 UUID，通常會將輸出儲存在範本 MIDL 檔案中。</span><span class="sxs-lookup"><span data-stu-id="76e51-111">If you generate a UUID for your interface, you will typically store the output in a template MIDL file.</span></span> <span data-ttu-id="76e51-112">如需 Uuid 的詳細資訊，請參閱 [產生介面 uuid](generating-interface-uuids.md)。</span><span class="sxs-lookup"><span data-stu-id="76e51-112">For more information on UUIDs, see [Generating Interface UUIDs](generating-interface-uuids.md).</span></span>

<span data-ttu-id="76e51-113">MIDL 中的所有介面都遵循相同的格式。</span><span class="sxs-lookup"><span data-stu-id="76e51-113">All interfaces in MIDL follow the same format.</span></span> <span data-ttu-id="76e51-114">它們的開頭是包含介面屬性清單和介面名稱的標頭。</span><span class="sxs-lookup"><span data-stu-id="76e51-114">They begin with a header that contains a list of interface attributes and the interface name.</span></span> <span data-ttu-id="76e51-115">屬性以方括弧括住。</span><span class="sxs-lookup"><span data-stu-id="76e51-115">The attributes are enclosed in square brackets.</span></span> <span data-ttu-id="76e51-116">介面標頭後面接著其主體，並以大括弧括住。</span><span class="sxs-lookup"><span data-stu-id="76e51-116">The interface header is followed by its body, which is enclosed in curly brackets.</span></span> <span data-ttu-id="76e51-117">下列範例會顯示簡單的介面：</span><span class="sxs-lookup"><span data-stu-id="76e51-117">A simple interface is shown in the following example:</span></span>

``` syntax
[
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface MyInterface
{
  const unsigned short INT_ARRAY_LEN = 100;

  void MyRemoteProc( 
      [in] int param1,
      [out] int outArray[INT_ARRAY_LEN]
  );
}
```

<span data-ttu-id="76e51-118">某些通常會出現在 MIDL 介面定義中的屬性是 UUID 和介面版本號碼。</span><span class="sxs-lookup"><span data-stu-id="76e51-118">Some of the attributes that typically appear in a MIDL interface definition are the UUID and the interface version number.</span></span> <span data-ttu-id="76e51-119">介面定義的主體必須包含介面中所有遠端程式的程式聲明。</span><span class="sxs-lookup"><span data-stu-id="76e51-119">The body of the interface definition must contain the procedure declarations of all of the remote procedures in the interface.</span></span> <span data-ttu-id="76e51-120">它也可以包含介面所需之資料類型和常數的宣告。</span><span class="sxs-lookup"><span data-stu-id="76e51-120">It can also contain the declarations of data types and constants required by the interface.</span></span>

<span data-ttu-id="76e51-121">遠端過程聲明中的所有參數都必須宣告為 \[ [**in**](/windows/desktop/Midl/in) \] 、 \[ [**out**](/windows/desktop/Midl/out-idl) \] 或 \[ **in**、 **out** \] 。</span><span class="sxs-lookup"><span data-stu-id="76e51-121">All parameters in the remote procedure declarations must be declared as \[[**in**](/windows/desktop/Midl/in)\], \[[**out**](/windows/desktop/Midl/out-idl)\], or \[**in**, **out**\].</span></span> <span data-ttu-id="76e51-122">這些宣告會指定用戶端程式將資料傳遞至遠端程式、從遠端程式取得資料，或同時從兩者取得資料。</span><span class="sxs-lookup"><span data-stu-id="76e51-122">These declarations specify that the client program passes data into a remote procedure, gets data out of a remote procedure, or both.</span></span> <span data-ttu-id="76e51-123">如需有關介面參數聲明的詳細資訊，請參閱 [IDL 介面主體](the-idl-interface-body.md)。</span><span class="sxs-lookup"><span data-stu-id="76e51-123">For more detailed information about interface parameter declarations, see [The IDL Interface Body](the-idl-interface-body.md).</span></span>

## <a name="compiling-a-midl-file"></a><span data-ttu-id="76e51-124">編譯 MIDL 檔案</span><span class="sxs-lookup"><span data-stu-id="76e51-124">Compiling a MIDL File</span></span>

<span data-ttu-id="76e51-125">MIDL 編譯器是一種命令列工具，會隨平臺軟體發展工具組 (SDK) 自動安裝。</span><span class="sxs-lookup"><span data-stu-id="76e51-125">The MIDL compiler is a command-line tool that is automatically installed with the Platform Software Development Kit (SDK).</span></span> <span data-ttu-id="76e51-126">在命令列中輸入 **midl** 的命令，並在命令列中輸入 midl 檔案的名稱，在命令視窗中叫用它。</span><span class="sxs-lookup"><span data-stu-id="76e51-126">Invoke it in a command window by typing the command **midl**, followed by the name of a MIDL file, at the command line.</span></span> <span data-ttu-id="76e51-127">請確定包含 MIDL 編譯器的目錄在您的路徑中。</span><span class="sxs-lookup"><span data-stu-id="76e51-127">Make sure that the directory containing the MIDL compiler is in your path.</span></span> <span data-ttu-id="76e51-128">下列範例說明其用途：</span><span class="sxs-lookup"><span data-stu-id="76e51-128">The following example illustrates its use:</span></span>

<span data-ttu-id="76e51-129">**midl MyApp .idl**</span><span class="sxs-lookup"><span data-stu-id="76e51-129">**midl MyApp.idl**</span></span>

<span data-ttu-id="76e51-130">請注意，如果檔案名具有 .idl 副檔名，就不需要包含副檔名。</span><span class="sxs-lookup"><span data-stu-id="76e51-130">Note that you do not have to include the extension if the file name has the .idl extension.</span></span> <span data-ttu-id="76e51-131">您也可以使用 MIDL 編譯器 [命令列參數](/windows/desktop/Midl/midl-command-line-reference) ，方法是將它們插入 **midl** 命令和檔案名之間。</span><span class="sxs-lookup"><span data-stu-id="76e51-131">You can also use the MIDL compiler [command-line switches](/windows/desktop/Midl/midl-command-line-reference) by inserting them between the **midl** command and the file name.</span></span> <span data-ttu-id="76e51-132">下列範例會示範這種情況：</span><span class="sxs-lookup"><span data-stu-id="76e51-132">This is demonstrated in the following example:</span></span>

<span data-ttu-id="76e51-133">**midl/acf MyApp. acf MyApp .idl**</span><span class="sxs-lookup"><span data-stu-id="76e51-133">**midl /acf MyApp.acf MyApp.idl**</span></span>

<span data-ttu-id="76e51-134">在此範例中，會使用 file MyApp 作為輸入檔來執行 MIDL 編譯器。</span><span class="sxs-lookup"><span data-stu-id="76e51-134">In this example, the MIDL compiler is executed using the file MyApp.idl as the input file.</span></span> <span data-ttu-id="76e51-135">命令列參數 **/acf** 會指示編譯器使用應用程式佈建檔， (acf 輸入的) 。</span><span class="sxs-lookup"><span data-stu-id="76e51-135">The command line switch **/acf** instructs the compiler to use an application configuration file (ACF) for input as well.</span></span> <span data-ttu-id="76e51-136">在 [IDL 和 ACF](the-idl-and-acf-files.md)檔案中，會更詳盡地討論應用程式佈建檔。</span><span class="sxs-lookup"><span data-stu-id="76e51-136">Application configuration files are discussed more thoroughly in [The IDL and ACF Files](the-idl-and-acf-files.md).</span></span>

<span data-ttu-id="76e51-137">如需使用 MIDL 編譯器的詳細資訊，請參閱 [Microsoft 介面定義語言 (midl) ](/windows/desktop/Midl/midl-start-page)，其中包含下列主題的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="76e51-137">For more detailed information on using the MIDL compiler, see the [Microsoft Interface Definition Language (MIDL)](/windows/desktop/Midl/midl-start-page), which contains information on the following topics:</span></span>

-   [<span data-ttu-id="76e51-138">C-MIDL 的預處理器需求</span><span class="sxs-lookup"><span data-stu-id="76e51-138">C-Preprocessor Requirements for MIDL</span></span>](/windows/desktop/Midl/c-preprocessor-requirements-for-midl)
-   [<span data-ttu-id="76e51-139">C/c + +-編譯器考慮</span><span class="sxs-lookup"><span data-stu-id="76e51-139">C/C++-Compiler Considerations</span></span>](/windows/desktop/Midl/c-c-compiler-considerations)
-   [<span data-ttu-id="76e51-140">針對 RPC 介面產生的檔案</span><span class="sxs-lookup"><span data-stu-id="76e51-140">Files Generated for an RPC Interface</span></span>](/windows/desktop/Midl/files-generated-for-an-rpc-interface)
-   [<span data-ttu-id="76e51-141">MIDL 命令列參考</span><span class="sxs-lookup"><span data-stu-id="76e51-141">MIDL Command-line Reference</span></span>](/windows/desktop/Midl/midl-command-line-reference)
-   [<span data-ttu-id="76e51-142">MIDL 語言參考</span><span class="sxs-lookup"><span data-stu-id="76e51-142">MIDL Language Reference</span></span>](/windows/desktop/Midl/midl-language-reference)
-   [<span data-ttu-id="76e51-143">MIDL 編譯器錯誤和警告</span><span class="sxs-lookup"><span data-stu-id="76e51-143">MIDL Compiler Errors and Warnings</span></span>](/windows/desktop/Midl/midl-compiler-errors-and-warnings)

 

 