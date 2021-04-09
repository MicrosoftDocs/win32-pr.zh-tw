---
description: HKLM \\ Software \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}。
ms.assetid: a0d9e959-d8fd-4546-9529-1dc42fa0bdd6
title: Exec
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2711b2c8882f9af12de2f060810ccd4219faa5ec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689056"
---
# <a name="exec"></a><span data-ttu-id="5f19c-103">Exec</span><span class="sxs-lookup"><span data-stu-id="5f19c-103">Exec</span></span>

<span data-ttu-id="5f19c-104">**HKLM \\ Software \\ Microsoft \\ Internet Explorer \\ Extensions \\ {e2e2dd38-d088-4134-82b7-f2ba38496583}**</span><span class="sxs-lookup"><span data-stu-id="5f19c-104">**HKLM\\Software\\Microsoft\\Internet Explorer\\Extensions\\{e2e2dd38-d088-4134-82b7-f2ba38496583}**</span></span>



| <span data-ttu-id="5f19c-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="5f19c-105">Data type</span></span> | <span data-ttu-id="5f19c-106">範圍</span><span class="sxs-lookup"><span data-stu-id="5f19c-106">Range</span></span>                    | <span data-ttu-id="5f19c-107">預設值</span><span class="sxs-lookup"><span data-stu-id="5f19c-107">Default value</span></span> |
|-----------|--------------------------|---------------|
| <span data-ttu-id="5f19c-108">REG \_ SZ</span><span class="sxs-lookup"><span data-stu-id="5f19c-108">REG\_SZ</span></span>   | <span data-ttu-id="5f19c-109">*可執行檔的路徑*</span><span class="sxs-lookup"><span data-stu-id="5f19c-109">*Path to the executable*</span></span> |               |



 

## <a name="browser-integration-steps"></a><span data-ttu-id="5f19c-110">瀏覽器整合步驟</span><span class="sxs-lookup"><span data-stu-id="5f19c-110">Browser Integration Steps</span></span>

1.  <span data-ttu-id="5f19c-111">使用 [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) 函數來判斷是否已安裝網路診斷。</span><span class="sxs-lookup"><span data-stu-id="5f19c-111">Use the [**RegOpenKeyEx**](/windows/win32/api/winreg/nf-winreg-regopenkeyexa) function to determine whether the Network Diagnostic is installed.</span></span> <span data-ttu-id="5f19c-112">如果已安裝，則會出現 **{e2e2dd38-d088-4134-82b7-f2ba38496583}** 機碼。</span><span class="sxs-lookup"><span data-stu-id="5f19c-112">If it is installed, the **{e2e2dd38-d088-4134-82b7-f2ba38496583}** key is present.</span></span>
2.  <span data-ttu-id="5f19c-113">您可以使用 [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) 函式，從 **Exec** 專案取出網路診斷可執行檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="5f19c-113">Use the [**RegQueryValueEx**](/windows/win32/api/winreg/nf-winreg-regqueryvalueexa) function to retrieve the path of the Network Diagnostic executable file from the **Exec** entry.</span></span>
3.  <span data-ttu-id="5f19c-114">如果系統上已安裝診斷，則會顯示新的錯誤頁面。</span><span class="sxs-lookup"><span data-stu-id="5f19c-114">Display the new error page if the diagnostic is installed on the system.</span></span>
4.  <span data-ttu-id="5f19c-115">建立瀏覽器延伸模組，以建立標準工具列專案（如果系統上已安裝診斷）。</span><span class="sxs-lookup"><span data-stu-id="5f19c-115">Create a browser extension that creates a standard toolbar item if the diagnostic is installed on the system.</span></span>
5.  <span data-ttu-id="5f19c-116">使用步驟2中取出的路徑執行網路診斷可執行檔。</span><span class="sxs-lookup"><span data-stu-id="5f19c-116">Execute the Network Diagnostic executable using the path retrieved in step 2.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5f19c-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="5f19c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5f19c-118">網路診斷工具功能總覽</span><span class="sxs-lookup"><span data-stu-id="5f19c-118">Network Diagnostics Tools Feature Overview</span></span>](https://www.microsoft.com/technet/prodtechnol/winxppro/maintain/netdiag.mspx)
</dt> </dl>

 

 
