---
title: 'ISoftKbd SetKeyboardLabelTextCombination 方法 (Softkbdc .h) '
description: ISoftKbd SetKeyboardLabelTextCombination 方法會設定用來描述軟鍵盤的標籤和文字的組合。
ms.assetid: fe054eae-1a44-41ad-9a44-bc0b46df7c7b
keywords:
- SetKeyboardLabelTextCombination 方法文字服務架構
- SetKeyboardLabelTextCombination 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，SetKeyboardLabelTextCombination 方法
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelTextCombination
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0f98dad124455625f0da3ada1a717c692437398
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965925"
---
# <a name="isoftkbdsetkeyboardlabeltextcombination-method"></a><span data-ttu-id="0482c-106">ISoftKbd：： SetKeyboardLabelTextCombination 方法</span><span class="sxs-lookup"><span data-stu-id="0482c-106">ISoftKbd::SetKeyboardLabelTextCombination method</span></span>

<span data-ttu-id="0482c-107">**ISoftKbd：： SetKeyboardLabelTextCombination** 方法會設定用來描述軟鍵盤的標籤和文字的組合。</span><span class="sxs-lookup"><span data-stu-id="0482c-107">The **ISoftKbd::SetKeyboardLabelTextCombination** method sets a combination of label and text used to describe a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="0482c-108">語法</span><span class="sxs-lookup"><span data-stu-id="0482c-108">Syntax</span></span>


```C++
HRESULT SetKeyboardLabelTextCombination(
  [in] DWORD nModifierCombination
);
```



## <a name="parameters"></a><span data-ttu-id="0482c-109">參數</span><span class="sxs-lookup"><span data-stu-id="0482c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0482c-110">*nModifierCombination* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0482c-110">*nModifierCombination* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0482c-111">用來描述軟鍵盤的標籤和文字的組合。</span><span class="sxs-lookup"><span data-stu-id="0482c-111">Combination of label and text used to describe the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0482c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0482c-112">Return value</span></span>

<span data-ttu-id="0482c-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0482c-113">This method can return one of these values.</span></span>



| <span data-ttu-id="0482c-114">值</span><span class="sxs-lookup"><span data-stu-id="0482c-114">Value</span></span>                                                                                        | <span data-ttu-id="0482c-115">描述</span><span class="sxs-lookup"><span data-stu-id="0482c-115">Description</span></span>                                                 |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <span data-ttu-id="0482c-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="0482c-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="0482c-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="0482c-117">The method was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="0482c-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="0482c-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="0482c-119">*NModifierCombination* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="0482c-119">The *nModifierCombination* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0482c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="0482c-120">Requirements</span></span>



| <span data-ttu-id="0482c-121">需求</span><span class="sxs-lookup"><span data-stu-id="0482c-121">Requirement</span></span> | <span data-ttu-id="0482c-122">值</span><span class="sxs-lookup"><span data-stu-id="0482c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0482c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0482c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0482c-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0482c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0482c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0482c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0482c-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0482c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0482c-127">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="0482c-127">Redistributable</span></span><br/>          | <span data-ttu-id="0482c-128">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="0482c-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="0482c-129">標頭</span><span class="sxs-lookup"><span data-stu-id="0482c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="0482c-130"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="0482c-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="0482c-131">Idl</span><span class="sxs-lookup"><span data-stu-id="0482c-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0482c-132"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="0482c-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="0482c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="0482c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0482c-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0482c-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0482c-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0482c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0482c-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="0482c-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="0482c-137">**ISoftKbd::SetKeyboardLabelText**</span><span class="sxs-lookup"><span data-stu-id="0482c-137">**ISoftKbd::SetKeyboardLabelText**</span></span>](isoftkbd-setkeyboardlabeltext.md)
</dt> </dl>

 

 





