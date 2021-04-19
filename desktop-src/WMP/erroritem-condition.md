---
title: ErrorItem。條件
description: Condition 屬性會抓取指出錯誤條件的值。
ms.assetid: efb54b48-cfaa-479f-9ee6-ce6724dca24c
keywords:
- ErrorItem 條件 Windows Media Player
topic_type:
- apiref
api_name:
- ErrorItem.condition
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c498e7479a7a3e067dea2d8a562800351effd672
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983162"
---
# <a name="erroritemcondition"></a><span data-ttu-id="d8d7e-104">ErrorItem。條件</span><span class="sxs-lookup"><span data-stu-id="d8d7e-104">ErrorItem.condition</span></span>

<span data-ttu-id="d8d7e-105">**Condition** 屬性會抓取指出錯誤條件的值。</span><span class="sxs-lookup"><span data-stu-id="d8d7e-105">The **condition** property retrieves a value indicating the condition for the error.</span></span>

``` syntax
player.error.item(
        index
        ).condition
      
```

## <a name="possible-values"></a><span data-ttu-id="d8d7e-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="d8d7e-106">Possible Values</span></span>

<span data-ttu-id="d8d7e-107">這個屬性是唯讀的 **數位** (**long**) ，代表條件碼。</span><span class="sxs-lookup"><span data-stu-id="d8d7e-107">This property is a read-only **Number** (**long**) that represents the condition code.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8d7e-108">備註</span><span class="sxs-lookup"><span data-stu-id="d8d7e-108">Remarks</span></span>

<span data-ttu-id="d8d7e-109">條件碼是 Microsoft 用來為技術支援人員提供其他資訊的值。</span><span class="sxs-lookup"><span data-stu-id="d8d7e-109">The condition code is a value that is used by Microsoft to provide additional information for technical support personnel.</span></span>

<span data-ttu-id="d8d7e-110">**Windows Media Player 10** 行動裝置版：此屬性一律會傳回0。</span><span class="sxs-lookup"><span data-stu-id="d8d7e-110">**Windows Media Player 10 Mobile:** This property always returns 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8d7e-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8d7e-111">Requirements</span></span>



| <span data-ttu-id="d8d7e-112">需求</span><span class="sxs-lookup"><span data-stu-id="d8d7e-112">Requirement</span></span> | <span data-ttu-id="d8d7e-113">值</span><span class="sxs-lookup"><span data-stu-id="d8d7e-113">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d8d7e-114">版本</span><span class="sxs-lookup"><span data-stu-id="d8d7e-114">Version</span></span><br/> | <span data-ttu-id="d8d7e-115">Windows Media Player  9  系列或更新的版本。</span><span class="sxs-lookup"><span data-stu-id="d8d7e-115">Windows Media Player 9 Series or later.</span></span><br/>                                 |
| <span data-ttu-id="d8d7e-116">DLL</span><span class="sxs-lookup"><span data-stu-id="d8d7e-116">DLL</span></span><br/>     | <dl> <span data-ttu-id="d8d7e-117"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8d7e-117"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8d7e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8d7e-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8d7e-119">**ErrorItem 物件**</span><span class="sxs-lookup"><span data-stu-id="d8d7e-119">**ErrorItem Object**</span></span>](erroritem-object.md)
</dt> </dl>

 

 





