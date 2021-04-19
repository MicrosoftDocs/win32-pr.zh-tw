---
title: AccNameLengthTooLong
description: AccNameLengthTooLong
ms.assetid: 68997AE9-91FC-4DAD-8356-FEE6C6919939
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d1efcb2b7d13c83a5972cb6e100d70500f9c5ed
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967446"
---
# <a name="accnamelengthtoolong"></a><span data-ttu-id="5aa16-103">AccNameLengthTooLong</span><span class="sxs-lookup"><span data-stu-id="5aa16-103">AccNameLengthTooLong</span></span>

## <a name="text"></a><span data-ttu-id="5aa16-104">Text</span><span class="sxs-lookup"><span data-stu-id="5aa16-104">Text</span></span>

<span data-ttu-id="5aa16-105">元素的名稱不應傳回長度超過字元的字串 {0}</span><span class="sxs-lookup"><span data-stu-id="5aa16-105">Element's name should not return a string longer than {0} character</span></span>

## <a name="type"></a><span data-ttu-id="5aa16-106">類型</span><span class="sxs-lookup"><span data-stu-id="5aa16-106">Type</span></span>

<span data-ttu-id="5aa16-107">錯誤</span><span class="sxs-lookup"><span data-stu-id="5aa16-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="5aa16-108">描述</span><span class="sxs-lookup"><span data-stu-id="5aa16-108">Description</span></span>

<span data-ttu-id="5aa16-109">元素名稱包含太多字元。</span><span class="sxs-lookup"><span data-stu-id="5aa16-109">The name of an element contains too many characters.</span></span> <span data-ttu-id="5aa16-110">例如，用來取出元素之 MSAA 名稱的 [**get \_ accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) 方法會傳回大於32000個字元限制的字串。</span><span class="sxs-lookup"><span data-stu-id="5aa16-110">For example, the [**get\_accName**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname) method used to retrieve the MSAA name of an element returns a string greater than the limit of 32000 characters.</span></span>

<span data-ttu-id="5aa16-111">這個問題會讓依賴螢幕讀取器和鍵盤進行導覽的人員遇到問題，因為元素可能有 unpronounceable、非直覺的名稱。</span><span class="sxs-lookup"><span data-stu-id="5aa16-111">This issue causes problems for people who rely on a screen-reader and keyboard for navigation because an element might have an unpronounceable, non-intuitive name.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="5aa16-112">可能的原因</span><span class="sxs-lookup"><span data-stu-id="5aa16-112">Possible causes</span></span>

<span data-ttu-id="5aa16-113">元素或其父系有不正確指派的名稱或標籤。</span><span class="sxs-lookup"><span data-stu-id="5aa16-113">The element or its parent has an incorrectly assigned name or label.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5aa16-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="5aa16-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5aa16-115">**IAccessible：： get \_ accName**</span><span class="sxs-lookup"><span data-stu-id="5aa16-115">**IAccessible::get\_accName**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accname)
</dt> <dt>

[<span data-ttu-id="5aa16-116">Name 屬性</span><span class="sxs-lookup"><span data-stu-id="5aa16-116">Name Property</span></span>](name-property.md)
</dt> </dl>

 

 




