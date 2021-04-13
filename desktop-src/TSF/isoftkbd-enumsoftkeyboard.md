---
title: 'ISoftKbd EnumSoftKeyboard 方法 (Softkbdc .h) '
description: ISoftKbd EnumSoftKeyboard 方法會列舉支援指定語言的可能軟鍵盤。
ms.assetid: c71f99e5-c4c2-4b09-a58f-d3f4348d0c5d
keywords:
- EnumSoftKeyboard 方法文字服務架構
- EnumSoftKeyboard 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，EnumSoftKeyboard 方法
topic_type:
- apiref
api_name:
- ISoftKbd.EnumSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ecdb083684163798a68674628a8b1abc2460268
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466164"
---
# <a name="isoftkbdenumsoftkeyboard-method"></a><span data-ttu-id="f4a8e-106">ISoftKbd：： EnumSoftKeyboard 方法</span><span class="sxs-lookup"><span data-stu-id="f4a8e-106">ISoftKbd::EnumSoftKeyboard method</span></span>

<span data-ttu-id="f4a8e-107">**ISoftKbd：： EnumSoftKeyboard** 方法會列舉支援指定語言的可能軟鍵盤。</span><span class="sxs-lookup"><span data-stu-id="f4a8e-107">The **ISoftKbd::EnumSoftKeyboard** method enumerates the possible soft keyboards that support the specified language.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4a8e-108">語法</span><span class="sxs-lookup"><span data-stu-id="f4a8e-108">Syntax</span></span>


```C++
HRESULT EnumSoftKeyboard(
  [in]  LANGID langid,
  [out] DWORD  *lpdwKeyboard
);
```



## <a name="parameters"></a><span data-ttu-id="f4a8e-109">參數</span><span class="sxs-lookup"><span data-stu-id="f4a8e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f4a8e-110">*langid* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f4a8e-110">*langid* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f4a8e-111">語言識別項。</span><span class="sxs-lookup"><span data-stu-id="f4a8e-111">Language identifier.</span></span>

</dd> <dt>

<span data-ttu-id="f4a8e-112">*lpdwKeyboard* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f4a8e-112">*lpdwKeyboard* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f4a8e-113">緩衝區的指標，此方法會在其中取得可用軟鍵盤的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f4a8e-113">Pointer to a buffer in which this method retrieves identifiers of the available soft keyboards.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f4a8e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f4a8e-114">Return value</span></span>

<span data-ttu-id="f4a8e-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f4a8e-115">This method can return one of these values.</span></span>



| <span data-ttu-id="f4a8e-116">值</span><span class="sxs-lookup"><span data-stu-id="f4a8e-116">Value</span></span>                                                                                        | <span data-ttu-id="f4a8e-117">描述</span><span class="sxs-lookup"><span data-stu-id="f4a8e-117">Description</span></span>                                   |
|----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <span data-ttu-id="f4a8e-118"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="f4a8e-118"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="f4a8e-119">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="f4a8e-119">The method was successful.</span></span><br/>         |
| <dl> <span data-ttu-id="f4a8e-120"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="f4a8e-120"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="f4a8e-121">*Langid* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="f4a8e-121">The *langid* parameter is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f4a8e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="f4a8e-122">Requirements</span></span>



| <span data-ttu-id="f4a8e-123">需求</span><span class="sxs-lookup"><span data-stu-id="f4a8e-123">Requirement</span></span> | <span data-ttu-id="f4a8e-124">值</span><span class="sxs-lookup"><span data-stu-id="f4a8e-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4a8e-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f4a8e-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f4a8e-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4a8e-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f4a8e-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f4a8e-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f4a8e-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f4a8e-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f4a8e-129">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f4a8e-129">Redistributable</span></span><br/>          | <span data-ttu-id="f4a8e-130">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="f4a8e-130">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="f4a8e-131">標頭</span><span class="sxs-lookup"><span data-stu-id="f4a8e-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4a8e-132"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="f4a8e-132"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="f4a8e-133">Idl</span><span class="sxs-lookup"><span data-stu-id="f4a8e-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f4a8e-134"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f4a8e-134"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="f4a8e-135">DLL</span><span class="sxs-lookup"><span data-stu-id="f4a8e-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4a8e-136"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4a8e-136"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4a8e-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f4a8e-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4a8e-138">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="f4a8e-138">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





