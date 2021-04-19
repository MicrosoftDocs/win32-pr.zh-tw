---
title: 'ISoftKbd DestroySoftKeyboardWindow 方法 (Softkbdc .h) '
description: ISoftKbd DestroySoftKeyboardWindow 方法會終結軟鍵盤視窗。
ms.assetid: 44030934-7b4a-46c1-95ea-709fc9004e43
keywords:
- DestroySoftKeyboardWindow 方法文字服務架構
- DestroySoftKeyboardWindow 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，DestroySoftKeyboardWindow 方法
topic_type:
- apiref
api_name:
- ISoftKbd.DestroySoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb0c460912e8b891503771425fc72484fcc471ff
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966116"
---
# <a name="isoftkbddestroysoftkeyboardwindow-method"></a><span data-ttu-id="2588f-106">ISoftKbd：:D estroySoftKeyboardWindow 方法</span><span class="sxs-lookup"><span data-stu-id="2588f-106">ISoftKbd::DestroySoftKeyboardWindow method</span></span>

<span data-ttu-id="2588f-107">**ISoftKbd：:D estroysoftkeyboardwindow** 方法會終結軟鍵盤視窗。</span><span class="sxs-lookup"><span data-stu-id="2588f-107">The **ISoftKbd::DestroySoftKeyboardWindow** method destroys a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="2588f-108">語法</span><span class="sxs-lookup"><span data-stu-id="2588f-108">Syntax</span></span>


```C++
HRESULT DestroySoftKeyboardWindow();
```



## <a name="parameters"></a><span data-ttu-id="2588f-109">參數</span><span class="sxs-lookup"><span data-stu-id="2588f-109">Parameters</span></span>

<span data-ttu-id="2588f-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="2588f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2588f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2588f-111">Return value</span></span>

<span data-ttu-id="2588f-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2588f-112">This method can return one of these values.</span></span>



| <span data-ttu-id="2588f-113">值</span><span class="sxs-lookup"><span data-stu-id="2588f-113">Value</span></span>                                                                                | <span data-ttu-id="2588f-114">描述</span><span class="sxs-lookup"><span data-stu-id="2588f-114">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="2588f-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2588f-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="2588f-116">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="2588f-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2588f-117">備註</span><span class="sxs-lookup"><span data-stu-id="2588f-117">Remarks</span></span>

<span data-ttu-id="2588f-118">這個方法會移除先前使用 [**ISoftKbd：： CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md)的呼叫所建立的軟鍵盤視窗。</span><span class="sxs-lookup"><span data-stu-id="2588f-118">This method removes a soft keyboard window previously created with a call to [**ISoftKbd::CreateSoftKeyboardWindow**](isoftkbd-createsoftkeyboardwindow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2588f-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="2588f-119">Requirements</span></span>



| <span data-ttu-id="2588f-120">需求</span><span class="sxs-lookup"><span data-stu-id="2588f-120">Requirement</span></span> | <span data-ttu-id="2588f-121">值</span><span class="sxs-lookup"><span data-stu-id="2588f-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2588f-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2588f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="2588f-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2588f-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2588f-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2588f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="2588f-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2588f-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2588f-126">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="2588f-126">Redistributable</span></span><br/>          | <span data-ttu-id="2588f-127">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="2588f-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="2588f-128">標頭</span><span class="sxs-lookup"><span data-stu-id="2588f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2588f-129"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="2588f-129"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="2588f-130">Idl</span><span class="sxs-lookup"><span data-stu-id="2588f-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2588f-131"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2588f-131"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="2588f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="2588f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2588f-133"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2588f-133"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2588f-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2588f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2588f-135">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="2588f-135">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="2588f-136">**ISoftKbd::CreateSoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="2588f-136">**ISoftKbd::CreateSoftKeyboardWindow**</span></span>](isoftkbd-createsoftkeyboardwindow.md)
</dt> </dl>

 

 





