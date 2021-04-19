---
description: 以更完整的方式檢查提供者文字，而不是 ISpellCheckProvider：： Check。
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: IComprehensiveSpellCheckProvider：： ComprehensiveCheck 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IComprehensiveSpellCheckProvider.ComprehensiveCheck
api_type:
- COM
api_location:
- spellcheckprovider.h
ms.openlocfilehash: d999a90166e0d54d537abc84c30f6c4e0ee3768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977105"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a><span data-ttu-id="6c6da-103">IComprehensiveSpellCheckProvider：： ComprehensiveCheck 方法</span><span class="sxs-lookup"><span data-stu-id="6c6da-103">IComprehensiveSpellCheckProvider::ComprehensiveCheck method</span></span>

<span data-ttu-id="6c6da-104">以更完整的方式檢查提供者文字，而不是 [**ISpellCheckProvider：： check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)。</span><span class="sxs-lookup"><span data-stu-id="6c6da-104">Spell-check the provider text in a more thorough manner than [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span></span>

## <a name="syntax"></a><span data-ttu-id="6c6da-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c6da-105">Syntax</span></span>


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a><span data-ttu-id="6c6da-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c6da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c6da-107">*文字* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c6da-107">*text* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6da-108">要檢查的文字。</span><span class="sxs-lookup"><span data-stu-id="6c6da-108">The text to check.</span></span>

</dd> <dt>

<span data-ttu-id="6c6da-109">*結果* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6c6da-109">*result* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6c6da-110">檢查此文字的結果，如拼寫錯誤的列舉 ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)) （如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="6c6da-110">The result of checking this text, as an enumeration of spelling errors ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)), if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c6da-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c6da-111">Return value</span></span>

<span data-ttu-id="6c6da-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="6c6da-112">This method can return one of these values.</span></span>



| <span data-ttu-id="6c6da-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c6da-113">Return value</span></span>                                                                             | <span data-ttu-id="6c6da-114">描述</span><span class="sxs-lookup"><span data-stu-id="6c6da-114">Description</span></span>                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="6c6da-115"><dt>S \_ 確定</dt></span><span class="sxs-lookup"><span data-stu-id="6c6da-115"><dt>S\_OK</dt></span></span> </dl>         | <span data-ttu-id="6c6da-116">成功。</span><span class="sxs-lookup"><span data-stu-id="6c6da-116">Successful.</span></span><br/>                |
| <dl> <span data-ttu-id="6c6da-117"><dt>E \_ INVALIDARG</dt></span><span class="sxs-lookup"><span data-stu-id="6c6da-117"><dt>E\_INVALIDARG</dt></span></span> </dl> | <span data-ttu-id="6c6da-118">*文字* 是空字串。</span><span class="sxs-lookup"><span data-stu-id="6c6da-118">*text* is an empty string.</span></span><br/> |
| <dl> <span data-ttu-id="6c6da-119"><dt>E \_ 指標</dt></span><span class="sxs-lookup"><span data-stu-id="6c6da-119"><dt>E\_POINTER</dt></span></span> </dl>    | <span data-ttu-id="6c6da-120">*文字* 是 null 指標。</span><span class="sxs-lookup"><span data-stu-id="6c6da-120">*text* is a null pointer.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="6c6da-121">備註</span><span class="sxs-lookup"><span data-stu-id="6c6da-121">Remarks</span></span>

<span data-ttu-id="6c6da-122">這個介面不需要由拼寫檢查提供者來執行。</span><span class="sxs-lookup"><span data-stu-id="6c6da-122">This interface isn't required to be implemented by a spell check provider.</span></span> <span data-ttu-id="6c6da-123">但是，如果提供者支援兩種拼寫檢查的「模式」 (更快速且更慢但更徹底的) ，則應該在執行 [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) 的相同物件中執行這個介面，以支援更徹底的檢查模式。</span><span class="sxs-lookup"><span data-stu-id="6c6da-123">But if the provider supports two "modes" of spell checking (a faster one and a slower but more thorough one), it should implement this interface in the same object that implements [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) to support the more thorough checking mode.</span></span> <span data-ttu-id="6c6da-124">當用戶端呼叫 [**ISpellChecker：： ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)時，拼寫檢查功能將會對 [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)的提供者進行 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))程式，並在支援介面時呼叫 **IComprehensiveSpellCheckProvider. ComprehensiveCheck** 。</span><span class="sxs-lookup"><span data-stu-id="6c6da-124">When a client calls [**ISpellChecker::ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck), the spell checking functionality will [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) the provider for [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider), and call **IComprehensiveSpellCheckProvider.ComprehensiveCheck** if the interface is supported.</span></span> <span data-ttu-id="6c6da-125">如果介面不受支援，則會以無訊息模式切換回 [**ISpellCheckProvider：： Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)。</span><span class="sxs-lookup"><span data-stu-id="6c6da-125">If the interface isn't supported, it will silently fall back to [**ISpellCheckProvider::Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check).</span></span>

## <a name="see-also"></a><span data-ttu-id="6c6da-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c6da-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c6da-127">**IComprehensiveSpellCheckProvider**</span><span class="sxs-lookup"><span data-stu-id="6c6da-127">**IComprehensiveSpellCheckProvider**</span></span>](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[<span data-ttu-id="6c6da-128">**IEnumSpellingError**</span><span class="sxs-lookup"><span data-stu-id="6c6da-128">**IEnumSpellingError**</span></span>](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[<span data-ttu-id="6c6da-129">**ISpellChecker::ComprehensiveCheck**</span><span class="sxs-lookup"><span data-stu-id="6c6da-129">**ISpellChecker::ComprehensiveCheck**</span></span>](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[<span data-ttu-id="6c6da-130">**ISpellCheckProvider**</span><span class="sxs-lookup"><span data-stu-id="6c6da-130">**ISpellCheckProvider**</span></span>](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[<span data-ttu-id="6c6da-131">**ISpellCheckProvider：： Check**</span><span class="sxs-lookup"><span data-stu-id="6c6da-131">**ISpellCheckProvider::Check**</span></span>](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
