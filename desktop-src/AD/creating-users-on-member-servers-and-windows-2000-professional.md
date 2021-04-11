---
title: 在成員伺服器與 Windows 2000 Professional 上建立使用者
description: 本主題說明在成員伺服器或執行 Windows 2000 Professional 的電腦上建立使用者時所使用的步驟。
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- 在成員伺服器與 Windows 2000 Professional AD 上建立使用者
- 使用者廣告，在成員伺服器和 Windows 2000 Professional 上建立使用者
- Active Directory、使用、使用者、在成員伺服器與 Windows 2000 Professional 上建立使用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050c9e8ecf68465097f2c185d2d31e0195c25a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023264"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a><span data-ttu-id="74ff2-106">在成員伺服器與 Windows 2000 Professional 上建立使用者</span><span class="sxs-lookup"><span data-stu-id="74ff2-106">Creating Users on Member Servers and Windows 2000 Professional</span></span>

<span data-ttu-id="74ff2-107">**建立使用者**</span><span class="sxs-lookup"><span data-stu-id="74ff2-107">**To create a user**</span></span>

1.  <span data-ttu-id="74ff2-108">使用下列規則系結至電腦：</span><span class="sxs-lookup"><span data-stu-id="74ff2-108">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="74ff2-109">使用具有足夠許可權的帳戶來存取該電腦。</span><span class="sxs-lookup"><span data-stu-id="74ff2-109">Use an account that has sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="74ff2-110">使用 WinNT 提供者、電腦名稱稱和額外的參數，來使用下列系結字串格式，以告訴 ADSI 系結至電腦： "WinNT://" <computer name> <computer> 。</span><span class="sxs-lookup"><span data-stu-id="74ff2-110">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to tell ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="74ff2-111">「 &lt; 電腦名稱稱」 &gt; 電腦是您想要存取其群組的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="74ff2-111">The "&lt;computer name&gt;" computer is the name of the computer whose groups you want to access.</span></span> <span data-ttu-id="74ff2-112">此參數會指示 ADSI 系結至電腦，並允許 WinNT 提供者的剖析器略過一些不明確的解析查詢，以判斷您要系結到的物件類型。</span><span class="sxs-lookup"><span data-stu-id="74ff2-112">This parameter tells ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="74ff2-113">系結至 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 介面。</span><span class="sxs-lookup"><span data-stu-id="74ff2-113">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="74ff2-114">使用 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) 來指定 "user" 作為類別，以新增使用者。</span><span class="sxs-lookup"><span data-stu-id="74ff2-114">Specify "user" as the class using [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) to add the user.</span></span>
3.  <span data-ttu-id="74ff2-115">使用 IADs 將使用者寫入電腦的安全性資料庫 [**。 SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo)。</span><span class="sxs-lookup"><span data-stu-id="74ff2-115">Write the user to the computer's security database using [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 