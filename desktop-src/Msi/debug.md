---
description: 如果每一電腦的系統原則設定為 &\# 0034; 1&\# 0034;，則安裝程式會使用 OutputDebugString 函式，將一般的偵錯工具訊息寫入偵錯工具。
ms.assetid: 0a9416ca-0535-4595-a4f3-b3ef7c2d3a13
title: 偵錯
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2615b12bb76f4c4da0677bbeb459fa549f8233e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850247"
---
# <a name="debug"></a><span data-ttu-id="a83fa-103">偵錯</span><span class="sxs-lookup"><span data-stu-id="a83fa-103">Debug</span></span>

<span data-ttu-id="a83fa-104">如果每一電腦的 [系統原則](system-policy.md) 設定為 "1"，則安裝程式會使用 [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) 函式，將一般的偵錯工具訊息寫入至偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="a83fa-104">If this per-machine [system policy](system-policy.md) is set to "1", the installer writes common debugging messages to the debugger using the [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) function.</span></span> <span data-ttu-id="a83fa-105">如果這個值設定為 "2"，則安裝程式會使用 [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) 函式，將所有有效的偵錯工具訊息寫入至偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="a83fa-105">If this value is set to "2", the installer writes all valid debugging messages to the debugger using the [**OutputDebugString**](/windows/desktop/api/debugapi/nf-debugapi-outputdebugstringw) function.</span></span> <span data-ttu-id="a83fa-106">這項原則僅供偵測之用，在未來的 Windows Installer 版本中可能不受支援。</span><span class="sxs-lookup"><span data-stu-id="a83fa-106">This policy is for debugging purposes only and may not be supported in future versions of Windows Installer.</span></span>

<span data-ttu-id="a83fa-107">如果第三個 (0x04) 位是在 Debug 原則的值中設定，Windows Installer 只會將命令列寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="a83fa-107">Windows Installer only writes command lines into the log file if the third (0x04) bit is set in the value of the Debug policy.</span></span> <span data-ttu-id="a83fa-108">因此，若要在記錄檔中顯示命令列，請將 [偵錯工具原則] 值設為 [7]。</span><span class="sxs-lookup"><span data-stu-id="a83fa-108">Therefore, to display command lines in the log, set the Debug policy value to 7.</span></span> <span data-ttu-id="a83fa-109">這不會顯示與具有[密碼控制屬性](password-control-attribute.md)之[編輯控制項](edit-control.md)相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="a83fa-109">This does not display properties associated with an [Edit Control](edit-control.md) having the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="a83fa-110">這會讓命令列上所設定的屬性，即使屬性包含在 [**MsiHiddenProperties**](msihiddenproperties.md) 屬性中也一樣。</span><span class="sxs-lookup"><span data-stu-id="a83fa-110">This will make properties set on the command line visible in the log even if the property is included in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span> <span data-ttu-id="a83fa-111">如需詳細資訊，請參閱 [防止機密資訊寫入至記錄](preventing-confidential-information-from-being-written-into-the-log-file.md)檔。</span><span class="sxs-lookup"><span data-stu-id="a83fa-111">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="a83fa-112">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="a83fa-112">Registry Key</span></span>

<span data-ttu-id="a83fa-113">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="a83fa-113">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="a83fa-114">資料類型</span><span class="sxs-lookup"><span data-stu-id="a83fa-114">Data Type</span></span>

<span data-ttu-id="a83fa-115">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="a83fa-115">**REG\_DWORD**</span></span>

 

 
