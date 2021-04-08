---
title: 設定 ADSI 開發的 Visual Basic 6。0
description: 本主題討論如何在 Visual Studio 中設定 Visual Basic，以開發 ADSI 應用程式。
ms.assetid: 167e89d7-80a3-4cc2-b79c-3744c1b184d6
ms.tgt_platform: multiple
keywords:
- 設定 ADSI 開發 ADSI 的 Visual Basic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0e6b1f39ec06d3716beab750dbf2a522d4c18cb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839131"
---
# <a name="setting-up-visual-basic-60-for-adsi-development"></a><span data-ttu-id="06387-104">設定 ADSI 開發的 Visual Basic 6。0</span><span class="sxs-lookup"><span data-stu-id="06387-104">Setting Up Visual Basic 6.0 for ADSI Development</span></span>

<span data-ttu-id="06387-105">**設定 Visual Basic 的 Microsoft Visual Studio 2010 開發環境**</span><span class="sxs-lookup"><span data-stu-id="06387-105">**Setting Up the Microsoft Visual Studio 2010 Development Environment For Visual Basic**</span></span>

1.  <span data-ttu-id="06387-106">啟動 Visual Studio 2010。</span><span class="sxs-lookup"><span data-stu-id="06387-106">Start Visual Studio 2010.</span></span>
2.  <span data-ttu-id="06387-107">建立新的 Visual Basic 專案。</span><span class="sxs-lookup"><span data-stu-id="06387-107">Create a new Visual Basic project.</span></span>
3.  <span data-ttu-id="06387-108">將參考新增至 **ACTIVE DS 型別程式庫**。</span><span class="sxs-lookup"><span data-stu-id="06387-108">Add a reference to the **Active DS Type Library**.</span></span>
    > [!Note]  
    > <span data-ttu-id="06387-109">如果您不需要早期的 COM 物件系結，請略過此步驟。</span><span class="sxs-lookup"><span data-stu-id="06387-109">If you do not require early COM object binding, ignore this step.</span></span>

     

    1.  <span data-ttu-id="06387-110">選取 [ **專案 \| 加入參考**]。</span><span class="sxs-lookup"><span data-stu-id="06387-110">Select **Project \| Add Reference**.</span></span>
    2.  <span data-ttu-id="06387-111">選取 [ **COM** ] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="06387-111">Select the **COM** tab.</span></span>
    3.  <span data-ttu-id="06387-112">選取 [ **ACTIVE DS 類型程式庫**]。</span><span class="sxs-lookup"><span data-stu-id="06387-112">Select **Active DS Type Library**.</span></span>

4.  <span data-ttu-id="06387-113">開始使用 ADSI 進行程式設計。</span><span class="sxs-lookup"><span data-stu-id="06387-113">Begin programming with ADSI.</span></span>

<span data-ttu-id="06387-114">開始之前，請先登入 Windows 網域。</span><span class="sxs-lookup"><span data-stu-id="06387-114">Before you begin, log on to a Windows domain.</span></span> <span data-ttu-id="06387-115">您必須擁有修改 Active Directory 資料庫的許可權。</span><span class="sxs-lookup"><span data-stu-id="06387-115">You must have permission to modify the Active Directory database.</span></span> <span data-ttu-id="06387-116">依預設，系統管理員具有此許可權。</span><span class="sxs-lookup"><span data-stu-id="06387-116">By default, the Administrator has this privilege.</span></span>

<span data-ttu-id="06387-117">**範例 Visual Basic 6.0 應用程式：修改使用者的 FullName 和描述**</span><span class="sxs-lookup"><span data-stu-id="06387-117">**A Sample Visual Basic 6.0 Application: Modifying FullName and Description for a User**</span></span>

1.  <span data-ttu-id="06387-118">遵循先前的步驟，建立標準可執行檔 Visual Basic 專案。</span><span class="sxs-lookup"><span data-stu-id="06387-118">Follow the previous steps to create a standard executable Visual Basic project.</span></span>
2.  <span data-ttu-id="06387-119">按兩下表單。</span><span class="sxs-lookup"><span data-stu-id="06387-119">Double-click the Form.</span></span> <span data-ttu-id="06387-120">在 [表單載入] 中 \_ ，輸入下列各項。</span><span class="sxs-lookup"><span data-stu-id="06387-120">In Form\_Load, type the following.</span></span> <span data-ttu-id="06387-121">您必須以網域中容器中現有使用者的 ADsPath 取代 "LDAP：//CN = jeffsmith，CN = users，DC = fabrikam，DC = com" 字串。</span><span class="sxs-lookup"><span data-stu-id="06387-121">You must replace the "LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com" string with the ADsPath of an existing user in a container in your domain.</span></span> <span data-ttu-id="06387-122">建立可針對此用途修改的測試使用者帳戶。</span><span class="sxs-lookup"><span data-stu-id="06387-122">Create a test user account that can be modified for this purpose.</span></span>
    ```VB
    '------------------------------------------------------------
    ' This code example is used to set the FullName and Description
    '------------------------------------------------------------
    Dim usr As IADsUser

    ' Bind to a user object.
    Set usr = GetObject("LDAP://CN=jeffsmith,CN=users,DC=fabrikam,DC=com")

    usr.FullName = "Jeff Smith"
    usr.Description = "A user for fabrikam.com" 
    usr.SetInfo ' Commit the changes to the directory
    ```

    

3.  <span data-ttu-id="06387-123">按下 **<F5>** 以執行程式。</span><span class="sxs-lookup"><span data-stu-id="06387-123">Press **<F5>** to run the program.</span></span>
4.  <span data-ttu-id="06387-124">若要確認變更，請使用 Active Directory 消費者和電腦管理工具。</span><span class="sxs-lookup"><span data-stu-id="06387-124">To verify changes, use the Active Directory Users and Computers management tool.</span></span> <span data-ttu-id="06387-125">如需使用 ADSI 和 Visual Basic 的詳細資訊，請參閱 [使用 Visual Basic 存取 Active Directory](accessing-active-directory-using-visual-basic.md)。</span><span class="sxs-lookup"><span data-stu-id="06387-125">For more information about using ADSI and Visual Basic, see [Accessing Active Directory Using Visual Basic](accessing-active-directory-using-visual-basic.md).</span></span>

 

 




