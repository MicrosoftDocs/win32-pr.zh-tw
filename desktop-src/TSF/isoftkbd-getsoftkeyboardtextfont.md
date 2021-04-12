---
title: 'ISoftKbd GetSoftKeyboardTextFont 方法 (Softkbdc .h) '
description: ISoftKbd GetSoftKeyboardTextFont 方法會抓取軟鍵盤所使用的文字字型。
ms.assetid: 73239359-70b4-47d6-abc5-9fee279ed3a6
keywords:
- GetSoftKeyboardTextFont 方法文字服務架構
- GetSoftKeyboardTextFont 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，GetSoftKeyboardTextFont 方法
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTextFont
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce939347042415a9060459102cd8a56665ac2de0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105251"
---
# <a name="isoftkbdgetsoftkeyboardtextfont-method"></a><span data-ttu-id="06952-106">ISoftKbd：： GetSoftKeyboardTextFont 方法</span><span class="sxs-lookup"><span data-stu-id="06952-106">ISoftKbd::GetSoftKeyboardTextFont method</span></span>

<span data-ttu-id="06952-107">**ISoftKbd：： GetSoftKeyboardTextFont** 方法會抓取軟鍵盤所使用的文字字型。</span><span class="sxs-lookup"><span data-stu-id="06952-107">The **ISoftKbd::GetSoftKeyboardTextFont** method retrieves the text font used by a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="06952-108">語法</span><span class="sxs-lookup"><span data-stu-id="06952-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardTextFont(
  [out] LOGFONTW *pLogFont
);
```



## <a name="parameters"></a><span data-ttu-id="06952-109">參數</span><span class="sxs-lookup"><span data-stu-id="06952-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06952-110">*pLogFont* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="06952-110">*pLogFont* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="06952-111">緩衝區的指標，此方法會在其中取得 [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) 結構，以定義軟鍵盤的文字字型。</span><span class="sxs-lookup"><span data-stu-id="06952-111">Pointer to a buffer in which this method retrieves a [**LOGFONTW**](/windows/win32/api/wingdi/ns-wingdi-logfonta) structure defining the text font for the soft keyboard.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06952-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="06952-112">Return value</span></span>

<span data-ttu-id="06952-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="06952-113">This method can return one of these values.</span></span>



| <span data-ttu-id="06952-114">值</span><span class="sxs-lookup"><span data-stu-id="06952-114">Value</span></span>                                                                                        | <span data-ttu-id="06952-115">描述</span><span class="sxs-lookup"><span data-stu-id="06952-115">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="06952-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="06952-116"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="06952-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="06952-117">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="06952-118"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="06952-118"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="06952-119">*PLogFont* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="06952-119">The *pLogFont* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="06952-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="06952-120">Requirements</span></span>



| <span data-ttu-id="06952-121">需求</span><span class="sxs-lookup"><span data-stu-id="06952-121">Requirement</span></span> | <span data-ttu-id="06952-122">值</span><span class="sxs-lookup"><span data-stu-id="06952-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="06952-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="06952-123">Minimum supported client</span></span><br/> | <span data-ttu-id="06952-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06952-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="06952-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="06952-125">Minimum supported server</span></span><br/> | <span data-ttu-id="06952-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="06952-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="06952-127">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="06952-127">Redistributable</span></span><br/>          | <span data-ttu-id="06952-128">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="06952-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="06952-129">標頭</span><span class="sxs-lookup"><span data-stu-id="06952-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="06952-130"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="06952-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="06952-131">Idl</span><span class="sxs-lookup"><span data-stu-id="06952-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="06952-132"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="06952-132"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="06952-133">DLL</span><span class="sxs-lookup"><span data-stu-id="06952-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="06952-134"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="06952-134"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06952-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="06952-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06952-136">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="06952-136">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="06952-137">**ISoftKbd::SetSoftKeyboardTextFont**</span><span class="sxs-lookup"><span data-stu-id="06952-137">**ISoftKbd::SetSoftKeyboardTextFont**</span></span>](isoftkbd-setsoftkeyboardtextfont.md)
</dt> </dl>

 

