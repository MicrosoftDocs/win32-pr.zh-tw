---
description: 包含資料流程的名稱。
ms.assetid: 80235820-761f-4deb-9bf6-82ef402b3ee4
title: 'MF_SD_STREAM_NAME 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 734c2d20390ba1a450a40c03054b4c67c5c0409a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320624"
---
# <a name="mf_sd_stream_name-attribute"></a><span data-ttu-id="27d8c-103">MF \_ SD \_ STREAM \_ NAME 屬性</span><span class="sxs-lookup"><span data-stu-id="27d8c-103">MF\_SD\_STREAM\_NAME attribute</span></span>

<span data-ttu-id="27d8c-104">包含資料流程的名稱。</span><span class="sxs-lookup"><span data-stu-id="27d8c-104">Contains the name of a stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="27d8c-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="27d8c-105">Data type</span></span>

<span data-ttu-id="27d8c-106">\**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="27d8c-106">\**WCHAR\** _</span></span>

## <a name="getset"></a><span data-ttu-id="27d8c-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="27d8c-107">Get/set</span></span>

<span data-ttu-id="27d8c-108">若要取得這個屬性，請呼叫 [_ *IMFAttributes：： GetString* \*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)。</span><span class="sxs-lookup"><span data-stu-id="27d8c-108">To get this attribute, call [_ *IMFAttributes::GetString*\*](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="27d8c-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)。</span><span class="sxs-lookup"><span data-stu-id="27d8c-109">To set this attribute, call [**IMFAttributes::SetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="27d8c-110">適用於</span><span class="sxs-lookup"><span data-stu-id="27d8c-110">Applies to</span></span>

[<span data-ttu-id="27d8c-111">**IMFStreamDescriptor**</span><span class="sxs-lookup"><span data-stu-id="27d8c-111">**IMFStreamDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfstreamdescriptor)

## <a name="remarks"></a><span data-ttu-id="27d8c-112">備註</span><span class="sxs-lookup"><span data-stu-id="27d8c-112">Remarks</span></span>

<span data-ttu-id="27d8c-113">如果 AVI 檔案包含 ' strn ' 區塊，則 AVI 媒體來源會設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="27d8c-113">The AVI media source sets this attribute if the AVI file contains a 'strn' chunk.</span></span>

<span data-ttu-id="27d8c-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="27d8c-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="27d8c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="27d8c-115">Requirements</span></span>



| <span data-ttu-id="27d8c-116">需求</span><span class="sxs-lookup"><span data-stu-id="27d8c-116">Requirement</span></span> | <span data-ttu-id="27d8c-117">值</span><span class="sxs-lookup"><span data-stu-id="27d8c-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="27d8c-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27d8c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="27d8c-119">Windows 7 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27d8c-119">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="27d8c-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27d8c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="27d8c-121">Windows Server 2008 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27d8c-121">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="27d8c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="27d8c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="27d8c-123"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="27d8c-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27d8c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27d8c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27d8c-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="27d8c-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="27d8c-126">資料流程描述元屬性</span><span class="sxs-lookup"><span data-stu-id="27d8c-126">Stream Descriptor Attributes</span></span>](stream-descriptor-attributes.md)
</dt> </dl>

 

 




