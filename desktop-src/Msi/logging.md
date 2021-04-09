---
description: 只有當 &0034 未啟用記錄 \# ;/l&\# 0034; 命令列選項或 MsiEnableLog 時，才會使用每部電腦的系統原則。
ms.assetid: d8649808-5dc3-4496-8c2f-da9b1512b5aa
title: '記錄 (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a461051022791e414fe7e211e4dde33c7e83101b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103693051"
---
# <a name="logging-windows-installer"></a><span data-ttu-id="6449f-103">記錄 (Windows Installer) </span><span class="sxs-lookup"><span data-stu-id="6449f-103">Logging (Windows Installer)</span></span>

<span data-ttu-id="6449f-104">只有當 "/L" 命令列選項或 [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)未啟用記錄功能時，才會使用每部電腦的 [系統原則](system-policy.md)。</span><span class="sxs-lookup"><span data-stu-id="6449f-104">This per-machine [system policy](system-policy.md) is used only if logging has not been enabled by the "/L" command line option or by [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga).</span></span> <span data-ttu-id="6449f-105">如果在此情況下設定此原則，安裝程式會在% temp% 中建立具有隨機名稱： MSI 的記錄檔 \* 。日誌。</span><span class="sxs-lookup"><span data-stu-id="6449f-105">If the policy is set in this case, the installer creates a log file in %temp% with the random name: MSI\*.LOG.</span></span> <span data-ttu-id="6449f-106">將原則值設定為字元字串，以指定記錄模式。</span><span class="sxs-lookup"><span data-stu-id="6449f-106">Specify the logging mode by setting the policy value to a string of characters.</span></span> <span data-ttu-id="6449f-107">使用相同的字元，指定 "/L" [命令列選項](command-line-options.md)所使用的記錄模式原則。</span><span class="sxs-lookup"><span data-stu-id="6449f-107">Use the same characters to specify logging mode policy as used by the "/L" [command line option](command-line-options.md).</span></span> <span data-ttu-id="6449f-108">請注意，您不能針對原則使用 "+" 和 " \* "。</span><span class="sxs-lookup"><span data-stu-id="6449f-108">Note that you cannot use "+" and "\*" for the policy.</span></span>

<span data-ttu-id="6449f-109">您可以使用原則、命令列選項或以程式設計方式來設定記錄模式。</span><span class="sxs-lookup"><span data-stu-id="6449f-109">The logging mode can be set using policy, a command line option, or programmatically.</span></span> <span data-ttu-id="6449f-110">如需可用於設定記錄模式之所有方法的詳細資訊，請參閱[Windows Installer 記錄](windows-installer-logging.md)] 區段中的[一般記錄](normal-logging.md)。</span><span class="sxs-lookup"><span data-stu-id="6449f-110">For more information about all the methods that are available for setting the logging mode, see [Normal Logging](normal-logging.md) in the [Windows Installer Logging](windows-installer-logging.md) section.</span></span>

<span data-ttu-id="6449f-111">您可以防止將機密資訊（例如密碼）輸入記錄檔中，並使其成為可見。</span><span class="sxs-lookup"><span data-stu-id="6449f-111">You can prevent confidential information, for example passwords, from being entered into the log file and made visible.</span></span> <span data-ttu-id="6449f-112">如需詳細資訊，請參閱[防止機密資訊寫入記錄](preventing-confidential-information-from-being-written-into-the-log-file.md)檔</span><span class="sxs-lookup"><span data-stu-id="6449f-112">For more information, see [Preventing Confidential Information from Being Written into the Log File](preventing-confidential-information-from-being-written-into-the-log-file.md)</span></span>

## <a name="registry-key"></a><span data-ttu-id="6449f-113">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="6449f-113">Registry Key</span></span>

<span data-ttu-id="6449f-114">在下列登錄機碼底下，設定名為 [記錄] 的值。</span><span class="sxs-lookup"><span data-stu-id="6449f-114">Set the value named Logging under the following registry key.</span></span>

<span data-ttu-id="6449f-115">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="6449f-115">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="6449f-116">資料類型</span><span class="sxs-lookup"><span data-stu-id="6449f-116">Data Type</span></span>

<span data-ttu-id="6449f-117">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="6449f-117">**REG\_SZ**</span></span>

 

 



