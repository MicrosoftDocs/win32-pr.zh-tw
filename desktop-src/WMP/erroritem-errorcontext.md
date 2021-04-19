---
title: ErrorItem.errorCoNtext
description: ErrorCoNtext 屬性會抓取指出錯誤內容的值。
ms.assetid: 700d2bf0-dd3b-4211-99ea-58f952cf24b0
keywords:
- ErrorItem. errorCoNtext Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.errorContext
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9b9ed91d34645f08e7d3d28860ced9ca51420dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986176"
---
# <a name="erroritemerrorcontext"></a><span data-ttu-id="55d4b-104">ErrorItem.errorCoNtext</span><span class="sxs-lookup"><span data-stu-id="55d4b-104">ErrorItem.errorContext</span></span>

<span data-ttu-id="55d4b-105">**ErrorCoNtext** 屬性會抓取指出錯誤內容的值。</span><span class="sxs-lookup"><span data-stu-id="55d4b-105">The **errorContext** property retrieves a value indicating the context of the error.</span></span>

``` syntax
player.error.item(
        index
        ).errorContext
```

## <a name="possible-values"></a><span data-ttu-id="55d4b-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="55d4b-106">Possible Values</span></span>

<span data-ttu-id="55d4b-107">這個屬性是唯讀 **字串** ，代表錯誤內容代碼。</span><span class="sxs-lookup"><span data-stu-id="55d4b-107">This property is a read-only **String** that represents the error context code.</span></span>

## <a name="remarks"></a><span data-ttu-id="55d4b-108">備註</span><span class="sxs-lookup"><span data-stu-id="55d4b-108">Remarks</span></span>

<span data-ttu-id="55d4b-109">錯誤內容是 Microsoft 用來為技術支援人員提供其他資訊的資訊。</span><span class="sxs-lookup"><span data-stu-id="55d4b-109">The error context is information that is used by Microsoft to provide additional information for technical support personnel.</span></span>

<span data-ttu-id="55d4b-110">**Windows Media Player 10** 行動裝置版：此屬性一律會傳回空字串。</span><span class="sxs-lookup"><span data-stu-id="55d4b-110">**Windows Media Player 10 Mobile:** This property always returns an empty string.</span></span>

## <a name="requirements"></a><span data-ttu-id="55d4b-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="55d4b-111">Requirements</span></span>



| <span data-ttu-id="55d4b-112">需求</span><span class="sxs-lookup"><span data-stu-id="55d4b-112">Requirement</span></span> | <span data-ttu-id="55d4b-113">值</span><span class="sxs-lookup"><span data-stu-id="55d4b-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="55d4b-114">版本</span><span class="sxs-lookup"><span data-stu-id="55d4b-114">Version</span></span><br/> | <span data-ttu-id="55d4b-115">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="55d4b-115">Windows Media Player version 7.0 or later</span></span><br/>                               |
| <span data-ttu-id="55d4b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="55d4b-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="55d4b-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55d4b-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55d4b-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55d4b-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55d4b-119">**ErrorItem 物件**</span><span class="sxs-lookup"><span data-stu-id="55d4b-119">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





