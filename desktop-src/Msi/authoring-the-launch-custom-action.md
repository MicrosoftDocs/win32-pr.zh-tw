---
description: 名為啟動的範例自訂動作的原始程式碼（符合範例規格）是由 Windows Installer SDK 提供，以做為檔案教學課程 .cpp。
ms.assetid: 6f6d45b0-759d-4d28-a542-5cdbb589448f
title: 撰寫啟動自訂動作
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4805b20b2250351927100ad978d8791e7acf045f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944003"
---
# <a name="authoring-the-launch-custom-action"></a><span data-ttu-id="97430-103">撰寫啟動自訂動作</span><span class="sxs-lookup"><span data-stu-id="97430-103">Authoring the Launch Custom Action</span></span>

<span data-ttu-id="97430-104">名為啟動的範例自訂動作的原始程式碼（符合範例規格）是由 Windows Installer SDK 提供，以做為檔案教學課程 .cpp。</span><span class="sxs-lookup"><span data-stu-id="97430-104">The source code for a sample custom action named Launch, which meets the sample specifications, is provided by the Windows Installer SDK as the file Tutorial.cpp.</span></span> <span data-ttu-id="97430-105">此自訂動作會使用 [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) 將包含屬性的字串格式化。</span><span class="sxs-lookup"><span data-stu-id="97430-105">This custom action makes use of [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) to format a string containing properties.</span></span> <span data-ttu-id="97430-106">屬性 \[ \# FileKey 會 \] 解析為 HTML 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="97430-106">The property \[\#FileKey\] resolves to the full path of the HTML file.</span></span> <span data-ttu-id="97430-107">使用來源檔案建立 Tutorial.dll 的檔案。</span><span class="sxs-lookup"><span data-stu-id="97430-107">Use the source file to create the file Tutorial.dll.</span></span> <span data-ttu-id="97430-108">此 DLL 的進入點為 LaunchTutorial。</span><span class="sxs-lookup"><span data-stu-id="97430-108">The entry point to this DLL is LaunchTutorial.</span></span>

<span data-ttu-id="97430-109">範例自訂動作啟動會呼叫以 c + + 撰寫的 DLL，並從暫存二進位資料流程產生。</span><span class="sxs-lookup"><span data-stu-id="97430-109">The sample custom action Launch calls a DLL written in C++ and is generated from a temporary binary stream.</span></span> <span data-ttu-id="97430-110">此類型的自訂動作包括基底類型常數 msidbCustomActionTypeDll 和 msidbCustomActionTypeBinaryData，其提供等於1的基底數數值型別。</span><span class="sxs-lookup"><span data-stu-id="97430-110">Custom actions of this type include the base type constants msidbCustomActionTypeDll and msidbCustomActionTypeBinaryData, which give a base numeric type equal to 1.</span></span> <span data-ttu-id="97430-111">請參閱 [自訂動作類型 1](custom-action-type-1.md)。</span><span class="sxs-lookup"><span data-stu-id="97430-111">See [Custom Action Type 1](custom-action-type-1.md).</span></span> <span data-ttu-id="97430-112">因為規格需要在自訂動作失敗時繼續安裝，所以啟動也會包含選用的常數 **msidbCustomActionTypeContinue**，也就是64。</span><span class="sxs-lookup"><span data-stu-id="97430-112">Because the specifications require that the installation continue if the custom action fails, Launch also includes the optional constant **msidbCustomActionTypeContinue**, which is 64.</span></span> <span data-ttu-id="97430-113">請參閱 [自訂動作傳回處理選項](custom-action-return-processing-options.md)。</span><span class="sxs-lookup"><span data-stu-id="97430-113">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span> <span data-ttu-id="97430-114">啟動的總數字類型為65。</span><span class="sxs-lookup"><span data-stu-id="97430-114">The total numeric type of Launch is 65.</span></span>

<span data-ttu-id="97430-115">繼續將 [啟動新增至 CustomAction 和二進位資料表](adding-launch-to-the-customaction-and-binary-tables.md)。</span><span class="sxs-lookup"><span data-stu-id="97430-115">Continue to [Adding Launch to the CustomAction and Binary Tables](adding-launch-to-the-customaction-and-binary-tables.md).</span></span>

 

 



