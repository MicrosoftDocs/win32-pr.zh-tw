---
description: 系統管理員動作是用來執行系統管理安裝的最上層動作。
ms.assetid: 9925a645-5909-42c7-9de8-f908a5e42be9
title: 管理動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00106c9ab7877918e122f1ec9bd201fe30bb68b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848986"
---
# <a name="admin-action"></a><span data-ttu-id="4d907-103">管理動作</span><span class="sxs-lookup"><span data-stu-id="4d907-103">ADMIN Action</span></span>

<span data-ttu-id="4d907-104">系統管理員動作是用來執行系統 [管理安裝](administrative-installation.md)的最上層動作。</span><span class="sxs-lookup"><span data-stu-id="4d907-104">The ADMIN action is a top-level action used to perform [administrative installations](administrative-installation.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4d907-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="4d907-105">Sequence Restrictions</span></span>

<span data-ttu-id="4d907-106">沒有任何順序限制。</span><span class="sxs-lookup"><span data-stu-id="4d907-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4d907-107">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="4d907-107">ActionData Messages</span></span>

<span data-ttu-id="4d907-108">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="4d907-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d907-109">備註</span><span class="sxs-lookup"><span data-stu-id="4d907-109">Remarks</span></span>

<span data-ttu-id="4d907-110">系統管理員動作不會從動作資料表序列內呼叫，Windows Installer 會在使用設定為 "ACTION = ADMIN" 的 *szCommandLine* 參數呼叫 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta)時執行此動作，或使用 '/a ' 命令列參數來呼叫命令列可執行檔 Msiexec.exe。</span><span class="sxs-lookup"><span data-stu-id="4d907-110">The ADMIN action is not called from within the action table sequence, Windows Installer executes this action when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called with the *szCommandLine* parameter set to "ACTION=ADMIN" or the command line executable Msiexec.exe is called with the '/a' command line switch.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4d907-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="4d907-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d907-112">AdminUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="4d907-112">AdminUISequence Table</span></span>](adminuisequence-table.md)
</dt> <dt>

[<span data-ttu-id="4d907-113">AdminExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="4d907-113">AdminExecuteSequence Table</span></span>](adminexecutesequence-table.md)
</dt> </dl>

 

 



