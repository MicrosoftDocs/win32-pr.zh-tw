---
description: 指定 h.264 video remux MFT 是否應將圖片標示為乾淨點，以取得更好的搜尋能力。 這可能會在搜尋不符合規範的最終將檔案中進行搜尋。
ms.assetid: BB521E13-40A4-4643-B071-76B8CBC62074
title: 'MFT_REMUX_MARK_I_PICTURE_AS_CLEAN_POINT 屬性 (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26c9fe8398507f6d7af5d0e4bf45a36a4454f220
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985633"
---
# <a name="mft_remux_mark_i_picture_as_clean_point-attribute"></a><span data-ttu-id="64819-104">MFT \_ REMUX \_ 將 \_ 我 \_ 的圖片標示 \_ 為 \_ 乾淨 \_ 點屬性</span><span class="sxs-lookup"><span data-stu-id="64819-104">MFT\_REMUX\_MARK\_I\_PICTURE\_AS\_CLEAN\_POINT attribute</span></span>

<span data-ttu-id="64819-105">指定 h.264 video remux MFT 是否應將圖片標示為乾淨點，以取得更好的搜尋能力。</span><span class="sxs-lookup"><span data-stu-id="64819-105">Specifies whether the H.264 video remux MFT should mark I pictures as clean point for better seek-ability.</span></span> <span data-ttu-id="64819-106">這可能會在搜尋不符合規範的最終將檔案中進行搜尋。</span><span class="sxs-lookup"><span data-stu-id="64819-106">This has the potential for corruptions on seeks in non-conforming final MP4 files.</span></span>

## <a name="data-type"></a><span data-ttu-id="64819-107">資料類型</span><span class="sxs-lookup"><span data-stu-id="64819-107">Data type</span></span>

<span data-ttu-id="64819-108">**Bool** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="64819-108">**Bool** stored as **UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="64819-109">備註</span><span class="sxs-lookup"><span data-stu-id="64819-109">Remarks</span></span>

<span data-ttu-id="64819-110">清理點圖片應依定義壓縮 IDR 圖片。</span><span class="sxs-lookup"><span data-stu-id="64819-110">Clean point picture should be compressed IDR pictures by definition.</span></span>

<span data-ttu-id="64819-111">這不建議用來錄製或 remuxing 操作檔案，除非這類練習會產生一些中繼虛擬操作檔案來進行影片編輯。</span><span class="sxs-lookup"><span data-stu-id="64819-111">This is not recommended for recording or remuxing MP4 files, unless such an exercise is to produce some intermediate pseudo MP4 files for video editing.</span></span>

## <a name="requirements"></a><span data-ttu-id="64819-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="64819-112">Requirements</span></span>



| <span data-ttu-id="64819-113">需求</span><span class="sxs-lookup"><span data-stu-id="64819-113">Requirement</span></span> | <span data-ttu-id="64819-114">值</span><span class="sxs-lookup"><span data-stu-id="64819-114">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="64819-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64819-115">Minimum supported client</span></span><br/> | <span data-ttu-id="64819-116">Windows 8.1 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64819-116">Windows 8.1 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="64819-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64819-117">Minimum supported server</span></span><br/> | <span data-ttu-id="64819-118">Windows Server 2012 R2 \[ 桌面應用程式 \| UWP 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="64819-118">Windows Server 2012 R2 \[desktop apps \| UWP apps\]</span></span><br/>                             |
| <span data-ttu-id="64819-119">標頭</span><span class="sxs-lookup"><span data-stu-id="64819-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="64819-120"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="64819-120"><dt>Mftransform.h</dt></span></span> </dl>   |
| <span data-ttu-id="64819-121">Idl</span><span class="sxs-lookup"><span data-stu-id="64819-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="64819-122"><dt>Mftransform .idl</dt></span><span class="sxs-lookup"><span data-stu-id="64819-122"><dt>Mftransform.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64819-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64819-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64819-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="64819-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




