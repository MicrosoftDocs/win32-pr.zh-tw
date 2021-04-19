---
description: LINELOCATIONOPTION \_ 常數會定義 LINELOCATIONENTRY 結構的 >dwoptions 成員所使用的值，這些值會在 lineGetTranslateCaps 所傳回之 LINETRANSLATECAPS 結構的一部分傳回。
ms.assetid: 3b185c16-2535-4a90-855b-29e52828ea4c
title: 'LINELOCATIONOPTION_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f60398953d2f809e29a78323e3b1dedfcac7a1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978441"
---
# <a name="linelocationoption_-constants"></a><span data-ttu-id="8fff5-103">LINELOCATIONOPTION \_ 常數</span><span class="sxs-lookup"><span data-stu-id="8fff5-103">LINELOCATIONOPTION\_ Constants</span></span>

<span data-ttu-id="8fff5-104">**\_ LINELOCATIONOPTION** 常數會定義 [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry)結構的 **>dwoptions** 成員所使用的值，這些值會在 [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)所傳回之 [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps)結構的一部分傳回。</span><span class="sxs-lookup"><span data-stu-id="8fff5-104">The **LINELOCATIONOPTION\_** constants define values used in the **dwOptions** member of the [**LINELOCATIONENTRY**](/windows/desktop/api/Tapi/ns-tapi-linelocationentry) structure returned as part of the [**LINETRANSLATECAPS**](/windows/desktop/api/Tapi/ns-tapi-linetranslatecaps) structure returned by [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps).</span></span>

<dl> <dt>

<span data-ttu-id="8fff5-105"><span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION \_ PULSEDIAL**</span><span class="sxs-lookup"><span data-stu-id="8fff5-105"><span id="LINELOCATIONOPTION_PULSEDIAL"></span><span id="linelocationoption_pulsedial"></span>**LINELOCATIONOPTION\_PULSEDIAL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="8fff5-106">這個位置的預設撥號模式是撥盤式撥號。</span><span class="sxs-lookup"><span data-stu-id="8fff5-106">The default dialing mode at this location is pulse dialing.</span></span> <span data-ttu-id="8fff5-107">如果設定此位， [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) 會在選取這個位置時所傳回之可撥出字串的開頭插入 "P" 撥號修飾詞。</span><span class="sxs-lookup"><span data-stu-id="8fff5-107">If this bit is set, [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress) will insert a "P" dial modifier at the beginning of the dialable string returned when this location is selected.</span></span> <span data-ttu-id="8fff5-108">如果未設定此位， **lineTranslateAddress** 會在可撥出字串的開頭插入 "T" 撥號修飾詞。</span><span class="sxs-lookup"><span data-stu-id="8fff5-108">If this bit is not set, **lineTranslateAddress** will insert a "T" dial modifier at the beginning of the dialable string.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8fff5-109">備註</span><span class="sxs-lookup"><span data-stu-id="8fff5-109">Remarks</span></span>

<span data-ttu-id="8fff5-110">不可延伸。</span><span class="sxs-lookup"><span data-stu-id="8fff5-110">Not extensible.</span></span> <span data-ttu-id="8fff5-111">所有32位都是保留的。</span><span class="sxs-lookup"><span data-stu-id="8fff5-111">All 32 bits are reserved.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fff5-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fff5-112">Requirements</span></span>



| <span data-ttu-id="8fff5-113">需求</span><span class="sxs-lookup"><span data-stu-id="8fff5-113">Requirement</span></span> | <span data-ttu-id="8fff5-114">值</span><span class="sxs-lookup"><span data-stu-id="8fff5-114">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="8fff5-115">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="8fff5-115">TAPI version</span></span><br/> | <span data-ttu-id="8fff5-116">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="8fff5-116">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="8fff5-117">標頭</span><span class="sxs-lookup"><span data-stu-id="8fff5-117">Header</span></span><br/>       | <dl> <span data-ttu-id="8fff5-118"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="8fff5-118"><dt>Tapi.h</dt></span></span> </dl> |



 

 




