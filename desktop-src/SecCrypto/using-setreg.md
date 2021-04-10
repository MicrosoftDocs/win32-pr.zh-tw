---
description: SetReg 工具會設定登錄機碼的值，以控制 Authenticode 憑證驗證程式的行為。
ms.assetid: c34c00fe-da99-4c2e-9e9a-0ef6406ae5ae
title: 使用 SetReg
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 706463f86d38a03bc3416713be7427df55424d09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114121"
---
# <a name="using-setreg"></a><span data-ttu-id="42668-103">使用 SetReg</span><span class="sxs-lookup"><span data-stu-id="42668-103">Using SetReg</span></span>

<span data-ttu-id="42668-104">SetReg 工具會設定登錄機碼的值，以控制 Authenticode 憑證驗證程式的行為。</span><span class="sxs-lookup"><span data-stu-id="42668-104">The SetReg tool sets the value of the registry keys controlling the behavior of the Authenticode certificate verification process.</span></span> <span data-ttu-id="42668-105">這些金鑰稱為軟體發佈狀態金鑰，可控制是否要信任測試根目錄、允許離線核准憑證、測試憑證到期日，以及執行撤銷檢查。</span><span class="sxs-lookup"><span data-stu-id="42668-105">These keys, called the Software Publishing State Keys, control whether to trust a test root, allow offline approval of certificates, test certificate expiration dates, and perform revocation checks.</span></span>

<span data-ttu-id="42668-106">下列命令會列出使用 SetReg 的語法和選項。</span><span class="sxs-lookup"><span data-stu-id="42668-106">The following command lists the syntax and options for using SetReg.</span></span>

<span data-ttu-id="42668-107">**setreg-？**</span><span class="sxs-lookup"><span data-stu-id="42668-107">**setreg -?**</span></span>

<span data-ttu-id="42668-108">下列命令會將測試根目錄信任。</span><span class="sxs-lookup"><span data-stu-id="42668-108">The following command makes a test root trusted.</span></span> <span data-ttu-id="42668-109">根據預設，測試根目錄不受信任。</span><span class="sxs-lookup"><span data-stu-id="42668-109">By default, a test root is not trusted.</span></span> <span data-ttu-id="42668-110">在索引鍵值的任何變更之後，就會顯示所有索引鍵值的目前值清單。</span><span class="sxs-lookup"><span data-stu-id="42668-110">After any changes in the key values are made, a list of the current value of all of the key values is displayed.</span></span> <span data-ttu-id="42668-111">如果使用 **-q** 選項，則不會顯示金鑰值。</span><span class="sxs-lookup"><span data-stu-id="42668-111">If the **-q** option is used, the key values are not displayed.</span></span>

<span data-ttu-id="42668-112">**setreg 1 TRUE**</span><span class="sxs-lookup"><span data-stu-id="42668-112">**setreg 1 TRUE**</span></span>

<span data-ttu-id="42668-113">下列命令會讓測試根目錄不受信任，並導致所有驗證檢查撤銷。</span><span class="sxs-lookup"><span data-stu-id="42668-113">The following command makes a test root untrusted and causes all verification to check for revocation.</span></span> <span data-ttu-id="42668-114">使用 **-q** 選項，因此不會顯示金鑰值清單</span><span class="sxs-lookup"><span data-stu-id="42668-114">The **-q** option is used so that the list of key values is not displayed</span></span>

<span data-ttu-id="42668-115">**setreg-q 1 FALSE 3 TRUE**</span><span class="sxs-lookup"><span data-stu-id="42668-115">**setreg -q 1 FALSE 3 TRUE**</span></span>

> [!Note]  
> <span data-ttu-id="42668-116">命令、選項和引數不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="42668-116">Commands, options, and arguments are not case sensitive.</span></span>

 

 

 



