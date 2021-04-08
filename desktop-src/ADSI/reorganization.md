---
title: 重組
description: 銷售組織已移至新的組織 \ 8212;\ 0034;銷售與支援。 \ 0034;Julie Bankert 已升階至副總裁，將帶領新的組織。
ms.assetid: 38b05d0b-2739-43c2-aac7-7555a5bfbc91
ms.tgt_platform: multiple
keywords:
- 重新組織 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 587f3de34738814b34ad250bb00bb7b71121d65c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020793"
---
# <a name="reorganization"></a><span data-ttu-id="16ed9-105">重組</span><span class="sxs-lookup"><span data-stu-id="16ed9-105">Reorganization</span></span>

<span data-ttu-id="16ed9-106">銷售組織已移至新的組織-「銷售和支援」。</span><span class="sxs-lookup"><span data-stu-id="16ed9-106">The sales organization has moved to a new organization — "Sales and Support."</span></span> <span data-ttu-id="16ed9-107">Julie Bankert 已升階至副總裁，將帶領新的組織。</span><span class="sxs-lookup"><span data-stu-id="16ed9-107">Julie Bankert has been promoted to vice president and will lead the new organization.</span></span> <span data-ttu-id="16ed9-108">Joe Worden 是企業系統管理員，必須將 Sales OU 移至新的 OU、銷售和支援人員。</span><span class="sxs-lookup"><span data-stu-id="16ed9-108">Joe Worden, the enterprise administrator, must move Sales OU to a new OU, Sales and Support.</span></span>


```VB
Set dom = GetObject("LDAP://DC=Fabrikam,DC=COM")
Set salesSupport = dom.Create("organizationalUnit", "CN=Sales and Support")
Set sales = salesSupport.MoveHere("LDAP://OU=Sales,DC=Fabrikam,DC=COM", vbNullString)
```



<span data-ttu-id="16ed9-109">使用此程式碼範例，銷售組織單位中的所有物件（包括子組織單位）都會移至新的組織單位。</span><span class="sxs-lookup"><span data-stu-id="16ed9-109">With this code example, all objects in the sales organizational unit, including the sub-organizational units, are moved to the new organizational unit.</span></span>

<span data-ttu-id="16ed9-110">現在，Joe 可將 Julie 移至銷售和支援組織單位。</span><span class="sxs-lookup"><span data-stu-id="16ed9-110">Now, Joe can move Julie into the Sales and Support organizational unit.</span></span>


```VB
Set usr = salesSupport.MoveHere("LDAP://CN=Julie Bankert,OU=Sales,OU=Sales and Support,DC=Fabrikam,DC=COM")
usr.Put "title", "Vice President"
usr.SetInfo
```



<span data-ttu-id="16ed9-111">請注意，Active Directory 會自動更新 Julie Bankert 和 Chris 灰色之間的經理直接報告連結。</span><span class="sxs-lookup"><span data-stu-id="16ed9-111">Be aware that the manager-direct report link between Julie Bankert and Chris Gray is automatically updated by Active Directory.</span></span>

<span data-ttu-id="16ed9-112">**若要建立 Active Directory 報表**</span><span class="sxs-lookup"><span data-stu-id="16ed9-112">**To create an Active Directory report**</span></span>

1.  <span data-ttu-id="16ed9-113">開啟 Visual Basic 版本6.0，當系統提示您輸入專案類型時，請選取 [ **資料項目目**]。</span><span class="sxs-lookup"><span data-stu-id="16ed9-113">Open Visual Basic version 6.0, and when prompted for the project type, select **Data Project**.</span></span>
2.  <span data-ttu-id="16ed9-114">在 [ **資料項目目**] 上，按兩下 [ **資料 Environment1**]。</span><span class="sxs-lookup"><span data-stu-id="16ed9-114">On **Data Project**, double-click **Data Environment1**.</span></span>
3.  <span data-ttu-id="16ed9-115">在 [ **資料環境** ] 視窗中，以滑鼠右鍵按一下連線物件 **(connection1.txt)** 然後選取 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="16ed9-115">On the **Data Environment** window, right-click the connection object **(Connection1)** and select **Properties**.</span></span>
4.  <span data-ttu-id="16ed9-116">選取 [ **Microsoft 目錄服務 OLE DB 提供者**]，然後按一下 **[下一步]**。</span><span class="sxs-lookup"><span data-stu-id="16ed9-116">Select **OLE DB Provider for Microsoft Directory Services**, and click **Next**.</span></span>
5.  <span data-ttu-id="16ed9-117">選取 [ **使用 Windows NT 整合式安全性**]，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="16ed9-117">Select **Use Windows NT Integrated security**, and click **OK**.</span></span> <span data-ttu-id="16ed9-118">這會建立連線物件。</span><span class="sxs-lookup"><span data-stu-id="16ed9-118">This creates a connection object.</span></span>
6.  <span data-ttu-id="16ed9-119">再以滑鼠右鍵按一下 [ **資料環境** ] 視窗，選取 [ **加入命令**]。</span><span class="sxs-lookup"><span data-stu-id="16ed9-119">Right-click the **Data Environment** window again to select **Add Command**.</span></span> <span data-ttu-id="16ed9-120">以滑鼠右鍵按一下 [ **Command1** ] 物件，然後選取 [ **屬性**]。</span><span class="sxs-lookup"><span data-stu-id="16ed9-120">Right-click the **Command1** object and select **Properties**.</span></span> <span data-ttu-id="16ed9-121">[下列 **Command1 屬性** ] 對話方塊隨即出現。</span><span class="sxs-lookup"><span data-stu-id="16ed9-121">The following **Command1 Properties** dialog box will appear.</span></span>

    ![command1 屬性對話方塊](images/adadsi3.png)

