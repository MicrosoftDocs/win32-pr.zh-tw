---
description: Msimerg.exe 是命令列公用程式，它會使用 MsiDatabaseMerge 將參考資料庫合併至基底資料庫。
ms.assetid: db0c9ae5-a8e8-4eff-ae14-67dcce352483
title: Msimerg.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0555aa7bd762b92ed67d0bac1487159fadb73a6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945055"
---
# <a name="msimergexe"></a><span data-ttu-id="ff8bb-103">Msimerg.exe</span><span class="sxs-lookup"><span data-stu-id="ff8bb-103">Msimerg.exe</span></span>

<span data-ttu-id="ff8bb-104">Msimerg.exe 是命令列公用程式，它會使用 [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) 將參考資料庫 [合併](merges-and-transforms.md) 至基底資料庫。</span><span class="sxs-lookup"><span data-stu-id="ff8bb-104">Msimerg.exe is a command line utility that uses [**MsiDatabaseMerge**](/windows/desktop/api/Msiquery/nf-msiquery-msidatabasemergea) to [merge](merges-and-transforms.md) a reference database into a base database.</span></span>

<span data-ttu-id="ff8bb-105">此工具僅適用于 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。</span><span class="sxs-lookup"><span data-stu-id="ff8bb-105">This tool is only available in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff8bb-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ff8bb-106">Syntax</span></span>

<span data-ttu-id="ff8bb-107">**Msimerg** *{基底資料庫} {參考資料庫}*</span><span class="sxs-lookup"><span data-stu-id="ff8bb-107">**Msimerg** *{base database}{reference database}*</span></span>

<span data-ttu-id="ff8bb-108">如果兩個資料庫之間有合併衝突，則會將衝突資訊放置在 \_ MergeErrors 資料表中。</span><span class="sxs-lookup"><span data-stu-id="ff8bb-108">If there is a merge conflict between the two databases, the conflict information is placed in the \_MergeErrors table.</span></span>

## <a name="command-line-options"></a><span data-ttu-id="ff8bb-109">命令列選項</span><span class="sxs-lookup"><span data-stu-id="ff8bb-109">Command Line Options</span></span>

<span data-ttu-id="ff8bb-110">無。</span><span class="sxs-lookup"><span data-stu-id="ff8bb-110">None.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ff8bb-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="ff8bb-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ff8bb-112">Windows Installer 開發工具</span><span class="sxs-lookup"><span data-stu-id="ff8bb-112">Windows Installer Development Tools</span></span>](windows-installer-development-tools.md)
</dt> <dt>

[<span data-ttu-id="ff8bb-113">已發行的版本、工具和可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="ff8bb-113">Released Versions, Tools, and Redistributables</span></span>](released-versions-tools-and-redistributables.md)
</dt> </dl>

 

 



