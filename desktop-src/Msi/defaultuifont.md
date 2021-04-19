---
description: DefaultUIFont 屬性會設定用於控制項的預設字型樣式。 若要指定預設值，請將 DefaultUIFont 設定為屬性工作表中的樣式表單中的其中一個預先定義樣式。
ms.assetid: 594183ce-ef13-47f6-a4ae-37ba09c06cbd
title: DefaultUIFont 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3791219dcef84253280fec3c797f2035afd239f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979625"
---
# <a name="defaultuifont-property"></a><span data-ttu-id="e7048-104">DefaultUIFont 屬性</span><span class="sxs-lookup"><span data-stu-id="e7048-104">DefaultUIFont property</span></span>

<span data-ttu-id="e7048-105">**DefaultUIFont** 屬性會設定用於控制項的預設字型樣式。</span><span class="sxs-lookup"><span data-stu-id="e7048-105">The **DefaultUIFont** property sets the default font style used for controls.</span></span> <span data-ttu-id="e7048-106">若要指定預設值，請將 **DefaultUIFont** 設定為 [屬性工作表](property-table.md)中的樣式 [表單](textstyle-table.md)中的其中一個預先定義樣式。</span><span class="sxs-lookup"><span data-stu-id="e7048-106">To specify the default, set **DefaultUIFont** to one of the predefined styles in the [TextStyle table](textstyle-table.md) in the [Property table](property-table.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="e7048-107">備註</span><span class="sxs-lookup"><span data-stu-id="e7048-107">Remarks</span></span>

<span data-ttu-id="e7048-108">您應在 [屬性工作表](property-table.md)中，將每個安裝套件的 **DefaultUIFont** 屬性設定為 [[樣式](textstyle-table.md)表單] 中所列的其中一個預先定義樣式。</span><span class="sxs-lookup"><span data-stu-id="e7048-108">The **DefaultUIFont** property of every installation package with a UI should be set in the [Property table](property-table.md) to one of the predefined styles listed in the [TextStyle table](textstyle-table.md).</span></span> <span data-ttu-id="e7048-109">如果未指定這個屬性，安裝程式會使用系統字型。</span><span class="sxs-lookup"><span data-stu-id="e7048-109">If this property is not specified, the installer uses the System font.</span></span> <span data-ttu-id="e7048-110">當套件的字碼頁與使用者的預設 UI 字碼頁不同時，這可能會導致安裝程式不正確地顯示文字字串。</span><span class="sxs-lookup"><span data-stu-id="e7048-110">This can cause the installer to improperly display text strings when the package's code page is different from the user's default UI code page.</span></span>

<span data-ttu-id="e7048-111">您可以如 [新增控制項和文字](adding-controls-and-text.md)中所述，設定控制項的文字與字型樣式。</span><span class="sxs-lookup"><span data-stu-id="e7048-111">The text and font style of a control can be set as described in [Adding Controls and Text](adding-controls-and-text.md).</span></span> <span data-ttu-id="e7048-112">如果 [控制資料表](control-table.md) 或 [BBControl 表](bbcontrol-table.md) 的 Text 資料行中所列的字元字串未指定字型樣式，控制項就會使用 **DefaultUIFont** 屬性的值做為字型樣式。</span><span class="sxs-lookup"><span data-stu-id="e7048-112">If the character string listed in the Text column of the [Control table](control-table.md) or [BBControl table](bbcontrol-table.md) does not specify the font style, the control uses the value of the **DefaultUIFont** property as the font style.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7048-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7048-113">Requirements</span></span>



| <span data-ttu-id="e7048-114">需求</span><span class="sxs-lookup"><span data-stu-id="e7048-114">Requirement</span></span> | <span data-ttu-id="e7048-115">值</span><span class="sxs-lookup"><span data-stu-id="e7048-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7048-116">版本</span><span class="sxs-lookup"><span data-stu-id="e7048-116">Version</span></span><br/> | <span data-ttu-id="e7048-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="e7048-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e7048-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="e7048-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e7048-119">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="e7048-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="e7048-120">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="e7048-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e7048-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7048-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7048-122">屬性</span><span class="sxs-lookup"><span data-stu-id="e7048-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




