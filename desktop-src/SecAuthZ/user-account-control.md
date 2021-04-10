---
description: 可讓使用者以非系統管理員（稱為標準使用者）和系統管理員身分執行一般工作，而不需要切換使用者、登出或使用 [執行身分]。
ms.assetid: 8a7ba726-c2a6-4b7b-b664-3c6fcfbfb221
title: " (授權) 的使用者帳戶控制"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7f3cd8f31dda8f1b15145bc4003fc9ede8782c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944966"
---
# <a name="user-account-control-authorization"></a><span data-ttu-id="310a2-103"> (授權) 的使用者帳戶控制</span><span class="sxs-lookup"><span data-stu-id="310a2-103">User Account Control (Authorization)</span></span>

<span data-ttu-id="310a2-104"> (UAC) 的使用者帳戶控制可讓使用者以非系統管理員的身分（稱為標準使用者）或系統管理員身分執行一般工作，而不需要切換使用者、登出或使用 [ **執行** 身分]。</span><span class="sxs-lookup"><span data-stu-id="310a2-104">User Account Control (UAC) enables users to perform common tasks as nonadministrators, called standard users, and as administrators without having to switch users, log off, or use **Run As**.</span></span> <span data-ttu-id="310a2-105">「永不通知」設定的 UAC 行為不再停用 UAC。</span><span class="sxs-lookup"><span data-stu-id="310a2-105">The behavior of UAC for the "Never notify" setting no longer disables UAC.</span></span> <span data-ttu-id="310a2-106">[永不通知] 設定會提供您一個分割權杖，而且一律會自動提升所需的許可權。</span><span class="sxs-lookup"><span data-stu-id="310a2-106">The "Never notify" setting gives you a split token and always automatically elevates the privilege required.</span></span> <span data-ttu-id="310a2-107">此奧妙可能會導致您的應用程式發生相容性問題。</span><span class="sxs-lookup"><span data-stu-id="310a2-107">This subtlety may cause your app to have compatibility problems.</span></span> <span data-ttu-id="310a2-108">您仍然可以使用群組原則或手動設定登錄機碼來停用 UAC。</span><span class="sxs-lookup"><span data-stu-id="310a2-108">You can still disable UAC by using Group Policies or manually setting the registry key.</span></span>

<span data-ttu-id="310a2-109">**Windows server 2008 R2、windows 7、Windows server 2008 和 Windows Vista：** [永不通知] 設定會停用 UAC。</span><span class="sxs-lookup"><span data-stu-id="310a2-109">**Windows Server 2008 R2, Windows 7, Windows Server 2008 and Windows Vista:** The "Never notify" setting disables UAC.</span></span>

<span data-ttu-id="310a2-110">例如，如果您執行下列步驟來變更 [永遠不要通知] 設定，當您嘗試在需要提高許可權的資料夾中建立檔案時，就會得到不同的結果。</span><span class="sxs-lookup"><span data-stu-id="310a2-110">For example, if you perform the following steps to change the "Never notify" setting, you get different outcomes when you attempt to create a file in a folder that requires elevated privileges.</span></span> <span data-ttu-id="310a2-111">Windows 8 行為是拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="310a2-111">The Windows 8 behavior is to deny access.</span></span> <span data-ttu-id="310a2-112">Windows 7 的行為可讓您建立 File.txt 檔案。</span><span class="sxs-lookup"><span data-stu-id="310a2-112">The Windows 7 behavior allows you to create the File.txt file.</span></span>

