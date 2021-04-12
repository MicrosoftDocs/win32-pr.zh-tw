---
description: 腳本可以存取硬體和軟體物件的所有 WMI 類別。
ms.assetid: dbb29bc8-a675-4538-99f4-00613c83eeaa
ms.tgt_platform: multiple
title: 腳本存取 WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd487c127c670f9ddee9596e44c4b2b9691ed880
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192079"
---
# <a name="scripting-access-to-wmi"></a><span data-ttu-id="1406e-103">腳本存取 WMI</span><span class="sxs-lookup"><span data-stu-id="1406e-103">Scripting Access to WMI</span></span>

<span data-ttu-id="1406e-104">腳本可以存取硬體和軟體物件的所有 WMI 類別。</span><span class="sxs-lookup"><span data-stu-id="1406e-104">Scripts can access all WMI classes for hardware and software objects.</span></span> <span data-ttu-id="1406e-105">Windows Script Host (WSH) 腳本可以對檔案系統物件執行作業、操作網路印表機，或變更環境變數。</span><span class="sxs-lookup"><span data-stu-id="1406e-105">Windows Script Host (WSH) scripts can perform operations on file system objects, manipulate network printers, or change environment variables.</span></span> <span data-ttu-id="1406e-106">您可以找到各種系統管理員工作，以及如何在 WMI 中完成 [腳本和應用程式之 wmi](wmi-tasks-for-scripts-and-applications.md)工作的簡單指引。</span><span class="sxs-lookup"><span data-stu-id="1406e-106">You can find a variety of administrator tasks and brief guidance on how to accomplish them in WMI at [WMI Tasks for Scripts and Applications](wmi-tasks-for-scripts-and-applications.md).</span></span> <span data-ttu-id="1406e-107">如需詳細資訊和範例，請參閱 TechNet ScriptCenter [腳本存放庫](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx)。</span><span class="sxs-lookup"><span data-stu-id="1406e-107">For more information and examples, see the TechNet ScriptCenter [Script Repository](https://www.microsoft.com/technet/scriptcenter/scripts/default.mspx).</span></span>

<span data-ttu-id="1406e-108">如果您不熟悉腳本或 WMI 特定腳本，請參閱 TechNet ScriptCenter 一節 [開始使用](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx)。</span><span class="sxs-lookup"><span data-stu-id="1406e-108">If you are new to scripting or to WMI-specific scripting, see the TechNet ScriptCenter section [Getting Started](https://www.microsoft.com/technet/scriptcenter/hubs/start.mspx).</span></span>

<span data-ttu-id="1406e-109">透過 [適用于 WMI 的腳本 API](scripting-api-for-wmi.md)，您可以開發快速、簡單的腳本或複雜的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1406e-109">With the [Scripting API for WMI](scripting-api-for-wmi.md), you can develop quick, simple scripts or complex applications.</span></span> <span data-ttu-id="1406e-110">腳本提供您取得資訊或在企業中設定大部分物件的相同功能，如同透過 c + + 或 c # 應用程式所做的一樣。</span><span class="sxs-lookup"><span data-stu-id="1406e-110">Scripting gives you the same capability of getting information or of configuring most objects in an enterprise as you would have through a C++ or C# application.</span></span> <span data-ttu-id="1406e-111">如需詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。</span><span class="sxs-lookup"><span data-stu-id="1406e-111">For more information, see [Scripting in WMI](/windows/desktop/WmiSdk/creating-a-wmi-script).</span></span>

<span data-ttu-id="1406e-112">您無法在腳本中寫入 [*WMI 提供者*](gloss-p.md) 。</span><span class="sxs-lookup"><span data-stu-id="1406e-112">You cannot write a [*WMI provider*](gloss-p.md) in script.</span></span> <span data-ttu-id="1406e-113">如需詳細資訊，請參閱 [將資料提供給 WMI](providing-data-to-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="1406e-113">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

<span data-ttu-id="1406e-114">您可以使用任何可與 ActiveX 物件互動的指令碼語言來撰寫 WMI 腳本。</span><span class="sxs-lookup"><span data-stu-id="1406e-114">WMI scripts can be written in any scripting language that can interact with ActiveX objects.</span></span>

<span data-ttu-id="1406e-115">Windows PowerShell 為 WMI 管理和腳本提供簡單的環境。</span><span class="sxs-lookup"><span data-stu-id="1406e-115">Windows PowerShell provides a simple environment for WMI administration and scripting.</span></span> <span data-ttu-id="1406e-116">如需 PowerShell 的詳細資訊，請參閱 [開始使用與 Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true)。</span><span class="sxs-lookup"><span data-stu-id="1406e-116">For more information about PowerShell, see [Getting Started with Windows PowerShell](/powershell/scripting/getting-started/getting-started-with-windows-powershell?view=powershell-7&preserve-view=true).</span></span>

<span data-ttu-id="1406e-117">Active Directory 服務介面 (ADSI) 腳本提供 Active Directory Domain Services (AD DS 物件的存取權。</span><span class="sxs-lookup"><span data-stu-id="1406e-117">Active Directory Service Interfaces (ADSI) scripts provides access to Active Directory Domain Services (AD DS) objects.</span></span> <span data-ttu-id="1406e-118">WSH 和 ADSI 腳本都會存取物件，並允許無法透過批次檔使用的程式。</span><span class="sxs-lookup"><span data-stu-id="1406e-118">Both WSH and ADSI scripts access objects and allow procedures not available through batch files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1406e-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="1406e-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1406e-120">關於 WMI</span><span class="sxs-lookup"><span data-stu-id="1406e-120">About WMI</span></span>](about-wmi.md)
</dt> <dt>

[<span data-ttu-id="1406e-121">適用于 WMI 的腳本 API</span><span class="sxs-lookup"><span data-stu-id="1406e-121">Scripting API for WMI</span></span>](scripting-api-for-wmi.md)
</dt> </dl>

 

 
