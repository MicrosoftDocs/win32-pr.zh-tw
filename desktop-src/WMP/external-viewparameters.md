---
title: ViewParameters
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |ViewParameters
ms.assetid: 0afabe35-2857-413a-a662-1a76d3fb75fe
keywords:
- ViewParameters Windows Media Player 的外部
topic_type:
- apiref
api_name:
- External.viewParameters
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ea0adec580a68bd3f6b92beef1de814729848179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995940"
---
# <a name="externalviewparameters"></a><span data-ttu-id="c8fa7-105">ViewParameters</span><span class="sxs-lookup"><span data-stu-id="c8fa7-105">External.viewParameters</span></span>

> [!Note]  
> <span data-ttu-id="c8fa7-106">本主題說明針對線上商店使用而設計的功能。</span><span class="sxs-lookup"><span data-stu-id="c8fa7-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="c8fa7-107">不支援在線上商店的內容之外使用這項功能。</span><span class="sxs-lookup"><span data-stu-id="c8fa7-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="c8fa7-108">**ViewParameters** 屬性會在 Windows Media Player 中，抓取與目前視圖相關聯的參數。</span><span class="sxs-lookup"><span data-stu-id="c8fa7-108">The **viewParameters** property retrieves parameters associated with the current view in Windows Media Player.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8fa7-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="c8fa7-109">Syntax</span></span>

<span data-ttu-id="c8fa7-110">**viewParameters**</span><span class="sxs-lookup"><span data-stu-id="c8fa7-110">**window.external.viewParameters**</span></span>

## <a name="possible-values"></a><span data-ttu-id="c8fa7-111">可能的值</span><span class="sxs-lookup"><span data-stu-id="c8fa7-111">Possible Values</span></span>

<span data-ttu-id="c8fa7-112">這個屬性會傳回唯讀 **字串**。</span><span class="sxs-lookup"><span data-stu-id="c8fa7-112">This property returns a read-only **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c8fa7-113">備註</span><span class="sxs-lookup"><span data-stu-id="c8fa7-113">Remarks</span></span>

<span data-ttu-id="c8fa7-114">這個屬性會抓取線上商店先前設定的參數。</span><span class="sxs-lookup"><span data-stu-id="c8fa7-114">This property retrieves parameters that were previously set by the online store.</span></span> <span data-ttu-id="c8fa7-115">例如，線上商店可以在 [changeView](external-changeview.md)方法的 *ViewParams* 參數或 [changeViewOnlineList](external-changeviewonlinelist.md)方法的 *Params* 參數中指定 view 參數。</span><span class="sxs-lookup"><span data-stu-id="c8fa7-115">For example, the online store can specify view parameters in the *ViewParams* parameter of the [changeView](external-changeview.md) method or the *Params* parameter of the [changeViewOnlineList](external-changeviewonlinelist.md) method.</span></span>

<span data-ttu-id="c8fa7-116">Windows Media Player 不會解讀 View 參數。</span><span class="sxs-lookup"><span data-stu-id="c8fa7-116">View parameters are not interpreted by Windows Media Player.</span></span> <span data-ttu-id="c8fa7-117">它們是由線上商店所建立，而且只有線上商店才有意義。</span><span class="sxs-lookup"><span data-stu-id="c8fa7-117">They are created by the online store and have meaning only to the online store.</span></span>

## <a name="requirements"></a><span data-ttu-id="c8fa7-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="c8fa7-118">Requirements</span></span>



| <span data-ttu-id="c8fa7-119">需求</span><span class="sxs-lookup"><span data-stu-id="c8fa7-119">Requirement</span></span> | <span data-ttu-id="c8fa7-120">值</span><span class="sxs-lookup"><span data-stu-id="c8fa7-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c8fa7-121">版本</span><span class="sxs-lookup"><span data-stu-id="c8fa7-121">Version</span></span><br/> | <span data-ttu-id="c8fa7-122">Windows Media Player 11。</span><span class="sxs-lookup"><span data-stu-id="c8fa7-122">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="c8fa7-123">DLL</span><span class="sxs-lookup"><span data-stu-id="c8fa7-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="c8fa7-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8fa7-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c8fa7-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c8fa7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c8fa7-126">**類型1線上商店的外部物件**</span><span class="sxs-lookup"><span data-stu-id="c8fa7-126">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





