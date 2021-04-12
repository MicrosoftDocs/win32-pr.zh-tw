---
description: 如同受控物件格式 (MOF) 的許多其他技術，將限定詞套用至您的程式碼是相當簡單的程式。
ms.assetid: aaa5c921-bdcd-40e6-ab4b-9441a1957e5b
ms.tgt_platform: multiple
title: 套用辨識符號
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 042a3cdbf7236dc838735ce0cbf18a6315dd02e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695827"
---
# <a name="applying-a-qualifier"></a><span data-ttu-id="3c6ab-103">套用辨識符號</span><span class="sxs-lookup"><span data-stu-id="3c6ab-103">Applying a Qualifier</span></span>

<span data-ttu-id="3c6ab-104">如同受控物件格式 (MOF) 的許多其他技術，將限定詞套用至您的程式碼是相當簡單的程式。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-104">Like many other techniques in Managed Object Format (MOF), applying a qualifier to your code is a relatively simple process.</span></span>

<span data-ttu-id="3c6ab-105">唯一真正的挑戰是 WMI 強制執行之命名慣例的下列限制：</span><span class="sxs-lookup"><span data-stu-id="3c6ab-105">The only real challenges are the following restrictions in naming conventions that WMI enforces:</span></span>

-   <span data-ttu-id="3c6ab-106">辨識符號可以描述類別、實例、屬性、方法或方法參數。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-106">A qualifier can describe a class, instance, property, method, or method parameter.</span></span>
-   <span data-ttu-id="3c6ab-107">辨識符號名稱不能有開頭或結尾的底線。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-107">Qualifier names cannot have either leading or trailing underscores.</span></span>
-   <span data-ttu-id="3c6ab-108">限定詞名稱的開頭不能是數位。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-108">A qualifier name cannot begin with a digit.</span></span>
-   <span data-ttu-id="3c6ab-109">辨識符號名稱不能包含特殊字元，例如 & \* @！</span><span class="sxs-lookup"><span data-stu-id="3c6ab-109">A qualifier name cannot contain special characters such as & \* @ !</span></span><span data-ttu-id="3c6ab-110"> ~ \\ /.</span><span class="sxs-lookup"><span data-stu-id="3c6ab-110"> ~ \\ /.</span></span>
-   <span data-ttu-id="3c6ab-111">所有限定詞名稱都不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-111">All qualifier names are case-insensitive.</span></span>
-   <span data-ttu-id="3c6ab-112">您無法重新定義標準的 WMI 限定詞或任何在「DMTF CIM」規格中描述的限定詞。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-112">You cannot redefine the standard WMI qualifiers or any qualifiers described in the DMTF CIM specification.</span></span>
-   <span data-ttu-id="3c6ab-113">未明確宣告辨識符號類型。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-113">Qualifier types are not explicitly declared.</span></span>

    <span data-ttu-id="3c6ab-114">如果您未宣告辨識符號類型，WMI 會將類型假設為布林值 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-114">If you do not declare a qualifier type, WMI assumes the type as Boolean with a value of **TRUE**.</span></span> <span data-ttu-id="3c6ab-115">否則，會以您宣告的辨識符號值為基礎的 WMI 類型限定詞。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-115">Otherwise, WMI types qualifiers based on the qualifier values you declare.</span></span>

-   <span data-ttu-id="3c6ab-116">建立您自己的限定詞時，您應該在您的架構名稱之前加上您的辨識符號名稱。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-116">When creating your own qualifiers, you should prefix your schema name to your qualifier name.</span></span>

    <span data-ttu-id="3c6ab-117">這項規則的目的是要避免與新的限定詞混淆。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-117">The purpose of this rule is to avoid confusion with new qualifiers.</span></span>

-   <span data-ttu-id="3c6ab-118">您可以建立同質的限定詞陣列。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-118">You can create homogeneous arrays of qualifiers.</span></span>

    <span data-ttu-id="3c6ab-119">下列程式碼範例示範如何使用以大括弧括住的值來指定限定詞陣列。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-119">The following code example shows how qualifier arrays are specified with curly braces that surround the values.</span></span>

    ``` syntax
    [StringArray{"hello", "there"}, SingleElementArray{3}]
    ```

-   <span data-ttu-id="3c6ab-120">WMI 不支援未列在參考中的 automation 類型，例如 VT \_ Null。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-120">WMI does not support automation types not listed in the reference, such as VT\_NULL.</span></span> <span data-ttu-id="3c6ab-121">如需詳細資訊，請參閱 [MOF 資料類型](mof-data-types.md)。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-121">For more information, see [MOF Data Types](mof-data-types.md).</span></span>

<span data-ttu-id="3c6ab-122">下列程式可協助您使用 c + +，將限定詞加入至屬性。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-122">The following procedure helps you to use C++ to add a qualifier to a property.</span></span>

<span data-ttu-id="3c6ab-123">**使用 c + + 套用限定詞**</span><span class="sxs-lookup"><span data-stu-id="3c6ab-123">**To apply a qualifier using C++**</span></span>

-   <span data-ttu-id="3c6ab-124">將限定詞套用至 [**IWbemQualifierSet：:P**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) ui 方法的呼叫。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-124">Apply the qualifier with a call to the [**IWbemQualifierSet::Put**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemqualifierset-put) method.</span></span>

    <span data-ttu-id="3c6ab-125">您可以使用 [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) 的其他方法來取出或刪除現有的限定詞。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-125">You can use other methods of [**IWbemQualifierSet**](/windows/desktop/api/Wbemcli/nn-wbemcli-iwbemqualifierset) to retrieve or delete existing qualifiers.</span></span>

<span data-ttu-id="3c6ab-126">下列程式可協助您將限定詞套用至 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-126">The following procedure helps you to apply a qualifier in MOF files.</span></span>

<span data-ttu-id="3c6ab-127">**使用 MOF 描述具有辨識符號的關鍵字或識別碼**</span><span class="sxs-lookup"><span data-stu-id="3c6ab-127">**To describe a keyword or identifier with a qualifier using MOF**</span></span>

-   <span data-ttu-id="3c6ab-128">在限定詞所描述的關鍵字或識別碼之前，將限定詞放在括弧中。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-128">Place a qualifier in brackets before the keyword or identifier described by the qualifier.</span></span>

    <span data-ttu-id="3c6ab-129">下列程式碼範例顯示如何使用限定詞。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-129">The following code example shows how qualifiers are used.</span></span>

    ``` syntax
    [qualifiers...]
    class StdDisk
    {
      [qualifiers...]  uint32 dwNumCylinders;
      [qualifiers...]  uint32 dwNumHeads;
      [qualifiers...]  sint32 Method1();
      sint32 Method2([qualifiers...] Parameter1);
    };
    ```

    <span data-ttu-id="3c6ab-130">下列範例說明適當的限定詞位置。</span><span class="sxs-lookup"><span data-stu-id="3c6ab-130">The following example describes the proper placement of qualifiers.</span></span>

    ``` syntax
    [Abstract]
    class MyClass
    {
        [Amendment, InstanceOf]  uint32 dwNumber;
        sint32 MyMethod ([in] sint32 Param);
    };
    ```

 

 



