---
description: 預先選取的屬性工作表示已選取功能，且不需要顯示選取對話方塊。相依於是否已安裝功能的條件運算式會使用這個值。
ms.assetid: 2bbab8b9-084a-4515-904c-d556d183d06e
title: 預先選取的屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 369a6d5fe7db99fab0032ee933afdb54bdb87efc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000930"
---
# <a name="preselected-property"></a><span data-ttu-id="13f1b-103">預先選取的屬性</span><span class="sxs-lookup"><span data-stu-id="13f1b-103">Preselected property</span></span>

<span data-ttu-id="13f1b-104">**預先** 選取的屬性工作表示已選取功能，且不需要顯示選取對話方塊。</span><span class="sxs-lookup"><span data-stu-id="13f1b-104">The **Preselected** property indicates that features have already been selected and that the selection dialog need not be shown.</span></span>

<span data-ttu-id="13f1b-105">相依於是否已安裝功能的條件運算式會使用這個值。</span><span class="sxs-lookup"><span data-stu-id="13f1b-105">Conditional expressions which depend on whether features are already installed use this value.</span></span> <span data-ttu-id="13f1b-106">例如，您可以使用屬性來隱藏在已暫停的安裝繼續進行時，牽涉到特徵選取的任何對話方塊。</span><span class="sxs-lookup"><span data-stu-id="13f1b-106">For example, the property can be used to suppress any dialogs involving feature selections during the resumption of a suspended installation.</span></span>

<span data-ttu-id="13f1b-107">安裝程式在停用的安裝期間，或在命令列上指定了下列任何屬性時，會將 **預先** 選取的屬性設定為 "1" 的值。</span><span class="sxs-lookup"><span data-stu-id="13f1b-107">The installer sets the **Preselected** property to a value of "1" during the resumption of a suspended installation or when any of the following properties are specified on the command line.</span></span> <span data-ttu-id="13f1b-108">如果 **預先** 選取的屬性已設定為1，安裝程式就不會使用 [Condition 資料表](condition-table.md) 來評估選取的功能。</span><span class="sxs-lookup"><span data-stu-id="13f1b-108">If the **Preselected** property has been set to 1, the installer does not use the [Condition table](condition-table.md) to evaluate the selection of features.</span></span> <span data-ttu-id="13f1b-109">您可以根據下列屬性來安裝功能。</span><span class="sxs-lookup"><span data-stu-id="13f1b-109">Features are installed based upon the following properties.</span></span> <span data-ttu-id="13f1b-110">安裝程式一律會以下列順序評估這些屬性：</span><span class="sxs-lookup"><span data-stu-id="13f1b-110">The installer always evaluates these properties in the following order:</span></span>

1.  [<span data-ttu-id="13f1b-111">**ADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="13f1b-111">**ADDLOCAL**</span></span>](addlocal.md)
2.  [<span data-ttu-id="13f1b-112">**刪除**</span><span class="sxs-lookup"><span data-stu-id="13f1b-112">**REMOVE**</span></span>](remove.md)
3.  [<span data-ttu-id="13f1b-113">**ADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="13f1b-113">**ADDSOURCE**</span></span>](addsource.md)
4.  [<span data-ttu-id="13f1b-114">**ADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="13f1b-114">**ADDDEFAULT**</span></span>](adddefault.md)
5.  [<span data-ttu-id="13f1b-115">**REINSTALL**</span><span class="sxs-lookup"><span data-stu-id="13f1b-115">**REINSTALL**</span></span>](reinstall.md)
6.  [<span data-ttu-id="13f1b-116">**做廣告**</span><span class="sxs-lookup"><span data-stu-id="13f1b-116">**ADVERTISE**</span></span>](advertise.md)
7.  [<span data-ttu-id="13f1b-117">**COMPADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="13f1b-117">**COMPADDLOCAL**</span></span>](compaddlocal.md)
8.  [<span data-ttu-id="13f1b-118">**COMPADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="13f1b-118">**COMPADDSOURCE**</span></span>](compaddsource.md)
9.  [<span data-ttu-id="13f1b-119">**COMPADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="13f1b-119">**COMPADDDEFAULT**</span></span>](compadddefault.md)
10. [<span data-ttu-id="13f1b-120">**FILEADDLOCAL**</span><span class="sxs-lookup"><span data-stu-id="13f1b-120">**FILEADDLOCAL**</span></span>](fileaddlocal.md)
11. [<span data-ttu-id="13f1b-121">**FILEADDSOURCE**</span><span class="sxs-lookup"><span data-stu-id="13f1b-121">**FILEADDSOURCE**</span></span>](fileaddsource.md)
12. [<span data-ttu-id="13f1b-122">**FILEADDDEFAULT**</span><span class="sxs-lookup"><span data-stu-id="13f1b-122">**FILEADDDEFAULT**</span></span>](fileadddefault.md)

## <a name="requirements"></a><span data-ttu-id="13f1b-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="13f1b-123">Requirements</span></span>



| <span data-ttu-id="13f1b-124">需求</span><span class="sxs-lookup"><span data-stu-id="13f1b-124">Requirement</span></span> | <span data-ttu-id="13f1b-125">值</span><span class="sxs-lookup"><span data-stu-id="13f1b-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13f1b-126">版本</span><span class="sxs-lookup"><span data-stu-id="13f1b-126">Version</span></span><br/> | <span data-ttu-id="13f1b-127">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="13f1b-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="13f1b-128">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="13f1b-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="13f1b-129">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="13f1b-129">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="13f1b-130">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="13f1b-130">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="13f1b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13f1b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f1b-132">屬性</span><span class="sxs-lookup"><span data-stu-id="13f1b-132">Properties</span></span>](properties.md)
</dt> </dl>

 

 




