---
title: WM/MCDI
description: WM/MCDI 屬性包含音樂 CD 識別碼。 這是 CD 中目錄的二進位傾印，可用來唯一識別 CD。
ms.assetid: cb16c62b-b9e0-4676-b1bb-ff26a2e09cb7
keywords:
- WM/MCDI windows Media 格式
topic_type:
- apiref
api_name:
- WM/MCDI
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2da5c629bcef9ca2072d0ddda433fde97932e97e
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "106966224"
---
# <a name="wmmcdi"></a><span data-ttu-id="86f9a-105">WM/MCDI</span><span class="sxs-lookup"><span data-stu-id="86f9a-105">WM/MCDI</span></span>

<span data-ttu-id="86f9a-106">**WM/MCDI** 屬性包含音樂 CD 識別碼。</span><span class="sxs-lookup"><span data-stu-id="86f9a-106">The **WM/MCDI** attribute contains the music CD identifier.</span></span> <span data-ttu-id="86f9a-107">這是 CD 中目錄的二進位傾印，可用來唯一識別 CD。</span><span class="sxs-lookup"><span data-stu-id="86f9a-107">This is a binary dump of the table of contents from the CD that is used to uniquely identify the CD.</span></span>

## <a name="global-constant"></a><span data-ttu-id="86f9a-108">全域常數</span><span class="sxs-lookup"><span data-stu-id="86f9a-108">Global Constant</span></span>

<span data-ttu-id="86f9a-109">g \_ wszWMMCDI</span><span class="sxs-lookup"><span data-stu-id="86f9a-109">g\_wszWMMCDI</span></span>

## <a name="data-type"></a><span data-ttu-id="86f9a-110">資料類型</span><span class="sxs-lookup"><span data-stu-id="86f9a-110">Data Type</span></span>

<span data-ttu-id="86f9a-111">**WMT \_ 類型 \_ 二進位**</span><span class="sxs-lookup"><span data-stu-id="86f9a-111">**WMT\_TYPE\_BINARY**</span></span>

## <a name="remarks"></a><span data-ttu-id="86f9a-112">備註</span><span class="sxs-lookup"><span data-stu-id="86f9a-112">Remarks</span></span>

<span data-ttu-id="86f9a-113">這個屬性與 ID3 框架 MCDI 相容。</span><span class="sxs-lookup"><span data-stu-id="86f9a-113">This attribute is compatible with the ID3 frame, MCDI.</span></span> <span data-ttu-id="86f9a-114">MCDI 框架的 ID3 規格需要每個檔案只有一個這類畫面格，而且有一個有效的 TRCK 框架存在。</span><span class="sxs-lookup"><span data-stu-id="86f9a-114">The ID3 specification for the MCDI frame requires that only one such frame exist per file and that a valid TRCK frame exist.</span></span> <span data-ttu-id="86f9a-115">中繼資料編輯器不會執行這些規則的任何驗證。</span><span class="sxs-lookup"><span data-stu-id="86f9a-115">The metadata editor does not perform any validation for these rules.</span></span> <span data-ttu-id="86f9a-116">此外，WM/MCDI 的大小不會限制為804個位元組，如同 MCDI ID3 框架一樣。</span><span class="sxs-lookup"><span data-stu-id="86f9a-116">Also, the size of WM/MCDI is not limited to 804 bytes, as is the MCDI ID3 frame.</span></span>

## <a name="see-also"></a><span data-ttu-id="86f9a-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="86f9a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="86f9a-118">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="86f9a-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




