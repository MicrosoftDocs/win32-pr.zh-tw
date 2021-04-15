---
title: 刪除本機群組
description: 本主題說明如何從執行于 Windows 2000 Professional 的成員伺服器或電腦刪除本機群組。
ms.assetid: 030da25a-a606-4521-a243-d902c772fd00
ms.tgt_platform: multiple
keywords:
- 刪除本機群組 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14b55f90a8e6ac5cb77bf878d5ac680a6da91f73
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462888"
---
# <a name="deleting-local-groups"></a><span data-ttu-id="bbdff-104">刪除本機群組</span><span class="sxs-lookup"><span data-stu-id="bbdff-104">Deleting Local Groups</span></span>

<span data-ttu-id="bbdff-105">本主題說明如何從執行于 Windows 2000 Professional 的成員伺服器或電腦刪除本機群組。</span><span class="sxs-lookup"><span data-stu-id="bbdff-105">This topic shows how to delete a local group from a member server or computer running on Windows 2000 Professional.</span></span>

<span data-ttu-id="bbdff-106">**刪除本機群組**</span><span class="sxs-lookup"><span data-stu-id="bbdff-106">**To delete a local group**</span></span>

1.  <span data-ttu-id="bbdff-107">使用下列規則系結至電腦：</span><span class="sxs-lookup"><span data-stu-id="bbdff-107">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="bbdff-108">使用具有足夠許可權的帳戶來存取該電腦。</span><span class="sxs-lookup"><span data-stu-id="bbdff-108">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="bbdff-109">使用 WinNT 提供者、電腦名稱稱和額外的參數來使用下列系結字串格式，以指示 ADSI 系結至電腦： "WinNT://" <computer name> <computer> 。</span><span class="sxs-lookup"><span data-stu-id="bbdff-109">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span> <span data-ttu-id="bbdff-110">「 &lt; 電腦名稱稱」 &gt; 參數是要存取的電腦群組名。</span><span class="sxs-lookup"><span data-stu-id="bbdff-110">The "&lt;computer name&gt;" parameter is the name of the computer group to access.</span></span> <span data-ttu-id="bbdff-111">此參數會指示 ADSI 系結至電腦，並允許 WinNT 提供者的剖析器略過一些不明確的解析查詢，以判斷您要系結到的物件類型。</span><span class="sxs-lookup"><span data-stu-id="bbdff-111">This parameter instruct ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>
    3.  <span data-ttu-id="bbdff-112">系結至 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 介面。</span><span class="sxs-lookup"><span data-stu-id="bbdff-112">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>
2.  <span data-ttu-id="bbdff-113">使用 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)將 "group" 指定為類別，以刪除群組。</span><span class="sxs-lookup"><span data-stu-id="bbdff-113">Specify "group" as the class using [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)to delete the group.</span></span>

    <span data-ttu-id="bbdff-114">您不需要呼叫 [**IADs SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 來認可容器的變更。</span><span class="sxs-lookup"><span data-stu-id="bbdff-114">You do not need to call [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) to commit the change to the container.</span></span> <span data-ttu-id="bbdff-115">[**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)呼叫會認可將群組直接刪除到目錄中的作業。</span><span class="sxs-lookup"><span data-stu-id="bbdff-115">The [**IADsContainer.Delete**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) call commits the deletion of the group directly to the directory.</span></span>

 

 