---
title: 修改現有的使用者介面
description: Active Directory 消費者和電腦 MMC 嵌入式管理單元的 [結果] 窗格會顯示容器內物件的幾個屬性資料行，例如 [名稱] 和 [描述] 屬性。
ms.assetid: 55f4ae82-c380-42a9-beba-047ffd0131eb
ms.tgt_platform: multiple
keywords:
- 修改現有的使用者介面 AD
- 使用者和電腦嵌入式管理單元 AD，修改顯示
- 使用者和電腦嵌入式管理單元 AD，新增資料行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd0765988a9ceed3e98966091ad94b868b96fd88
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839291"
---
# <a name="modifying-existing-user-interfaces"></a><span data-ttu-id="b6970-106">修改現有的使用者介面</span><span class="sxs-lookup"><span data-stu-id="b6970-106">Modifying Existing User Interfaces</span></span>

<span data-ttu-id="b6970-107">Active Directory 消費者和電腦 MMC 嵌入式管理單元的 [結果] 窗格會顯示容器內物件的幾個屬性資料行，例如 [ **名稱** ] 和 [ **描述** ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="b6970-107">The results pane of the Active Directory Users and Computers MMC snap-in displays several columns of attribute data for objects within a container, such as the **Name** and **Description** attributes.</span></span> <span data-ttu-id="b6970-108">此嵌入式管理單元可讓使用者新增及移除嵌入式管理單元結果窗格中顯示的資料行。</span><span class="sxs-lookup"><span data-stu-id="b6970-108">The snap-in enables the user to add and remove the columns displayed in the results pane of the snap-in.</span></span>

<span data-ttu-id="b6970-109">若要變更顯示，使用者會使用 **View** 下拉式功能表，並選取 [ **新增/移除欄位**]。</span><span class="sxs-lookup"><span data-stu-id="b6970-109">To change the display, the user uses the **View** pull-down menu and selects **Add/Remove Columns**.</span></span> <span data-ttu-id="b6970-110">在 [ **新增/移除資料行** ] 對話方塊中，有一份資料行清單可供使用者選擇，以顯示在 [結果] 窗格中。</span><span class="sxs-lookup"><span data-stu-id="b6970-110">In the **Add/Remove Columns** dialog box, there is a list of columns that the user can choose from to display in the results pane.</span></span>

<span data-ttu-id="b6970-111">Windows Server 2003、Standard Edition、Windows Server 2003、Enterprise Edition 和 Windows Server 2003 Datacenter Edition 隨附的 Active Directory 消費者和電腦 MMC 嵌入式管理單元，可讓您修改可在容器的嵌入式管理單元結果窗格中顯示的資料行清單。</span><span class="sxs-lookup"><span data-stu-id="b6970-111">The Active Directory Users and Computers MMC snap-in that is included with Windows Server 2003, Standard Edition, Windows Server 2003, Enterprise Edition, and Windows Server 2003, Datacenter Edition, provides the ability to modify the list of columns that can be displayed in the results pane of the snap-in for a container.</span></span> <span data-ttu-id="b6970-112">只有當嵌入式管理單元是以 Windows Server 2003 架構的樹系為目標時，才會有此功能。</span><span class="sxs-lookup"><span data-stu-id="b6970-112">This feature only exists if the snap-in is targeted at a forest with Windows Server 2003 schema.</span></span>

<span data-ttu-id="b6970-113">若要將資料行加入至清單，請在與屬性相關聯的物件類型中，將值加入至顯示規範的 **extraColumns** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="b6970-113">To add a column to the list, add a value to the **extraColumns** attribute of the display specifier for the object type that the attribute is associated with.</span></span> <span data-ttu-id="b6970-114">**ExtraColumns** 屬性是多重值字串屬性，其中每個字串都採用下列格式。</span><span class="sxs-lookup"><span data-stu-id="b6970-114">The **extraColumns** attribute is a multi-valued string attribute where each string is in the following format.</span></span>


```C++

<ldapdisplayname>,<column header>,<default visibility>,<width>,<unused>

```



<span data-ttu-id="b6970-115">下表列出這些值的內容。</span><span class="sxs-lookup"><span data-stu-id="b6970-115">The following table lists the contents of these values.</span></span>



| <span data-ttu-id="b6970-116">值</span><span class="sxs-lookup"><span data-stu-id="b6970-116">Value</span></span>                        | <span data-ttu-id="b6970-117">描述</span><span class="sxs-lookup"><span data-stu-id="b6970-117">Description</span></span>                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b6970-118">" &lt; ldapdisplayname &gt; "</span><span class="sxs-lookup"><span data-stu-id="b6970-118">"&lt;ldapdisplayname&gt;"</span></span>    | <span data-ttu-id="b6970-119">包含表示屬性之 **ldapDisplayName** 的字串。</span><span class="sxs-lookup"><span data-stu-id="b6970-119">Contains a string that represents the **ldapDisplayName** of the attribute.</span></span>                                                         |
| <span data-ttu-id="b6970-120">" &lt; 資料行標題 &gt; "</span><span class="sxs-lookup"><span data-stu-id="b6970-120">"&lt;column header&gt;"</span></span>      | <span data-ttu-id="b6970-121">包含字串，表示顯示在資料行標頭中的文字。</span><span class="sxs-lookup"><span data-stu-id="b6970-121">Contains a string that represents the text displayed in the header for the column.</span></span>                                                  |
| <span data-ttu-id="b6970-122">「 &lt; 預設可見度 &gt; 」</span><span class="sxs-lookup"><span data-stu-id="b6970-122">"&lt;default visibility&gt;"</span></span> | <span data-ttu-id="b6970-123">如果預設為隱藏屬性，則包含數值 0; 如果預設為可見，則為1。</span><span class="sxs-lookup"><span data-stu-id="b6970-123">Contains a numeric value that is 0 if the attribute is hidden by default or 1 if the attribute is visible by default.</span></span>               |
| <span data-ttu-id="b6970-124">「 &lt; 寬度 &gt; 」</span><span class="sxs-lookup"><span data-stu-id="b6970-124">"&lt;width&gt;"</span></span>              | <span data-ttu-id="b6970-125">包含資料行的寬度（以圖元為單位）。</span><span class="sxs-lookup"><span data-stu-id="b6970-125">Contains the width of the column, in pixels.</span></span> <span data-ttu-id="b6970-126">如果這個值是-1，則會將資料行的寬度設定為數據行標頭的寬度。</span><span class="sxs-lookup"><span data-stu-id="b6970-126">If this value is -1, the width of the column is set to the width of the column header.</span></span> |
| <span data-ttu-id="b6970-127">「 &lt; 未使用」 &gt;</span><span class="sxs-lookup"><span data-stu-id="b6970-127">"&lt;unused&gt;"</span></span>             | <span data-ttu-id="b6970-128">未使用的。</span><span class="sxs-lookup"><span data-stu-id="b6970-128">Unused.</span></span> <span data-ttu-id="b6970-129">必須為零。</span><span class="sxs-lookup"><span data-stu-id="b6970-129">Must be zero.</span></span>                                                                                                               |



 

<span data-ttu-id="b6970-130">例如，若要加入將在組織單位中顯示物件之正式名稱的資料行， **canonicalName** 屬性的值會加入至顯示規範容器中 **organizationalUnit-Display** 物件的 **extraColumns** 屬性。</span><span class="sxs-lookup"><span data-stu-id="b6970-130">For example, to add a column that will display the canonical name for objects in an organizational unit, a value for the **canonicalName** attribute is added to the **extraColumns** attribute of the **organizationalUnit-Display** object in the display specifiers container.</span></span> <span data-ttu-id="b6970-131">加入至 **OrganizationalUnit 顯示** 物件之 **extraColumns** 屬性的字串看起來會像下面這樣。</span><span class="sxs-lookup"><span data-stu-id="b6970-131">The string added to the **extraColumns** attribute of the **organizationalUnit-Display** object will look like the following.</span></span>


```C++
canonicalName,Canonical Name,0,150,0
```



<span data-ttu-id="b6970-132">[**新增/移除資料行**] 對話方塊只會顯示所顯示之容器類型之 **DisplaySpecifier** 物件的 **extraColumns** 屬性所包含的資料行。</span><span class="sxs-lookup"><span data-stu-id="b6970-132">The **Add/Remove Columns** dialog box displays only the columns that are contained in the **extraColumns** attribute of the **displaySpecifier** object of the container type that is being displayed.</span></span> <span data-ttu-id="b6970-133">如果 [ **extraColumns** ] 屬性不包含任何值，[ **加入/移除資料行** ] 對話方塊會顯示一組固定的資料行。</span><span class="sxs-lookup"><span data-stu-id="b6970-133">If the **extraColumns** attribute does not contain any values, the **Add/Remove Columns** dialog box will display a fixed set of columns.</span></span> <span data-ttu-id="b6970-134">一組固定的資料行複本包含在 **預設顯示** 物件的 **extraColumns** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="b6970-134">A copy of the fixed set of columns is contained in the **extraColumns** attribute of the **default-Display** object.</span></span>

<span data-ttu-id="b6970-135">若要將一或多個資料行加入特定物件的資料行清單中，您必須將所有的 **extraColumns** 值從 **預設的顯示** 物件複製到目標物件，然後加入自訂資料行。</span><span class="sxs-lookup"><span data-stu-id="b6970-135">To add one or more columns to the list of columns for a specific object, you must copy all of the **extraColumns** values from the **default-Display** object to the target object and then add the custom columns.</span></span> <span data-ttu-id="b6970-136">如果您在指定類別上指定 **extraColumns** 屬性，則該類別會使用這些資料行，而且不會將它們與 **預設顯示** 類別中指定的資料行合併。</span><span class="sxs-lookup"><span data-stu-id="b6970-136">If you specify the **extraColumns** attribute on a given class, then that class will use those columns and will not merge them with the columns that are specified in the **default-Display** class.</span></span> <span data-ttu-id="b6970-137">因此，對 **預設顯示** 類別的進一步變更將不會影響該物件。</span><span class="sxs-lookup"><span data-stu-id="b6970-137">Therefore, further changes to the **default-Display** class will have no effect on that object.</span></span>

<span data-ttu-id="b6970-138">若要針對未註冊任何自訂資料行的所有容器類型顯示自訂資料行，請將資料行的值加入 **預設顯示** 物件的 **extraColumns** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="b6970-138">To display a custom column for all container types that do not have any custom columns registered, add a value for the column to the **extraColumns** attribute of the **default-Display** object.</span></span>

 

 




