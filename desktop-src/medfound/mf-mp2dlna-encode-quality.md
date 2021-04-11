---
description: 指定數位客廳網路聯盟 (DLNA) 媒體接收器的編碼品質。
ms.assetid: 4cf745ab-66ae-40f2-b5c4-3f72f1b9badb
title: 'MF_MP2DLNA_ENCODE_QUALITY 屬性 (Mfmp2dlna) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c785ff12524d45d096d566014a5c0a5e24eea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026830"
---
# <a name="mf_mp2dlna_encode_quality-attribute"></a><span data-ttu-id="108af-103">MF \_ MP2DLNA \_ 編碼 \_ 品質屬性</span><span class="sxs-lookup"><span data-stu-id="108af-103">MF\_MP2DLNA\_ENCODE\_QUALITY attribute</span></span>

<span data-ttu-id="108af-104">指定數位客廳網路聯盟 (DLNA) 媒體接收器的編碼品質。</span><span class="sxs-lookup"><span data-stu-id="108af-104">Specifies the encoding quality for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="108af-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="108af-105">Data type</span></span>

<span data-ttu-id="108af-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="108af-106">**UINT32**</span></span>

<span data-ttu-id="108af-107">範圍：0到18</span><span class="sxs-lookup"><span data-stu-id="108af-107">Range: 0–18</span></span>

## <a name="getset"></a><span data-ttu-id="108af-108">取得/設定</span><span class="sxs-lookup"><span data-stu-id="108af-108">Get/set</span></span>

<span data-ttu-id="108af-109">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="108af-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="108af-110">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="108af-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="108af-111">備註</span><span class="sxs-lookup"><span data-stu-id="108af-111">Remarks</span></span>

<span data-ttu-id="108af-112">較高的數位表示較佳的編碼品質。</span><span class="sxs-lookup"><span data-stu-id="108af-112">Higher numbers indicate better encoding quality.</span></span> <span data-ttu-id="108af-113">數位越低表示編碼速度較快，但編碼品質較低。</span><span class="sxs-lookup"><span data-stu-id="108af-113">Lower numbers indicate faster encoding, but lower encoding quality.</span></span> <span data-ttu-id="108af-114">預設值為9。</span><span class="sxs-lookup"><span data-stu-id="108af-114">The default value is 9.</span></span>

<span data-ttu-id="108af-115">若要在 DLNA 媒體接收器上設定此屬性，請查詢媒體接收器以取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。</span><span class="sxs-lookup"><span data-stu-id="108af-115">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="108af-116">開始串流之前，請設定屬性。</span><span class="sxs-lookup"><span data-stu-id="108af-116">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="108af-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="108af-117">Requirements</span></span>



| <span data-ttu-id="108af-118">需求</span><span class="sxs-lookup"><span data-stu-id="108af-118">Requirement</span></span> | <span data-ttu-id="108af-119">值</span><span class="sxs-lookup"><span data-stu-id="108af-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="108af-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="108af-120">Minimum supported client</span></span><br/> | <span data-ttu-id="108af-121">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="108af-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="108af-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="108af-122">Minimum supported server</span></span><br/> | <span data-ttu-id="108af-123">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="108af-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="108af-124">標頭</span><span class="sxs-lookup"><span data-stu-id="108af-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="108af-125"><dt>Mfmp2dlna。h</dt></span><span class="sxs-lookup"><span data-stu-id="108af-125"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="108af-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="108af-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="108af-127">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="108af-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




