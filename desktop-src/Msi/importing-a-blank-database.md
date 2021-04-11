---
description: 若要重現範例，您必須使用軟體工具（Windows Installer 資料庫檔案）複製或建立。
ms.assetid: e239bbe4-3290-40f0-9f28-0e8aa4ed23f8
title: 匯入空白資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b654b0de118013e8f211a9b06e896cc3f486faf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193682"
---
# <a name="importing-a-blank-database"></a><span data-ttu-id="b90ec-103">匯入空白資料庫</span><span class="sxs-lookup"><span data-stu-id="b90ec-103">Importing a Blank Database</span></span>

<span data-ttu-id="b90ec-104">若要重現範例，您必須使用軟體工具（Windows Installer 資料庫檔案）複製或建立。</span><span class="sxs-lookup"><span data-stu-id="b90ec-104">To reproduce the sample you need to copy, or create with a software tool, a Windows Installer database file.</span></span> <span data-ttu-id="b90ec-105">[Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)提供了完全空白的安裝資料庫，Schema.msi。</span><span class="sxs-lookup"><span data-stu-id="b90ec-105">A totally blank installation database, Schema.msi, is provided with the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span> <span data-ttu-id="b90ec-106">SDK 也會提供部分空白的資料庫 uisample.msi，其中包含簡單使用者介面所需的建議順序資料表和資料。</span><span class="sxs-lookup"><span data-stu-id="b90ec-106">The SDK also provides a partially blank database, uisample.msi, that contains the suggested sequence tables and data required for a simple user interface.</span></span> <span data-ttu-id="b90ec-107">製作 uisample.msi 的複本，並將它移至包含您在 [規劃安裝](planning-the-installation.md)時所建立之 [記事本] 資料夾的相同目錄中。</span><span class="sxs-lookup"><span data-stu-id="b90ec-107">Make a copy of uisample.msi and move it into the same directory containing the Notepad folder you created in [Planning the Installation](planning-the-installation.md).</span></span> <span data-ttu-id="b90ec-108">MNP2000.msi 重新命名檔案。</span><span class="sxs-lookup"><span data-stu-id="b90ec-108">Rename the file MNP2000.msi.</span></span> <span data-ttu-id="b90ec-109">安裝資料庫檔案和來源檔案都必須位於相同目錄的根目錄中。</span><span class="sxs-lookup"><span data-stu-id="b90ec-109">The installation database file and the source files must both be located at the root of the same directory.</span></span> <span data-ttu-id="b90ec-110">例如：</span><span class="sxs-lookup"><span data-stu-id="b90ec-110">For example:</span></span>

<span data-ttu-id="b90ec-111">C： \\ 範例 \\MNP2000.msi</span><span class="sxs-lookup"><span data-stu-id="b90ec-111">C:\\Sample\\MNP2000.msi</span></span>

<span data-ttu-id="b90ec-112">C： \\ 範例 \\ 記事本</span><span class="sxs-lookup"><span data-stu-id="b90ec-112">C:\\Sample\\Notepad</span></span>\\

<span data-ttu-id="b90ec-113">如果您不使用 Uisample.msi，則必須取得空白的資料庫（例如 Schema.msi），並使用資料庫編輯工具（例如，在 SDK 中提供的 Orca）或其他資料庫編輯器來輸入安裝的資訊。</span><span class="sxs-lookup"><span data-stu-id="b90ec-113">If you do not use Uisample.msi, then you must obtain a blank database, such as Schema.msi, and enter information for the installation using a database editing tool such as Orca, which is provided with the SDK, or another database editor.</span></span>

[<span data-ttu-id="b90ec-114">繼續</span><span class="sxs-lookup"><span data-stu-id="b90ec-114">Continue</span></span>](specifying-directory-structure.md)

 

 



