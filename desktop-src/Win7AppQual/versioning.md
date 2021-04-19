---
description: .
ms.assetid: d1014801-a93a-40e8-ae96-31784c192753
title: Windows 7 和 Windows Server 2008 R2 應用程式品質操作手冊)  (版本控制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2da50dae53fd2309f1a5de10996c57a2b4ac29c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971667"
---
# <a name="versioning-windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="2f1b5-103">Windows 7 和 Windows Server 2008 R2 應用程式品質操作手冊)  (版本控制</span><span class="sxs-lookup"><span data-stu-id="2f1b5-103">Versioning (Windows 7 and Windows Server 2008 R2 Application Quality Cookbook)</span></span>

<span data-ttu-id="2f1b5-104">Windows Internet Explorer 最常見的應用程式相容性問題之一，就是使用者代理程式 (UA) 字串和版本向量。</span><span class="sxs-lookup"><span data-stu-id="2f1b5-104">One of the most common application compatibility issues for Windows Internet Explorer is User Agent (UA) Strings and Version Vectors.</span></span> <span data-ttu-id="2f1b5-105">Windows Internet Explorer 8 引進了新的 UA 字串，可協助應用程式偵測使用者正在執行的版本。</span><span class="sxs-lookup"><span data-stu-id="2f1b5-105">Windows Internet Explorer 8 introduces a new UA String to help applications detect which version that users are running.</span></span> <span data-ttu-id="2f1b5-106">除了只增加與 UA 字串中 Internet Explorer 相關聯的 MSIE 值，Internet Explorer 8 還新增了 Trident/4.0 值，以協助您偵測 Internet Explorer 8 是否在相容性檢視模式中執行。</span><span class="sxs-lookup"><span data-stu-id="2f1b5-106">In addition to simply increasing the MSIE value that is associated with Internet Explorer in the UA String, Internet Explorer 8 adds a Trident/4.0 value to help you detect if Internet Explorer 8 is running in Compatibility View mode.</span></span> <span data-ttu-id="2f1b5-107">這些變更，加上硬式編碼版本檢查，可能會導致瀏覽器之間的相容性問題。</span><span class="sxs-lookup"><span data-stu-id="2f1b5-107">These changes, plus hardcoded version checks, can potentially introduce compatibility issues between browsers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f1b5-108">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f1b5-108">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f1b5-109">設計影響瀏覽器相容性的更新</span><span class="sxs-lookup"><span data-stu-id="2f1b5-109">Design Updates that Impact Compatibility between Browsers</span></span>](design-updates-that-impact-compatibility-between-browsers.md)
</dt> </dl>

 

 



