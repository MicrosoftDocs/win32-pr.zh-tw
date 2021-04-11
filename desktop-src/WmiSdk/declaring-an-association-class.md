---
description: 關聯類別是一種特殊類型的類別，可定義兩個其他類別之間的關聯性。
ms.assetid: 21fd6e39-5dd3-41b8-a2f5-0135a6637ce8
ms.tgt_platform: multiple
title: 宣告關聯類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 083ce578ca912290fd026f225799793f89685aab
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027236"
---
# <a name="declaring-an-association-class"></a><span data-ttu-id="baf46-103">宣告關聯類別</span><span class="sxs-lookup"><span data-stu-id="baf46-103">Declaring an Association Class</span></span>

<span data-ttu-id="baf46-104">關聯類別是一種特殊類型的類別，可定義兩個其他類別之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="baf46-104">An association class is a special type of class that defines a relationship between two other classes.</span></span>

<span data-ttu-id="baf46-105">下列程式描述如何使用 MOF 程式碼建立關聯類別。</span><span class="sxs-lookup"><span data-stu-id="baf46-105">The following procedure describes how to create an association class using MOF code.</span></span>

<span data-ttu-id="baf46-106">**使用 MOF 程式碼建立關聯類別**</span><span class="sxs-lookup"><span data-stu-id="baf46-106">**To create an association class using MOF code**</span></span>

1.  <span data-ttu-id="baf46-107">將 **關聯** 限定詞指派給您的類別。</span><span class="sxs-lookup"><span data-stu-id="baf46-107">Assign the **Association** qualifier to your class.</span></span>

    <span data-ttu-id="baf46-108">雖然您可以使用關聯辨識符號來建立具有物件或類別參考的類別，但使用 **關聯** 辨識符號並不只會讓它清楚地指出您的類別是關聯類別，但最佳做法是確保您的類別會完整地做為關聯類別。</span><span class="sxs-lookup"><span data-stu-id="baf46-108">Although it is possible to create a class with references to objects or classes, using the **Association** qualifier not only makes it clear that your class is an association class, but, as a best practice, ensures that your class fully functions as an association class.</span></span>

2.  <span data-ttu-id="baf46-109">在類別內建立兩個參考，描述您想要使用 **ref** 型別來建立關聯的兩個物件實例。</span><span class="sxs-lookup"><span data-stu-id="baf46-109">Create two references within the class describing the two object instances you wish to associate together using the **ref** type.</span></span>

    <span data-ttu-id="baf46-110">參考會藉由包含物件的路徑，系結關聯中的兩個物件。</span><span class="sxs-lookup"><span data-stu-id="baf46-110">The references bind the two objects in the association by containing paths to the objects.</span></span> <span data-ttu-id="baf46-111">雖然並非必要，但也請使用參考屬性做為索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="baf46-111">Although not required, use the reference properties as key properties as well.</span></span>

    <span data-ttu-id="baf46-112">雖然您可以建立完整或命名空間相關的參考，但 WMI 對於跨命名空間的參考只有有限的支援。</span><span class="sxs-lookup"><span data-stu-id="baf46-112">Although you can create fully qualified or namespace-relative references, WMI has only limited support for cross-namespace references.</span></span> <span data-ttu-id="baf46-113">具體而言，只有靜態定義的物件可以跨命名空間界限彼此參考;動態支援的物件無法彼此參考。</span><span class="sxs-lookup"><span data-stu-id="baf46-113">Specifically, only statically defined objects can reference each other across namespace boundaries; dynamically supported objects cannot reference each other.</span></span>

    <span data-ttu-id="baf46-114">如有必要，請使用 **HasClassRef** 和 **Classref** 限定詞搭配 **物件 ref** 類型，以參考類別。</span><span class="sxs-lookup"><span data-stu-id="baf46-114">If necessary, use the **HasClassRef** and **Classref** qualifiers in conjunction with the **object ref** type to reference a class.</span></span>

    <span data-ttu-id="baf46-115">WMI 支援對實例使用一個 **ref** 參考點，而另一個 **物件** 參考指向類別。</span><span class="sxs-lookup"><span data-stu-id="baf46-115">WMI supports having one **ref** reference point to an instance, and the other **object** reference point to a class.</span></span> <span data-ttu-id="baf46-116">在此情況下，您的關聯類別會描述將實例系結至類別的關聯。</span><span class="sxs-lookup"><span data-stu-id="baf46-116">In this case, your association class would describe an association that binds instances to classes.</span></span>

    <span data-ttu-id="baf46-117">下列程式碼範例說明搭配 **物件** 類型使用 **HasClassRef** 和 **Classref** 的語法。</span><span class="sxs-lookup"><span data-stu-id="baf46-117">The following code example describes the syntax for using **HasClassRef** and **Classref** with an **object** type.</span></span>

    ``` syntax
    [HasClassRefs, Association]
    class SomeAssocClass
    {
         [key, classref{ "MyEndpoint", "OtherContainer" }]
         object ref ep1;
         [key] object ref ep2;
    }; 
    ```

    <span data-ttu-id="baf46-118">在上述範例中， **ep1** 參考可指向 **MyEndpoint** 類別或 **OtherContainer** 類別的類別定義。</span><span class="sxs-lookup"><span data-stu-id="baf46-118">In the previous example, the **ep1** reference can point to the class definitions for either the **MyEndpoint** class or the **OtherContainer** class.</span></span> <span data-ttu-id="baf46-119">請注意，雖然您必須弱型別參考類別，但您無法將 **Classref** 限定詞本身的型別弱：這麼做會大幅降低 WMI 查詢引擎的效率。</span><span class="sxs-lookup"><span data-stu-id="baf46-119">Note that while you must weakly type the reference class, you cannot weakly type the **Classref** qualifier itself; doing so would severely reduce the efficiency of the WMI query engine.</span></span> <span data-ttu-id="baf46-120">弱式類型是使用 **object** 關鍵字和 **ref** 資料類型來建立可包含任何資料類型的參考。</span><span class="sxs-lookup"><span data-stu-id="baf46-120">Weak typing is creating a reference that can contain any data type by using the **object** keyword and **ref** data type.</span></span> <span data-ttu-id="baf46-121">若要成功使用 **HasClassRef**，您必須設定相關的限定詞類別，以傳播至所有實例和子類別。</span><span class="sxs-lookup"><span data-stu-id="baf46-121">To successfully use **HasClassRef**, you must set the relevant qualifier flavors to propagate to all instances and subclasses.</span></span>

