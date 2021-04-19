---
title: 'ISoftKbd SetSoftKeyboardTextFont 方法 (Softkbdc .h) '
description: ISoftKbd SetSoftKeyboardTextFont 方法會設定軟鍵盤所使用的文字字型。
ms.assetid: 14705723-4592-40ef-9ebb-1c44c10c3cda
keywords:
- SetSoftKeyboardTextFont 方法文字服務架構
- SetSoftKeyboardTextFont 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，SetSoftKeyboardTextFont 方法
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ff0a9adce61bc1a671d28c6e5d6ac5b6d329b42
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965924"
---
# <a name="isoftkbdsetsoftkeyboardtextfont-method"></a><span data-ttu-id="f7d7d-106">ISoftKbd：： SetSoftKeyboardTextFont 方法</span><span class="sxs-lookup"><span data-stu-id="f7d7d-106">ISoftKbd::SetSoftKeyboardTextFont method</span></span>

<span data-ttu-id="f7d7d-107">**ISoftKbd：： SetSoftKeyboardTextFont** 方法會設定軟鍵盤所使用的文字字型。</span><span class="sxs-lookup"><span data-stu-id="f7d7d-107">The **ISoftKbd::SetSoftKeyboardTextFont** method sets the text font used by a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7d7d-108">語法</span><span class="sxs-lookup"><span data-stu-id="f7d7d-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardTextFont(
  [in] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a><span data-ttu-id="f7d7d-109">參數</span><span class="sxs-lookup"><span data-stu-id="f7d7d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f7d7d-110">*pLogFont* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f7d7d-110">*pLogFont* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f7d7d-111">[**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta)結構的指標，此結構定義了軟鍵盤的文字字型。</span><span class="sxs-lookup"><span data-stu-id="f7d7d-111">Pointer to a [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure defining the text font for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f7d7d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f7d7d-112">Return value</span></span>

<span data-ttu-id="f7d7d-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f7d7d-113">This method can return one of these values.</span></span>



| <span data-ttu-id="f7d7d-114">值</span><span class="sxs-lookup"><span data-stu-id="f7d7d-114">Value</span></span>                                                                                        | <span data-ttu-id="f7d7d-115">描述</span><span class="sxs-lookup"><span data-stu-id="f7d7d-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="f7d7d-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f7d7d-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f7d7d-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="f7d7d-117">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="f7d7d-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f7d7d-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f7d7d-119">*PLogFont* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="f7d7d-119">The *pLogFont* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f7d7d-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f7d7d-120">Requirements</span></span>



| <span data-ttu-id="f7d7d-121">需求</span><span class="sxs-lookup"><span data-stu-id="f7d7d-121">Requirement</span></span> | <span data-ttu-id="f7d7d-122">值</span><span class="sxs-lookup"><span data-stu-id="f7d7d-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f7d7d-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f7d7d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f7d7d-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7d7d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f7d7d-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f7d7d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f7d7d-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f7d7d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f7d7d-127">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f7d7d-127">Redistributable</span></span><br/>          | <span data-ttu-id="f7d7d-128">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="f7d7d-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="f7d7d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="f7d7d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f7d7d-130"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="f7d7d-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="f7d7d-131">Idl</span><span class="sxs-lookup"><span data-stu-id="f7d7d-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f7d7d-132"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f7d7d-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="f7d7d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f7d7d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f7d7d-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f7d7d-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f7d7d-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f7d7d-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f7d7d-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="f7d7d-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="f7d7d-137">**ISoftKbd::GetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="f7d7d-137">**ISoftKbd::GetSoftKeyboardTextFont**</span></span>](isoftkbd-getsoftkeyboardtextfont.md)
</dt> </dl>

 

