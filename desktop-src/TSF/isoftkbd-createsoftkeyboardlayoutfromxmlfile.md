---
title: 'ISoftKbd CreateSoftKeyboardLayoutFromXMLFile 方法 (Softkbdc .h) '
description: ISoftKbd CreateSoftKeyboardLayoutFromXMLFile 方法會從指定的 XML 檔案建立軟鍵盤版面配置。
ms.assetid: e665adab-1d75-4e41-87bf-c8ce0f7a0399
keywords:
- CreateSoftKeyboardLayoutFromXMLFile 方法文字服務架構
- CreateSoftKeyboardLayoutFromXMLFile 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，CreateSoftKeyboardLayoutFromXMLFile 方法
topic_type:
- apiref
api_name:
- ISoftKbd.CreateSoftKeyboardLayoutFromXMLFile
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9252db845c5e1cc732adc295e1989fee83d4ac6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968577"
---
# <a name="isoftkbdcreatesoftkeyboardlayoutfromxmlfile-method"></a><span data-ttu-id="2daa4-106">ISoftKbd：： CreateSoftKeyboardLayoutFromXMLFile 方法</span><span class="sxs-lookup"><span data-stu-id="2daa4-106">ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile method</span></span>

<span data-ttu-id="2daa4-107">**ISoftKbd：： CreateSoftKeyboardLayoutFromXMLFile** 方法會從指定的 XML 檔案建立軟鍵盤版面配置。</span><span class="sxs-lookup"><span data-stu-id="2daa4-107">The **ISoftKbd::CreateSoftKeyboardLayoutFromXMLFile** method creates a soft keyboard layout from the specified XML file.</span></span>

## <a name="syntax"></a><span data-ttu-id="2daa4-108">語法</span><span class="sxs-lookup"><span data-stu-id="2daa4-108">Syntax</span></span>


```C++
HRESULT CreateSoftKeyboardLayoutFromXMLFile(
  [in]  WCHAR *lpszKeyboardDesFile,
  [in]  INT   szFileStrLen,
  [out] DWORD *pdwLayoutCookie
);
```



## <a name="parameters"></a><span data-ttu-id="2daa4-109">參數</span><span class="sxs-lookup"><span data-stu-id="2daa4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2daa4-110">*lpszKeyboardDesFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2daa4-110">*lpszKeyboardDesFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2daa4-111">以零結尾的字串指標，表示 XML 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="2daa4-111">Pointer to a zero-terminated string indicating the name of the XML file.</span></span>

</dd> <dt>

<span data-ttu-id="2daa4-112">*szFileStrLen* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2daa4-112">*szFileStrLen* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2daa4-113">以零結束的字串，指出 XML 檔案的長度。</span><span class="sxs-lookup"><span data-stu-id="2daa4-113">Zero-terminated string indicating the length of the XML file.</span></span>

</dd> <dt>

<span data-ttu-id="2daa4-114">*pdwLayoutCookie* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2daa4-114">*pdwLayoutCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2daa4-115">緩衝區的指標，此方法會在其中捕獲軟鍵盤配置 cookie。</span><span class="sxs-lookup"><span data-stu-id="2daa4-115">Pointer to the buffer in which this method retrieves a soft keyboard layout cookie.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2daa4-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="2daa4-116">Return value</span></span>

<span data-ttu-id="2daa4-117">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="2daa4-117">This method can return one of these values.</span></span>



| <span data-ttu-id="2daa4-118">值</span><span class="sxs-lookup"><span data-stu-id="2daa4-118">Value</span></span>                                                                                        | <span data-ttu-id="2daa4-119">描述</span><span class="sxs-lookup"><span data-stu-id="2daa4-119">Description</span></span>                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="2daa4-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="2daa4-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="2daa4-121">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="2daa4-121">The method was successful.</span></span><br/>          |
| <dl> <span data-ttu-id="2daa4-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="2daa4-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="2daa4-123">一或多個參數無效。</span><span class="sxs-lookup"><span data-stu-id="2daa4-123">One or more parameters are invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="2daa4-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="2daa4-124">Requirements</span></span>



| <span data-ttu-id="2daa4-125">需求</span><span class="sxs-lookup"><span data-stu-id="2daa4-125">Requirement</span></span> | <span data-ttu-id="2daa4-126">值</span><span class="sxs-lookup"><span data-stu-id="2daa4-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2daa4-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2daa4-127">Minimum supported client</span></span><br/> | <span data-ttu-id="2daa4-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2daa4-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2daa4-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2daa4-129">Minimum supported server</span></span><br/> | <span data-ttu-id="2daa4-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2daa4-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="2daa4-131">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="2daa4-131">Redistributable</span></span><br/>          | <span data-ttu-id="2daa4-132">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="2daa4-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="2daa4-133">標頭</span><span class="sxs-lookup"><span data-stu-id="2daa4-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2daa4-134"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="2daa4-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="2daa4-135">Idl</span><span class="sxs-lookup"><span data-stu-id="2daa4-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="2daa4-136"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="2daa4-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="2daa4-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2daa4-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2daa4-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2daa4-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2daa4-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2daa4-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2daa4-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="2daa4-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="2daa4-141">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span><span class="sxs-lookup"><span data-stu-id="2daa4-141">**ISoftKbd::CreateSoftKeyboardLayoutFromResource**</span></span>](isoftkbd-createsoftkeyboardlayoutfromresource.md)
</dt> </dl>

 

 





