---
title: 'VariantNotInt (CheckState) '
description: 'VariantNotInt (CheckState) '
ms.assetid: 77140193-22E8-427D-AE9C-FEC6B93483DD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d951a51ae6aa3f4d9454fc95a56c76cfe30500c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183516"
---
# <a name="variantnotint-checkstate"></a><span data-ttu-id="60275-103">VariantNotInt (CheckState) </span><span class="sxs-lookup"><span data-stu-id="60275-103">VariantNotInt (CheckState)</span></span>

## <a name="text"></a><span data-ttu-id="60275-104">Text</span><span class="sxs-lookup"><span data-stu-id="60275-104">Text</span></span>

<span data-ttu-id="60275-105">從傳回的變異數 {0} 應為， {1} 但為 {2} 。</span><span class="sxs-lookup"><span data-stu-id="60275-105">The variant returned from {0} should be an {1} but is a {2}.</span></span>

## <a name="type"></a><span data-ttu-id="60275-106">類型</span><span class="sxs-lookup"><span data-stu-id="60275-106">Type</span></span>

<span data-ttu-id="60275-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="60275-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="60275-108">描述</span><span class="sxs-lookup"><span data-stu-id="60275-108">Description</span></span>

<span data-ttu-id="60275-109">元素報告的 MSAA 狀態無效。</span><span class="sxs-lookup"><span data-stu-id="60275-109">An element is reporting an invalid MSAA state.</span></span> <span data-ttu-id="60275-110">例如，用來取出專案之 MSAA 狀態的 [**get \_ accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) 方法，應該傳回代表其中一個 msaa 狀態常數的整數值，但改為傳回另一個 variant。</span><span class="sxs-lookup"><span data-stu-id="60275-110">For example, the [**get\_accState**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate) method used to retrieve the MSAA state of an element should return an integer value that represents one of the MSAA state constants, but is returning another variant instead.</span></span>

<span data-ttu-id="60275-111">這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員遇到問題，因為可能會向使用者回報不正確的元素狀態。</span><span class="sxs-lookup"><span data-stu-id="60275-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an incorrect element state might be reported to the user.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="60275-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="60275-112">Possible causes</span></span>

<span data-ttu-id="60275-113">元素或其父系的 MSAA 狀態設定不當。</span><span class="sxs-lookup"><span data-stu-id="60275-113">The element or its parent has an MSAA state set inappropriately.</span></span>

## <a name="related-topics"></a><span data-ttu-id="60275-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="60275-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60275-115">**IAccessible：： get \_ accState**</span><span class="sxs-lookup"><span data-stu-id="60275-115">**IAccessible::get\_accState**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accstate)
</dt> <dt>

[<span data-ttu-id="60275-116">**物件狀態常數**</span><span class="sxs-lookup"><span data-stu-id="60275-116">**Object State Constants**</span></span>](object-state-constants.md)
</dt> </dl>

 

 




