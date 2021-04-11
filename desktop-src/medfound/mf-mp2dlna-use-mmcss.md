---
description: 指定數位客廳網路聯盟 (DLNA) 媒體接收器是否使用多媒體類別排程器服務 (MMCSS) 。
ms.assetid: 4c27e2ec-624a-4b1f-bea9-3aaad1534c9b
title: 'MF_MP2DLNA_USE_MMCSS 屬性 (Mfmp2dlna) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccfdaf36ce51f1158e110dcb3682a5b072c060dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026828"
---
# <a name="mf_mp2dlna_use_mmcss-attribute"></a><span data-ttu-id="9b351-103">MF \_ MP2DLNA \_ 使用 \_ MMCSS 屬性</span><span class="sxs-lookup"><span data-stu-id="9b351-103">MF\_MP2DLNA\_USE\_MMCSS attribute</span></span>

<span data-ttu-id="9b351-104">指定數位客廳網路聯盟 (DLNA) 媒體接收器是否使用多媒體類別排程器服務 (MMCSS) 。</span><span class="sxs-lookup"><span data-stu-id="9b351-104">Specifies whether the Digital Living Network Alliance (DLNA) media sink uses the Multimedia Class Scheduler Service (MMCSS).</span></span>

## <a name="data-type"></a><span data-ttu-id="9b351-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="9b351-105">Data type</span></span>

<span data-ttu-id="9b351-106">**BOOL** 儲存為 **UINT32**</span><span class="sxs-lookup"><span data-stu-id="9b351-106">**BOOL** stored as **UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="9b351-107">取得/設定</span><span class="sxs-lookup"><span data-stu-id="9b351-107">Get/set</span></span>

<span data-ttu-id="9b351-108">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="9b351-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="9b351-109">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="9b351-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="9b351-110">備註</span><span class="sxs-lookup"><span data-stu-id="9b351-110">Remarks</span></span>

<span data-ttu-id="9b351-111">若要在 DLNA 媒體接收器上設定此屬性，請查詢媒體接收器以取得 [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) 介面。</span><span class="sxs-lookup"><span data-stu-id="9b351-111">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="9b351-112">開始串流之前，請設定屬性。</span><span class="sxs-lookup"><span data-stu-id="9b351-112">Set the attribute before streaming begins.</span></span>

<span data-ttu-id="9b351-113">如果此屬性為 **TRUE**，則 DLNA 媒體接收器會向 MMCSS 註冊其本身。</span><span class="sxs-lookup"><span data-stu-id="9b351-113">If this attribute is **TRUE**, the DLNA media sink registers itself with MMCSS.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b351-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="9b351-114">Requirements</span></span>



| <span data-ttu-id="9b351-115">需求</span><span class="sxs-lookup"><span data-stu-id="9b351-115">Requirement</span></span> | <span data-ttu-id="9b351-116">值</span><span class="sxs-lookup"><span data-stu-id="9b351-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b351-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9b351-117">Minimum supported client</span></span><br/> | <span data-ttu-id="9b351-118">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b351-118">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="9b351-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9b351-119">Minimum supported server</span></span><br/> | <span data-ttu-id="9b351-120">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9b351-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9b351-121">標頭</span><span class="sxs-lookup"><span data-stu-id="9b351-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b351-122"><dt>Mfmp2dlna。h</dt></span><span class="sxs-lookup"><span data-stu-id="9b351-122"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b351-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9b351-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b351-124">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="9b351-124">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




