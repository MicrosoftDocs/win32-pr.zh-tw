---
title: '預先定義的清單屬性 (TsAttrid) '
description: 下列值會識別以 ITfCoNtext GetAppProperty 方法取得的清單屬性。 包含每個屬性類型的資料格式和內容。
ms.assetid: 9a9e1912-51c0-40e0-9e3a-b84ea7077dbe
keywords:
- 預先定義的清單屬性文字服務架構
topic_type:
- apiref
api_name:
- Predefined List Attributes
api_location:
- TsAttrid.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81ade2403e124b934c6872f39c01fc7fc1ea6f6b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105384"
---
# <a name="predefined-list-attributes"></a><span data-ttu-id="cd090-105">預先定義的清單屬性</span><span class="sxs-lookup"><span data-stu-id="cd090-105">Predefined List Attributes</span></span>

<span data-ttu-id="cd090-106">下列值會識別以 [ITfCoNtext：： GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) 方法取得的清單屬性。</span><span class="sxs-lookup"><span data-stu-id="cd090-106">The following values identify list attributes obtained with the [ITfContext::GetAppProperty](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty) method.</span></span> <span data-ttu-id="cd090-107">包含每個屬性類型的資料格式和內容。</span><span class="sxs-lookup"><span data-stu-id="cd090-107">The data format and contents of each property type are included.</span></span>

## <a name="properties"></a><span data-ttu-id="cd090-108">屬性</span><span class="sxs-lookup"><span data-stu-id="cd090-108">Properties</span></span>



