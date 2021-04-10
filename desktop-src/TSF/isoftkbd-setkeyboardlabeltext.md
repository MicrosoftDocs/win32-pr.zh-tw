---
title: 'ISoftKbd SetKeyboardLabelText 方法 (Softkbdc .h) '
description: ISoftKbd SetKeyboardLabelText 方法會從軟鍵盤的版面配置設定標籤文字。
ms.assetid: 86c45c37-fe50-4596-b4c9-960de760a2e0
keywords:
- SetKeyboardLabelText 方法文字服務架構
- SetKeyboardLabelText 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，SetKeyboardLabelText 方法
topic_type:
- apiref
api_name:
- ISoftKbd.SetKeyboardLabelText
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 862341182b9c97a751ba4a130566d5cf18437c2b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686230"
---
# <a name="isoftkbdsetkeyboardlabeltext-method"></a><span data-ttu-id="a068c-106">ISoftKbd：： SetKeyboardLabelText 方法</span><span class="sxs-lookup"><span data-stu-id="a068c-106">ISoftKbd::SetKeyboardLabelText method</span></span>

<span data-ttu-id="a068c-107">**ISoftKbd：： SetKeyboardLabelText** 方法會從軟鍵盤的配置設定標籤文字。</span><span class="sxs-lookup"><span data-stu-id="a068c-107">The **ISoftKbd::SetKeyboardLabelText** method sets the label text from the layout for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="a068c-108">語法</span><span class="sxs-lookup"><span data-stu-id="a068c-108">Syntax</span></span>


```C++
HRESULT SetKeyboardLabelText(
  [in] HKL hKl
);
```



## <a name="parameters"></a><span data-ttu-id="a068c-109">參數</span><span class="sxs-lookup"><span data-stu-id="a068c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a068c-110">*hKl* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a068c-110">*hKl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a068c-111">用來取得已安裝之軟鍵盤配置的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a068c-111">Handle that is used to retrieve the installed layout for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a068c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a068c-112">Return value</span></span>

<span data-ttu-id="a068c-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a068c-113">This method can return one of these values.</span></span>



| <span data-ttu-id="a068c-114">值</span><span class="sxs-lookup"><span data-stu-id="a068c-114">Value</span></span>                                                                                        | <span data-ttu-id="a068c-115">描述</span><span class="sxs-lookup"><span data-stu-id="a068c-115">Description</span></span>                                |
|----------------------------------------------------------------------------------------------|--------------------------------------------|
| <dl> <span data-ttu-id="a068c-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a068c-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a068c-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="a068c-117">The method was successful.</span></span><br/>      |
| <dl> <span data-ttu-id="a068c-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a068c-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a068c-119">*HKl* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="a068c-119">The *hKl* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a068c-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="a068c-120">Requirements</span></span>



| <span data-ttu-id="a068c-121">需求</span><span class="sxs-lookup"><span data-stu-id="a068c-121">Requirement</span></span> | <span data-ttu-id="a068c-122">值</span><span class="sxs-lookup"><span data-stu-id="a068c-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a068c-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a068c-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a068c-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a068c-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a068c-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a068c-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a068c-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a068c-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a068c-127">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a068c-127">Redistributable</span></span><br/>          | <span data-ttu-id="a068c-128">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="a068c-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="a068c-129">標頭</span><span class="sxs-lookup"><span data-stu-id="a068c-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="a068c-130"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="a068c-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="a068c-131">Idl</span><span class="sxs-lookup"><span data-stu-id="a068c-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a068c-132"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a068c-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="a068c-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a068c-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a068c-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a068c-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a068c-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a068c-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a068c-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="a068c-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="a068c-137">**ISoftKbd::SetKeyboardLabelTextCombination**</span><span class="sxs-lookup"><span data-stu-id="a068c-137">**ISoftKbd::SetKeyboardLabelTextCombination**</span></span>](isoftkbd-setkeyboardlabeltextcombination.md)
</dt> </dl>

 

 