1.  <span data-ttu-id="310a2-113">按一下或點擊 [ **開始**]。</span><span class="sxs-lookup"><span data-stu-id="310a2-113">Click or tap **Start**.</span></span> <span data-ttu-id="310a2-114">在搜尋方塊中，輸入「變更使用者帳戶控制設定」。</span><span class="sxs-lookup"><span data-stu-id="310a2-114">In the search box, type "Change User Account Control settings".</span></span>
2.  <span data-ttu-id="310a2-115">按一下或按一下 [ **變更使用者帳戶控制設定** ] 以開啟它。</span><span class="sxs-lookup"><span data-stu-id="310a2-115">Click or tap **Change User Account Control settings** to open it.</span></span>
3.  <span data-ttu-id="310a2-116">將滑杆移至 [ **永不通知**]。</span><span class="sxs-lookup"><span data-stu-id="310a2-116">Move the slider to **Never notify**.</span></span>
4.  <span data-ttu-id="310a2-117">按一下或點擊 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="310a2-117">Click or tap **OK**.</span></span>
5.  <span data-ttu-id="310a2-118">重新啟動您的電腦。</span><span class="sxs-lookup"><span data-stu-id="310a2-118">Restart your computer.</span></span>
6.  <span data-ttu-id="310a2-119">按一下或按一下 [ **開始** ]，然後 **執行**。</span><span class="sxs-lookup"><span data-stu-id="310a2-119">Click or tap **Start** and then **Run**.</span></span> <span data-ttu-id="310a2-120">在 [ **開啟** ] 方塊中，輸入 "Cmd.exe"。</span><span class="sxs-lookup"><span data-stu-id="310a2-120">In the **Open** box, type "Cmd.exe".</span></span> <span data-ttu-id="310a2-121">請注意，視窗的標題不包含 "Administrator" 字串。</span><span class="sxs-lookup"><span data-stu-id="310a2-121">Note that the title of the window doesn't contain the string "Administrator".</span></span>
7.  <span data-ttu-id="310a2-122">輸入「echo >% windir% \\ system32 \\File.txt」。</span><span class="sxs-lookup"><span data-stu-id="310a2-122">Type "echo > %windir%\\system32\\File.txt".</span></span>

<span data-ttu-id="310a2-123">UAC 是在 Windows Server 2008 和 Windows Vista 中新增的。</span><span class="sxs-lookup"><span data-stu-id="310a2-123">UAC was added in Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="310a2-124">標準使用者帳戶與 Windows XP 中的使用者帳戶同義。</span><span class="sxs-lookup"><span data-stu-id="310a2-124">A standard user account is synonymous with a user account in Windows XP.</span></span> <span data-ttu-id="310a2-125">屬於本機 Administrators 群組成員的使用者帳戶將以標準使用者的身分執行大部分的應用程式。</span><span class="sxs-lookup"><span data-stu-id="310a2-125">User accounts that are members of the local Administrators group will run most applications as a standard user.</span></span>

<span data-ttu-id="310a2-126">如需 UAC 的詳細資訊，請參閱下列主題。</span><span class="sxs-lookup"><span data-stu-id="310a2-126">For information about UAC, see the following topics.</span></span>



| <span data-ttu-id="310a2-127">主題</span><span class="sxs-lookup"><span data-stu-id="310a2-127">Topic</span></span>                                                                                                                                        | <span data-ttu-id="310a2-128">描述</span><span class="sxs-lookup"><span data-stu-id="310a2-128">Description</span></span>                                                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="310a2-129">[UI 開發中的使用者帳戶控制指導方針](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)</span><span class="sxs-lookup"><span data-stu-id="310a2-129">[Guidelines for User Account Control in UI Development](https://msdn.microsoft.com/library/aa511445(l=en-us,v=MSDN.10).aspx)</span></span><br/> | <span data-ttu-id="310a2-130">UAC 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="310a2-130">General information about UAC.</span></span><br/>                                                                                                     |
| [<span data-ttu-id="310a2-131">開發需要系統管理員許可權的應用程式</span><span class="sxs-lookup"><span data-stu-id="310a2-131">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)<br/>  | <span data-ttu-id="310a2-132">適用于開發應用程式的模型，這些應用程式會執行需要系統管理許可權，但以標準使用者的身份執行的作業。</span><span class="sxs-lookup"><span data-stu-id="310a2-132">Models for developing applications that perform operations that require administrative privilege, but that run as a standard user.</span></span><br/> |
| [<span data-ttu-id="310a2-133">授權參考</span><span class="sxs-lookup"><span data-stu-id="310a2-133">Authorization Reference</span></span>](authorization-reference.md)<br/>                                                                            | <span data-ttu-id="310a2-134">授權函數、介面、結構和其他程式設計專案的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="310a2-134">Detailed information about authorization functions, interfaces, structures, and other programming elements.</span></span><br/>                        |



 

 

 




