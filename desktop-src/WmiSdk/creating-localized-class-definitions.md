---
description: 建立當地語系化的類別定義是三個步驟的處理常式。
ms.assetid: e303b894-07c4-44e3-9c57-58b1db16ae9a
ms.tgt_platform: multiple
title: 建立當地語系化的類別定義
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d41a183c1478c259b0428cd827088a769e680425
ms.sourcegitcommit: b7a1da2711221fa99072079bf52399cbdfc6bd9d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106976638"
---
# <a name="creating-localized-class-definitions"></a><span data-ttu-id="4a737-103">建立當地語系化的類別定義</span><span class="sxs-lookup"><span data-stu-id="4a737-103">Creating Localized Class Definitions</span></span>

<span data-ttu-id="4a737-104">建立當地語系化的類別定義是三個步驟的處理常式。</span><span class="sxs-lookup"><span data-stu-id="4a737-104">Creating localized class definitions is a three-step process.</span></span> <span data-ttu-id="4a737-105">首先，撰寫定義類別的 MOF 程式碼，包括必須當地語系化的所有限定詞。</span><span class="sxs-lookup"><span data-stu-id="4a737-105">You start by writing MOF code that defines the classes, including all qualifiers that must be localized.</span></span> <span data-ttu-id="4a737-106">此原始檔案稱為「主要 MOF」檔案，因為它包含定義類別的所有限定詞和屬性。</span><span class="sxs-lookup"><span data-stu-id="4a737-106">This original file is called the "master MOF" file because it contains all of the qualifiers and properties that define the class.</span></span>

<span data-ttu-id="4a737-107">接下來，使用 [mof 編譯器](mofcomp.md) 來建立特定語言和特定語言版本的 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="4a737-107">Next, use the [MOF compiler](mofcomp.md) to create the language-neutral and language-specific versions of the MOF file.</span></span> <span data-ttu-id="4a737-108">MOF 編譯器會將基本類別描述放置在新的 MOF 檔案中，並建立 MOF 檔案的當地語系化版本，其中只包含必須當地語系化的屬性和限定詞。</span><span class="sxs-lookup"><span data-stu-id="4a737-108">The MOF compiler places the basic class description in a new MOF file and creates a localized version of the MOF file that contains only the properties and qualifiers that must be localized.</span></span> <span data-ttu-id="4a737-109">雖然 MOF 檔案的語言特定和語言中性版本可以有相同的檔案名，但您應該使用 mfl 副檔名來指出檔案包含當地語系化的資訊。</span><span class="sxs-lookup"><span data-stu-id="4a737-109">Although the language-specific and language-neutral versions of the MOF file can have the same file name, you should use a .mfl file name extension to indicate that the file contains localized information.</span></span> <span data-ttu-id="4a737-110">如有必要，您可以將 mfl 檔案當地語系化為其他地區設定。</span><span class="sxs-lookup"><span data-stu-id="4a737-110">You can localize the .mfl file to other locales, if necessary.</span></span> <span data-ttu-id="4a737-111">將類別定義儲存在 CIM 存放庫中，需要額外的步驟來使用 MOF 編譯器，以編譯非語言相關和語言專屬的 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="4a737-111">Storing the class definitions in the CIM repository requires an additional step of using the MOF compiler to compile both the language-neutral and the language-specific MOF files.</span></span>

<span data-ttu-id="4a737-112">下列步驟說明如何建立和儲存當地語系化的類別定義。</span><span class="sxs-lookup"><span data-stu-id="4a737-112">The following steps describe how to create and store a localized class definition.</span></span>

<span data-ttu-id="4a737-113">**若要建立和儲存當地語系化的類別定義**</span><span class="sxs-lookup"><span data-stu-id="4a737-113">**To create and store a localized class definition**</span></span>

1.  <span data-ttu-id="4a737-114">建立主要 MOF 檔案，以定義您要當地語系化的類別。</span><span class="sxs-lookup"><span data-stu-id="4a737-114">Create the master MOF file that defines the classes that you want localized.</span></span>

    <span data-ttu-id="4a737-115">將此 MOF 程式碼儲存在名為 Mastermof 的檔案中。</span><span class="sxs-lookup"><span data-stu-id="4a737-115">Save this MOF code in a file called Mastermof.mof.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root")

    instance of __Namespace
    {
        Name = "TEST" ;
    } ;

    #pragma namespace("\\\\.\\root\\TEST")

    [Description("Localized version of MyClass for American English") 
        : Amended, LOCALE(0x409)] 

    class myclass
    {
        [DisplayName("User Name") : Amended,
        Description("The Name property contains the name of the user") : 
        Amended, key]
         string Name;

        uint64 Value; // non-localized value field

          [DisplayName("Time Stamp") : Amended,
        Description("This property shows when the object was created") : 
        Amended] 
         uint64 Timestamp;
    };
    ```

2.  <span data-ttu-id="4a737-116">藉由編譯 MasterMOF mof 檔案，建立特定語言和特定語言版本的 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="4a737-116">Create language-neutral and language-specific versions of the MOF file by compiling the MasterMOF.mof file.</span></span>

    <span data-ttu-id="4a737-117">在命令提示字元中輸入下列命令，以編譯 MasterMOF mof 檔案。</span><span class="sxs-lookup"><span data-stu-id="4a737-117">Type the following command at a command prompt to compile the MasterMOF.mof file.</span></span>

    <span data-ttu-id="4a737-118">**mofcomp.exe-MOF： Lnmof MFL： Lsmof. MFL-修訂： MS \_ 409 Mastermof. MOF**</span><span class="sxs-lookup"><span data-stu-id="4a737-118">**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS\_409 Mastermof.mof**</span></span>

3.  <span data-ttu-id="4a737-119">編譯語言中立的 (Lnmof mof) 和特定語言的 (Lsmof mfl) 檔，並將類別資訊儲存在 CIM 存放庫中。</span><span class="sxs-lookup"><span data-stu-id="4a737-119">Compile the language-neutral (Lnmof.mof) and language-specific (Lsmof.mfl) files and store the class information in the CIM repository.</span></span>

    <span data-ttu-id="4a737-120">在命令提示字元中輸入下列命令，將類別資訊儲存在 CIM 存放庫中。</span><span class="sxs-lookup"><span data-stu-id="4a737-120">Type the following commands at a command prompt to store the class information in the CIM repository.</span></span>

    <span data-ttu-id="4a737-121">**Mofcomp.exe Lnmof**</span><span class="sxs-lookup"><span data-stu-id="4a737-121">**Mofcomp Lnmof.mof**</span></span>

    <span data-ttu-id="4a737-122">**Mofcomp.exe Lsmof. mfl**</span><span class="sxs-lookup"><span data-stu-id="4a737-122">**Mofcomp Lsmof.mfl**</span></span>

    <span data-ttu-id="4a737-123">編譯這些檔案之後，根測試命名空間中將會有語言中立的類別定義 \\ ，以及根 \\ 測試 \\ ms \_ 409 命名空間中的當地語系化類別定義。</span><span class="sxs-lookup"><span data-stu-id="4a737-123">After you compile these files, you will have a language-neutral class definition in the root\\test namespace and a localized class definition in the root\\test\\ms\_409 namespace.</span></span> <span data-ttu-id="4a737-124">如需編譯當地語系化 MOF 檔案的詳細資訊，請參閱 [編譯當地語系化的 mof](compiling-localized-mof-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="4a737-124">For more information about compiling localized MOF files, see [Compiling Localized MOF files](compiling-localized-mof-files.md).</span></span>

 

 



