---
description: 通告動作是一種最上層的動作，稱為用以安裝或移除已公告的元件。
ms.assetid: d9c843e4-fcd9-4d47-9ca9-ffa83ed80574
title: 通告動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0985990d69863f250cfd6f589deb43a59f9c66e9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692804"
---
# <a name="advertise-action"></a><span data-ttu-id="4adbc-103">通告動作</span><span class="sxs-lookup"><span data-stu-id="4adbc-103">ADVERTISE Action</span></span>

<span data-ttu-id="4adbc-104">通告動作是一種最上層的動作，稱為用以安裝或移除已公告的元件。</span><span class="sxs-lookup"><span data-stu-id="4adbc-104">The ADVERTISE action is a top-level action called to install or remove advertised components.</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="4adbc-105">順序限制</span><span class="sxs-lookup"><span data-stu-id="4adbc-105">Sequence Restrictions</span></span>

<span data-ttu-id="4adbc-106">沒有任何順序限制。</span><span class="sxs-lookup"><span data-stu-id="4adbc-106">There are no sequence restrictions.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="4adbc-107">ActionData 訊息</span><span class="sxs-lookup"><span data-stu-id="4adbc-107">ActionData Messages</span></span>

<span data-ttu-id="4adbc-108">沒有任何 ActionData 訊息。</span><span class="sxs-lookup"><span data-stu-id="4adbc-108">There are no ActionData messages.</span></span>

## <a name="remarks"></a><span data-ttu-id="4adbc-109">備註</span><span class="sxs-lookup"><span data-stu-id="4adbc-109">Remarks</span></span>

<span data-ttu-id="4adbc-110">[*廣告*](a-gly.md) 指的是，安裝程式能夠提供應用程式的載入和啟動介面，而不需要實際安裝應用程式。</span><span class="sxs-lookup"><span data-stu-id="4adbc-110">[*Advertising*](a-gly.md) refers to the installer's ability to provide the loading and launching interfaces of an application without physically installing the application.</span></span> <span data-ttu-id="4adbc-111">在使用者或應用程式啟動已公告的介面之前，安裝程式不會安裝必要的元件。</span><span class="sxs-lookup"><span data-stu-id="4adbc-111">The installer does not install the necessary components until a user or application activates an advertised interface.</span></span> <span data-ttu-id="4adbc-112">這個概念稱為 [*隨選安裝*](i-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="4adbc-112">This concept is called [*install-on-demand*](i-gly.md).</span></span>

<span data-ttu-id="4adbc-113">未從動作資料表序列內呼叫公告動作，Windows Installer 會在使用 '/j ' 命令列參數呼叫命令列可執行檔 Msiexec.exe，或呼叫 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) 時，將 *szCommandLine* 參數設定為 action = 通告時執行此動作。</span><span class="sxs-lookup"><span data-stu-id="4adbc-113">The ADVERTISE action is not called from within the action table sequence, the Windows Installer executes this action when the command line executable Msiexec.exe is called with the '/j' command line switch or when [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) is called with the *szCommandLine* parameter set to ACTION=ADVERTISE.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4adbc-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="4adbc-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4adbc-115">AdvtExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="4adbc-115">AdvtExecuteSequence Table</span></span>](advtexecutesequence-table.md)
</dt> </dl>

 

 



