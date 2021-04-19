---
description: 將原始單字形式放在 IWordFormSink 物件中。
ms.assetid: 333A3109-6C0A-42AE-9E10-87F53C7F737C
title: 'IWordFormSink：:P utWord 方法 (搜尋 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWordFormSink.PutWord
api_type:
- COM
api_location:
- search.h
ms.openlocfilehash: 438cb41e50f264bd373ae2ef8e84598b651b0352
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985401"
---
# <a name="iwordformsinkputword-method"></a><span data-ttu-id="215a0-103">IWordFormSink：:P utWord 方法</span><span class="sxs-lookup"><span data-stu-id="215a0-103">IWordFormSink::PutWord method</span></span>

<span data-ttu-id="215a0-104">將原始單字形式放在 [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) 物件中。</span><span class="sxs-lookup"><span data-stu-id="215a0-104">Puts the original word form in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="215a0-105">語法</span><span class="sxs-lookup"><span data-stu-id="215a0-105">Syntax</span></span>


```C++
HRESULT PutWord(
  [in] const WCHAR *pwcInBuf ,
  [in]       ULONG cwc
);
```



## <a name="parameters"></a><span data-ttu-id="215a0-106">參數</span><span class="sxs-lookup"><span data-stu-id="215a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="215a0-107">*pwcInBuf* \[在\]</span><span class="sxs-lookup"><span data-stu-id="215a0-107">*pwcInBuf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="215a0-108">緩衝區的指標，其中包含單字的最終替代形式，一律為原始單字。</span><span class="sxs-lookup"><span data-stu-id="215a0-108">A pointer to a buffer that contains the final alternative form of a word, which is always the original word.</span></span>

</dd> <dt>

<span data-ttu-id="215a0-109">*cwc* \[在\]</span><span class="sxs-lookup"><span data-stu-id="215a0-109">*cwc* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="215a0-110">*PwcInBuf* 中的字元數。</span><span class="sxs-lookup"><span data-stu-id="215a0-110">The number of characters in *pwcInBuf*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="215a0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="215a0-111">Return value</span></span>

<span data-ttu-id="215a0-112">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="215a0-112">This method can return one of these values.</span></span>



| <span data-ttu-id="215a0-113">傳回碼</span><span class="sxs-lookup"><span data-stu-id="215a0-113">Return code</span></span>                                                                          | <span data-ttu-id="215a0-114">Description</span><span class="sxs-lookup"><span data-stu-id="215a0-114">Description</span></span>                                           |
|--------------------------------------------------------------------------------------|-------------------------------------------------------|
| <dl> <span data-ttu-id="215a0-115"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="215a0-115"><dt>**S\_OK**</dt></span></span> </dl> | <span data-ttu-id="215a0-116">作業已順利完成。</span><span class="sxs-lookup"><span data-stu-id="215a0-116">The operation was completed successfully.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="215a0-117">備註</span><span class="sxs-lookup"><span data-stu-id="215a0-117">Remarks</span></span>

<span data-ttu-id="215a0-118">**PutWord** 是從 [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer)執行的 [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms)方法中呼叫。</span><span class="sxs-lookup"><span data-stu-id="215a0-118">**PutWord** is called from the [**GenerateWordForms**](/windows/win32/api/indexsrv/nf-indexsrv-istemmer-generatewordforms) method of the [**IStemmer**](/windows/win32/api/indexsrv/nn-indexsrv-istemmer) implementation.</span></span> <span data-ttu-id="215a0-119">這個方法會處理單字的原始形式，最後會呼叫。</span><span class="sxs-lookup"><span data-stu-id="215a0-119">This method handles the original form of a word and is called last.</span></span> <span data-ttu-id="215a0-120">所有上述的單字替代形式都會藉由呼叫 [**IWordFormSink：:P utaltword**](iwordformsink-putphrase.md)來放置於 [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)物件中。</span><span class="sxs-lookup"><span data-stu-id="215a0-120">All preceding alternative forms for a word are put in the [**IWordFormSink**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink) object by calling [**IWordFormSink::PutAltWord**](iwordformsink-putphrase.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="215a0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="215a0-121">Requirements</span></span>



| <span data-ttu-id="215a0-122">需求</span><span class="sxs-lookup"><span data-stu-id="215a0-122">Requirement</span></span> | <span data-ttu-id="215a0-123">值</span><span class="sxs-lookup"><span data-stu-id="215a0-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="215a0-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="215a0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="215a0-125">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="215a0-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="215a0-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="215a0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="215a0-127">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="215a0-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="215a0-128">標頭</span><span class="sxs-lookup"><span data-stu-id="215a0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="215a0-129"><dt>搜尋。h</dt></span><span class="sxs-lookup"><span data-stu-id="215a0-129"><dt>Search.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="215a0-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="215a0-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="215a0-131">**IWordFormSink**</span><span class="sxs-lookup"><span data-stu-id="215a0-131">**IWordFormSink**</span></span>](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordformsink)
</dt> </dl>

 

 
