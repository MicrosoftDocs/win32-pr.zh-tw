---
description: 如果每個使用者的系統原則設定為 &\# 0034; 1&\# 0034;; 安裝程式會在產品的來源清單中，于任何網路來源的根目錄中搜尋轉換檔案。 根據預設，轉換會儲存在使用者設定檔的 Application Data 資料夾中。
ms.assetid: 24881078-1610-4a37-a52d-fcabd78e1738
title: TransformsAtSource 原則
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91be9c56f2e68a27d904acf98088204dc4012b4f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111992"
---
# <a name="transformsatsource-policy"></a><span data-ttu-id="23914-104">TransformsAtSource 原則</span><span class="sxs-lookup"><span data-stu-id="23914-104">TransformsAtSource Policy</span></span>

<span data-ttu-id="23914-105">如果每個使用者的 [系統原則](system-policy.md) 設定為 "1";安裝程式會在產品的來源清單中，于任何網路來源的根目錄中搜尋轉換檔案。</span><span class="sxs-lookup"><span data-stu-id="23914-105">If this per-user [system policy](system-policy.md) is set to "1"; the installer searches for transform files in the root of any network sources in the source list for the product.</span></span> <span data-ttu-id="23914-106">根據預設，轉換會儲存在使用者設定檔的 Application Data 資料夾中。</span><span class="sxs-lookup"><span data-stu-id="23914-106">By default, transforms are stored in the Application Data folder of a user's profile.</span></span>

<span data-ttu-id="23914-107">Windows Installer 會將 TransformsAtSource 原則解釋為與 [TransformsSecure 原則](transformssecure-policy.md)相同的原則。</span><span class="sxs-lookup"><span data-stu-id="23914-107">Windows Installer interprets the TransformsAtSource policy to be the same as the [TransformsSecure policy](transformssecure-policy.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="23914-108">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="23914-108">Registry Key</span></span>

<span data-ttu-id="23914-109">**HKEY \_目前的 \_ 使用者** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="23914-109">**HKEY\_CURRENT\_USER**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="23914-110">資料類型</span><span class="sxs-lookup"><span data-stu-id="23914-110">Data Type</span></span>

<span data-ttu-id="23914-111">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="23914-111">**REG\_SZ**</span></span>

 

 



