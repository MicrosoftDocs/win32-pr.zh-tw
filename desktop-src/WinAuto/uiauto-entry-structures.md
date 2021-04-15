---
title: 消費者介面自動化結構
description: 本節說明消費者介面自動化用戶端應用程式和 Microsoft Win32 的消費者介面自動化提供者所使用的結構。
ms.assetid: 37d6a7c0-6925-443b-aa21-da2a14a9ddad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55ddf9086f0714665c944a5a80e53e63eb3a91a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462101"
---
# <a name="ui-automation-structures"></a><span data-ttu-id="13db7-103">消費者介面自動化結構</span><span class="sxs-lookup"><span data-stu-id="13db7-103">UI Automation Structures</span></span>

<span data-ttu-id="13db7-104">本節說明消費者介面自動化用戶端應用程式和 Microsoft Win32 的消費者介面自動化提供者所使用的結構。</span><span class="sxs-lookup"><span data-stu-id="13db7-104">This section describes the structures used by UI Automation client applications and UI Automation provider for Microsoft Win32.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="13db7-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="13db7-105">In this section</span></span>



| <span data-ttu-id="13db7-106">結構</span><span class="sxs-lookup"><span data-stu-id="13db7-106">Structure</span></span>                                                                            | <span data-ttu-id="13db7-107">Description</span><span class="sxs-lookup"><span data-stu-id="13db7-107">Description</span></span>                                                                                   |
|--------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="13db7-108">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="13db7-108">**ExtendedProperty**</span></span>](/windows/desktop/api/UIAutomationClient/ns-uiautomationclient-extendedproperty)<br/>                       | <span data-ttu-id="13db7-109">包含擴充屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="13db7-109">Contains information about an extended property.</span></span> <br/>                                  |
| [<span data-ttu-id="13db7-110">**UIAutomationEventInfo**</span><span class="sxs-lookup"><span data-stu-id="13db7-110">**UIAutomationEventInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationeventinfo)<br/>       | <span data-ttu-id="13db7-111">包含自訂事件的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="13db7-111">Contains information about a custom event.</span></span><br/>                                         |
| [<span data-ttu-id="13db7-112">**UIAutomationMethodInfo**</span><span class="sxs-lookup"><span data-stu-id="13db7-112">**UIAutomationMethodInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationmethodinfo)<br/>     | <span data-ttu-id="13db7-113">包含自訂控制項模式所支援之方法的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="13db7-113">Contains information about a method that is supported by a custom control pattern.</span></span><br/> |
| [<span data-ttu-id="13db7-114">**UIAutomationParameter**</span><span class="sxs-lookup"><span data-stu-id="13db7-114">**UIAutomationParameter**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationparameter)<br/>       | <span data-ttu-id="13db7-115">包含自訂控制項模式之參數的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="13db7-115">Contains information about a parameter of a custom control pattern.</span></span><br/>                |
| [<span data-ttu-id="13db7-116">**UIAutomationPatternInfo**</span><span class="sxs-lookup"><span data-stu-id="13db7-116">**UIAutomationPatternInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpatterninfo)<br/>   | <span data-ttu-id="13db7-117">包含自訂控制項模式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="13db7-117">Contains information about a custom control pattern.</span></span><br/>                               |
| [<span data-ttu-id="13db7-118">**UIAutomationPropertyInfo**</span><span class="sxs-lookup"><span data-stu-id="13db7-118">**UIAutomationPropertyInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiautomationpropertyinfo)<br/> | <span data-ttu-id="13db7-119">包含自訂屬性的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="13db7-119">Contains information about a custom property.</span></span><br/>                                      |
| [<span data-ttu-id="13db7-120">**UiaChangeInfo**</span><span class="sxs-lookup"><span data-stu-id="13db7-120">**UiaChangeInfo**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiachangeinfo)<br/>                                    | <span data-ttu-id="13db7-121">包含發生之消費者介面自動化變更的相關資料。</span><span class="sxs-lookup"><span data-stu-id="13db7-121">Contains data about a UI Automation change that occurred.</span></span><br/>                          |
| [<span data-ttu-id="13db7-122">**UiaPoint**</span><span class="sxs-lookup"><span data-stu-id="13db7-122">**UiaPoint**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiapoint)<br/>                                 | <span data-ttu-id="13db7-123">包含點的座標。</span><span class="sxs-lookup"><span data-stu-id="13db7-123">Contains the coordinates of a point.</span></span> <br/>                                              |
| [<span data-ttu-id="13db7-124">**UiaRect**</span><span class="sxs-lookup"><span data-stu-id="13db7-124">**UiaRect**</span></span>](/windows/desktop/api/UIAutomationCore/ns-uiautomationcore-uiarect)<br/>                                   | <span data-ttu-id="13db7-125">包含矩形的位置和大小（以螢幕座標表示）。</span><span class="sxs-lookup"><span data-stu-id="13db7-125">Contains the position and size of a rectangle, in screen coordinates.</span></span><br/>              |



 

 

 