7.  <span data-ttu-id="16ed9-123">按一下 [ **SQL 語句** ] 選項按鈕，然後輸入下列內容：</span><span class="sxs-lookup"><span data-stu-id="16ed9-123">Click the **SQL Statement** option button and type the following:</span></span>

    <span data-ttu-id="16ed9-124">SELECT Name，telephoneNumber FROM ' LDAP：//DC = Fabrikam，DC = com ' WHERE objectCategory = ' Person ' AND objectClass = ' user '</span><span class="sxs-lookup"><span data-stu-id="16ed9-124">SELECT Name,telephoneNumber FROM 'LDAP://DC=Fabrikam,DC=com' WHERE objectCategory='Person' AND objectClass='user'</span></span>

    <span data-ttu-id="16ed9-125">會建立 **命令** 物件。</span><span class="sxs-lookup"><span data-stu-id="16ed9-125">The **Command** object is created.</span></span> <span data-ttu-id="16ed9-126">將 **命令** 物件加入至報表。</span><span class="sxs-lookup"><span data-stu-id="16ed9-126">Add the **Command** object to the report.</span></span>

8.  <span data-ttu-id="16ed9-127">按兩下 [**專案**] 視窗中的 [**資料 report1.rdl** ]。</span><span class="sxs-lookup"><span data-stu-id="16ed9-127">Double-click **Data Report1** from the **Project** window.</span></span>
9.  <span data-ttu-id="16ed9-128">將 **Command1** 物件從 [ **DataEnvironment1** ] 視窗拖曳到 [**資料包表**] 視窗中的 [**詳細** 資料] 區段。</span><span class="sxs-lookup"><span data-stu-id="16ed9-128">Drag the **Command1** object from the **DataEnvironment1** window to the **Detail** section in the **Data Report** window.</span></span>
10. <span data-ttu-id="16ed9-129">在 [ **DataReport1 屬性**] 的 [**資料來源**] 中，從下拉式功能表中選取 [ **DataEnvironment1** ]，然後在 [ **DataMember** ] 欄位中選取 [ **Command1** ]。</span><span class="sxs-lookup"><span data-stu-id="16ed9-129">On **DataReport1 Properties**, for **DataSource**, select **DataEnvironment1** from the pull-down menu, and select **Command1** in the **DataMember** field.</span></span>
11. <span data-ttu-id="16ed9-130">在 [專案] 視窗中，以滑鼠右鍵按一下 [ **資料項目目**]，然後選取 [ **DataProject 屬性**]。</span><span class="sxs-lookup"><span data-stu-id="16ed9-130">On the project window, right-click **Data Project**, and select **DataProject Properties**.</span></span>
12. <span data-ttu-id="16ed9-131">在 [ **DataProject 專案屬性** ] 對話方塊視窗的 [ **啟始物件**] 下，從下拉式功能表中選取 [ **DataReport1** ]。</span><span class="sxs-lookup"><span data-stu-id="16ed9-131">On the **DataProject - Project Properties** dialog window, under **Startup Object**, select **DataReport1** from the pull-down menu.</span></span> <span data-ttu-id="16ed9-132">按一下 [確定]  以儲存。</span><span class="sxs-lookup"><span data-stu-id="16ed9-132">Click **OK** to save.</span></span>
13. <span data-ttu-id="16ed9-133">編譯。</span><span class="sxs-lookup"><span data-stu-id="16ed9-133">Compile.</span></span> <span data-ttu-id="16ed9-134">將會出現下列 [ **DataReport1** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="16ed9-134">The following **DataReport1** dialog box will appear.</span></span>

    ![datareport1 對話方塊](images/adadsi4.png)

## <a name="related-topics"></a><span data-ttu-id="16ed9-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="16ed9-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16ed9-137">聯結異質資料</span><span class="sxs-lookup"><span data-stu-id="16ed9-137">Joining Heterogeneous Data</span></span>](joining-heterogeneous-data.md)
</dt> </dl>

 

 




