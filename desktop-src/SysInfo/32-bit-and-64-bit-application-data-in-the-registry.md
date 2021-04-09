---
description: 在64位的 Windows 上，會針對32位應用程式和64位應用程式分別儲存部分的登錄專案，並使用登錄重新導向程式和登錄反映來對應到個別的邏輯登錄區，因為應用程式的64位版本可能會使用不同的登錄機碼和值，而不是使用32位版本。 也有共用的登錄機碼不會重新導向或反映。
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: 登錄中的32位和64位應用程式資料
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc82dfbf9b22cf90866e13109aeea2bcdb10e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103849430"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a><span data-ttu-id="e3689-104">登錄中的32位和64位應用程式資料</span><span class="sxs-lookup"><span data-stu-id="e3689-104">32-bit and 64-bit Application Data in the Registry</span></span>

<span data-ttu-id="e3689-105">在64位的 Windows 上，會針對32位應用程式和64位應用程式分別儲存部分的登錄專案，並使用登錄 [重定向](/windows/desktop/WinProg64/registry-redirector) 程式和登錄 [反映](/windows/desktop/WinProg64/registry-reflection)來對應到個別的邏輯登錄區，因為應用程式的64位版本可能會使用不同的登錄機碼和值，而不是使用32位版本。</span><span class="sxs-lookup"><span data-stu-id="e3689-105">On 64-bit Windows, portions of the registry entries are stored separately for 32-bit application and 64-bit applications and mapped into separate logical registry views using the [registry redirector](/windows/desktop/WinProg64/registry-redirector) and [registry reflection](/windows/desktop/WinProg64/registry-reflection), because the 64-bit version of an application may use different registry keys and values than the 32-bit version.</span></span> <span data-ttu-id="e3689-106">也有共用的登錄機 [碼](/windows/desktop/WinProg64/shared-registry-keys) 不會重新導向或反映。</span><span class="sxs-lookup"><span data-stu-id="e3689-106">There are also [shared registry keys](/windows/desktop/WinProg64/shared-registry-keys) that are not redirected or reflected.</span></span>

<span data-ttu-id="e3689-107">每個64位登錄節點的父系都是 Image-Specific 節點。</span><span class="sxs-lookup"><span data-stu-id="e3689-107">The parent of each 64-bit registry node is the Image-Specific Node or ISN.</span></span> <span data-ttu-id="e3689-108">登錄重新導向程式會以透明的方式，將應用程式的登錄存取導向適當的節點。</span><span class="sxs-lookup"><span data-stu-id="e3689-108">The registry redirector transparently directs an application's registry access to the appropriate ISN subnode.</span></span> <span data-ttu-id="e3689-109">WOW64 元件會使用名稱 **Wow6432Node** 自動建立登錄樹狀結構中的重新導向子節點。</span><span class="sxs-lookup"><span data-stu-id="e3689-109">Redirection subnodes in the registry tree are created automatically by the WOW64 component using the name **Wow6432Node**.</span></span> <span data-ttu-id="e3689-110">因此，不需要為您建立的任何登錄機碼命名 **Wow6432Node**。</span><span class="sxs-lookup"><span data-stu-id="e3689-110">As a result, it is essential not to name any registry key you create **Wow6432Node**.</span></span>

<span data-ttu-id="e3689-111">KEY \_ wow64 \_ 64KEY 和 key \_ wow64 \_ 32KEY 旗標分別啟用對64位登錄視圖和32位視圖的明確存取權。</span><span class="sxs-lookup"><span data-stu-id="e3689-111">The KEY\_WOW64\_64KEY and KEY\_WOW64\_32KEY flags enable explicit access to the 64-bit registry view and the 32-bit view, respectively.</span></span> <span data-ttu-id="e3689-112">如需詳細資訊，請參閱 [存取替代登錄視圖](/windows/desktop/WinProg64/accessing-an-alternate-registry-view)。</span><span class="sxs-lookup"><span data-stu-id="e3689-112">For more information, see [Accessing an Alternate Registry View](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).</span></span>

<span data-ttu-id="e3689-113">若要停用並啟用特定索引鍵的登錄反映，請使用 [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) 和 [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) 函數。</span><span class="sxs-lookup"><span data-stu-id="e3689-113">To disable and enable registry reflection for a particular key, use the [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) and [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) functions.</span></span> <span data-ttu-id="e3689-114">應用程式應該只針對其所建立的登錄機碼停用反映，而不會嘗試停用預先定義之索引鍵的反映，例如 **HKEY \_ 本機 \_ 電腦** 或 **HKEY \_ 目前的 \_ 使用者**。</span><span class="sxs-lookup"><span data-stu-id="e3689-114">Applications should disable reflection only for the registry keys that they create and not attempt to disable reflection for the predefined keys such as **HKEY\_LOCAL\_MACHINE** or **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="e3689-115">若要判斷反映清單上有哪些索引鍵，請使用 [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) 函數。</span><span class="sxs-lookup"><span data-stu-id="e3689-115">To determine which keys are on the reflection list, use the [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e3689-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3689-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3689-117">登錄重新導向程式</span><span class="sxs-lookup"><span data-stu-id="e3689-117">registry redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[<span data-ttu-id="e3689-118">登錄反映</span><span class="sxs-lookup"><span data-stu-id="e3689-118">registry reflection</span></span>](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
