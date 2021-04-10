---
description: 開發人員可以防止在 Windows Installer 安裝期間，將機密資訊（例如密碼）輸入記錄檔中。
ms.assetid: 950c3c56-3f16-4e1a-875f-d31f45065076
title: 防止機密資訊寫入記錄檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f17880f18ca08745ab1f4f764397e17b7af8827e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026628"
---
# <a name="preventing-confidential-information-from-being-written-into-the-log-file"></a><span data-ttu-id="73424-103">防止機密資訊寫入記錄檔</span><span class="sxs-lookup"><span data-stu-id="73424-103">Preventing Confidential Information from Being Written into the Log File</span></span>

<span data-ttu-id="73424-104">使用 Windows Installer 時，您可以防止將機密資訊（例如密碼）輸入記錄檔中，並使其成為可見的。</span><span class="sxs-lookup"><span data-stu-id="73424-104">When using the Windows Installer, you can prevent confidential information, for example passwords, from being entered into the log file and made visible.</span></span>

-   <span data-ttu-id="73424-105">安裝程式永遠不會將 [ServiceInstall 資料表](serviceinstall-table.md) 之 Password 資料行中的資訊寫入記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="73424-105">The Installer never writes the information in the Password column of the [ServiceInstall table](serviceinstall-table.md) into the log.</span></span>
-   <span data-ttu-id="73424-106">您可以藉由設定[Password Control 屬性](password-control-attribute.md)，防止安裝程式將與[編輯控制項](edit-control.md)相關聯的屬性寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="73424-106">You can prevent the Installer from writing the property that is associated with an [Edit Control](edit-control.md) into the log by setting the [Password Control Attribute](password-control-attribute.md).</span></span> <span data-ttu-id="73424-107">即使 [Debug](debug.md) 原則設定為7的值，也會隱藏與具有 Password control 屬性之編輯控制項相關聯的屬性。</span><span class="sxs-lookup"><span data-stu-id="73424-107">The property associated with an Edit Control that has the Password Control Attribute is hidden even if the [Debug](debug.md) policy is set to a value of 7.</span></span>
-   <span data-ttu-id="73424-108">您可以將屬性包含在 [**MsiHiddenProperties**](msihiddenproperties.md) 屬性中，以防止安裝程式將私用屬性寫入記錄檔。</span><span class="sxs-lookup"><span data-stu-id="73424-108">You can prevent the Installer from writing a private property into the log by including the property in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span>
    > [!Note]  
    > <span data-ttu-id="73424-109">此方法可讓您在記錄檔中顯示的命令列上輸入機密資訊。</span><span class="sxs-lookup"><span data-stu-id="73424-109">This method can make confidential information entered on a command line visible in the log.</span></span> <span data-ttu-id="73424-110">當 [調試](debug.md) 程式原則設定為7的值時，安裝程式會將命令列上輸入的資訊寫入記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="73424-110">When the [Debug](debug.md) policy is set to a value of 7, the installer will write information entered on a command line into the log.</span></span> <span data-ttu-id="73424-111">如此一來，即使屬性包含在 [**MsiHiddenProperties**](msihiddenproperties.md) 屬性中，也會顯示在命令列上輸入的屬性。</span><span class="sxs-lookup"><span data-stu-id="73424-111">This makes the property entered on a command line visible even if the property is included in the [**MsiHiddenProperties**](msihiddenproperties.md) property.</span></span>

     

-   <span data-ttu-id="73424-112">您可以藉由在 CustomAction 資料表的類型欄位中加入 HideTarget 位旗標，來防止將 [CustomAction](customaction-table.md) 資料表的目標資料行中的資訊寫入記錄檔中。</span><span class="sxs-lookup"><span data-stu-id="73424-112">You can prevent the information in the Target column of the [CustomAction](customaction-table.md) Table from being written into the log by including the HideTarget bit flag in the Type field of the CustomAction table.</span></span> <span data-ttu-id="73424-113">此旗標的值為 8192 (0x2000) 。</span><span class="sxs-lookup"><span data-stu-id="73424-113">The value of this flag is 8192 (0x2000).</span></span> <span data-ttu-id="73424-114">如需詳細資訊，請參閱 [自訂動作隱藏目標選項](custom-action-hidden-target-option.md)。</span><span class="sxs-lookup"><span data-stu-id="73424-114">For more information, see [Custom Action Hidden Target Option](custom-action-hidden-target-option.md).</span></span>

 

 



