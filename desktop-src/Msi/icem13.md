---
description: ICEM13 會確認合併模組不包含發行者原則和設定元件。
ms.assetid: 1281ee21-a154-4275-a9e6-6e92fff548ed
title: ICEM13
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3286906cf162f24dce7105835544c3a387993ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848934"
---
# <a name="icem13"></a><span data-ttu-id="0629f-103">ICEM13</span><span class="sxs-lookup"><span data-stu-id="0629f-103">ICEM13</span></span>

<span data-ttu-id="0629f-104">ICEM13 會確認合併模組不包含發行者原則和設定元件。</span><span class="sxs-lookup"><span data-stu-id="0629f-104">ICEM13 verifies that the merge module does not contain publisher policy and configuration assemblies.</span></span> <span data-ttu-id="0629f-105">發行者原則和設定元件不應該包含在要用於轉散發的合併模組中，因為這可能會影響使用者電腦上的其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="0629f-105">Publisher policy and configuration assemblies should not be included in merge modules intended for redistribution because this can affect other applications on a user's computer.</span></span>

<span data-ttu-id="0629f-106">此 ICEM 可在 Windows Installer 2.0 SDK 和更新版本提供的 Mergemod 檔中找到。</span><span class="sxs-lookup"><span data-stu-id="0629f-106">This ICEM is available in the Mergemod.cub file provided in the Windows Installer 2.0 SDK and later.</span></span> <span data-ttu-id="0629f-107">如需詳細資訊，請參閱 [Windows Installer 開發人員 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)。</span><span class="sxs-lookup"><span data-stu-id="0629f-107">For details, see [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

## <a name="result"></a><span data-ttu-id="0629f-108">結果</span><span class="sxs-lookup"><span data-stu-id="0629f-108">Result</span></span>

<span data-ttu-id="0629f-109">如果 ICEM13 在合併模組的 [MsiAssembly 資料表](msiassembly-table.md) （屬於發行者原則或設定元件）的 [元件] 欄位中找到指定的元件，則會張貼一則警告訊息。</span><span class="sxs-lookup"><span data-stu-id="0629f-109">ICEM13 posts a warning message if it finds a component specified in the Component field of the merge module's [MsiAssembly Table](msiassembly-table.md) that is a publisher policy or configuration assembly.</span></span>

## <a name="example"></a><span data-ttu-id="0629f-110">範例</span><span class="sxs-lookup"><span data-stu-id="0629f-110">Example</span></span>

<span data-ttu-id="0629f-111">ICEM13 會在 [MsiAssembly 資料表](msiassembly-table.md) 中找到具有元件 ' 1 ' 的資料列，而該資料表中的元件 \[ \] 欄位是已包含在合併模組中的發行者原則或設定元件，以張貼下列警告訊息。</span><span class="sxs-lookup"><span data-stu-id="0629f-111">ICEM13 posts the following warning message if it finds a row in the [MsiAssembly Table](msiassembly-table.md) with a component '\[1\]' specified in the Component field that is a publisher policy or configuration assembly that has been included in the merge module.</span></span>

``` syntax
This entry Component_=`[1]` in MsiAssembly Table is a Policy/Configuration Assembly. A Publisher Policy/Configuration assembly should not be redistributed with a merge module. Policy/Configuration may impact other applications and should only be installed with products.
```

<span data-ttu-id="0629f-112">您可以使用 Windows Installer 安裝發行者原則和設定元件，不建議在合併模組中重新分配這些元件。</span><span class="sxs-lookup"><span data-stu-id="0629f-112">It is possible to install publisher policy and configuration assemblies using the Windows Installer, it is not recommended that these assemblies be redistributed in merge modules.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0629f-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="0629f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0629f-114">Merge Module ICE 參考</span><span class="sxs-lookup"><span data-stu-id="0629f-114">Merge Module ICE Reference</span></span>](merge-module-ice-reference.md)
</dt> </dl>

 

 



