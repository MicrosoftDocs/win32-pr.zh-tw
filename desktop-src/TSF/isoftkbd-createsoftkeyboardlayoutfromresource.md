---
title: 'ISoftKbd CreateSoftKeyboardLayoutFromResource 方法 (Softkbdc .h) '
description: ISoftKbd CreateSoftKeybboardLayoutFromResource 方法會從指定的資源建立軟鍵盤版面配置。
ms.assetid: c1b2f8bd-8065-426d-9c23-67fa46a33dc8
keywords:
- CreateSoftKeyboardLayoutFromResource 方法文字服務架構
- CreateSoftKeyboardLayoutFromResource 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，CreateSoftKeyboardLayoutFromResource 方法
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromResource
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f454b5d8f3366517d91170d6a92d6a9dbed5764
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969992"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromresource-method"></a><span data-ttu-id="48e93-106">ISoftKbd：： CreateSoftKeyboardLayoutFromResource 方法</span><span class="sxs-lookup"><span data-stu-id="48e93-106">ISoftKbd::CreateSoftKeyboardLayoutFromResource method</span></span>

<span data-ttu-id="48e93-107">**ISoftKbd：： CreateSoftKeybboardLayoutFromResource** 方法會從指定的資源建立軟鍵盤版面配置。</span><span class="sxs-lookup"><span data-stu-id="48e93-107">The **ISoftKbd::CreateSoftKeybboardLayoutFromResource** method creates a soft keyboard layout from the specified resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="48e93-108">語法</span><span class="sxs-lookup"><span data-stu-id="48e93-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardLayoutFromResource(
  [in]  WCHAR *lpszResFile,
  [in]  WCHAR *lpszResType,
  [in]  WCHAR *lpszXMLResString,
  [out] DWORD *lpdwLayoutCookie
);
```



## <a name="parameters"></a><span data-ttu-id="48e93-109">參數</span><span class="sxs-lookup"><span data-stu-id="48e93-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48e93-110">*lpszResFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48e93-110">*lpszResFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e93-111">以零結尾的字串指標，指出資源檔的名稱。</span><span class="sxs-lookup"><span data-stu-id="48e93-111">Pointer to a zero-terminated string indicating the name of the resource file.</span></span>

</dd> <dt>

<span data-ttu-id="48e93-112">*lpszResType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48e93-112">*lpszResType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e93-113">表示資源類型之以零結尾的字串指標。</span><span class="sxs-lookup"><span data-stu-id="48e93-113">Pointer to a zero-terminated string indicating the type of resource.</span></span>

</dd> <dt>

<span data-ttu-id="48e93-114">*lpszXMLResString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="48e93-114">*lpszXMLResString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48e93-115">識別資源之以零結尾的字串指標。</span><span class="sxs-lookup"><span data-stu-id="48e93-115">Pointer to a zero-terminated string identifying the resource.</span></span>

</dd> <dt>

<span data-ttu-id="48e93-116">*lpdwLayoutCookie* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="48e93-116">*lpdwLayoutCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48e93-117">緩衝區的指標，此方法會在其中捕獲軟鍵盤配置 cookie。</span><span class="sxs-lookup"><span data-stu-id="48e93-117">Pointer to the buffer in which this method retrieves a soft keyboard layout cookie.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48e93-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="48e93-118">Return value</span></span>

<span data-ttu-id="48e93-119">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="48e93-119">This method can return one of these values.</span></span>



| <span data-ttu-id="48e93-120">值</span><span class="sxs-lookup"><span data-stu-id="48e93-120">Value</span></span>                                                                                        | <span data-ttu-id="48e93-121">描述</span><span class="sxs-lookup"><span data-stu-id="48e93-121">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="48e93-122"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="48e93-122"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="48e93-123">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="48e93-123">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="48e93-124"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="48e93-124"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="48e93-125">一或多個參數無效。</span><span class="sxs-lookup"><span data-stu-id="48e93-125">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="48e93-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="48e93-126">Requirements</span></span>



| <span data-ttu-id="48e93-127">需求</span><span class="sxs-lookup"><span data-stu-id="48e93-127">Requirement</span></span> | <span data-ttu-id="48e93-128">值</span><span class="sxs-lookup"><span data-stu-id="48e93-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="48e93-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48e93-129">Minimum supported client</span></span><br/> | <span data-ttu-id="48e93-130">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48e93-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="48e93-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48e93-131">Minimum supported server</span></span><br/> | <span data-ttu-id="48e93-132">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48e93-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="48e93-133">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="48e93-133">Redistributable</span></span><br/>          | <span data-ttu-id="48e93-134">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="48e93-134">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="48e93-135">標頭</span><span class="sxs-lookup"><span data-stu-id="48e93-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="48e93-136"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="48e93-136"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="48e93-137">Idl</span><span class="sxs-lookup"><span data-stu-id="48e93-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="48e93-138"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="48e93-138"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="48e93-139">DLL</span><span class="sxs-lookup"><span data-stu-id="48e93-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48e93-140"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48e93-140"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48e93-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48e93-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48e93-142">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="48e93-142">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="48e93-143">**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**</span><span class="sxs-lookup"><span data-stu-id="48e93-143">**ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile**</span></span>](isoftkbd-createsoftkeyboardlayoutfromxmlfile.md)
</dt> <dt>

[<span data-ttu-id="48e93-144">**ISoftKbd::ShowSoftKeyboard**</span><span class="sxs-lookup"><span data-stu-id="48e93-144">**ISoftKbd::ShowSoftKeyboard**</span></span>](isoftkbd-showsoftkeyboard.md)
</dt> </dl>

 

 





