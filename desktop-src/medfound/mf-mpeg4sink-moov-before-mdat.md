---
description: 表示在產生的檔案中，moov 會在 mdat box 之前寫入。
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: 'MF_MPEG4SINK_MOOV_BEFORE_MDAT 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b5d345dc027c457ceb6123ce3854fff4b74f987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106993179"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a><span data-ttu-id="c6f56-103">\_ \_ \_ MDAT 屬性之前的 MF MPEG4SINK MOOV \_</span><span class="sxs-lookup"><span data-stu-id="c6f56-103">MF\_MPEG4SINK\_MOOV\_BEFORE\_MDAT attribute</span></span>

<span data-ttu-id="c6f56-104">表示在產生的檔案中，' mdat ' 方塊之前會寫入 ' moov '。</span><span class="sxs-lookup"><span data-stu-id="c6f56-104">Indicates that 'moov' will be written before 'mdat' box in the generated file.</span></span>

## <a name="data-type"></a><span data-ttu-id="c6f56-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c6f56-105">Data type</span></span>

<span data-ttu-id="c6f56-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c6f56-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="c6f56-107">備註</span><span class="sxs-lookup"><span data-stu-id="c6f56-107">Remarks</span></span>

<span data-ttu-id="c6f56-108">Mpeg4 媒體接收器的預設行為是在 [mdat] 方塊後面寫入 ' moov '。</span><span class="sxs-lookup"><span data-stu-id="c6f56-108">The default behavior of the mpeg4 media sink is to write 'moov' after 'mdat' box.</span></span> <span data-ttu-id="c6f56-109">設定這個屬性會導致產生的檔案在 ' mdat ' 方塊之前寫入 ' moov '。</span><span class="sxs-lookup"><span data-stu-id="c6f56-109">Setting this attribute causes the generated file to write 'moov' before 'mdat' box.</span></span>

<span data-ttu-id="c6f56-110">為了讓 mpeg4 接收使用此屬性，傳入的位元組資料流程在的搜尋或遠端中不一定要太慢。</span><span class="sxs-lookup"><span data-stu-id="c6f56-110">In order for the mpeg4 sink to use this attribute, the byte stream passed in must not be slow seek or remote for .</span></span>

<span data-ttu-id="c6f56-111">這項功能牽涉到額外的檔案複製/remuxing。</span><span class="sxs-lookup"><span data-stu-id="c6f56-111">This feature involves an additional file copying/remuxing.</span></span>

## <a name="requirements"></a><span data-ttu-id="c6f56-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="c6f56-112">Requirements</span></span>



| <span data-ttu-id="c6f56-113">需求</span><span class="sxs-lookup"><span data-stu-id="c6f56-113">Requirement</span></span> | <span data-ttu-id="c6f56-114">值</span><span class="sxs-lookup"><span data-stu-id="c6f56-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f56-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c6f56-115">Minimum supported client</span></span><br/> | <span data-ttu-id="c6f56-116">Windows 8 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6f56-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="c6f56-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c6f56-117">Minimum supported server</span></span><br/> | <span data-ttu-id="c6f56-118">Windows Server 2012 \[ desktop app \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c6f56-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="c6f56-119">標頭</span><span class="sxs-lookup"><span data-stu-id="c6f56-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="c6f56-120"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c6f56-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6f56-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c6f56-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6f56-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="c6f56-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c6f56-123">媒體類型屬性</span><span class="sxs-lookup"><span data-stu-id="c6f56-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




