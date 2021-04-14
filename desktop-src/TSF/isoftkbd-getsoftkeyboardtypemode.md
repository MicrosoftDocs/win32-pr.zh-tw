---
title: 'ISoftKbd GetSoftKeyboardTypeMode 方法 (Softkbdc .h) '
description: ISoftKbd GetSoftKeyboardTypeMode 方法會抓取軟鍵盤的類型模式。
ms.assetid: 77294652-b82e-4b69-bb55-5ebebc3c97c7
keywords:
- GetSoftKeyboardTypeMode 方法文字服務架構
- GetSoftKeyboardTypeMode 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，GetSoftKeyboardTypeMode 方法
topic_type:
- apiref
api_name:
- ISoftKbd.GetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6aad6d60c50ee0050cf418018dd6db1c7a33efc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104383825"
---
# <a name="isoftkbdgetsoftkeyboardtypemode-method"></a><span data-ttu-id="19edc-106">ISoftKbd：： GetSoftKeyboardTypeMode 方法</span><span class="sxs-lookup"><span data-stu-id="19edc-106">ISoftKbd::GetSoftKeyboardTypeMode method</span></span>

<span data-ttu-id="19edc-107">**ISoftKbd：： GetSoftKeyboardTypeMode** 方法會抓取軟鍵盤的類型模式。</span><span class="sxs-lookup"><span data-stu-id="19edc-107">The **ISoftKbd::GetSoftKeyboardTypeMode** method retrieves the type mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="19edc-108">語法</span><span class="sxs-lookup"><span data-stu-id="19edc-108">Syntax</span></span>


```C++
HRESULT GetSoftKeyboardTypeMode(
  [out] TYPEMODE *lpTypeMode
);
```



## <a name="parameters"></a><span data-ttu-id="19edc-109">參數</span><span class="sxs-lookup"><span data-stu-id="19edc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19edc-110">*lpTypeMode* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="19edc-110">*lpTypeMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="19edc-111">緩衝區的指標，此方法會在其中捕獲型別模式。</span><span class="sxs-lookup"><span data-stu-id="19edc-111">Pointer to a buffer in which this method retrieves the type mode.</span></span> <span data-ttu-id="19edc-112">可能的值是針對 [**TYPEMODE**](typemode.md) 列舉而定義的。</span><span class="sxs-lookup"><span data-stu-id="19edc-112">Possible values are defined for the [**TYPEMODE**](typemode.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19edc-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="19edc-113">Return value</span></span>

<span data-ttu-id="19edc-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="19edc-114">This method can return one of these values.</span></span>



| <span data-ttu-id="19edc-115">值</span><span class="sxs-lookup"><span data-stu-id="19edc-115">Value</span></span>                                                                                        | <span data-ttu-id="19edc-116">描述</span><span class="sxs-lookup"><span data-stu-id="19edc-116">Description</span></span>                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <span data-ttu-id="19edc-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="19edc-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="19edc-118">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="19edc-118">The method was successful.</span></span><br/>             |
| <dl> <span data-ttu-id="19edc-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="19edc-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="19edc-120">*LpTypeMode* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="19edc-120">The *lpTypeMode* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="19edc-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="19edc-121">Requirements</span></span>



| <span data-ttu-id="19edc-122">需求</span><span class="sxs-lookup"><span data-stu-id="19edc-122">Requirement</span></span> | <span data-ttu-id="19edc-123">值</span><span class="sxs-lookup"><span data-stu-id="19edc-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="19edc-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19edc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="19edc-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19edc-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="19edc-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19edc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="19edc-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19edc-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="19edc-128">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="19edc-128">Redistributable</span></span><br/>          | <span data-ttu-id="19edc-129">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="19edc-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="19edc-130">標頭</span><span class="sxs-lookup"><span data-stu-id="19edc-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="19edc-131"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="19edc-131"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="19edc-132">Idl</span><span class="sxs-lookup"><span data-stu-id="19edc-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="19edc-133"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="19edc-133"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="19edc-134">DLL</span><span class="sxs-lookup"><span data-stu-id="19edc-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="19edc-135"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19edc-135"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19edc-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19edc-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19edc-137">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="19edc-137">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="19edc-138">**ISoftKbd::SetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="19edc-138">**ISoftKbd::SetSoftKeyboardTypeMode**</span></span>](isoftkbd-setsoftkeyboardtypemode.md)
</dt> <dt>

[<span data-ttu-id="19edc-139">**TYPEMODE**</span><span class="sxs-lookup"><span data-stu-id="19edc-139">**TYPEMODE**</span></span>](typemode.md)
</dt> </dl>

 

 





