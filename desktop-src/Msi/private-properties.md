---
description: 私用屬性是由安裝程式在內部使用，且其值必須由安裝封裝的作者在資料庫中輸入，或是由安裝程式在安裝期間由安裝程式設定為由作業環境決定的值。
ms.assetid: 7d574bf0-bcb3-4e19-9659-fe741ace9f21
title: 私用屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab7b0196be016fecb625e139f308219582620d40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971508"
---
# <a name="private-properties"></a><span data-ttu-id="06873-103">私用屬性</span><span class="sxs-lookup"><span data-stu-id="06873-103">Private Properties</span></span>

<span data-ttu-id="06873-104">私用屬性是由安裝程式在內部使用，且其值必須由安裝封裝的作者在資料庫中輸入，或是由安裝程式在安裝期間由安裝程式設定為由作業環境決定的值。</span><span class="sxs-lookup"><span data-stu-id="06873-104">Private properties are used internally by the installer and their values must be entered into the database by the author of the installation package or set by the installer during the installation to values determined by the operating environment.</span></span> <span data-ttu-id="06873-105">使用者可以與私用屬性互動的唯一方式，是透過在套件撰寫的使用者介面中 [控制事件](control-events.md) 。</span><span class="sxs-lookup"><span data-stu-id="06873-105">The only way a user can interact with private properties is through [Control Events](control-events.md) in the package's authored user interface.</span></span> <span data-ttu-id="06873-106">私用屬性名稱必須包含小寫字母。</span><span class="sxs-lookup"><span data-stu-id="06873-106">Private property names must include lowercase letters.</span></span> <span data-ttu-id="06873-107">請參閱 [屬性名稱的限制](restrictions-on-property-names.md)。</span><span class="sxs-lookup"><span data-stu-id="06873-107">See [Restrictions on Property Names](restrictions-on-property-names.md).</span></span>

<span data-ttu-id="06873-108">私用屬性通常會描述操作環境。</span><span class="sxs-lookup"><span data-stu-id="06873-108">Private properties commonly describe the operating environment.</span></span> <span data-ttu-id="06873-109">例如，如果是在 Windows 平臺上執行安裝，安裝程式會將 [**WindowsFolder**](windowsfolder.md) 屬性設定為屬性工作表中指定的值。</span><span class="sxs-lookup"><span data-stu-id="06873-109">For example, if the installation is run on a Windows platform, the installer sets the [**WindowsFolder**](windowsfolder.md) property to the value specified in the Property table.</span></span>

<span data-ttu-id="06873-110">無法在命令列覆寫私用屬性值。</span><span class="sxs-lookup"><span data-stu-id="06873-110">Private property values cannot be overridden at a command line.</span></span> <span data-ttu-id="06873-111">若要從安裝清除私用屬性，請將它保留在 [屬性工作表](property-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="06873-111">To clear a private property from an installation, leave it out of the [Property table](property-table.md).</span></span> <span data-ttu-id="06873-112">在 Windows XP 與 Windows 2000 上，您無法在安裝的使用者介面階段設定私用屬性，然後將值傳遞至執行階段。</span><span class="sxs-lookup"><span data-stu-id="06873-112">On Windows XP, and Windows 2000 you cannot set a private property in the user interface phase of the installation and then pass the value to the execution phase.</span></span>

<span data-ttu-id="06873-113">如需安裝程式所使用之所有標準私用屬性的清單，請參閱 [屬性參考](property-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="06873-113">For a list of all the standard private properties used by the installer, see [Property Reference](property-reference.md).</span></span> <span data-ttu-id="06873-114">您可以藉由在屬性工作表中輸入屬性的名稱和初始值，來定義自訂私用屬性。</span><span class="sxs-lookup"><span data-stu-id="06873-114">You can define a custom private property by entering the property's name and initial value in the Property table.</span></span> <span data-ttu-id="06873-115">私用屬性名稱一律必須包含小寫字母。</span><span class="sxs-lookup"><span data-stu-id="06873-115">Private property names must always include lowercase letters.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06873-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="06873-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06873-117">公用屬性</span><span class="sxs-lookup"><span data-stu-id="06873-117">Public Properties</span></span>](public-properties.md)
</dt> </dl>

 

 



