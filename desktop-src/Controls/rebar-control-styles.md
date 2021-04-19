---
title: 'Rebar 控制項樣式 (CommCtrl .h) '
description: 除了標準視窗樣式之外，Rebar 控制項還支援各種控制項樣式。
ms.assetid: 9690a4bd-51bd-4df9-8988-7da3ece7899f
topic_type:
- apiref
api_name:
- RBS_AUTOSIZE
- RBS_BANDBORDERS
- RBS_DBLCLKTOGGLE
- RBS_FIXEDORDER
- RBS_REGISTERDROP
- RBS_TOOLTIPS
- RBS_VARHEIGHT
- RBS_VERTICALGRIPPER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67b9f447df2cbf1bb2b956a7ec300d1f29280eef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000793"
---
# <a name="rebar-control-styles"></a><span data-ttu-id="034f4-103">Rebar 控制項樣式</span><span class="sxs-lookup"><span data-stu-id="034f4-103">Rebar Control Styles</span></span>

<span data-ttu-id="034f4-104">除了標準視窗樣式之外，Rebar 控制項還支援各種控制項樣式。</span><span class="sxs-lookup"><span data-stu-id="034f4-104">Rebar controls support a variety of control styles in addition to standard window styles.</span></span>



| <span data-ttu-id="034f4-105">常數</span><span class="sxs-lookup"><span data-stu-id="034f4-105">Constant</span></span>                                                                                                                                                                        | <span data-ttu-id="034f4-106">描述</span><span class="sxs-lookup"><span data-stu-id="034f4-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RBS_AUTOSIZE"></span><span id="rbs_autosize"></span><dl> <span data-ttu-id="034f4-107"><dt>**RBS 自動 \_ 調整**</dt></span><span class="sxs-lookup"><span data-stu-id="034f4-107"><dt>**RBS\_AUTOSIZE**</dt></span></span> </dl>                      | <span data-ttu-id="034f4-108">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="034f4-108">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="034f4-109">當控制項的大小或位置變更時，Rebar 控制項將會自動變更群組的版面配置。</span><span class="sxs-lookup"><span data-stu-id="034f4-109">The rebar control will automatically change the layout of the bands when the size or position of the control changes.</span></span> <span data-ttu-id="034f4-110">當發生這種情況時，將會傳送 [RBN \_ AUTOSIZE](rbn-autosize.md) 通知。</span><span class="sxs-lookup"><span data-stu-id="034f4-110">An [RBN\_AUTOSIZE](rbn-autosize.md) notification will be sent when this occurs.</span></span><br/>                                                                                              |
| <span id="RBS_BANDBORDERS"></span><span id="rbs_bandborders"></span><dl> <span data-ttu-id="034f4-111"><dt>**RBS \_ BANDBORDERS**</dt></span><span class="sxs-lookup"><span data-stu-id="034f4-111"><dt>**RBS\_BANDBORDERS**</dt></span></span> </dl>             | <span data-ttu-id="034f4-112">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="034f4-112">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="034f4-113">Rebar 控制項會顯示窄行以分隔連續的群組。</span><span class="sxs-lookup"><span data-stu-id="034f4-113">The rebar control displays narrow lines to separate adjacent bands.</span></span><br/>                                                                                                                                                                                                                                 |
| <span id="RBS_DBLCLKTOGGLE"></span><span id="rbs_dblclktoggle"></span><dl> <span data-ttu-id="034f4-114"><dt>**RBS \_ DBLCLKTOGGLE**</dt></span><span class="sxs-lookup"><span data-stu-id="034f4-114"><dt>**RBS\_DBLCLKTOGGLE**</dt></span></span> </dl>          | <span data-ttu-id="034f4-115">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="034f4-115">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="034f4-116">當使用者按兩下此寬線時，Rebar 波段會切換其最大化或最小化的狀態。</span><span class="sxs-lookup"><span data-stu-id="034f4-116">The rebar band will toggle its maximized or minimized state when the user double-clicks the band.</span></span> <span data-ttu-id="034f4-117">如果沒有這種樣式，當使用者按一下此寬線時，就會切換最大化或最小化的狀態。</span><span class="sxs-lookup"><span data-stu-id="034f4-117">Without this style, the maximized or minimized state is toggled when the user single-clicks on the band.</span></span><br/>                                                                                          |
| <span id="RBS_FIXEDORDER"></span><span id="rbs_fixedorder"></span><dl> <span data-ttu-id="034f4-118"><dt>**RBS \_ FIXEDORDER**</dt></span><span class="sxs-lookup"><span data-stu-id="034f4-118"><dt>**RBS\_FIXEDORDER**</dt></span></span> </dl>                | <span data-ttu-id="034f4-119">[版本 4.70](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="034f4-119">[Version 4.70](common-control-versions.md).</span></span> <span data-ttu-id="034f4-120">Rebar 控制項一律會以相同的順序顯示群組。</span><span class="sxs-lookup"><span data-stu-id="034f4-120">The rebar control always displays bands in the same order.</span></span> <span data-ttu-id="034f4-121">您可以將多個群組移至不同的資料列，但帶狀順序是靜態的。</span><span class="sxs-lookup"><span data-stu-id="034f4-121">You can move bands to different rows, but the band order is static.</span></span><br/>                                                                                                                                                                      |
| <span id="RBS_REGISTERDROP"></span><span id="rbs_registerdrop"></span><dl> <span data-ttu-id="034f4-122"><dt>**RBS \_ REGISTERDROP**</dt></span><span class="sxs-lookup"><span data-stu-id="034f4-122"><dt>**RBS\_REGISTERDROP**</dt></span></span> </dl>          | <span data-ttu-id="034f4-123">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="034f4-123">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="034f4-124">當物件拖曳到控制項中的波段上方時，Rebar 控制項會產生 [RBN 的 \_ GETOBJECT](rbn-getobject.md) 通知代碼。</span><span class="sxs-lookup"><span data-stu-id="034f4-124">The rebar control generates [RBN\_GETOBJECT](rbn-getobject.md) notification codes when an object is dragged over a band in the control.</span></span> <span data-ttu-id="034f4-125">若要接收 RBN 的 \_ GETOBJECT 通知，請呼叫 [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) 或 [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize)來初始化 OLE。</span><span class="sxs-lookup"><span data-stu-id="034f4-125">To receive the RBN\_GETOBJECT notifications, initialize OLE with a call to [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) or [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).</span></span><br/> |
| <span id="RBS_TOOLTIPS"></span><span id="rbs_tooltips"></span><dl> <span data-ttu-id="034f4-126"><dt>**RBS \_ 工具提示**</dt></span><span class="sxs-lookup"><span data-stu-id="034f4-126"><dt>**RBS\_TOOLTIPS**</dt></span></span> </dl>                      | <span data-ttu-id="034f4-127">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="034f4-127">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="034f4-128">尚不支援。</span><span class="sxs-lookup"><span data-stu-id="034f4-128">Not yet supported.</span></span><br/>                                                                                                                                                                                                                                                                                  |
| <span id="RBS_VARHEIGHT"></span><span id="rbs_varheight"></span><dl> <span data-ttu-id="034f4-129"><dt>**RBS \_ VARHEIGHT**</dt></span><span class="sxs-lookup"><span data-stu-id="034f4-129"><dt>**RBS\_VARHEIGHT**</dt></span></span> </dl>                   | <span data-ttu-id="034f4-130">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="034f4-130">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="034f4-131">如果可能的話，Rebar 控制項會以最小的必要高度顯示群組。</span><span class="sxs-lookup"><span data-stu-id="034f4-131">The rebar control displays bands at the minimum required height, when possible.</span></span> <span data-ttu-id="034f4-132">如果沒有這個樣式，Rebar 控制項會使用最高可見寬線的高度來顯示所有的條紋，以判斷其他條紋的高度。</span><span class="sxs-lookup"><span data-stu-id="034f4-132">Without this style, the rebar control displays all bands at the same height, using the height of the tallest visible band to determine the height of other bands.</span></span><br/>                                                   |
| <span id="RBS_VERTICALGRIPPER"></span><span id="rbs_verticalgripper"></span><dl> <span data-ttu-id="034f4-133"><dt>**RBS \_ VERTICALGRIPPER**</dt></span><span class="sxs-lookup"><span data-stu-id="034f4-133"><dt>**RBS\_VERTICALGRIPPER**</dt></span></span> </dl> | <span data-ttu-id="034f4-134">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="034f4-134">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="034f4-135">大小的底框將會垂直顯示，而不是在垂直 Rebar 控制項中以水準方式顯示。</span><span class="sxs-lookup"><span data-stu-id="034f4-135">The size grip will be displayed vertically instead of horizontally in a vertical rebar control.</span></span> <span data-ttu-id="034f4-136">如果沒有 [**CCS \_ 垂直**](common-control-styles.md) 樣式的 Rebar 控制項，則會忽略這個樣式。</span><span class="sxs-lookup"><span data-stu-id="034f4-136">This style is ignored for rebar controls that do not have the [**CCS\_VERT**](common-control-styles.md) style.</span></span><br/>                                                                            |



## <a name="requirements"></a><span data-ttu-id="034f4-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="034f4-137">Requirements</span></span>



| <span data-ttu-id="034f4-138">需求</span><span class="sxs-lookup"><span data-stu-id="034f4-138">Requirement</span></span> | <span data-ttu-id="034f4-139">值</span><span class="sxs-lookup"><span data-stu-id="034f4-139">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="034f4-140">標頭</span><span class="sxs-lookup"><span data-stu-id="034f4-140">Header</span></span><br/> | <dl> <span data-ttu-id="034f4-141"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="034f4-141"><dt>CommCtrl.h</dt></span></span> </dl> |



 

