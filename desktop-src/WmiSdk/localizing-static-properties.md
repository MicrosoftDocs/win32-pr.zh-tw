---
description: 您可以使用部分值對應來當地語系化靜態屬性。
ms.assetid: 67e91454-c065-4ab2-a373-245c9392c71c
ms.tgt_platform: multiple
title: 將靜態屬性當地語系化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecaba200b7880991d349c6e0c0196c88ffa54b11
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/16/2021
ms.locfileid: "104323443"
---
# <a name="localizing-static-properties"></a><span data-ttu-id="8b1fb-103">將靜態屬性當地語系化</span><span class="sxs-lookup"><span data-stu-id="8b1fb-103">Localizing Static Properties</span></span>

<span data-ttu-id="8b1fb-104">您可以使用部分值對應來當地語系化靜態屬性。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-104">You can localize static properties by using partial value maps.</span></span>

<span data-ttu-id="8b1fb-105">下列程式描述如何搭配使用部分值對應與正則運算式來當地語系化靜態屬性。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-105">The following procedure describes how static properties can be localized using partial value maps with regular expressions.</span></span>

<span data-ttu-id="8b1fb-106">**使用值對應將靜態屬性當地語系化**</span><span class="sxs-lookup"><span data-stu-id="8b1fb-106">**To use value maps to localize static properties**</span></span>

1.  <span data-ttu-id="8b1fb-107">建立 (Mastervm mof) 的主要 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-107">Create a master MOF file (Mastervm.mof).</span></span>

    <span data-ttu-id="8b1fb-108">下列程式碼範例可用來建立 (Mastervm mof) 的主要 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-108">The following code example can be used to create a master MOF file (Mastervm.mof).</span></span>

    ```syntax
    [Locale(0x409)]
    class Group1
    {
        [key] string ID;
        [DisplayName("Numbers"),
            ValueMap{0,1,2,3}:amended,
            Values{"Zero", "One", "Two", "Three"}:amended]
        Uint32 Numbers;
    };
    ```

2.  <span data-ttu-id="8b1fb-109">建立 MOF 檔案的語言中性和語言特定版本。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-109">Create the language-neutral and language-specific versions of the MOF file.</span></span>

    <span data-ttu-id="8b1fb-110">在命令提示字元中輸入下列命令，以建立特定語言和特定語言版本的 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-110">Type the following command at a command prompt to create the language-neutral and language-specific versions of the MOF file.</span></span>

    ```syntax
    mofcomp -MOF:LnVm.mof -MFL:LsVm.mfl -Amendment:MS_409 MasterVm.mof
    ```

    <span data-ttu-id="8b1fb-111">MOF 編譯器會產生語言特定和語言中性的 MOF 檔案，LnVm. MOF 和 LsVm mfl。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-111">The MOF compiler generates the language-specific and language-neutral MOF files, LnVm.mof and LsVm.mfl.</span></span> <span data-ttu-id="8b1fb-112">[ [數位](numbers.md) ] 屬性的美式英文值會放在美式英文命名空間的 mfl 檔案中。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-112">The American English values for the [Numbers](numbers.md) property is placed in the .mfl file for the American English namespace.</span></span>

    <span data-ttu-id="8b1fb-113">下列程式碼範例顯示 LsVm mfl 檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-113">The following code example shows the contents of the LsVm.mfl file.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_409";};
    #pragma namespace("\\\\.\\root\\default\\ms_409")

    [AMENDMENT, LOCALE(0x409)] 
    class Group1
    {
      [ValueMap{0, 1, 2, 3} : Amended,
          Values{"Zero", "One", "Two", "Three"} : Amended] 
      Uint32 Numbers;
    };
    ```

3.  <span data-ttu-id="8b1fb-114">編譯兩個 MOF 檔案，並將類別資訊儲存在 CIM 存放庫中。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-114">Compile the two MOF files and store the class information in the CIM repository.</span></span>

    <span data-ttu-id="8b1fb-115">在命令提示字元中輸入下列命令，以編譯兩個 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-115">Type the following command at a command prompt to compile the two MOF files.</span></span>

    ```syntax
    Mofcomp LnVm.mof 
    Mofcomp LsVm.mfl
    ```

4.  <span data-ttu-id="8b1fb-116">當地語系化其他地區設定的 MFL 檔案。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-116">Localize the MFL file for other locales.</span></span>

    <span data-ttu-id="8b1fb-117">下列程式碼範例會顯示法文命名空間之 MFL 檔的內容。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-117">The following code example shows the contents of an MFL file for the French namespace.</span></span>

    ```syntax
    #pragma namespace("\\\\.\\root\\default")
    instance of __namespace{ name="ms_40C";};
    #pragma namespace("\\\\.\\root\\default\\ms_40C")

    [AMENDMENT, LOCALE(0x40C)] 
    class Group1
    {
        [key] string ID;
        [ValueMap{0, 1, 2, 3} : Amended,
            Values{"Zero", "Un", "Deux", "Trois"} : Amended]
        Uint32 Numbers;
    };
    ```

<span data-ttu-id="8b1fb-118">最後的結果是，[ [數位](numbers.md) ] 屬性的顯示名稱和值都取決於已登入使用者的地區設定。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-118">The net result is that both the display name and the value of the [Numbers](numbers.md) property depend on the locale of the logged-on user.</span></span> <span data-ttu-id="8b1fb-119">如果使用者指定了尚未提供的地區設定，則預設的辨識符號資料會來自英文 (ms \_ 409) 命名空間。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-119">If the user specifies a locale that has not been provided, the default qualifier data comes from the English (ms\_409) namespace.</span></span>

<span data-ttu-id="8b1fb-120">這項設計的含意是，每個字串值都是用來做為無法當地語系化的查閱識別碼。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-120">The implication of this design is that each string value is used as a lookup identifier, which cannot be localized.</span></span> <span data-ttu-id="8b1fb-121">定義此配置時，您必須確定提供者所放置的值與地區設定無關。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-121">When defining this scheme, you must ensure that the value the provider puts in is locale-independent.</span></span>

> [!Note]  
> <span data-ttu-id="8b1fb-122">WMI 目前未提供將值對應至由限定詞所定義之字串的執行時間支援。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-122">WMI does not currently provide run-time support for mapping values to strings defined by qualifiers.</span></span> <span data-ttu-id="8b1fb-123">建議語法的解讀是應用程式的責任。</span><span class="sxs-lookup"><span data-stu-id="8b1fb-123">Interpretation of the suggested syntax is the application's responsibility.</span></span>

 

 

 



