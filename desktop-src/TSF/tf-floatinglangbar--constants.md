---
title: 'TF_FLOATINGLANGBAR_ 常數 (Ctfutb) '
description: '\_針對語言列視窗的標題定義 TF FLOATINGLANGBAR \_ \ 常數位符串。'
ms.assetid: 05394b71-2cc3-440e-943b-d69ee0432fb0
topic_type:
- apiref
api_name:
- TF_FLOATINGLANGBAR_WNDTITLEW
- TF_FLOATINGLANGBAR_WNDTITLEA
- TF_FLOATINGLANGBAR_WNDTITLE
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c789e507b2cc56281dc61750d4fe0748bee8841
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968348"
---
# <a name="tf_floatinglangbar_-constants"></a><span data-ttu-id="b4877-103">TF \_ FLOATINGLANGBAR \_ \* 常數</span><span class="sxs-lookup"><span data-stu-id="b4877-103">TF\_FLOATINGLANGBAR\_\* Constants</span></span>

<span data-ttu-id="b4877-104">\_針對語言列視窗的標題定義 TF FLOATINGLANGBAR \_ \* 常數位符串。</span><span class="sxs-lookup"><span data-stu-id="b4877-104">The define a TF\_FLOATINGLANGBAR\_\* constants string for the title of the language bar window.</span></span>



| <span data-ttu-id="b4877-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="b4877-105">Constant/value</span></span>                                                                                                                                                                                                                                                                                  | <span data-ttu-id="b4877-106">Description</span><span class="sxs-lookup"><span data-stu-id="b4877-106">Description</span></span>                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_FLOATINGLANGBAR_WNDTITLEW"></span><span id="tf_floatinglangbar_wndtitlew"></span><dl> <span data-ttu-id="b4877-107"><dt>**TF \_FLOATINGLANGBAR \_ WNDTITLEW**</dt> <dt>LTF \_ FLOATINGLANGBAR \_ WndTitle</dt></span><span class="sxs-lookup"><span data-stu-id="b4877-107"><dt>**TF\_FLOATINGLANGBAR\_WNDTITLEW**</dt> <dt>LTF\_FloatingLangBar\_WndTitle</dt></span></span> </dl> | <span data-ttu-id="b4877-108">標題的 Unicode 字元 L "TF \_ FloatingLangBar \_ WndTitle" 字串。</span><span class="sxs-lookup"><span data-stu-id="b4877-108">The string of Unicode characters L"TF\_FloatingLangBar\_WndTitle" for the title.</span></span><br/>                                                                                  |
| <span id="TF_FLOATINGLANGBAR_WNDTITLEA"></span><span id="tf_floatinglangbar_wndtitlea"></span><dl> <span data-ttu-id="b4877-109"><dt>**TF \_FLOATINGLANGBAR \_ WNDTITLEA**</dt> <dt>TF \_ FLOATINGLANGBAR \_ WndTitle</dt></span><span class="sxs-lookup"><span data-stu-id="b4877-109"><dt>**TF\_FLOATINGLANGBAR\_WNDTITLEA**</dt> <dt>TF\_FloatingLangBar\_WndTitle</dt></span></span> </dl>  | <span data-ttu-id="b4877-110">標題的 ANSI 字元 "TF \_ FloatingLangBar \_ WndTitle" 字串。</span><span class="sxs-lookup"><span data-stu-id="b4877-110">The string of ANSI characters "TF\_FloatingLangBar\_WndTitle" for the title.</span></span><br/>                                                                                      |
| <span id="TF_FLOATINGLANGBAR_WNDTITLE"></span><span id="tf_floatinglangbar_wndtitle"></span><dl> <span data-ttu-id="b4877-111"><dt>**TF \_FLOATINGLANGBAR \_ WNDTITLE**</dt> <dt>TF \_ FLOATINGLANGBAR \_ WNDTITLEA</dt></span><span class="sxs-lookup"><span data-stu-id="b4877-111"><dt>**TF\_FLOATINGLANGBAR\_WNDTITLE**</dt> <dt>TF\_FLOATINGLANGBAR\_WNDTITLEA</dt></span></span> </dl>    | <span data-ttu-id="b4877-112">如果已定義 Unicode，則會接受 TF \_ FLOATINGLANGBAR \_ WNDTITLEW 常數的值。</span><span class="sxs-lookup"><span data-stu-id="b4877-112">If Unicode is defined, takes the value of the TF\_FLOATINGLANGBAR\_WNDTITLEW constant.</span></span> <span data-ttu-id="b4877-113">否則，會取得 TF \_ FLOATINGLANGBAR \_ WNDTITLEA 常數的值。</span><span class="sxs-lookup"><span data-stu-id="b4877-113">Otherwise, takes the value of the TF\_FLOATINGLANGBAR\_WNDTITLEA constant.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b4877-114">備註</span><span class="sxs-lookup"><span data-stu-id="b4877-114">Remarks</span></span>

<span data-ttu-id="b4877-115">雖然此群組中有三個常數，但主要一個是 TF \_ FLOATINGLANGBAR \_ WNDTITLE，視需要採用 ANSI 或 Unicode 值。</span><span class="sxs-lookup"><span data-stu-id="b4877-115">Although there are three constants in this group, the primary one is TF\_FLOATINGLANGBAR\_WNDTITLE, which takes either the ANSI or Unicode value, as appropriate.</span></span>

## <a name="requirements"></a><span data-ttu-id="b4877-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4877-116">Requirements</span></span>



| <span data-ttu-id="b4877-117">需求</span><span class="sxs-lookup"><span data-stu-id="b4877-117">Requirement</span></span> | <span data-ttu-id="b4877-118">值</span><span class="sxs-lookup"><span data-stu-id="b4877-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b4877-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b4877-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b4877-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4877-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="b4877-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b4877-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b4877-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b4877-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b4877-123">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="b4877-123">Redistributable</span></span><br/>          | <span data-ttu-id="b4877-124">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="b4877-124">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="b4877-125">標頭</span><span class="sxs-lookup"><span data-stu-id="b4877-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b4877-126"><dt>Ctfutb。h</dt></span><span class="sxs-lookup"><span data-stu-id="b4877-126"><dt>Ctfutb.h</dt></span></span> </dl>   |
| <span data-ttu-id="b4877-127">Idl</span><span class="sxs-lookup"><span data-stu-id="b4877-127">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b4877-128"><dt>Ctfutb .idl</dt></span><span class="sxs-lookup"><span data-stu-id="b4877-128"><dt>Ctfutb.idl</dt></span></span> </dl> |



 

 