| <span data-ttu-id="cd090-109">屬性</span><span class="sxs-lookup"><span data-stu-id="cd090-109">Property</span></span>                          | <span data-ttu-id="cd090-110">描述</span><span class="sxs-lookup"><span data-stu-id="cd090-110">Description</span></span>                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cd090-111">TSATTRID \_ 清單</span><span class="sxs-lookup"><span data-stu-id="cd090-111">TSATTRID\_List</span></span>                    | <span data-ttu-id="cd090-112">未使用。</span><span class="sxs-lookup"><span data-stu-id="cd090-112">Not used.</span></span>                                                                                       |
| <span data-ttu-id="cd090-113">TSATTRID \_ 清單 \_ LevelIndel</span><span class="sxs-lookup"><span data-stu-id="cd090-113">TSATTRID\_List\_LevelIndel</span></span>        | <span data-ttu-id="cd090-114">包含清單的索引層級。</span><span class="sxs-lookup"><span data-stu-id="cd090-114">Contains the index level of the list.</span></span> <span data-ttu-id="cd090-115">1是最外層的層級，2是下一個層級，依此類推。</span><span class="sxs-lookup"><span data-stu-id="cd090-115">1 is the outermost level, 2 is the next level, and so on.</span></span> |
| <span data-ttu-id="cd090-116">TSATTRID \_ 清單 \_ 類型</span><span class="sxs-lookup"><span data-stu-id="cd090-116">TSATTRID\_List\_Type</span></span>              | <span data-ttu-id="cd090-117">未使用。</span><span class="sxs-lookup"><span data-stu-id="cd090-117">Not used.</span></span>                                                                                       |
| <span data-ttu-id="cd090-118">TSATTRID \_ 清單 \_ 類型 \_ 阿拉伯文</span><span class="sxs-lookup"><span data-stu-id="cd090-118">TSATTRID\_List\_Type\_Arabic</span></span>      | <span data-ttu-id="cd090-119">如果清單是阿拉伯文數位清單，則包含非零值，否則為零。</span><span class="sxs-lookup"><span data-stu-id="cd090-119">Contains a nonzero value if the list is an arabic numeral list or zero otherwise.</span></span>               |
| <span data-ttu-id="cd090-120">TSATTRID \_ 清單 \_ 類型 \_ 專案符號</span><span class="sxs-lookup"><span data-stu-id="cd090-120">TSATTRID\_List\_Type\_Bullet</span></span>      | <span data-ttu-id="cd090-121">如果清單是項目符號清單，則包含非零值，否則為零。</span><span class="sxs-lookup"><span data-stu-id="cd090-121">Contains a nonzero value if the list is a bulleted list or zero otherwise.</span></span>                      |
| <span data-ttu-id="cd090-122">TSATTRID \_ 清單 \_ 類型 \_ LowerLetter</span><span class="sxs-lookup"><span data-stu-id="cd090-122">TSATTRID\_List\_Type\_LowerLetter</span></span> | <span data-ttu-id="cd090-123">如果清單是小寫字母清單，則包含非零值，否則為零。</span><span class="sxs-lookup"><span data-stu-id="cd090-123">Contains a nonzero value if the list is a lowercase lettered list or zero otherwise.</span></span>            |
| <span data-ttu-id="cd090-124">TSATTRID \_ 清單 \_ 類型 \_ LowerRoman</span><span class="sxs-lookup"><span data-stu-id="cd090-124">TSATTRID\_List\_Type\_LowerRoman</span></span>  | <span data-ttu-id="cd090-125">如果清單是小寫的羅馬數字清單，則包含非零值，否則為零。</span><span class="sxs-lookup"><span data-stu-id="cd090-125">Contains a nonzero value if the list is a lowercase roman numeral list or zero otherwise.</span></span>       |
| <span data-ttu-id="cd090-126">TSATTRID \_ 清單 \_ 類型 \_ UpperLetter</span><span class="sxs-lookup"><span data-stu-id="cd090-126">TSATTRID\_List\_Type\_UpperLetter</span></span> | <span data-ttu-id="cd090-127">如果清單是大寫的字母清單，則包含非零值，否則為零。</span><span class="sxs-lookup"><span data-stu-id="cd090-127">Contains a nonzero value if the list is an upper-case lettered list or zero otherwise.</span></span>          |
| <span data-ttu-id="cd090-128">TSATTRID \_ 清單 \_ 類型 \_ UpperRoman</span><span class="sxs-lookup"><span data-stu-id="cd090-128">TSATTRID\_List\_Type\_UpperRoman</span></span>  | <span data-ttu-id="cd090-129">如果清單是大寫的羅馬數字清單，則包含非零值，否則為零。</span><span class="sxs-lookup"><span data-stu-id="cd090-129">Contains a nonzero value if the list is an uppercase roman numeral list or zero otherwise.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="cd090-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd090-130">Requirements</span></span>



| <span data-ttu-id="cd090-131">需求</span><span class="sxs-lookup"><span data-stu-id="cd090-131">Requirement</span></span> | <span data-ttu-id="cd090-132">值</span><span class="sxs-lookup"><span data-stu-id="cd090-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cd090-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd090-133">Minimum supported client</span></span><br/> | <span data-ttu-id="cd090-134">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd090-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="cd090-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd090-135">Minimum supported server</span></span><br/> | <span data-ttu-id="cd090-136">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd090-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="cd090-137">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="cd090-137">Redistributable</span></span><br/>          | <span data-ttu-id="cd090-138">Windows 2000 Professional 上的 TSF 1。0</span><span class="sxs-lookup"><span data-stu-id="cd090-138">TSF 1.0 on Windows 2000 Professional</span></span><br/>                                       |
| <span data-ttu-id="cd090-139">標頭</span><span class="sxs-lookup"><span data-stu-id="cd090-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd090-140"><dt>TsAttrid。h</dt></span><span class="sxs-lookup"><span data-stu-id="cd090-140"><dt>TsAttrid.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd090-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd090-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd090-142">ITfCoNtext：： GetAppProperty</span><span class="sxs-lookup"><span data-stu-id="cd090-142">ITfContext::GetAppProperty</span></span>](/windows/desktop/api/msctf/nf-msctf-itfcontext-getappproperty)
</dt> </dl>

 

