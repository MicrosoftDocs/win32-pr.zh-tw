---
title: AccNameContainsInvalidString
description: AccNameContainsInvalidString
ms.assetid: 392E4D10-4A8E-4118-B0E7-F74571812043
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 670672769c22cba556c164b8d03b2e9148fb8b1d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106996357"
---
# <a name="accnamecontainsinvalidstring"></a><span data-ttu-id="eaa2d-103">AccNameContainsInvalidString</span><span class="sxs-lookup"><span data-stu-id="eaa2d-103">AccNameContainsInvalidString</span></span>

## <a name="text"></a><span data-ttu-id="eaa2d-104">Text</span><span class="sxs-lookup"><span data-stu-id="eaa2d-104">Text</span></span>

<span data-ttu-id="eaa2d-105">accName 不能包含字串 {0}</span><span class="sxs-lookup"><span data-stu-id="eaa2d-105">accName should not contain the string {0}</span></span>

## <a name="type"></a><span data-ttu-id="eaa2d-106">類型</span><span class="sxs-lookup"><span data-stu-id="eaa2d-106">Type</span></span>

<span data-ttu-id="eaa2d-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="eaa2d-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="eaa2d-108">描述</span><span class="sxs-lookup"><span data-stu-id="eaa2d-108">Description</span></span>

<span data-ttu-id="eaa2d-109">專案名稱包含不正確字元 (這些字元會取代為 AccChecker) 。</span><span class="sxs-lookup"><span data-stu-id="eaa2d-109">The name of an element contains invalid characters (these characters are replaced by AccChecker).</span></span> <span data-ttu-id="eaa2d-110">例如，用來抓取專案之 MSAA 名稱的 [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) 方法會傳回字串，其中包含定位字元、換行字元或連字號字元。</span><span class="sxs-lookup"><span data-stu-id="eaa2d-110">For example, the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method used to retrieve the MSAA name of an element returns a string that contains tab, newline, or ampersand characters.</span></span>

<span data-ttu-id="eaa2d-111">這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員遇到問題，因為元素可能有 unpronounceable、非直覺的名稱。</span><span class="sxs-lookup"><span data-stu-id="eaa2d-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="eaa2d-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="eaa2d-112">Possible causes</span></span>

<span data-ttu-id="eaa2d-113">元素或其父系有不正確指派的名稱或標籤。</span><span class="sxs-lookup"><span data-stu-id="eaa2d-113">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="eaa2d-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="eaa2d-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eaa2d-115">**IAccessible：： get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="eaa2d-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="eaa2d-116">Name 屬性</span><span class="sxs-lookup"><span data-stu-id="eaa2d-116">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




