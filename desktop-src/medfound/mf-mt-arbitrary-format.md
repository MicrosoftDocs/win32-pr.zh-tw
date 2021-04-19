---
description: 使用 Advanced Systems 格式之二進位資料流程的其他格式資料 (ASF) 檔。
ms.assetid: fc5b9890-1508-498e-b2ce-ed4fa2052f9c
title: 'MF_MT_ARBITRARY_FORMAT 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6cf98da23fbc4631ca67462dfc58f870abe73885
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990309"
---
# <a name="mf_mt_arbitrary_format-attribute"></a><span data-ttu-id="9337d-103">MF \_ MT \_ 任意 \_ 格式屬性</span><span class="sxs-lookup"><span data-stu-id="9337d-103">MF\_MT\_ARBITRARY\_FORMAT attribute</span></span>

<span data-ttu-id="9337d-104">使用 Advanced Systems 格式之二進位資料流程的其他格式資料 (ASF) 檔。</span><span class="sxs-lookup"><span data-stu-id="9337d-104">Additional format data for a binary stream in an Advanced Systems Format (ASF) file.</span></span>

## <a name="data-type"></a><span data-ttu-id="9337d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="9337d-105">Data type</span></span>

<span data-ttu-id="9337d-106">**位元組\[\]**</span><span class="sxs-lookup"><span data-stu-id="9337d-106">**BYTE\[\]**</span></span>

## <a name="getset"></a><span data-ttu-id="9337d-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="9337d-107">Get/set</span></span>

<span data-ttu-id="9337d-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)。</span><span class="sxs-lookup"><span data-stu-id="9337d-108">To get this attribute, call [**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob).</span></span>

<span data-ttu-id="9337d-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)。</span><span class="sxs-lookup"><span data-stu-id="9337d-109">To set this attribute, call [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob).</span></span>

## <a name="remarks"></a><span data-ttu-id="9337d-110">備註</span><span class="sxs-lookup"><span data-stu-id="9337d-110">Remarks</span></span>

<span data-ttu-id="9337d-111">應用程式可以使用二進位資料流程來保存自訂資料類型。</span><span class="sxs-lookup"><span data-stu-id="9337d-111">Applications can use binary streams to hold custom data types.</span></span> <span data-ttu-id="9337d-112">ASF 媒體來源會將此屬性的值視為不透明 blob。</span><span class="sxs-lookup"><span data-stu-id="9337d-112">The ASF media source treats the value of this attribute as an opaque blob.</span></span> <span data-ttu-id="9337d-113">[**MT \_ 任意 \_ 標頭**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header)結構的 **formattype** 成員定義格式資料的版面配置。</span><span class="sxs-lookup"><span data-stu-id="9337d-113">The **formattype** member of the [**MT\_ARBITRARY\_HEADER**](/windows/desktop/api/mfapi/ns-mfapi-mt_arbitrary_header) structure defines the layout of the format data.</span></span>

<span data-ttu-id="9337d-114">在資料流程類型為 **ASF \_ 二進位 \_ 媒體** 的檔案中，此結構對應于資料流程屬性物件中特定類型資料的格式資料欄位。</span><span class="sxs-lookup"><span data-stu-id="9337d-114">This structure corresponds to the Format Data field of the type-specific data in the Stream Properties Object, in files where the stream type is **ASF\_Binary\_Media**.</span></span> <span data-ttu-id="9337d-115">如需詳細資訊，請參閱 ASF 規格。</span><span class="sxs-lookup"><span data-stu-id="9337d-115">For more information, see the ASF specification.</span></span>

> [!Note]  
> <span data-ttu-id="9337d-116">在 Windows Media 格式 SDK 中，二進位資料流程稱為 *任意資料流程* 或 *任意* 資料流程。</span><span class="sxs-lookup"><span data-stu-id="9337d-116">In the Windows Media Format SDK, binary streams are called *arbitrary streams* or *arbitrary data streams*.</span></span>

 

<span data-ttu-id="9337d-117">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="9337d-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9337d-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="9337d-118">Requirements</span></span>



| <span data-ttu-id="9337d-119">需求</span><span class="sxs-lookup"><span data-stu-id="9337d-119">Requirement</span></span> | <span data-ttu-id="9337d-120">值</span><span class="sxs-lookup"><span data-stu-id="9337d-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9337d-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9337d-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9337d-122">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9337d-122">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9337d-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9337d-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9337d-124">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9337d-124">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="9337d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="9337d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9337d-126"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9337d-126"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9337d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9337d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9337d-128">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="9337d-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9337d-129">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="9337d-129">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="9337d-130">MF \_ MT \_ 任意 \_ 標頭</span><span class="sxs-lookup"><span data-stu-id="9337d-130">MF\_MT\_ARBITRARY\_HEADER</span></span>](mf-mt-arbitrary-header.md)
</dt> </dl>

 

 




