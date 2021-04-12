---
description: 您必須編譯主要 MOF 檔案，以建立語言中性和特定語言的 MOF 檔案。
ms.assetid: ae2fa320-8294-4991-be30-403088c34b7a
ms.tgt_platform: multiple
title: 編譯當地語系化的 MOF 檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41ab1341a37269ba98fdbbdecaa64b5e5a119703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319683"
---
# <a name="compiling-localized-mof-files"></a><span data-ttu-id="11172-103">編譯當地語系化的 MOF 檔案</span><span class="sxs-lookup"><span data-stu-id="11172-103">Compiling Localized MOF Files</span></span>

<span data-ttu-id="11172-104">您必須編譯主要 MOF 檔案，以建立語言中性和特定語言的 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="11172-104">You must compile your master MOF file to create the language-neutral and language-specific MOF files.</span></span>

<span data-ttu-id="11172-105">在命令提示字元中輸入下列命令，以編譯主要 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="11172-105">Type the following command at a command prompt to compile a master MOF file.</span></span>

<span data-ttu-id="11172-106">**mofcomp.exe-MOF： Lnmof MFL： Lsmof. MFL-修訂： MS \_ 409 Mastermof. MOF**</span><span class="sxs-lookup"><span data-stu-id="11172-106">**mofcomp -MOF:Lnmof.mof -MFL:Lsmof.mfl -Amendment:MS\_409 Mastermof.mof**</span></span>

<span data-ttu-id="11172-107">當您執行此命令時，MOF 編譯器會從原始的 Mastermof mof 檔案建立兩個 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="11172-107">When you run this command, the MOF compiler creates two MOF files from the original Mastermof.mof file.</span></span> <span data-ttu-id="11172-108">MOF 編譯器會產生語言中性版本 Lnmof，其中所有語言特定專案都會被移除。</span><span class="sxs-lookup"><span data-stu-id="11172-108">The MOF compiler produces a language-neutral version, Lnmof.mof, in which all language-specific items are removed.</span></span> <span data-ttu-id="11172-109">此外，也會建立第二個語言特定版本 Lsmof。此檔案僅包含在 Mastermof 中以 [**修改**](qualifier-flavors.md) 過的限定詞類別標記的專案。</span><span class="sxs-lookup"><span data-stu-id="11172-109">A second, language-specific version, Lsmof.mof, is also created; this file contains only items that were marked with the [**Amended**](qualifier-flavors.md) Qualifier Flavor in the Mastermof.mof file.</span></span>

<span data-ttu-id="11172-110">下列程式碼範例會顯示所產生的語言中性 MOF 檔案 (Lnmof) 的內容。</span><span class="sxs-lookup"><span data-stu-id="11172-110">The following code example shows the contents of the language-neutral MOF file (Lnmof.mof) that is generated.</span></span>

``` syntax
#pragma namespace("\\\\.\\root")

Instance of __Namespace
{
  Name = "TEST";
};
#pragma namespace("\\\\.\\root\\TEST")

[LOCALE(1033)] 
class myclass
{
  [key] string Name;
  uint64 Value;
  uint64 Timestamp;
};
```

<span data-ttu-id="11172-111">下列程式碼範例會顯示所產生之特定語言 MOF 檔案 (Lsmof mfl) 的內容。</span><span class="sxs-lookup"><span data-stu-id="11172-111">The following code example shows the contents of the language-specific MOF file (Lsmof.mfl) that is generated.</span></span>

``` syntax
#pragma namespace("\\\\.\\root\\TEST")
instance of __namespace{ name="ms_409";};
#pragma namespace("\\\\.\\root\\TEST\\ms_409")

[Description("Localized version of MyClass for American English") :
    Amended, LOCALE(0x409)] 

class myclass
{
    [DisplayName("User Name") : Amended,
    Description("The Name property contains the name of the user") : 
    Amended, key]
     string Name;

    [DisplayName("Time Stamp") : Amended,
    Description("This property shows when the object was created") : 
    Amended] 
     uint64 Timestamp;
};
```

