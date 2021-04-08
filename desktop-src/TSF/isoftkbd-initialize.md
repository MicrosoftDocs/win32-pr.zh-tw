---
title: 'ISoftKbd Initialize 方法 (Softkbdc .h) '
description: ISoftKbd Initialize 方法會初始化軟鍵盤的所有必要欄位，並產生標準的軟鍵盤配置。
ms.assetid: c997864c-2596-4086-8062-cd30f371c38f
keywords:
- Initialize 方法文字服務架構
- Initialize 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，Initialize 方法
topic_type:
- apiref
api_name:
- ISoftKbd.Initialize
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e6e820becb05d7c474004b4889735f9637e0135a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685584"
---
# <a name="isoftkbdinitialize-method"></a><span data-ttu-id="13f60-106">ISoftKbd：： Initialize 方法</span><span class="sxs-lookup"><span data-stu-id="13f60-106">ISoftKbd::Initialize method</span></span>

<span data-ttu-id="13f60-107">**ISoftKbd：： Initialize** 方法會初始化軟鍵盤的所有必要欄位，並產生標準的軟鍵盤配置。</span><span class="sxs-lookup"><span data-stu-id="13f60-107">The **ISoftKbd::Initialize** method initializes all necessary fields for a soft keyboard and generates standard soft keyboard layouts.</span></span>

## <a name="syntax"></a><span data-ttu-id="13f60-108">語法</span><span class="sxs-lookup"><span data-stu-id="13f60-108">Syntax</span></span>


```C++
HRESULT Initialize();
```



## <a name="parameters"></a><span data-ttu-id="13f60-109">參數</span><span class="sxs-lookup"><span data-stu-id="13f60-109">Parameters</span></span>

<span data-ttu-id="13f60-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="13f60-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="13f60-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="13f60-111">Return value</span></span>

<span data-ttu-id="13f60-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="13f60-112">This method can return one of these values.</span></span>



| <span data-ttu-id="13f60-113">值</span><span class="sxs-lookup"><span data-stu-id="13f60-113">Value</span></span>                                                                                | <span data-ttu-id="13f60-114">描述</span><span class="sxs-lookup"><span data-stu-id="13f60-114">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="13f60-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="13f60-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="13f60-116">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="13f60-116">The method was successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="13f60-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="13f60-117">Requirements</span></span>



| <span data-ttu-id="13f60-118">需求</span><span class="sxs-lookup"><span data-stu-id="13f60-118">Requirement</span></span> | <span data-ttu-id="13f60-119">值</span><span class="sxs-lookup"><span data-stu-id="13f60-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="13f60-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13f60-120">Minimum supported client</span></span><br/> | <span data-ttu-id="13f60-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13f60-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="13f60-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13f60-122">Minimum supported server</span></span><br/> | <span data-ttu-id="13f60-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="13f60-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="13f60-124">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="13f60-124">Redistributable</span></span><br/>          | <span data-ttu-id="13f60-125">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="13f60-125">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="13f60-126">標頭</span><span class="sxs-lookup"><span data-stu-id="13f60-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="13f60-127"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="13f60-127"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="13f60-128">Idl</span><span class="sxs-lookup"><span data-stu-id="13f60-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="13f60-129"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="13f60-129"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="13f60-130">DLL</span><span class="sxs-lookup"><span data-stu-id="13f60-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13f60-131"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13f60-131"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13f60-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13f60-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13f60-133">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="13f60-133">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





