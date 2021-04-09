---
title: 'ISoftKbd ShowSoftKeyboard 方法 (Softkbdc .h) '
description: ISoftKbd ShowSoftKeyboard 方法會顯示軟鍵盤。
ms.assetid: 7e24bef1-accb-40f6-a549-fb676abf9971
keywords:
- ShowSoftKeyboard 方法文字服務架構
- ShowSoftKeyboard 方法文字服務架構，ISoftKbd 介面
- ISoftKbd 介面文字服務架構，ShowSoftKeyboard 方法
topic_type:
- apiref
api_name:
- ISoftKbd.ShowSoftKeyboard
api_location:
- Softkbd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b319e7782a19571cf827175566e1af056c34cd4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024550"
---
# <a name="isoftkbdshowsoftkeyboard-method"></a><span data-ttu-id="80598-106">ISoftKbd：： ShowSoftKeyboard 方法</span><span class="sxs-lookup"><span data-stu-id="80598-106">ISoftKbd::ShowSoftKeyboard method</span></span>

<span data-ttu-id="80598-107">**ISoftKbd：： ShowSoftKeyboard** 方法會顯示軟鍵盤。</span><span class="sxs-lookup"><span data-stu-id="80598-107">The **ISoftKbd::ShowSoftKeyboard** method displays a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="80598-108">語法</span><span class="sxs-lookup"><span data-stu-id="80598-108">Syntax</span></span>


```C++
HRESULT ShowSoftKeyboard(
  [in] INT iShow
);
```



## <a name="parameters"></a><span data-ttu-id="80598-109">參數</span><span class="sxs-lookup"><span data-stu-id="80598-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80598-110">*iShow* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80598-110">*iShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80598-111">整數，表示要顯示的軟鍵盤類型。</span><span class="sxs-lookup"><span data-stu-id="80598-111">Integer indicating the type of soft keyboard to display.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="80598-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="80598-112">Return value</span></span>

<span data-ttu-id="80598-113">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="80598-113">This method can return one of these values.</span></span>



| <span data-ttu-id="80598-114">值</span><span class="sxs-lookup"><span data-stu-id="80598-114">Value</span></span>                                                                                | <span data-ttu-id="80598-115">描述</span><span class="sxs-lookup"><span data-stu-id="80598-115">Description</span></span>                           |
|--------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="80598-116"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="80598-116"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="80598-117">此方法成功。</span><span class="sxs-lookup"><span data-stu-id="80598-117">The method was successful.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="80598-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="80598-118">Requirements</span></span>



| <span data-ttu-id="80598-119">需求</span><span class="sxs-lookup"><span data-stu-id="80598-119">Requirement</span></span> | <span data-ttu-id="80598-120">值</span><span class="sxs-lookup"><span data-stu-id="80598-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80598-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80598-121">Minimum supported client</span></span><br/> | <span data-ttu-id="80598-122">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80598-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="80598-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80598-123">Minimum supported server</span></span><br/> | <span data-ttu-id="80598-124">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="80598-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="80598-125">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="80598-125">Redistributable</span></span><br/>          | <span data-ttu-id="80598-126">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="80598-126">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="80598-127">標頭</span><span class="sxs-lookup"><span data-stu-id="80598-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="80598-128"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="80598-128"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="80598-129">Idl</span><span class="sxs-lookup"><span data-stu-id="80598-129">IDL</span></span><br/>                      | <dl> <span data-ttu-id="80598-130"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="80598-130"><dt>Softkbd.idl</dt></span></span> </dl> |
| <span data-ttu-id="80598-131">DLL</span><span class="sxs-lookup"><span data-stu-id="80598-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80598-132"><dt>Softkbd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80598-132"><dt>Softkbd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80598-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80598-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80598-134">**ISoftKbd**</span><span class="sxs-lookup"><span data-stu-id="80598-134">**ISoftKbd**</span></span>](isoftkbd.md)
</dt> </dl>

 

 





