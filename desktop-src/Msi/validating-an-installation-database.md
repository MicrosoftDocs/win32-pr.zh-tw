---
description: 安裝套件的作者應該一律先在封裝上執行驗證，再嘗試第一次安裝套件，並在對套件進行任何變更時重新執行驗證。
ms.assetid: 1f16a349-4919-46d2-9b78-2533b8679a73
title: 驗證安裝資料庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f6db262a280afa1d9222696d40a6f5949d69ece0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847678"
---
# <a name="validating-an-installation-database"></a><span data-ttu-id="60ac6-103">驗證安裝資料庫</span><span class="sxs-lookup"><span data-stu-id="60ac6-103">Validating an Installation Database</span></span>

<span data-ttu-id="60ac6-104">安裝套件的作者應該一律先在封裝上執行驗證，再嘗試第一次安裝套件，並在對套件進行任何變更時重新執行驗證。</span><span class="sxs-lookup"><span data-stu-id="60ac6-104">Authors of installation packages should always run validation on their packages before attempting to install the package for the first time and rerun validation whenever making any changes to the package.</span></span> <span data-ttu-id="60ac6-105">驗證會掃描資料庫的錯誤，這些錯誤可能會個別出現，但在整個資料庫的內容中造成不正確的行為。</span><span class="sxs-lookup"><span data-stu-id="60ac6-105">Validation scans the database for errors that may appear valid individually but that cause incorrect behavior in the context of the whole database.</span></span> <span data-ttu-id="60ac6-106">嘗試安裝驗證失敗的封裝可能會損毀使用者的系統。</span><span class="sxs-lookup"><span data-stu-id="60ac6-106">Attempting to install a package that fails validation can damage the user's system.</span></span> <span data-ttu-id="60ac6-107">請參閱 [套件驗證](package-validation.md) 和 [內部一致性評估](internal-consistency-evaluators-ices.md)工具的章節。</span><span class="sxs-lookup"><span data-stu-id="60ac6-107">See the sections [Package Validation](package-validation.md) and [Internal Consistency Evaluators - ICEs](internal-consistency-evaluators-ices.md).</span></span>

<span data-ttu-id="60ac6-108">您可以使用 [Orca.exe](orca-exe.md) 或 [Msival2.exe](msival2-exe.md)來驗證範例封裝。</span><span class="sxs-lookup"><span data-stu-id="60ac6-108">You can validate the sample package using [Orca.exe](orca-exe.md) or [Msival2.exe](msival2-exe.md).</span></span> <span data-ttu-id="60ac6-109">若要查看 Msival2.exe 變更目錄的說明，並在命令列上輸入。</span><span class="sxs-lookup"><span data-stu-id="60ac6-109">To view the help for Msival2.exe change directories and enter on the command line.</span></span>

<span data-ttu-id="60ac6-110">Msival2 -?</span><span class="sxs-lookup"><span data-stu-id="60ac6-110">Msival2 -?</span></span>

<span data-ttu-id="60ac6-111">.Cub 檔 darice 包含 Msival2.exe 執行驗證所需的 ICE 自訂動作。</span><span class="sxs-lookup"><span data-stu-id="60ac6-111">The .cub file darice.cub contains the ICE custom actions needed by Msival2.exe to perform validation.</span></span> <span data-ttu-id="60ac6-112">若要驗證 MNP2000.msi 輸入</span><span class="sxs-lookup"><span data-stu-id="60ac6-112">To validate the MNP2000.msi enter</span></span>

<span data-ttu-id="60ac6-113">msival2 MNP2000.msi Darice .cub</span><span class="sxs-lookup"><span data-stu-id="60ac6-113">msival2 MNP2000.msi Darice.cub</span></span>

<span data-ttu-id="60ac6-114">如需驗證所傳回之錯誤和警告訊息的說明，請參閱 [ICE 參考](ice-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="60ac6-114">For a description of the error and warning messages returned by validation see the [ICE Reference](ice-reference.md).</span></span> <span data-ttu-id="60ac6-115">更正封裝中的所有錯誤，並視需要重新執行驗證，直到封裝通過驗證而沒有錯誤。</span><span class="sxs-lookup"><span data-stu-id="60ac6-115">Correct all the errors in the package and rerun validation as necessary until the package passes validation without errors.</span></span>

<span data-ttu-id="60ac6-116">當套件通過驗證之後，您可以按一下 MNP2000.msi 圖示，或從命令列使用 [命令列選項](command-line-options.md)來安裝範例封裝。</span><span class="sxs-lookup"><span data-stu-id="60ac6-116">Once the package passes validation, you can install the sample package by clicking on the MNP2000.msi icon or from the command line using the [Command Line Options](command-line-options.md).</span></span>

<span data-ttu-id="60ac6-117">這會完成範例安裝。</span><span class="sxs-lookup"><span data-stu-id="60ac6-117">This completes the sample installation.</span></span>

## <a name="next-example"></a><span data-ttu-id="60ac6-118">下一個範例</span><span class="sxs-lookup"><span data-stu-id="60ac6-118">Next example</span></span>

[<span data-ttu-id="60ac6-119">升級範例</span><span class="sxs-lookup"><span data-stu-id="60ac6-119">An Upgrade Example</span></span>](an-upgrade-example.md)

 

 