<span data-ttu-id="11172-112">使用 [**修改**](qualifier-flavors.md) 過的辨識符號編譯 MOF 檔案，只會產生不同的語言中性和特定語言的 mof 檔案;CIM 存放庫未更新為新的類別資訊。</span><span class="sxs-lookup"><span data-stu-id="11172-112">Compiling a MOF file with the [**Amended**](qualifier-flavors.md) qualifier only generates separate language-neutral and language-specific MOF files; the CIM repository is not updated with the new class information.</span></span> <span data-ttu-id="11172-113">您必須使用 MOF 編譯器來編譯兩個 MOF 檔案，這些檔案是在任何類別資訊可供 WMI 使用之前所產生的第一次編譯。</span><span class="sxs-lookup"><span data-stu-id="11172-113">You must use the MOF compiler to compile the two MOF files that the first compilation produced before any class information is available to WMI.</span></span>

<span data-ttu-id="11172-114">當您編譯主要 MOF 檔案時，只有已 [**修改**](qualifier-flavors.md) 之類別的限定詞會移至特定語言的 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="11172-114">When you compile a master MOF file, only qualifiers with the [**Amended**](qualifier-flavors.md) flavor are moved to the language-specific MOF file.</span></span> <span data-ttu-id="11172-115">沒有 **修改** 過之類別的限定詞不會當地語系化，而且只存在於語言中立的 MOF 檔案中的基本類別定義中。</span><span class="sxs-lookup"><span data-stu-id="11172-115">Qualifiers that do not have the **Amended** flavor are not localized and only exist in the basic class definition in the language-neutral MOF file.</span></span> <span data-ttu-id="11172-116">如果未提供當地語系化的說明，則可使用未當地語系化的限定詞作為預設描述。</span><span class="sxs-lookup"><span data-stu-id="11172-116">Nonlocalized qualifiers can be used for default descriptions if localized descriptions are not available.</span></span>

<span data-ttu-id="11172-117">您可以使用 [pragma 修訂](pragma-amendment.md) 命令，而不是指定 [**修改**](qualifier-flavors.md) 為 MOF 編譯器的參數。</span><span class="sxs-lookup"><span data-stu-id="11172-117">You can use the [pragma amendment](pragma-amendment.md) command instead of specifying [**Amended**](qualifier-flavors.md) as a switch to the MOF compiler.</span></span> <span data-ttu-id="11172-118">其中一個選項相當於要求特定語言和語言中性版本的 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="11172-118">Either of these options are equivalent to requesting language-specific and language-neutral versions of a MOF file.</span></span> <span data-ttu-id="11172-119">如果您使用 pragma 修訂命令或 **修改** 過的命令列選項，您必須在命令提示字元中使用 **-MFL** 和 **-MOF** 選項來指定輸出檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="11172-119">If you use either the pragma amendment command or the **Amended** command-line option, you must specify the name of the output files using the **-MFL** and **-MOF** options at the command prompt.</span></span>

> [!Note]  
> <span data-ttu-id="11172-120">MOF 編譯器所產生的非語言相關 MOF 檔案包含地區設定識別碼的十進位對等專案，即使以十六進位輸入此值也是如此。</span><span class="sxs-lookup"><span data-stu-id="11172-120">The language-neutral MOF file that the MOF compiler generates contains the decimal equivalent of the locale ID, even if this value was entered in hexadecimal.</span></span> <span data-ttu-id="11172-121">在上述範例中，編譯器已將 Lnmof mof 輸出檔的值0x409 轉換為十進位數1033。</span><span class="sxs-lookup"><span data-stu-id="11172-121">In the example above, the compiler has converted the value 0x409 to the decimal number 1033 for the Lnmof.mof output file.</span></span>

 

 

 



