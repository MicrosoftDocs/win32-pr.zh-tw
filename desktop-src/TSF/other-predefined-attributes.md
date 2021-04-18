---
title: '其他預先定義的屬性 (TsAttrid) '
description: 下列值會識別以 ITfCoNtext GetAppProperty 方法取得的其他屬性。 包含每個屬性類型的資料格式和內容。
ms.assetid: 8536938b-98a1-415b-b5f2-45b90215c270
keywords:
- 其他預先定義的屬性文字服務架構
topic_type:
- apiref
api_name:
- Other Predefined Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0d0a3ff72a5ea84a6b9e5b47106012a945dbf45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968586"
---
# <a name="other-predefined-attributes"></a><span data-ttu-id="32457-105">其他預先定義的屬性</span><span class="sxs-lookup"><span data-stu-id="32457-105">Other Predefined Attributes</span></span>

<span data-ttu-id="32457-106">下列值會識別以 [ITfCoNtext：： GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) 方法取得的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="32457-106">The following values identify miscellaneous attributes obtained with the [ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) method.</span></span> <span data-ttu-id="32457-107">包含每個屬性類型的資料格式和內容。</span><span class="sxs-lookup"><span data-stu-id="32457-107">The data format and contents of each property type are included.</span></span>

## <a name="properties"></a><span data-ttu-id="32457-108">屬性</span><span class="sxs-lookup"><span data-stu-id="32457-108">Properties</span></span>



| <span data-ttu-id="32457-109">屬性</span><span class="sxs-lookup"><span data-stu-id="32457-109">Property</span></span>                             | <span data-ttu-id="32457-110">描述</span><span class="sxs-lookup"><span data-stu-id="32457-110">Description</span></span>                                                                       |
|--------------------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="32457-111">**TSATTRID \_ 應用程式**</span><span class="sxs-lookup"><span data-stu-id="32457-111">**TSATTRID\_App**</span></span>                    | <span data-ttu-id="32457-112">未使用。</span><span class="sxs-lookup"><span data-stu-id="32457-112">Not used.</span></span>                                                                         |
| <span data-ttu-id="32457-113">**TSATTRID \_ 應用程式 \_ IncorrectGrammar**</span><span class="sxs-lookup"><span data-stu-id="32457-113">**TSATTRID\_App\_IncorrectGrammar**</span></span>  | <span data-ttu-id="32457-114">如果文字包含文法錯誤，則包含非零值，否則為零。</span><span class="sxs-lookup"><span data-stu-id="32457-114">Contains a nonzero value if the text contains a grammar error or zero otherwise.</span></span>  |
| <span data-ttu-id="32457-115">**TSATTRID \_ 應用程式 \_ IncorrectSpelling**</span><span class="sxs-lookup"><span data-stu-id="32457-115">**TSATTRID\_App\_IncorrectSpelling**</span></span> | <span data-ttu-id="32457-116">如果文字包含拼寫錯誤，則包含非零值，否則為零。</span><span class="sxs-lookup"><span data-stu-id="32457-116">Contains a nonzero value if the text contains a spelling error or zero otherwise.</span></span> |
| <span data-ttu-id="32457-117">**TSATTRID \_ 其他人**</span><span class="sxs-lookup"><span data-stu-id="32457-117">**TSATTRID\_OTHERS**</span></span>                 | <span data-ttu-id="32457-118">未使用。</span><span class="sxs-lookup"><span data-stu-id="32457-118">Not used.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="32457-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="32457-119">Requirements</span></span>



| <span data-ttu-id="32457-120">需求</span><span class="sxs-lookup"><span data-stu-id="32457-120">Requirement</span></span> | <span data-ttu-id="32457-121">值</span><span class="sxs-lookup"><span data-stu-id="32457-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32457-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32457-122">Minimum supported client</span></span><br/> | <span data-ttu-id="32457-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32457-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="32457-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32457-124">Minimum supported server</span></span><br/> | <span data-ttu-id="32457-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="32457-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="32457-126">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="32457-126">Redistributable</span></span><br/>          | <span data-ttu-id="32457-127">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="32457-127">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="32457-128">標頭</span><span class="sxs-lookup"><span data-stu-id="32457-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="32457-129"><dt>TsAttrid。h</dt></span><span class="sxs-lookup"><span data-stu-id="32457-129"><dt>TsAttrid.h</dt></span></span> </dl> |



 

