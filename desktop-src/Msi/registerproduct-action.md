---
description: RegisterProduct 動作會向安裝程式和 [新增/移除程式] 註冊產品資訊。 此外，此動作會將 Windows Installer 資料庫封裝儲存在本機電腦上。
ms.assetid: 689b09c7-9c17-42f5-ba31-cf9c6252e453
title: RegisterProduct 動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5afa2d3e9f00f736b8c4c7864d8ec4baa3aa8ad9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993120"
---
# <a name="registerproduct-action"></a><span data-ttu-id="b2f00-104">RegisterProduct 動作</span><span class="sxs-lookup"><span data-stu-id="b2f00-104">RegisterProduct Action</span></span>

<span data-ttu-id="b2f00-105">RegisterProduct 動作會向安裝程式和 [新增/移除程式] 註冊產品資訊。</span><span class="sxs-lookup"><span data-stu-id="b2f00-105">The RegisterProduct action registers the product information with the installer and with Add/Remove Programs.</span></span> <span data-ttu-id="b2f00-106">此外，此動作會將 Windows Installer 資料庫封裝儲存在本機電腦上。</span><span class="sxs-lookup"><span data-stu-id="b2f00-106">Additionally, this action stores the Windows Installer database package on the local computer.</span></span>

<span data-ttu-id="b2f00-107">RegisterProduct 動作會設定主控台中的 [新增/移除程式] 所顯示的控制項。</span><span class="sxs-lookup"><span data-stu-id="b2f00-107">The RegisterProduct action configures the controls displayed by the Add/Remove Programs in Control Panel.</span></span> <span data-ttu-id="b2f00-108">如需詳細資訊，請參閱 [使用 Windows Installer 設定 [新增/移除程式](configuring-add-remove-programs-with-windows-installer.md)]。</span><span class="sxs-lookup"><span data-stu-id="b2f00-108">For more information, see [Configuring Add/Remove Programs with Windows Installer](configuring-add-remove-programs-with-windows-installer.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="b2f00-109">順序限制</span><span class="sxs-lookup"><span data-stu-id="b2f00-109">Sequence Restrictions</span></span>

<span data-ttu-id="b2f00-110">沒有任何順序限制。</span><span class="sxs-lookup"><span data-stu-id="b2f00-110">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="b2f00-111">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="b2f00-111">ActionData Messages</span></span>



| <span data-ttu-id="b2f00-112">欄位</span><span class="sxs-lookup"><span data-stu-id="b2f00-112">Field</span></span> | <span data-ttu-id="b2f00-113">動作資料的描述</span><span class="sxs-lookup"><span data-stu-id="b2f00-113">Description of action data</span></span>            |
|-------|---------------------------------------|
| <span data-ttu-id="b2f00-114">\[1\]</span><span class="sxs-lookup"><span data-stu-id="b2f00-114">\[1\]</span></span> | <span data-ttu-id="b2f00-115">已註冊產品的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b2f00-115">Information about registered product.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="b2f00-116">備註</span><span class="sxs-lookup"><span data-stu-id="b2f00-116">Remarks</span></span>

<span data-ttu-id="b2f00-117">在安裝期間，系統管理安裝點不會執行 RegisterProduct 動作。</span><span class="sxs-lookup"><span data-stu-id="b2f00-117">The RegisterProduct action is not performed during installation to an administrative installation point.</span></span>

 

 



