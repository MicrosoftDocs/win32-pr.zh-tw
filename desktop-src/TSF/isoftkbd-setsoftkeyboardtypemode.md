---
title: 'ISoftKbd SetSoftKeyboardTypeMode 方法 (Softkbdc .h) '
description: ISoftKbd SetSoftKeyboardTypeMode 方法會設定軟鍵盤的類型模式。
ms.assetid: 0b5b5056-59b3-41c7-bc43-70b5c3cd51c2
keywords:
- SetSoftKeyboardTypeMode 方法文字服務架構
- SetSoftKeyboardTypeMode 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，SetSoftKeyboardTypeMode 方法
topic_type:
- apiref
api_name:
- ISoftKbd.SetSoftKeyboardTypeMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55c01465debc42926888e2cb12a3a5b9d884498b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466304"
---
# <a name="isoftkbdsetsoftkeyboardtypemode-method"></a><span data-ttu-id="a651f-106">ISoftKbd：： SetSoftKeyboardTypeMode 方法</span><span class="sxs-lookup"><span data-stu-id="a651f-106">ISoftKbd::SetSoftKeyboardTypeMode method</span></span>

<span data-ttu-id="a651f-107">**ISoftKbd：： SetSoftKeyboardTypeMode** 方法會設定軟鍵盤的類型模式。</span><span class="sxs-lookup"><span data-stu-id="a651f-107">The **ISoftKbd::SetSoftKeyboardTypeMode** method sets the type mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="a651f-108">語法</span><span class="sxs-lookup"><span data-stu-id="a651f-108">Syntax</span></span>


```C++
HRESULT SetSoftKeyboardTypeMode(
  [in] TYPEMODE TypeMode
);
```



## <a name="parameters"></a><span data-ttu-id="a651f-109">參數</span><span class="sxs-lookup"><span data-stu-id="a651f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a651f-110">*TypeMode* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a651f-110">*TypeMode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a651f-111">型別模式。</span><span class="sxs-lookup"><span data-stu-id="a651f-111">The type mode.</span></span> <span data-ttu-id="a651f-112">可能的值是針對 [**TYPEMODE**](typemode.md) 列舉而定義的。</span><span class="sxs-lookup"><span data-stu-id="a651f-112">Possible values are defined for the [**TYPEMODE**](typemode.md) enumeration.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a651f-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a651f-113">Return value</span></span>

<span data-ttu-id="a651f-114">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a651f-114">This method can return one of these values.</span></span>



| <span data-ttu-id="a651f-115">值</span><span class="sxs-lookup"><span data-stu-id="a651f-115">Value</span></span>                                                                                        | <span data-ttu-id="a651f-116">描述</span><span class="sxs-lookup"><span data-stu-id="a651f-116">Description</span></span>                                     |
|----------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="a651f-117"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="a651f-117"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="a651f-118">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="a651f-118">The method was successful.</span></span><br/>           |
| <dl> <span data-ttu-id="a651f-119"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="a651f-119"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="a651f-120">*TypeMode* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="a651f-120">The *TypeMode* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="a651f-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="a651f-121">Requirements</span></span>



| <span data-ttu-id="a651f-122">需求</span><span class="sxs-lookup"><span data-stu-id="a651f-122">Requirement</span></span> | <span data-ttu-id="a651f-123">值</span><span class="sxs-lookup"><span data-stu-id="a651f-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a651f-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a651f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="a651f-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a651f-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a651f-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a651f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="a651f-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a651f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a651f-128">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="a651f-128">Redistributable</span></span><br/>          | <span data-ttu-id="a651f-129">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="a651f-129">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="a651f-130">標頭</span><span class="sxs-lookup"><span data-stu-id="a651f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="a651f-131"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="a651f-131"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="a651f-132">Idl</span><span class="sxs-lookup"><span data-stu-id="a651f-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a651f-133"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="a651f-133"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="a651f-134">DLL</span><span class="sxs-lookup"><span data-stu-id="a651f-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a651f-135"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a651f-135"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a651f-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a651f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a651f-137">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="a651f-137">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> <dt>

[<span data-ttu-id="a651f-138">**ISoftKbd::GetSoftKeyboardTypeMode**</span><span class="sxs-lookup"><span data-stu-id="a651f-138">**ISoftKbd::GetSoftKeyboardTypeMode**</span></span>](isoftkbd-getsoftkeyboardtypemode.md)
</dt> <dt>

[<span data-ttu-id="a651f-139">**TYPEMODE**</span><span class="sxs-lookup"><span data-stu-id="a651f-139">**TYPEMODE**</span></span>](typemode.md)
</dt> </dl>

 

 





