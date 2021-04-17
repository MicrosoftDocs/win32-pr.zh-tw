---
title: 'ISoftKbd ShowKeysForKeyScanMode 方法 (Softkbdc .h) '
description: ISoftKbd ShowKeysForKeyScanMode 方法會顯示軟鍵盤的金鑰掃描模式所使用的金鑰。
ms.assetid: bfa76e5b-6f6e-470a-ba3a-7ecff9f67f7b
keywords:
- ShowKeysForKeyScanMode 方法文字服務架構
- ShowKeysForKeyScanMode 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，ShowKeysForKeyScanMode 方法
topic_type:
- apiref
api_name:
- ISoftKbd.ShowKeysForKeyScanMode
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7c46fbfc103c0ba40294e4c149d5fd427296765
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466300"
---
# <a name="isoftkbdshowkeysforkeyscanmode-method"></a><span data-ttu-id="bd367-106">ISoftKbd：： ShowKeysForKeyScanMode 方法</span><span class="sxs-lookup"><span data-stu-id="bd367-106">ISoftKbd::ShowKeysForKeyScanMode method</span></span>

<span data-ttu-id="bd367-107">**ISoftKbd：： ShowKeysForKeyScanMode** 方法會顯示軟鍵盤的金鑰掃描模式所使用的金鑰。</span><span class="sxs-lookup"><span data-stu-id="bd367-107">The **ISoftKbd::ShowKeysForKeyScanMode** method displays the keys used for the key scan mode for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd367-108">語法</span><span class="sxs-lookup"><span data-stu-id="bd367-108">Syntax</span></span>


```C++
HRESULT ShowKeysForKeyScanMode(
  [in] KEYID *lpKeyID,
  [in] INT   iKeyNum,
  [in] BOOL  fHighL
);
```



## <a name="parameters"></a><span data-ttu-id="bd367-109">參數</span><span class="sxs-lookup"><span data-stu-id="bd367-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bd367-110">*lpKeyID* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bd367-110">*lpKeyID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd367-111">KEYID 元素陣列的指標，指出要顯示之索引鍵的識別碼。</span><span class="sxs-lookup"><span data-stu-id="bd367-111">Pointer to an array of KEYID elements indicating the identifiers of keys to display.</span></span>

</dd> <dt>

<span data-ttu-id="bd367-112">*iKeyNum* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bd367-112">*iKeyNum* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd367-113">要顯示的索引鍵數目。</span><span class="sxs-lookup"><span data-stu-id="bd367-113">The number of keys to display.</span></span>

</dd> <dt>

<span data-ttu-id="bd367-114">*fHighL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="bd367-114">*fHighL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bd367-115">如果方法是反白顯示索引鍵，則為 TRUE，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="bd367-115">TRUE if the method is to highlight the keys, and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bd367-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="bd367-116">Return value</span></span>

<span data-ttu-id="bd367-117">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="bd367-117">This method can return one of these values.</span></span>



| <span data-ttu-id="bd367-118">值</span><span class="sxs-lookup"><span data-stu-id="bd367-118">Value</span></span>                                                                                        | <span data-ttu-id="bd367-119">描述</span><span class="sxs-lookup"><span data-stu-id="bd367-119">Description</span></span>                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="bd367-120"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="bd367-120"><dt>**S\_OK**</dt></span></span> </dl>         | <span data-ttu-id="bd367-121">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="bd367-121">The method was successful.</span></span><br/>        |
| <dl> <span data-ttu-id="bd367-122"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="bd367-122"><dt>**E\_INVALIDARG**</dt></span></span> </dl> | <span data-ttu-id="bd367-123">其中一個參數無效。</span><span class="sxs-lookup"><span data-stu-id="bd367-123">One of the parameters is invalid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bd367-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd367-124">Requirements</span></span>



| <span data-ttu-id="bd367-125">需求</span><span class="sxs-lookup"><span data-stu-id="bd367-125">Requirement</span></span> | <span data-ttu-id="bd367-126">值</span><span class="sxs-lookup"><span data-stu-id="bd367-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bd367-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd367-127">Minimum supported client</span></span><br/> | <span data-ttu-id="bd367-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd367-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bd367-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd367-129">Minimum supported server</span></span><br/> | <span data-ttu-id="bd367-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bd367-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bd367-131">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="bd367-131">Redistributable</span></span><br/>          | <span data-ttu-id="bd367-132">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="bd367-132">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="bd367-133">標頭</span><span class="sxs-lookup"><span data-stu-id="bd367-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="bd367-134"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="bd367-134"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="bd367-135">Idl</span><span class="sxs-lookup"><span data-stu-id="bd367-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bd367-136"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="bd367-136"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="bd367-137">DLL</span><span class="sxs-lookup"><span data-stu-id="bd367-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd367-138"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd367-138"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bd367-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd367-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd367-140">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="bd367-140">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





