---
title: LoadPreference
description: LoadPreference 方法會從登錄載入喜好設定。
ms.assetid: 51d6b0f8-f1fd-4999-a575-0b7c177b2bc8
keywords:
- LoadPreference Windows Media Player
topic_type:
- apiref
api_name:
- THEME.loadPreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d92135113495ac32ca81f602ea5836332159164c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979619"
---
# <a name="themeloadpreference"></a><span data-ttu-id="97e90-104">LoadPreference</span><span class="sxs-lookup"><span data-stu-id="97e90-104">THEME.loadPreference</span></span>

<span data-ttu-id="97e90-105">**LoadPreference** 方法會從登錄載入喜好設定。</span><span class="sxs-lookup"><span data-stu-id="97e90-105">The **loadPreference** method loads a preference from the registry.</span></span>

``` syntax
        theme.loadPreference(theKey)
```

## <a name="parameters"></a><span data-ttu-id="97e90-106">參數</span><span class="sxs-lookup"><span data-stu-id="97e90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97e90-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span><span class="sxs-lookup"><span data-stu-id="97e90-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span></span>
</dt> <dd>

<span data-ttu-id="97e90-108">**字串**，指定要載入之喜好設定值的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="97e90-108">A **String** specifying the key of the preference value to load.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97e90-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="97e90-109">Return Value</span></span>

<span data-ttu-id="97e90-110">這個方法會傳回 **字串**。</span><span class="sxs-lookup"><span data-stu-id="97e90-110">This method returns a **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="97e90-111">備註</span><span class="sxs-lookup"><span data-stu-id="97e90-111">Remarks</span></span>

<span data-ttu-id="97e90-112">喜好設定是一組索引鍵/值組，可以儲存在登錄中，以保留執行之間 Windows Media Player 狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="97e90-112">A preference is a key/value pair that can be stored in the registry to retain information about the state of the Windows Media Player between runs.</span></span> <span data-ttu-id="97e90-113">例如，您可以使用這項功能來儲存自訂設定，這樣就不需要在每次啟動 Windows Media Player 時重新輸入。</span><span class="sxs-lookup"><span data-stu-id="97e90-113">This feature can be used, for example, to save customization settings so that they won't have to be re-entered each time Windows Media Player is started.</span></span>

<span data-ttu-id="97e90-114">喜好設定不會加密，因此不是保存資料的安全方法。</span><span class="sxs-lookup"><span data-stu-id="97e90-114">Preferences are not encrypted and therefore are not a secure method for persisting data.</span></span> <span data-ttu-id="97e90-115">請勿使用喜好設定來儲存私用資料。</span><span class="sxs-lookup"><span data-stu-id="97e90-115">Do not use preferences to store private data.</span></span>

## <a name="requirements"></a><span data-ttu-id="97e90-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="97e90-116">Requirements</span></span>



| <span data-ttu-id="97e90-117">需求</span><span class="sxs-lookup"><span data-stu-id="97e90-117">Requirement</span></span> | <span data-ttu-id="97e90-118">值</span><span class="sxs-lookup"><span data-stu-id="97e90-118">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="97e90-119">版本</span><span class="sxs-lookup"><span data-stu-id="97e90-119">Version</span></span><br/> | <span data-ttu-id="97e90-120">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="97e90-120">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97e90-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97e90-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97e90-122">**主題元素**</span><span class="sxs-lookup"><span data-stu-id="97e90-122">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="97e90-123">**SavePreference**</span><span class="sxs-lookup"><span data-stu-id="97e90-123">**THEME.savePreference**</span></span>](theme-savepreference.md)
</dt> </dl>

 

 





