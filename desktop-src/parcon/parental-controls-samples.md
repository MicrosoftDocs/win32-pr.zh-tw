---
description: 家長監護範例
ms.assetid: 19dac95c-2279-4bf9-a58c-dd30177c0c9d
title: 家長監護範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26962f4edd16e1e860883607316d5a7cbf3d9122
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988360"
---
# <a name="parental-controls-samples"></a><span data-ttu-id="eab22-103">家長監護範例</span><span class="sxs-lookup"><span data-stu-id="eab22-103">Parental Controls Samples</span></span>

<span data-ttu-id="eab22-104">家長監護的範例程式碼可在 [路徑 <installation directory> \\ Windows \\ <version number> \\ 範例 \\ 安全性 \\ ParentalControls] 底下取得。</span><span class="sxs-lookup"><span data-stu-id="eab22-104">Sample code for Parental Controls is available under path <installation directory>\\Windows\\<version number>\\Samples\\Security\\ParentalControls.</span></span> <span data-ttu-id="eab22-105">範例如下所示：</span><span class="sxs-lookup"><span data-stu-id="eab22-105">The samples are as follows:</span></span>

## <a name="utilities"></a><span data-ttu-id="eab22-106">公用程式</span><span class="sxs-lookup"><span data-stu-id="eab22-106">Utilities</span></span>

<span data-ttu-id="eab22-107">適用于基本 COM 管理、SID 字串作業，以及 WMI 讀取和寫入功能的 Helper 功能。</span><span class="sxs-lookup"><span data-stu-id="eab22-107">Helper functionality for basic COM management, SID string operations, and WMI read and write functionality.</span></span> <span data-ttu-id="eab22-108">除非另有指定，否則所有其他範例都會相依于這個專案。</span><span class="sxs-lookup"><span data-stu-id="eab22-108">All of the other samples depend on this project unless otherwise specified.</span></span>

## <a name="complianceapi"></a><span data-ttu-id="eab22-109">ComplianceAPI</span><span class="sxs-lookup"><span data-stu-id="eab22-109">ComplianceAPI</span></span>

<span data-ttu-id="eab22-110">命令列導向的主控台應用程式，示範如何使用合規性 API 來取得使用者的主要設定子集。</span><span class="sxs-lookup"><span data-stu-id="eab22-110">Command-line driven console application demonstrating how to use the Compliance API to retrieve a key subset of settings for a user.</span></span>

## <a name="complianceapp"></a><span data-ttu-id="eab22-111">ComplianceApp</span><span class="sxs-lookup"><span data-stu-id="eab22-111">ComplianceApp</span></span>

<span data-ttu-id="eab22-112">簡單的主控台應用程式，示範如何使用合規性 API 來檢查所需的記錄和特定的限制。</span><span class="sxs-lookup"><span data-stu-id="eab22-112">Simple console application demonstrating use of the Compliance API to check for logging required and specific restrictions.</span></span> <span data-ttu-id="eab22-113">如果啟用時間限制，應用程式也會等待即將進行的登出事件。</span><span class="sxs-lookup"><span data-stu-id="eab22-113">If time restrictions are enabled, the application also waits for the impending logout events.</span></span>

## <a name="uiextensibility"></a><span data-ttu-id="eab22-114">UIExtensibility</span><span class="sxs-lookup"><span data-stu-id="eab22-114">UIExtensibility</span></span>

<span data-ttu-id="eab22-115">命令列導向的主控台應用程式，示範如何使用 WMI Api 和 WPC 架構來列出、查詢、新增、修改和刪除 UI 擴充性連結專案。</span><span class="sxs-lookup"><span data-stu-id="eab22-115">Command-line driven console application demonstrating use of the WMI APIs and WPC schema to list, query, add, modify, and delete UI Extensibility link entries.</span></span>

<span data-ttu-id="eab22-116">範例命令列範例：</span><span class="sxs-lookup"><span data-stu-id="eab22-116">Example command line for sample:</span></span>

<span data-ttu-id="eab22-117">"D： \\ WPC \\ Samples \\ Security \\ ParentalControls \\ UIExtensibility \\ debug \\ UIExtensibility" add/g： {FD59BB7F-54AB-11DB-9666-00E08161165F}/c： 0/N： D：/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll，-101/S： D：/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll，-103/I： D：/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll，-104/D： D：/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll，-106/e： c： \\ windows \\Notepad.exe</span><span class="sxs-lookup"><span data-stu-id="eab22-117">"D:\\WPC\\Samples\\Security\\ParentalControls\\UIExtensibility\\debug\\UIExtensibility" add /g:{FD59BB7F-54AB-11DB-9666-00E08161165F} /c:0 /n:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-101 /s:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-103 /i:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-104 /d:D:/WPC/Samples/Security/ParentalControls/UiExtRC/debug/UiExtRC.dll,-106 /e:c:\\windows\\Notepad.exe</span></span>

<span data-ttu-id="eab22-118">其中 UiExtRC 是簡單的資源 DLL，其中包含識別碼為101和103的字串資源，而24x24 圖元32位具有適用于資源104和106的 Alpha 點陣圖。</span><span class="sxs-lookup"><span data-stu-id="eab22-118">where UiExtRC is a simple resource DLL with string resources for ID's 101 and 103, and 24x24 pixel 32-bit with alpha bitmaps for resources 104 and 106.</span></span>

## <a name="webextensibility"></a><span data-ttu-id="eab22-119">WebExtensibility</span><span class="sxs-lookup"><span data-stu-id="eab22-119">WebExtensibility</span></span>

<span data-ttu-id="eab22-120">命令列導向的主控台應用程式，示範如何使用 WMI Api 和 WPC 架構來列出、新增和刪除 HTTP 應用程式或 URL 豁免專案，以及使用 FilterID 和 FilterName 屬性來設定和重設 Web 內容篩選覆寫。</span><span class="sxs-lookup"><span data-stu-id="eab22-120">Command-line driven console application demonstrating how to use the WMI APIs and WPC schema to list, add, and delete HTTP application or URL exemption entries, and to set and reset a Web Content Filter override with the FilterID and FilterName properties.</span></span>

<span data-ttu-id="eab22-121">不會顯示唯讀 HTTP 應用程式和 URL 豁免清單的存取權，但讀取清單的程式碼與讀取/寫入案例的程式碼相同，除了 WMI 參數的修改之外。</span><span class="sxs-lookup"><span data-stu-id="eab22-121">Access to the read-only HTTP application and URL exemption lists is not shown, but the code to read the lists would be the same as for the read/write case except for modification of the WMI parameter.</span></span>

 

 



