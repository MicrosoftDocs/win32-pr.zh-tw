---
title: 'ISoftKbd CreateSoftKeyboardWindow 方法 (Softkbdc .h) '
description: ISoftKbd CreateSoftKeyboardWindow 方法會建立一個軟鍵盤視窗。
ms.assetid: e9aa9d88-d0bb-407f-9b53-98c8747be5d3
keywords:
- CreateSoftKeyboardWindow 方法文字服務架構
- CreateSoftKeyboardWindow 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，CreateSoftKeyboardWindow 方法
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardWindow
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e0ed6f9f91f335945d40dd0b995226a400965ab
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508995"
---
# <a name="isoftkbdcreatesoftkeyboardwindow-method"></a><span data-ttu-id="22c7a-106">ISoftKbd：： CreateSoftKeyboardWindow 方法</span><span class="sxs-lookup"><span data-stu-id="22c7a-106">ISoftKbd::CreateSoftKeyboardWindow method</span></span>

<span data-ttu-id="22c7a-107">**ISoftKbd：： CreateSoftKeyboardWindow** 方法會建立一個軟鍵盤視窗。</span><span class="sxs-lookup"><span data-stu-id="22c7a-107">The **ISoftKbd::CreateSoftKeyboardWindow** method creates a soft keyboard window.</span></span>

## <a name="syntax"></a><span data-ttu-id="22c7a-108">語法</span><span class="sxs-lookup"><span data-stu-id="22c7a-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardWindow(
  [in] HWND          hOwner,
  [in] TITLEBAR_TYPE Titlebar_type,
  [in] INT           xPos,
  [in] INT           yPos,
  [in] INT           width,
  [in] INT           height
);
```



## <a name="parameters"></a><span data-ttu-id="22c7a-109">參數</span><span class="sxs-lookup"><span data-stu-id="22c7a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="22c7a-110">*hOwner* \[在\]</span><span class="sxs-lookup"><span data-stu-id="22c7a-110">*hOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c7a-111">要包含軟鍵盤的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="22c7a-111">Handle of the window to contain the soft keyboard.</span></span>

</dd> <dt>

<span data-ttu-id="22c7a-112">*標題列 \_ 類型* \[\]</span><span class="sxs-lookup"><span data-stu-id="22c7a-112">*Titlebar\_type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c7a-113">[螢幕小鍵盤] 視窗的標題列類型。</span><span class="sxs-lookup"><span data-stu-id="22c7a-113">Type of title bar for the soft keyboard window.</span></span> <span data-ttu-id="22c7a-114">可能的類型是由 [**標題列 \_ 類型**](titlebar-type.md) 列舉所定義。</span><span class="sxs-lookup"><span data-stu-id="22c7a-114">Possible types are defined by the [**TITLEBAR\_TYPE**](titlebar-type.md) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="22c7a-115">*xPos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="22c7a-115">*xPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c7a-116">軟鍵盤視窗左上角的 x 位置。</span><span class="sxs-lookup"><span data-stu-id="22c7a-116">The x position of the upper left corner of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="22c7a-117">*yPos* \[在\]</span><span class="sxs-lookup"><span data-stu-id="22c7a-117">*yPos* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c7a-118">軟鍵盤視窗左上角的 y 位置。</span><span class="sxs-lookup"><span data-stu-id="22c7a-118">The y position of the upper left corner of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="22c7a-119">*寬度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="22c7a-119">*width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c7a-120">軟鍵盤視窗的寬度。</span><span class="sxs-lookup"><span data-stu-id="22c7a-120">The width of the soft keyboard window.</span></span>

</dd> <dt>

<span data-ttu-id="22c7a-121">*高度* \[在\]</span><span class="sxs-lookup"><span data-stu-id="22c7a-121">*height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="22c7a-122">軟鍵盤視窗的高度。</span><span class="sxs-lookup"><span data-stu-id="22c7a-122">The height of the soft keyboard window.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="22c7a-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="22c7a-123">Return value</span></span>

<span data-ttu-id="22c7a-124">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="22c7a-124">This method can return one of these values.</span></span>



| <span data-ttu-id="22c7a-125">值</span><span class="sxs-lookup"><span data-stu-id="22c7a-125">Value</span></span>                                                                                        | <span data-ttu-id="22c7a-126">描述</span><span class="sxs-lookup"><span data-stu-id="22c7a-126">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="22c7a-127"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="22c7a-127"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="22c7a-128">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="22c7a-128">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="22c7a-129"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="22c7a-129"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="22c7a-130">一或多個參數無效。</span><span class="sxs-lookup"><span data-stu-id="22c7a-130">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="22c7a-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="22c7a-131">Requirements</span></span>



| <span data-ttu-id="22c7a-132">需求</span><span class="sxs-lookup"><span data-stu-id="22c7a-132">Requirement</span></span> | <span data-ttu-id="22c7a-133">值</span><span class="sxs-lookup"><span data-stu-id="22c7a-133">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="22c7a-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="22c7a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="22c7a-135">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22c7a-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="22c7a-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="22c7a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="22c7a-137">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="22c7a-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="22c7a-138">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="22c7a-138">Redistributable</span></span><br/>          | <span data-ttu-id="22c7a-139">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="22c7a-139">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="22c7a-140">標頭</span><span class="sxs-lookup"><span data-stu-id="22c7a-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="22c7a-141"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="22c7a-141"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="22c7a-142">Idl</span><span class="sxs-lookup"><span data-stu-id="22c7a-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="22c7a-143"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="22c7a-143"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="22c7a-144">DLL</span><span class="sxs-lookup"><span data-stu-id="22c7a-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="22c7a-145"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="22c7a-145"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="22c7a-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="22c7a-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="22c7a-147">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="22c7a-147">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="22c7a-148">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span><span class="sxs-lookup"><span data-stu-id="22c7a-148">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> <dt>

[<span data-ttu-id="22c7a-149">**ISoftKbd：:D estroySoftKeyboardWindow**</span><span class="sxs-lookup"><span data-stu-id="22c7a-149">**ISoftKbd::DestroySoftKeyboardWindow**</span></span>](isoftkbd-destroysoftkeyboardwindow.md)
</dt> <dt>

[<span data-ttu-id="22c7a-150">**ISoftKbd::ShowSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="22c7a-150">**ISoftKbd::ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)
</dt> <dt>

[<span data-ttu-id="22c7a-151">**標題列 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="22c7a-151">**TITLEBAR\_TYPE**</span></span>](titlebar-type.md)
</dt> </dl>

 

 





