---
title: 'ISoftKbd SelectSoftKeyboard 方法 (Softkbdc .h) '
description: ISoftKbd SelectSoftKeyboard 方法會選取指定的軟鍵盤。
ms.assetid: 7e85d346-3741-457d-aadd-11d3a6710e85
keywords:
- SelectSoftKeyboard 方法文字服務架構
- SelectSoftKeyboard 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，SelectSoftKeyboard 方法
topic_type:
- apiref
api_name:
- ISoftKbd.SelectSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bbda9399297e9776e7fbd7cecb364fd7f6cd4604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509067"
---
# <a name="isoftkbdselectsoftkeyboard-method"></a><span data-ttu-id="1baf6-106">ISoftKbd：： SelectSoftKeyboard 方法</span><span class="sxs-lookup"><span data-stu-id="1baf6-106">ISoftKbd::SelectSoftKeyboard method</span></span>

<span data-ttu-id="1baf6-107">**ISoftKbd：： SelectSoftKeyboard** 方法會選取指定的軟鍵盤。</span><span class="sxs-lookup"><span data-stu-id="1baf6-107">The **ISoftKbd::SelectSoftKeyboard** method selects the specified soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="1baf6-108">語法</span><span class="sxs-lookup"><span data-stu-id="1baf6-108">Syntax</span></span>


```C++
HRESULT SelectSoftKeyboard(
  [in] DWORD dwKeyboardId
);
```



## <a name="parameters"></a><span data-ttu-id="1baf6-109">參數</span><span class="sxs-lookup"><span data-stu-id="1baf6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1baf6-110">*dwKeyboardId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1baf6-110">*dwKeyboardId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1baf6-111">要選取之軟鍵盤的識別碼。</span><span class="sxs-lookup"><span data-stu-id="1baf6-111">Identifier of the soft keyboard to select.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1baf6-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="1baf6-112">Return value</span></span>

<span data-ttu-id="1baf6-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1baf6-113">This method can return one of these values.</span></span>



| <span data-ttu-id="1baf6-114">值</span><span class="sxs-lookup"><span data-stu-id="1baf6-114">Value</span></span>                                                                                        | <span data-ttu-id="1baf6-115">描述</span><span class="sxs-lookup"><span data-stu-id="1baf6-115">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <span data-ttu-id="1baf6-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="1baf6-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="1baf6-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="1baf6-117">The method was successful.</span></span><br/>               |
| <dl> <span data-ttu-id="1baf6-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="1baf6-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="1baf6-119">*DwKeyboardId* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="1baf6-119">The *dwKeyboardId* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="1baf6-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="1baf6-120">Requirements</span></span>



| <span data-ttu-id="1baf6-121">需求</span><span class="sxs-lookup"><span data-stu-id="1baf6-121">Requirement</span></span> | <span data-ttu-id="1baf6-122">值</span><span class="sxs-lookup"><span data-stu-id="1baf6-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1baf6-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1baf6-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1baf6-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1baf6-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1baf6-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1baf6-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1baf6-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1baf6-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1baf6-127">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="1baf6-127">Redistributable</span></span><br/>          | <span data-ttu-id="1baf6-128">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="1baf6-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="1baf6-129">標頭</span><span class="sxs-lookup"><span data-stu-id="1baf6-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="1baf6-130"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="1baf6-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="1baf6-131">Idl</span><span class="sxs-lookup"><span data-stu-id="1baf6-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1baf6-132"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="1baf6-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="1baf6-133">DLL</span><span class="sxs-lookup"><span data-stu-id="1baf6-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1baf6-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1baf6-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1baf6-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1baf6-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1baf6-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="1baf6-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





