---
title: SavePreference
description: SavePreference 方法會在登錄中儲存喜好設定。
ms.assetid: 4c253d8d-15c0-4c18-bb3f-fdbcef79c999
keywords:
- SavePreference Windows Media Player
topic_type:
- apiref
api_name:
- THEME.savePreference
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 89633d71dd75f4ef5e804aefddc85cf00ad5c03b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981656"
---
# <a name="themesavepreference"></a><span data-ttu-id="2a435-104">SavePreference</span><span class="sxs-lookup"><span data-stu-id="2a435-104">THEME.savePreference</span></span>

<span data-ttu-id="2a435-105">**SavePreference** 方法會在登錄中儲存喜好設定。</span><span class="sxs-lookup"><span data-stu-id="2a435-105">The **savePreference** method saves a preference in the registry.</span></span>

``` syntax
        theme.savePreference(theKey, theValue)
```

## <a name="parameters"></a><span data-ttu-id="2a435-106">參數</span><span class="sxs-lookup"><span data-stu-id="2a435-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a435-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span><span class="sxs-lookup"><span data-stu-id="2a435-107"><span id="theKey"></span><span id="thekey"></span><span id="THEKEY"></span>*theKey*</span></span>
</dt> <dd>

<span data-ttu-id="2a435-108">**字串**，指定要儲存之喜好設定值的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="2a435-108">A **String** specifying the key of the preference value to save.</span></span>

</dd> <dt>

<span data-ttu-id="2a435-109"><span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*表示*</span><span class="sxs-lookup"><span data-stu-id="2a435-109"><span id="theValue"></span><span id="thevalue"></span><span id="THEVALUE"></span>*theValue*</span></span>
</dt> <dd>

<span data-ttu-id="2a435-110">**字串**，指定要儲存的值。</span><span class="sxs-lookup"><span data-stu-id="2a435-110">A **String** specifying the value to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a435-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a435-111">Return Value</span></span>

<span data-ttu-id="2a435-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="2a435-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a435-113">備註</span><span class="sxs-lookup"><span data-stu-id="2a435-113">Remarks</span></span>

<span data-ttu-id="2a435-114">喜好設定是一組索引鍵/值組，可以儲存在登錄中，以保留執行之間 Windows Media Player 狀態的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2a435-114">A preference is a key/value pair that can be stored in the registry to retain information about the state of Windows Media Player between runs.</span></span> <span data-ttu-id="2a435-115">例如，您可以使用這項功能來儲存自訂設定，這樣就不需要在每次啟動 Windows Media Player 時重新輸入。</span><span class="sxs-lookup"><span data-stu-id="2a435-115">This feature can be used, for example, to save customization settings so that they won't have to be re-entered each time Windows Media Player is started.</span></span>

<span data-ttu-id="2a435-116">喜好設定不會加密，因此不是保存資料的安全方法。</span><span class="sxs-lookup"><span data-stu-id="2a435-116">Preferences are not encrypted and therefore are not a secure method for persisting data.</span></span> <span data-ttu-id="2a435-117">請勿使用喜好設定來儲存私用資料。</span><span class="sxs-lookup"><span data-stu-id="2a435-117">Do not use preferences to store private data.</span></span>

## <a name="examples"></a><span data-ttu-id="2a435-118">範例</span><span class="sxs-lookup"><span data-stu-id="2a435-118">Examples</span></span>


```JScript
<THEME>
  <VIEW 
    id="View1" 
    onclose="jscript:theme.savePreference('drawer1','open');
             theme.savePreference('drawer2','close')">
  </VIEW>
</THEME>
```



## <a name="requirements"></a><span data-ttu-id="2a435-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a435-119">Requirements</span></span>



| <span data-ttu-id="2a435-120">需求</span><span class="sxs-lookup"><span data-stu-id="2a435-120">Requirement</span></span> | <span data-ttu-id="2a435-121">值</span><span class="sxs-lookup"><span data-stu-id="2a435-121">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="2a435-122">版本</span><span class="sxs-lookup"><span data-stu-id="2a435-122">Version</span></span><br/> | <span data-ttu-id="2a435-123">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="2a435-123">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2a435-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a435-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a435-125">**主題元素**</span><span class="sxs-lookup"><span data-stu-id="2a435-125">**THEME Element**</span></span>](theme-element.md)
</dt> <dt>

[<span data-ttu-id="2a435-126">**LoadPreference**</span><span class="sxs-lookup"><span data-stu-id="2a435-126">**THEME.loadPreference**</span></span>](theme-loadpreference.md)
</dt> </dl>

 

 