3.  <span data-ttu-id="baf46-122">視需要建立任何其他屬性。</span><span class="sxs-lookup"><span data-stu-id="baf46-122">Create any other properties as necessary.</span></span>

    <span data-ttu-id="baf46-123">下列程式碼範例顯示 WMI 目前不支援具有少於或等於兩個參考屬性的關聯類別。</span><span class="sxs-lookup"><span data-stu-id="baf46-123">The following code example shows that WMI does not currently support association classes having less or more than two reference properties.</span></span>

    ``` syntax
    [Association : ToInstance] 
    class MyAssocClass
    {
        ClassX ref PathToClassX ;
        ClassY ref PathToClassY ;
    };
    ```

4.  <span data-ttu-id="baf46-124">完成時，使用 MOF 編譯器編譯您的 MOF 程式碼。</span><span class="sxs-lookup"><span data-stu-id="baf46-124">When finished, compile your MOF code with the MOF compiler.</span></span>

    <span data-ttu-id="baf46-125">如需詳細資訊，請參閱 [編譯 MOF](compiling-mof-files.md)檔案。</span><span class="sxs-lookup"><span data-stu-id="baf46-125">For more information, see [Compiling MOF Files](compiling-mof-files.md).</span></span>

<span data-ttu-id="baf46-126">步驟3中的程式碼範例會定義 **MyAssocClass** 關聯類別。</span><span class="sxs-lookup"><span data-stu-id="baf46-126">The code example in Step 3 defines the **MyAssocClass** association class.</span></span> <span data-ttu-id="baf46-127">**MyAssocClass** 類別會定義 **ClassX** 和 **一些優質** 之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="baf46-127">The **MyAssocClass** class defines a relationship between **ClassX** and **ClassY**.</span></span> <span data-ttu-id="baf46-128">**PathToClassX** 和 **PathToClassY** 屬性包含要關聯之類別實例的物件路徑。</span><span class="sxs-lookup"><span data-stu-id="baf46-128">The **PathToClassX** and **PathToClassY** properties contain object paths to the instances of the classes to be associated.</span></span> <span data-ttu-id="baf46-129">關鍵字 **ToInstance** 是數個類別旗標的其中一個，WMI 會定義這些旗標來提供使用限定詞的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="baf46-129">The keyword **ToInstance** is one of several flavor flags that WMI defines to provide information about the use of a qualifier.</span></span> <span data-ttu-id="baf46-130">**ToInstance** 關鍵字指出 WMI 應該將 **關聯** 辨識符號傳播至 association 類別的所有實例。</span><span class="sxs-lookup"><span data-stu-id="baf46-130">The **ToInstance** keyword indicates that WMI should propagate the **Association** qualifier to all instances of the association class.</span></span> <span data-ttu-id="baf46-131">藉由檢查此實例限定詞，用戶端軟體可以判斷實例是否屬於關聯類別，而不需要取得類別定義來尋找 **關聯** 辨識符號。</span><span class="sxs-lookup"><span data-stu-id="baf46-131">By checking this instance qualifier, the client software can determine that an instance belongs to an association class, without having to retrieve the class definition to look for the **Association** qualifier.</span></span> <span data-ttu-id="baf46-132">如需詳細資訊，請參閱使用限定詞類別和[參考](references.md)[描述限定詞](describing-a-qualifier-with-a-qualifier-flavor.md)。</span><span class="sxs-lookup"><span data-stu-id="baf46-132">For more information, see [Describing a Qualifier With a Qualifier Flavor](describing-a-qualifier-with-a-qualifier-flavor.md) and [References](references.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="baf46-133">相關主題</span><span class="sxs-lookup"><span data-stu-id="baf46-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="baf46-134">設計受控物件格式 (MOF) 類別</span><span class="sxs-lookup"><span data-stu-id="baf46-134">Designing Managed Object Format (MOF) Classes</span></span>](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



