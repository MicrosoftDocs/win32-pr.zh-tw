---
description: Windows Installer 支援廣告應用程式和功能。
ms.assetid: 9e5158bc-4877-49d1-9bb9-4dd17abb444d
title: 廣告的平臺支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48016241998473a5bb5ae8ecff05a14fd702f8be
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106975605"
---
# <a name="platform-support-of-advertisement"></a><span data-ttu-id="7bc82-103">廣告的平臺支援</span><span class="sxs-lookup"><span data-stu-id="7bc82-103">Platform Support of Advertisement</span></span>

<span data-ttu-id="7bc82-104">Windows Installer 支援廣告應用程式和功能。</span><span class="sxs-lookup"><span data-stu-id="7bc82-104">The Windows Installer supports advertisement of applications and features.</span></span>

<span data-ttu-id="7bc82-105">下列公告功能可在 Windows Server 2008 R2、Windows 7、Windows Server 2008、Windows Vista、Windows Server 2003、Windows XP 及 Windows 2000 上取得。</span><span class="sxs-lookup"><span data-stu-id="7bc82-105">The following advertisement capabilities are available on Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003, Windows XP, and Windows 2000.</span></span>

-   <span data-ttu-id="7bc82-106">快速鍵及其圖示。</span><span class="sxs-lookup"><span data-stu-id="7bc82-106">Shortcuts and their icons.</span></span>

-   <span data-ttu-id="7bc82-107">[ProgId 資料表](progid-table.md)中指定的延伸模組及其圖示。</span><span class="sxs-lookup"><span data-stu-id="7bc82-107">Extensions and their icons specified in the [ProgId Table](progid-table.md).</span></span>

-   <span data-ttu-id="7bc82-108">在 ProgId 索引鍵下註冊的 Shell 和命令動詞。</span><span class="sxs-lookup"><span data-stu-id="7bc82-108">Shell and command Verbs registered underneath the ProgId key.</span></span>

-   <span data-ttu-id="7bc82-109">CLSID 內容和 InProcHandler。</span><span class="sxs-lookup"><span data-stu-id="7bc82-109">CLSID contexts and InProcHandler.</span></span>

-   <span data-ttu-id="7bc82-110">透過 OLE 的隨選安裝僅可透過 [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) 以程式設計方式透過 CoCreateInstance (C/c + +) ，而 CreateObject 函式 **(Visual Basic)** 或 **GetObject 函數 (Visual Basic)**。</span><span class="sxs-lookup"><span data-stu-id="7bc82-110">Install-On-Demand through OLE is only available programmatically through [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) (C/C++), and **CreateObject Function (Visual Basic)** or **GetObject Function (Visual Basic)**.</span></span>

> [!Note]
> <span data-ttu-id="7bc82-111">只有在安裝公告的元件時，才會寫入 AppId 和 Typelib 資訊。</span><span class="sxs-lookup"><span data-stu-id="7bc82-111">AppId and Typelib information is only written when an advertised component is installed.</span></span>
> 
> <span data-ttu-id="7bc82-112">若要支援副檔名，必須將應用程式發佈至使用群組原則的系統管理員 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="7bc82-112">To support file name extensions, the application must be published to Active Directory by an administrator using Group Policy.</span></span>

## <a name="remarks"></a><span data-ttu-id="7bc82-113">備註</span><span class="sxs-lookup"><span data-stu-id="7bc82-113">Remarks</span></span>

<span data-ttu-id="7bc82-114">產品的安裝可能不需要重新開機，但是在重新開機電腦之前，任何通告的快捷方式都無法運作。</span><span class="sxs-lookup"><span data-stu-id="7bc82-114">The installation of the product may not require a restart, but any advertised shortcuts do not work until the machine is restarted.</span></span> <span data-ttu-id="7bc82-115">後續安裝的已公告快捷方式不需要重新開機即可運作。</span><span class="sxs-lookup"><span data-stu-id="7bc82-115">The advertised shortcuts of subsequent installations work without a restart.</span></span>

<span data-ttu-id="7bc82-116">為了確保通告的快捷方式正確運作，套件作者應該在安裝結束時排程強制重新開機。</span><span class="sxs-lookup"><span data-stu-id="7bc82-116">To ensure that advertised shortcuts work correctly, the package author should schedule a forced restart at the end of the installation.</span></span>

<span data-ttu-id="7bc82-117">若要避免系統不必要的重新開機，請將重新開機排程為只有在未安裝任何版本的 Windows Installer 時才執行。</span><span class="sxs-lookup"><span data-stu-id="7bc82-117">To avoid unnecessary restarts of the system, schedule a restart to run only if no version of the Windows Installer is installed.</span></span>

<span data-ttu-id="7bc82-118">條件陳述式可以檢查 [**ShellAdvtSupport**](shelladvtsupport.md) 屬性和 [**Version9X**](version9x.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="7bc82-118">Conditional statements can check the [**ShellAdvtSupport**](shelladvtsupport.md) property and [**Version9X**](version9x.md) property.</span></span> <span data-ttu-id="7bc82-119">如需排程條件式強制重新開機的詳細資訊，請參閱 [系統重新開機](system-reboots.md) 和 [在條件陳述式中使用屬性](using-properties-in-conditional-statements.md)。</span><span class="sxs-lookup"><span data-stu-id="7bc82-119">For more information about scheduling a conditional forced restarts, see [System Reboots](system-reboots.md) and [Using Properties in Conditional Statements](using-properties-in-conditional-statements.md).</span></span>

 

 
