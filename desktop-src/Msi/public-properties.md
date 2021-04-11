---
description: 您可以用與私用屬性相同的方式，將公用屬性撰寫至安裝資料庫。
ms.assetid: 032aa55f-d97a-4455-bd32-571b0e05763b
title: 公用屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 822dfc55e0ab659e5580580edd04eb156540cb61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849159"
---
# <a name="public-properties"></a><span data-ttu-id="1d528-103">公用屬性</span><span class="sxs-lookup"><span data-stu-id="1d528-103">Public Properties</span></span>

<span data-ttu-id="1d528-104">您可以用與 [私用屬性](private-properties.md)相同的方式，將公用屬性撰寫至安裝資料庫。</span><span class="sxs-lookup"><span data-stu-id="1d528-104">Public properties can be authored into the installation database in the same way as [private properties](private-properties.md).</span></span> <span data-ttu-id="1d528-105">此外，使用者或系統管理員可以藉由在命令列上設定屬性、套用轉換，或與撰寫的使用者介面互動，來變更公用屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1d528-105">In addition, the values of public properties can be changed by a user or system administrator by setting the property on the command line, by applying a transform, or by interacting with an authored user interface.</span></span> <span data-ttu-id="1d528-106">公用屬性名稱不能包含小寫字母。</span><span class="sxs-lookup"><span data-stu-id="1d528-106">Public property names cannot contain lowercase letters.</span></span> <span data-ttu-id="1d528-107">請參閱 [屬性名稱的限制](restrictions-on-property-names.md)。</span><span class="sxs-lookup"><span data-stu-id="1d528-107">See [Restrictions on Property Names](restrictions-on-property-names.md).</span></span>

<span data-ttu-id="1d528-108">公用屬性通常會在安裝期間由使用者設定。</span><span class="sxs-lookup"><span data-stu-id="1d528-108">Public properties are commonly set by users during the installation.</span></span> <span data-ttu-id="1d528-109">例如，您可以在用來啟動安裝的命令列或使用撰寫的使用者介面選擇的命令列中指定 public property [**INSTALLLEVEL**](installlevel.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="1d528-109">For example, the public property [**INSTALLLEVEL**](installlevel.md) property can be specified at the command line used to launch the installation or chosen by using an authored user interface.</span></span>

<span data-ttu-id="1d528-110">您可以在命令列使用 [標準](standard-actions.md) 或 [自訂](custom-actions.md) 動作、套用轉換，或讓使用者與撰寫的使用者介面進行互動，來覆寫公用屬性值。</span><span class="sxs-lookup"><span data-stu-id="1d528-110">Public property values can be overridden either at a command line, by using a [standard](standard-actions.md) or [custom](custom-actions.md) action, by applying a transform, or by having the user interact with an authored user interface.</span></span> <span data-ttu-id="1d528-111">若要清除屬性工作表中的公用屬性，請將它保留在資料表中。</span><span class="sxs-lookup"><span data-stu-id="1d528-111">To clear a public property in the property table, leave it out of the table.</span></span> <span data-ttu-id="1d528-112">在安裝期間要由使用者介面設定，然後傳遞至安裝的執行時間的屬性必須是公用的。</span><span class="sxs-lookup"><span data-stu-id="1d528-112">Properties that are to be set by the user interface during the installation and then passed to the execution phase of the installation must be public.</span></span>

<span data-ttu-id="1d528-113">如需安裝程式所使用的標準公用屬性清單，請參閱 [屬性參考](property-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="1d528-113">For a list of the standard public properties used by the installer see [Property Reference](property-reference.md).</span></span> <span data-ttu-id="1d528-114">作者也可以藉由在 [屬性工作表](property-table.md)中輸入屬性的名稱和初始值，來定義自訂的公用屬性。</span><span class="sxs-lookup"><span data-stu-id="1d528-114">An author can also define a custom public property by entering the property's name and an initial value into the [Property table](property-table.md).</span></span> <span data-ttu-id="1d528-115">如果下列任何一個條件成立，則所有使用者都可以覆寫所有公用屬性。</span><span class="sxs-lookup"><span data-stu-id="1d528-115">All public properties can be overridden by all users if any of the following conditions are true.</span></span>

-   <span data-ttu-id="1d528-116">使用者是系統管理員。</span><span class="sxs-lookup"><span data-stu-id="1d528-116">The user is a system administrator.</span></span>
-   <span data-ttu-id="1d528-117">每一電腦的 EnableUserControl 原則設定為1。</span><span class="sxs-lookup"><span data-stu-id="1d528-117">The per-machine EnableUserControl policy is set to 1.</span></span> <span data-ttu-id="1d528-118">請參閱 [系統原則](system-policy.md)。</span><span class="sxs-lookup"><span data-stu-id="1d528-118">See [System Policy](system-policy.md).</span></span>
-   <span data-ttu-id="1d528-119">[**EnableUserControl**](-enableusercontrol.md)屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="1d528-119">The [**EnableUserControl**](-enableusercontrol.md) property is set to 1.</span></span>
-   <span data-ttu-id="1d528-120">這是未以較高許可權執行的非受控安裝。</span><span class="sxs-lookup"><span data-stu-id="1d528-120">This is an unmanaged installation that is not being done with elevated privileges.</span></span>

<span data-ttu-id="1d528-121">如果上述條件都不成立，則安裝程式會預設為限制不是系統管理員的使用者可覆寫哪些公用屬性。</span><span class="sxs-lookup"><span data-stu-id="1d528-121">If none of the above conditions are true, the installer defaults to limiting which public properties can be overridden by a user that is not a system administrator.</span></span> <span data-ttu-id="1d528-122">請參閱 [**受限制的公用屬性**](restricted-public-properties.md)。</span><span class="sxs-lookup"><span data-stu-id="1d528-122">See [**Restricted Public Properties**](restricted-public-properties.md).</span></span>

 

 



