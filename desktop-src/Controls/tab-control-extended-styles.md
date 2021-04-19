---
title: '索引標籤控制項擴充樣式 (CommCtrl .h) '
description: 索引標籤控制項現在支援擴充樣式。 這些樣式是使用 TCM \_ GETEXTENDEDSTYLE 和 tcm \_ SETEXTENDEDSTYLE 訊息來操作，不應該與傳遞給 CreateWindowEx 的延伸視窗樣式混淆。
ms.assetid: 24294037-598c-4fcd-8a7c-8647ccfb1d81
topic_type:
- apiref
api_name:
- TCS_EX_FLATSEPARATORS
- TCS_EX_REGISTERDROP
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c4e16b40a394bc9b808386d3cbdc3abf9b3d928
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981625"
---
# <a name="tab-control-extended-styles"></a><span data-ttu-id="c4841-104">索引標籤控制項擴充樣式</span><span class="sxs-lookup"><span data-stu-id="c4841-104">Tab Control Extended Styles</span></span>

<span data-ttu-id="c4841-105">索引標籤控制項現在支援擴充樣式。</span><span class="sxs-lookup"><span data-stu-id="c4841-105">The tab control now supports extended styles.</span></span> <span data-ttu-id="c4841-106">這些樣式是使用 [**tcm \_ GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) 和 [**tcm \_ SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) 訊息來操作，不應該與傳遞給 [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)的延伸視窗樣式混淆。</span><span class="sxs-lookup"><span data-stu-id="c4841-106">These styles are manipulated using the [**TCM\_GETEXTENDEDSTYLE**](tcm-getextendedstyle.md) and [**TCM\_SETEXTENDEDSTYLE**](tcm-setextendedstyle.md) messages and should not be confused with extended window styles that are passed to [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).</span></span>



| <span data-ttu-id="c4841-107">常數</span><span class="sxs-lookup"><span data-stu-id="c4841-107">Constant</span></span>                                                                                                                                                                               | <span data-ttu-id="c4841-108">描述</span><span class="sxs-lookup"><span data-stu-id="c4841-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TCS_EX_FLATSEPARATORS"></span><span id="tcs_ex_flatseparators"></span><dl> <span data-ttu-id="c4841-109"><dt>**TCS \_ EX \_ FLATSEPARATORS**</dt></span><span class="sxs-lookup"><span data-stu-id="c4841-109"><dt>**TCS\_EX\_FLATSEPARATORS**</dt></span></span> </dl> | <span data-ttu-id="c4841-110">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="c4841-110">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="c4841-111">索引標籤控制項將會在索引標籤專案之間繪製分隔符號。</span><span class="sxs-lookup"><span data-stu-id="c4841-111">The tab control will draw separators between the tab items.</span></span> <span data-ttu-id="c4841-112">此擴充樣式只會影響具有 [TCS] [**\_ 按鈕**](tab-control-styles.md) 和 [**TCS \_ FLATBUTTONS**](tab-control-styles.md) 樣式的索引標籤控制項。</span><span class="sxs-lookup"><span data-stu-id="c4841-112">This extended style only affects tab controls that have the [**TCS\_BUTTONS**](tab-control-styles.md) and [**TCS\_FLATBUTTONS**](tab-control-styles.md) styles.</span></span> <span data-ttu-id="c4841-113">根據預設，建立具有 **TCS \_ FLATBUTTONS** 樣式的索引標籤控制項，會設定此延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="c4841-113">By default, creating the tab control with the **TCS\_FLATBUTTONS** style sets this extended style.</span></span> <span data-ttu-id="c4841-114">如果您不需要分隔符號，則應該在建立控制項之後移除此延伸樣式。</span><span class="sxs-lookup"><span data-stu-id="c4841-114">If you do not require separators, you should remove this extended style after creating the control.</span></span><br/> |
| <span id="TCS_EX_REGISTERDROP"></span><span id="tcs_ex_registerdrop"></span><dl> <span data-ttu-id="c4841-115"><dt>**TCS \_ EX \_ REGISTERDROP**</dt></span><span class="sxs-lookup"><span data-stu-id="c4841-115"><dt>**TCS\_EX\_REGISTERDROP**</dt></span></span> </dl>       | <span data-ttu-id="c4841-116">[版本 4.71](common-control-versions.md)。</span><span class="sxs-lookup"><span data-stu-id="c4841-116">[Version 4.71](common-control-versions.md).</span></span> <span data-ttu-id="c4841-117">當物件拖曳至控制項中的索引標籤專案上方時，此索引標籤控制項會產生 [TCN 的 \_ GETOBJECT](tcn-getobject.md) 通知碼，以要求卸載目標物件。</span><span class="sxs-lookup"><span data-stu-id="c4841-117">The tab control generates [TCN\_GETOBJECT](tcn-getobject.md) notification codes to request a drop target object when an object is dragged over the tab items in the control.</span></span> <span data-ttu-id="c4841-118">應用程式必須先呼叫 [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) 或 [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) ，才能設定此樣式。</span><span class="sxs-lookup"><span data-stu-id="c4841-118">The application must call [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) or [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) before setting this style.</span></span> <br/>                                                                                                                                               |



## <a name="requirements"></a><span data-ttu-id="c4841-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4841-119">Requirements</span></span>



| <span data-ttu-id="c4841-120">需求</span><span class="sxs-lookup"><span data-stu-id="c4841-120">Requirement</span></span> | <span data-ttu-id="c4841-121">值</span><span class="sxs-lookup"><span data-stu-id="c4841-121">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4841-122">標頭</span><span class="sxs-lookup"><span data-stu-id="c4841-122">Header</span></span><br/> | <dl> <span data-ttu-id="c4841-123"><dt>CommCtrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4841-123"><dt>CommCtrl.h</dt></span></span> </dl> |



 

