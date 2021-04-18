---
title: 'COLORTYPE 列舉 (Softkbdc) '
description: COLORTYPE 列舉的元素可用來指定可供軟鍵盤使用的色彩類型。
ms.assetid: 63a51f67-d85c-4017-a569-03df164198db
keywords:
- COLORTYPE 列舉文字服務架構
topic_type:
- apiref
api_name:
- COLORTYPE
api_location:
- Softkbdc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28f3b4111973e9676a34c548db566b1c95ac43
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965510"
---
# <a name="colortype-enumeration"></a><span data-ttu-id="f27c8-104">COLORTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="f27c8-104">COLORTYPE enumeration</span></span>

<span data-ttu-id="f27c8-105">**COLORTYPE** 列舉的元素可用來指定可供軟鍵盤使用的色彩類型。</span><span class="sxs-lookup"><span data-stu-id="f27c8-105">Elements of the **COLORTYPE** enumeration are used to specify types of colors that are available for a soft keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="f27c8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f27c8-106">Syntax</span></span>


```C++
typedef enum tagCOLORTYPE { 
  bkcolor         = 0,
  UnSelForeColor  = 1,
  UnSelTextColor  = 2,
  SelForeColor    = 3,
  SelTextColor    = 4,
  Max_color_Type  = 5
} COLORTYPE;
```



## <a name="constants"></a><span data-ttu-id="f27c8-107">常數</span><span class="sxs-lookup"><span data-stu-id="f27c8-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="f27c8-108"><span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**</span><span class="sxs-lookup"><span data-stu-id="f27c8-108"><span id="bkcolor"></span><span id="BKCOLOR"></span>**bkcolor**</span></span>
</dt> <dd>

<span data-ttu-id="f27c8-109">背景色彩。</span><span class="sxs-lookup"><span data-stu-id="f27c8-109">Background color.</span></span>

</dd> <dt>

<span data-ttu-id="f27c8-110"><span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**UnSelForeColor**</span><span class="sxs-lookup"><span data-stu-id="f27c8-110"><span id="UnSelForeColor"></span><span id="unselforecolor"></span><span id="UNSELFORECOLOR"></span>**UnSelForeColor**</span></span>
</dt> <dd>

<span data-ttu-id="f27c8-111">未選取的前景色彩。</span><span class="sxs-lookup"><span data-stu-id="f27c8-111">Unselected foreground color.</span></span>

</dd> <dt>

<span data-ttu-id="f27c8-112"><span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**UnSelTextColor**</span><span class="sxs-lookup"><span data-stu-id="f27c8-112"><span id="UnSelTextColor"></span><span id="unseltextcolor"></span><span id="UNSELTEXTCOLOR"></span>**UnSelTextColor**</span></span>
</dt> <dd>

<span data-ttu-id="f27c8-113">未選取的文字色彩。</span><span class="sxs-lookup"><span data-stu-id="f27c8-113">Unselected text color.</span></span>

</dd> <dt>

<span data-ttu-id="f27c8-114"><span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**SelForeColor**</span><span class="sxs-lookup"><span data-stu-id="f27c8-114"><span id="SelForeColor"></span><span id="selforecolor"></span><span id="SELFORECOLOR"></span>**SelForeColor**</span></span>
</dt> <dd>

<span data-ttu-id="f27c8-115">選取的前景色彩。</span><span class="sxs-lookup"><span data-stu-id="f27c8-115">Selected foreground color.</span></span>

</dd> <dt>

<span data-ttu-id="f27c8-116"><span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**SelTextColor**</span><span class="sxs-lookup"><span data-stu-id="f27c8-116"><span id="SelTextColor"></span><span id="seltextcolor"></span><span id="SELTEXTCOLOR"></span>**SelTextColor**</span></span>
</dt> <dd>

<span data-ttu-id="f27c8-117">選取的文字色彩。</span><span class="sxs-lookup"><span data-stu-id="f27c8-117">Selected text color.</span></span>

</dd> <dt>

<span data-ttu-id="f27c8-118"><span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**最大 \_ 色彩 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="f27c8-118"><span id="Max_color_Type"></span><span id="max_color_type"></span><span id="MAX_COLOR_TYPE"></span>**Max\_color\_Type**</span></span>
</dt> <dd>

<span data-ttu-id="f27c8-119">最大色彩類型。</span><span class="sxs-lookup"><span data-stu-id="f27c8-119">Maximum color type.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f27c8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="f27c8-120">Requirements</span></span>



| <span data-ttu-id="f27c8-121">需求</span><span class="sxs-lookup"><span data-stu-id="f27c8-121">Requirement</span></span> | <span data-ttu-id="f27c8-122">值</span><span class="sxs-lookup"><span data-stu-id="f27c8-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f27c8-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f27c8-123">Minimum supported client</span></span><br/> | <span data-ttu-id="f27c8-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f27c8-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="f27c8-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f27c8-125">Minimum supported server</span></span><br/> | <span data-ttu-id="f27c8-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f27c8-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="f27c8-127">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="f27c8-127">Redistributable</span></span><br/>          | <span data-ttu-id="f27c8-128">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="f27c8-128">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                        |
| <span data-ttu-id="f27c8-129">標頭</span><span class="sxs-lookup"><span data-stu-id="f27c8-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="f27c8-130"><dt>Softkbdc。h</dt></span><span class="sxs-lookup"><span data-stu-id="f27c8-130"><dt>Softkbdc.h</dt></span></span> </dl>  |
| <span data-ttu-id="f27c8-131">Idl</span><span class="sxs-lookup"><span data-stu-id="f27c8-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f27c8-132"><dt>Softkbd .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f27c8-132"><dt>Softkbd.idl</dt></span></span> </dl> |



 

 





