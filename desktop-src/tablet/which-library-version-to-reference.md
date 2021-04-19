---
description: 本主題說明 Tablet PC library 二進位版本之間的差異。
ms.assetid: 708567b8-33bd-43cd-b56f-8ee9c96fb315
title: 要參考的程式庫版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19f2092cc762a047ac5f0c2408a87f761fc584a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970982"
---
# <a name="which-library-version-to-reference"></a><span data-ttu-id="7d379-103">要參考的程式庫版本</span><span class="sxs-lookup"><span data-stu-id="7d379-103">Which Library Version to Reference</span></span>

<span data-ttu-id="7d379-104">本主題說明 Tablet PC library 二進位版本之間的差異。</span><span class="sxs-lookup"><span data-stu-id="7d379-104">This topic describes the differences between the Tablet PC library binary versions.</span></span>

## <a name="tablet-pc-library-versions"></a><span data-ttu-id="7d379-105">Tablet PC Library 版本</span><span class="sxs-lookup"><span data-stu-id="7d379-105">Tablet PC Library Versions</span></span>

<span data-ttu-id="7d379-106">Windows Vista 已更新 Tablet PC library 二進位檔 (Microsoft.Ink.dll) 。</span><span class="sxs-lookup"><span data-stu-id="7d379-106">The Tablet PC library binaries (Microsoft.Ink.dll) have been updated in Windows Vista.</span></span> <span data-ttu-id="7d379-107">這些二進位檔稱為 "version 6.0"，與發行的 Windows 版本共同 incide。</span><span class="sxs-lookup"><span data-stu-id="7d379-107">Theses binaries are referred to as "version 6.0" to co-incide with the version of Windows in which they are being released.</span></span>

<span data-ttu-id="7d379-108">最新版本的二進位檔與 Windows XP 相容，稱為「版本1.7」。</span><span class="sxs-lookup"><span data-stu-id="7d379-108">The most recent release of the binaries that are compatible with Windows XP is referred to as "version 1.7".</span></span>

<span data-ttu-id="7d379-109">Windows SDK 可以安裝在 Vista 和 XP 電腦上，而 Windows SDK 包含兩種 Microsoft.Ink.dll 版本。</span><span class="sxs-lookup"><span data-stu-id="7d379-109">The Windows SDK can be installed on both Vista and XP machines, and the Windows SDK includes both versions of Microsoft.Ink.dll.</span></span>

<span data-ttu-id="7d379-110">這些都安裝在：</span><span class="sxs-lookup"><span data-stu-id="7d379-110">These are installed in:</span></span>

1. <span data-ttu-id="7d379-111">% programfiles% \\ 參考元件 \\ MICROSOFT \\ Tablet PC \\ 1.7 版 \\Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="7d379-111">%programfiles%\\Reference Assemblies\\Microsoft\\Tablet PC\\v1.7\\Microsoft.Ink.dll</span></span>

2. <span data-ttu-id="7d379-112">% programfiles% \\ 參考元件 \\ MICROSOFT \\ Tablet PC \\ 6.0 6.0 \\Microsoft.Ink.dll</span><span class="sxs-lookup"><span data-stu-id="7d379-112">%programfiles%\\Reference Assemblies\\Microsoft\\Tablet PC\\v6.0\\Microsoft.Ink.dll</span></span>

<span data-ttu-id="7d379-113">版本6.0 二進位檔只與 Windows Vista 相容，而針對它們撰寫的應用程式應該只在 Windows Vista 上執行。</span><span class="sxs-lookup"><span data-stu-id="7d379-113">The version 6.0 binaries are only compatible with Windows Vista, and applications written against them should only ever be run on Windows Vista.</span></span>

<span data-ttu-id="7d379-114">在 Windows Vista 上安裝時，不需修改就能執行針對1.7 版二進位檔所撰寫的應用程式。</span><span class="sxs-lookup"><span data-stu-id="7d379-114">An application written against the version 1.7 binaries should run without modification when installed on Windows Vista.</span></span>

 

 



