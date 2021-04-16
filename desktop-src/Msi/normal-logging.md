---
description: 安裝程式會在自己的錯誤記錄檔中記錄錯誤和事件。
ms.assetid: 244e9afa-2052-469e-aa57-424e03ce5673
title: 一般記錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0846305ef53c596fbd6f117eaf76b0715a94c313
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512773"
---
# <a name="normal-logging"></a><span data-ttu-id="6588c-103">一般記錄</span><span class="sxs-lookup"><span data-stu-id="6588c-103">Normal Logging</span></span>

<span data-ttu-id="6588c-104">安裝程式會在自己的錯誤記錄檔中記錄錯誤和事件。</span><span class="sxs-lookup"><span data-stu-id="6588c-104">The installer records errors and events in its own error log.</span></span> <span data-ttu-id="6588c-105">安裝程式所執行的記錄類型是由記錄模式的設定所決定。</span><span class="sxs-lookup"><span data-stu-id="6588c-105">The type of logging that is performed by the installer is determined by the setting of the logging mode.</span></span> <span data-ttu-id="6588c-106">記錄已啟用，而且可以使用下列方法來設定模式：</span><span class="sxs-lookup"><span data-stu-id="6588c-106">Logging is enabled and the mode can be set by using the following methods:</span></span>

-   <span data-ttu-id="6588c-107">您可以使用 [命令列選項](command-line-options.md)的/l 選項，來指定從命令列啟動之安裝的記錄模式。</span><span class="sxs-lookup"><span data-stu-id="6588c-107">The logging mode of an installation launched from the command line can be specified by using the /L option of the [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="6588c-108">如果未使用/L 命令列選項指定記錄模式，則會使用預設的記錄模式。</span><span class="sxs-lookup"><span data-stu-id="6588c-108">If the logging mode is not specified by using the /L command-line option, the default logging mode will be used.</span></span>
-   <span data-ttu-id="6588c-109">您可以使用 [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) 函數或 [**EnableLog**](installer-enablelog.md) 方法，以程式設計方式指定安裝程式的記錄模式。</span><span class="sxs-lookup"><span data-stu-id="6588c-109">The logging mode of an installation process can be specified programmatically by using the [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga) function or the [**EnableLog**](installer-enablelog.md) method.</span></span> <span data-ttu-id="6588c-110">如果未使用 **MsiEnableLog** 函數或 **EnableLog** 方法來指定記錄模式，則會使用預設的記錄模式。</span><span class="sxs-lookup"><span data-stu-id="6588c-110">If the logging mode is not specified by using the **MsiEnableLog** function or the **EnableLog** method, the default logging mode will be used.</span></span>
-   <span data-ttu-id="6588c-111">您可以藉由在封裝的 [屬性工作表](property-table.md)中設定 [**MsiLogging**](msilogging.md)屬性，來指定特定安裝封裝的預設記錄模式。</span><span class="sxs-lookup"><span data-stu-id="6588c-111">The default logging mode of a particular installation package can be specified by setting the [**MsiLogging**](msilogging.md) property in the [Property table](property-table.md) of the package.</span></span> <span data-ttu-id="6588c-112">從 Windows Installer 4.0 開始，可以使用此屬性。</span><span class="sxs-lookup"><span data-stu-id="6588c-112">This property is available starting with Windows Installer 4.0.</span></span>
-   <span data-ttu-id="6588c-113">如果 [屬性工作表](property-table.md)中有 [**MsiLogging**](msilogging.md)屬性，則可以使用 [資料庫轉換](database-transforms.md)來變更值，藉以修改封裝的預設記錄模式。</span><span class="sxs-lookup"><span data-stu-id="6588c-113">If the [**MsiLogging**](msilogging.md) property is present in the [Property table](property-table.md), the default logging mode of the package can be modified by changing the value by using a [database transform](database-transforms.md).</span></span> <span data-ttu-id="6588c-114">使用 (.msp 檔的 [Patch 封裝](patch-packages.md) ，無法變更預設的記錄模式。 ) </span><span class="sxs-lookup"><span data-stu-id="6588c-114">The default logging mode cannot be changed by using [Patch Packages](patch-packages.md) (a .msp file.)</span></span>
-   <span data-ttu-id="6588c-115">如果未設定 [**MsiLogging**](msilogging.md) 屬性，則可以使用 [記錄](logging.md) 原則來指定電腦上所有使用者的預設記錄模式。</span><span class="sxs-lookup"><span data-stu-id="6588c-115">If the [**MsiLogging**](msilogging.md) property has not been set, the default logging mode for all users of the computer can be specified by using the [Logging](logging.md) policy.</span></span>
-   <span data-ttu-id="6588c-116">如果已設定 [**MsiLogging**](msilogging.md) 屬性，則可以藉由設定 [DisableLoggingFromPackage](disableloggingfrompackage.md) 原則和 [記錄](logging.md) 原則來指定電腦上所有使用者的預設記錄模式。</span><span class="sxs-lookup"><span data-stu-id="6588c-116">If the [**MsiLogging**](msilogging.md) property has been set, the default logging mode for all users of the computer can be specified by setting both the [DisableLoggingFromPackage](disableloggingfrompackage.md) policy and [Logging](logging.md) policy.</span></span>
-   <span data-ttu-id="6588c-117">如果/L 選項、 [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga)、 [**EnableLog**](installer-enablelog.md)、 [**MsiLogging**](msilogging.md) 屬性或 [記錄](logging.md) 原則未指定記錄模式，則封裝的預設記錄模式會與將 **MsiLogging** 屬性設定為 ' iwearmo ' 時所取得的模式相同。</span><span class="sxs-lookup"><span data-stu-id="6588c-117">If the logging mode has not been specified by the /L option, [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), [**EnableLog**](installer-enablelog.md), [**MsiLogging**](msilogging.md) property, or the [Logging](logging.md) policy, then the default logging mode for the package is the same mode that is obtained as setting the **MsiLogging** property to 'iwearmo'.</span></span>

 

 



