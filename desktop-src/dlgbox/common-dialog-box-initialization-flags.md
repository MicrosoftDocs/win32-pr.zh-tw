---
title: 通用對話方塊初始化旗標
description: 旗標是用來修改通用對話方塊的行為和外觀。
ms.assetid: 072cdcab-00d1-4a09-97fb-a6de2d51392e
keywords:
- 一般對話方塊程式庫，初始化
- 通用對話方塊，初始化
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b0c994e743178e3b6a17129275affed099d3004
ms.sourcegitcommit: 56f8e4d5119e5018363fa2dc3472cdff203c6913
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/19/2020
ms.locfileid: "104463984"
---
# <a name="common-dialog-box-initialization-flags"></a><span data-ttu-id="b3514-105">通用對話方塊初始化旗標</span><span class="sxs-lookup"><span data-stu-id="b3514-105">Common Dialog Box Initialization Flags</span></span>

<span data-ttu-id="b3514-106">旗標是用來修改通用對話方塊的行為和外觀。</span><span class="sxs-lookup"><span data-stu-id="b3514-106">Flags are used to modify the behavior and appearance of a common dialog box.</span></span> <span data-ttu-id="b3514-107">初始化旗標是您在用來建立對話方塊的結構 **旗標** 成員中設定的值。</span><span class="sxs-lookup"><span data-stu-id="b3514-107">Initialization flags are the values that you set in the **Flags** member of the structure that is used to create the dialog box.</span></span> <span data-ttu-id="b3514-108">您可以使用旗標來指定對話方塊中的哪些控制項接收初始值、停用選取的控制項，以及修改使用者可使用控制項設定的值範圍。</span><span class="sxs-lookup"><span data-stu-id="b3514-108">You use the flags to specify which controls in a dialog box receive initial values, to disable selected controls, and to modify the range of values that the user can set with the controls.</span></span> <span data-ttu-id="b3514-109">您也可以使用旗標來啟用對話方塊的攔截程式和自訂範本。</span><span class="sxs-lookup"><span data-stu-id="b3514-109">You also use the flags to enable hook procedures and custom templates for the dialog boxes.</span></span>

<span data-ttu-id="b3514-110">例如，您可以在 [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta)結構的 **旗標** 成員中設定 **CF \_ 效果** 值，以指示 [**字型**] 對話方塊來顯示效果控制項。</span><span class="sxs-lookup"><span data-stu-id="b3514-110">For example, you can set the **CF\_EFFECTS** value in the **Flags** member of the [**CHOOSEFONT**](/windows/win32/api/commdlg/ns-commdlg-choosefonta) structure to direct the **Font** dialog box to display the effects controls.</span></span> <span data-ttu-id="b3514-111">這些控制項可讓使用者選擇字型色彩以及刪除線和底線效果。</span><span class="sxs-lookup"><span data-stu-id="b3514-111">These controls let the user choose a font color as well as strikethrough and underline effects.</span></span>

<span data-ttu-id="b3514-112">初始化旗標值對於每個通用對話方塊都是唯一的，而且會詳細說明下列對應的下列結構的 **旗標** 成員：</span><span class="sxs-lookup"><span data-stu-id="b3514-112">The initialization flag values are unique to each common dialog box and are described in detail by the **Flags** members of the following structures that correspond to them:</span></span>

-   [<span data-ttu-id="b3514-113">**CHOOSECOLOR**</span><span class="sxs-lookup"><span data-stu-id="b3514-113">**CHOOSECOLOR**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosecolora-r1)
-   [<span data-ttu-id="b3514-114">**CHOOSEFONT**</span><span class="sxs-lookup"><span data-stu-id="b3514-114">**CHOOSEFONT**</span></span>](/windows/win32/api/commdlg/ns-commdlg-choosefonta)
-   [<span data-ttu-id="b3514-115">**FINDREPLACE**</span><span class="sxs-lookup"><span data-stu-id="b3514-115">**FINDREPLACE**</span></span>](/windows/win32/api/commdlg/ns-commdlg-findreplacea)
-   [<span data-ttu-id="b3514-116">**OPENFILENAME**</span><span class="sxs-lookup"><span data-stu-id="b3514-116">**OPENFILENAME**</span></span>](/windows/win32/api/commdlg/ns-commdlg-openfilenamea)
-   [<span data-ttu-id="b3514-117">**PAGESETUPDLG**</span><span class="sxs-lookup"><span data-stu-id="b3514-117">**PAGESETUPDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-pagesetupdlga)
-   [<span data-ttu-id="b3514-118">**PRINTDLG**</span><span class="sxs-lookup"><span data-stu-id="b3514-118">**PRINTDLG**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlga)
-   [<span data-ttu-id="b3514-119">**PRINTDLGEX**</span><span class="sxs-lookup"><span data-stu-id="b3514-119">**PRINTDLGEX**</span></span>](/windows/win32/api/commdlg/ns-commdlg-printdlgexa)

 

 




