---
title: MissingItemInTabOrder
description: MissingItemInTabOrder
ms.assetid: 49DE892E-1B15-4F46-B316-217CC76AA1A9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9841ab71e9f5d40cf25454e737b9790ce27a04de
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682412"
---
# <a name="missingitemintaborder"></a><span data-ttu-id="7d57b-103">MissingItemInTabOrder</span><span class="sxs-lookup"><span data-stu-id="7d57b-103">MissingItemInTabOrder</span></span>

## <a name="text"></a><span data-ttu-id="7d57b-104">Text</span><span class="sxs-lookup"><span data-stu-id="7d57b-104">Text</span></span>

<span data-ttu-id="7d57b-105">這個元素似乎是 tabbable，但不在定位順序中。</span><span class="sxs-lookup"><span data-stu-id="7d57b-105">This element appears to be tabbable but is not in the tab order.</span></span>

## <a name="type"></a><span data-ttu-id="7d57b-106">類型</span><span class="sxs-lookup"><span data-stu-id="7d57b-106">Type</span></span>

<span data-ttu-id="7d57b-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="7d57b-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="7d57b-108">描述</span><span class="sxs-lookup"><span data-stu-id="7d57b-108">Description</span></span>

<span data-ttu-id="7d57b-109">您無法使用標準鍵盤流覽 (Tab 或 Shift + Tab) 來存取可設定焦點的元素。</span><span class="sxs-lookup"><span data-stu-id="7d57b-109">A focusable element is not accessible using standard keyboard navigation (Tab or Shift+Tab).</span></span> <span data-ttu-id="7d57b-110">例如，元素未標示為定位停駐點或指派索引標籤索引。</span><span class="sxs-lookup"><span data-stu-id="7d57b-110">For example, the element has not been marked as a tab stop or assigned a tab index.</span></span> <span data-ttu-id="7d57b-111">此問題會造成依賴螢幕讀取器和鍵盤進行流覽的人員發生問題，原因如下：</span><span class="sxs-lookup"><span data-stu-id="7d57b-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because:</span></span>

-   <span data-ttu-id="7d57b-112">元素無法探索。</span><span class="sxs-lookup"><span data-stu-id="7d57b-112">The element is not discoverable.</span></span>
-   <span data-ttu-id="7d57b-113">如果元素是自訂清單控制項的子系，則表示可以使用箭號或頁面索引鍵來導覽子項目的提示可能會遺失。</span><span class="sxs-lookup"><span data-stu-id="7d57b-113">If the element is a child of a custom list control, cues indicating the child element can be navigated using the Arrow or Page keys may be missing.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="7d57b-114">可能的原因</span><span class="sxs-lookup"><span data-stu-id="7d57b-114">Possible causes</span></span>

-   <span data-ttu-id="7d57b-115">未正確設定元素或其父系的 MSAA 角色。</span><span class="sxs-lookup"><span data-stu-id="7d57b-115">The MSAA role of the element or its parent is not set correctly.</span></span> <span data-ttu-id="7d57b-116">例如，如果清單視圖控制項中的所有清單專案都不會透過 MSAA 以角色系統專案識別碼公開 \_ \_ ，驗證就會失敗，因為無法使用 Tab 鍵來存取清單專案。</span><span class="sxs-lookup"><span data-stu-id="7d57b-116">For example, if all list items in a list view control are not exposed through MSAA as a ROLE\_SYSTEM\_LISTITEM, the verification fails because the list items are not accessible using the Tab key.</span></span>
-   <span data-ttu-id="7d57b-117">元素或其父代是未正確執行 tab 鍵的自訂控制項。</span><span class="sxs-lookup"><span data-stu-id="7d57b-117">The element or its parent is a custom control that doesn't implement tabbing correctly.</span></span> <span data-ttu-id="7d57b-118">例如，[MSAA 狀態] 屬性永遠不會設定為 [狀態 \_ 系統可 \_ 設定]。</span><span class="sxs-lookup"><span data-stu-id="7d57b-118">For example, the MSAA State property is never set to STATE\_SYSTEM\_FOCUSABLE.</span></span>
-   <span data-ttu-id="7d57b-119">做為其他元素之容器的專案，已選取要進行驗證，但不支援鍵盤流覽本身。</span><span class="sxs-lookup"><span data-stu-id="7d57b-119">An element that acts as a container for other elements was selected for verification but does not support keyboard navigation itself.</span></span> <span data-ttu-id="7d57b-120">例如，無法使用 TAB 鍵來存取工具列和其子項目。</span><span class="sxs-lookup"><span data-stu-id="7d57b-120">For example, a toolbar and its child elements are not accessible using the TAB key.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7d57b-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="7d57b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7d57b-122">鍵盤使用者介面設計指導方針</span><span class="sxs-lookup"><span data-stu-id="7d57b-122">Guidelines for Keyboard User Interface Design</span></span>](/previous-versions/windows/desktop/dnacc/guidelines-for-keyboard-user-interface-design)
</dt> </dl>

 

 