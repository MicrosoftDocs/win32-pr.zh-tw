---
title: " (設計基本概念的命令) "
description: 命令是使用者在使用您的應用程式時可以採取的動作。 瞭解將命令新增至您的應用程式功能表、功能區和工具列的指導方針。
ms.assetid: 64DF83BC-CC6D-4F0F-A1B2-AB3CF6DA33B3
ms.topic: reference
ms.date: 10/20/2020
ms.openlocfilehash: ece3f8f4fe395bb6ccf20a2b8b3db6bb36b00aee
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "103696051"
---
# <a name="commands-design-basics"></a><span data-ttu-id="6b772-104"> (設計基本概念的命令) </span><span class="sxs-lookup"><span data-stu-id="6b772-104">Commands (Design basics)</span></span>

> [!NOTE]
> <span data-ttu-id="6b772-105">此設計指南是針對 Windows 7 所建立，而且尚未針對較新版本的 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="6b772-105">This design guide was created for Windows 7 and has not been updated for newer versions of Windows.</span></span> <span data-ttu-id="6b772-106">大部分的指引仍然適用于準則，但展示和範例不會反映我們目前的 [設計指引](/windows/uwp/design/)。</span><span class="sxs-lookup"><span data-stu-id="6b772-106">Much of the guidance still applies in principle, but the presentation and examples do not reflect our [current design guidance](/windows/uwp/design/).</span></span>

<span data-ttu-id="6b772-107">命令是使用者在使用您的應用程式時可以採取的動作。</span><span class="sxs-lookup"><span data-stu-id="6b772-107">Commands are actions users can take while using your app.</span></span> <span data-ttu-id="6b772-108">瞭解將命令新增至您的應用程式功能表、功能區和工具列的指導方針。</span><span class="sxs-lookup"><span data-stu-id="6b772-108">Learn the guidelines for adding commands to your app's menus, ribbons, and toolbars.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6b772-109">本節內容</span><span class="sxs-lookup"><span data-stu-id="6b772-109">In this section</span></span>



| <span data-ttu-id="6b772-110">主題</span><span class="sxs-lookup"><span data-stu-id="6b772-110">Topic</span></span>                                   | <span data-ttu-id="6b772-111">描述</span><span class="sxs-lookup"><span data-stu-id="6b772-111">Description</span></span>                                                                                                                                                                                                                        |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6b772-112">功能表</span><span class="sxs-lookup"><span data-stu-id="6b772-112">Menus</span></span>](cmd-menus.md)<br/>       | <span data-ttu-id="6b772-113">功能表是命令的階層式清單，或可供使用者在目前內容中使用的選項。</span><span class="sxs-lookup"><span data-stu-id="6b772-113">Menus are hierarchical lists of commands or options available to users in the current context.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="6b772-114">絲帶</span><span class="sxs-lookup"><span data-stu-id="6b772-114">Ribbons</span></span>](cmd-ribbons.md)<br/>   | <span data-ttu-id="6b772-115">功能區是一種現代化的方法，可協助使用者以最少點擊次數的方式，有效率地尋找、瞭解及使用命令，而不需要設法解決試用和錯誤，也不需要參考說明。</span><span class="sxs-lookup"><span data-stu-id="6b772-115">Ribbons are the modern way to help users find, understand, and use commands efficiently and directly with a minimum number of clicks, with less need to resort to trial-and-error, and without having to refer to Help.</span></span><br/> |
| [<span data-ttu-id="6b772-116">工具列</span><span class="sxs-lookup"><span data-stu-id="6b772-116">Toolbars</span></span>](cmd-toolbars.md)<br/> | <span data-ttu-id="6b772-117">工具列是一種將命令分組以進行有效率存取的方式。</span><span class="sxs-lookup"><span data-stu-id="6b772-117">Toolbars are a way to group commands for efficient access.</span></span><br/>                                                                                                                                                              |



 

 

