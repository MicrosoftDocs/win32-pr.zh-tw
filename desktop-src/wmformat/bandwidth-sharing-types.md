---
title: 頻寬共用類型
description: 頻寬共用類型
ms.assetid: 2da15981-65d4-4d77-a68c-810ded18670c
keywords:
- Windows Media Format SDK，頻寬共用
- Advanced Systems Format (ASF) 、頻寬共用
- ASF (Advanced 系統格式) 、頻寬共用
- 頻寬共用，類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c30f7995f63cd07e5bc2315e0881de95a1400b4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103681420"
---
# <a name="bandwidth-sharing-types"></a><span data-ttu-id="389c4-107">頻寬共用類型</span><span class="sxs-lookup"><span data-stu-id="389c4-107">Bandwidth Sharing Types</span></span>

<span data-ttu-id="389c4-108">您可以使用頻寬共用類型來識別設定檔中頻寬共用物件的本質。</span><span class="sxs-lookup"><span data-stu-id="389c4-108">You can use bandwidth sharing types to identify the nature of a bandwidth sharing object in a profile.</span></span> <span data-ttu-id="389c4-109">頻寬共用類型可做為 [**IWMBandwidthSharing：： GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-gettype) 和 [**IWMBandwidthSharing：： >advanced.field.settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-settype)的參數。</span><span class="sxs-lookup"><span data-stu-id="389c4-109">Bandwidth sharing types are used as parameters for [**IWMBandwidthSharing::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-gettype) and [**IWMBandwidthSharing::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmbandwidthsharing-settype).</span></span>

<span data-ttu-id="389c4-110">下表列出頻寬共用類型的識別碼。</span><span class="sxs-lookup"><span data-stu-id="389c4-110">The following table lists the identifiers for bandwidth sharing types.</span></span>



| <span data-ttu-id="389c4-111">頻寬共用類型常數</span><span class="sxs-lookup"><span data-stu-id="389c4-111">Bandwidth sharing type constant</span></span>      | <span data-ttu-id="389c4-112">GUID</span><span class="sxs-lookup"><span data-stu-id="389c4-112">GUID</span></span>                                 |
|--------------------------------------|--------------------------------------|
| <span data-ttu-id="389c4-113">CLSID \_ WMBandwidthSharing \_ 專有</span><span class="sxs-lookup"><span data-stu-id="389c4-113">CLSID\_WMBandwidthSharing\_Exclusive</span></span> | <span data-ttu-id="389c4-114">af6060aa-5197-11d2-b6af-00c04fd908e9</span><span class="sxs-lookup"><span data-stu-id="389c4-114">af6060aa-5197-11d2-b6af-00c04fd908e9</span></span> |
| <span data-ttu-id="389c4-115">CLSID \_ WMBandwidthSharing \_ 部分</span><span class="sxs-lookup"><span data-stu-id="389c4-115">CLSID\_WMBandwidthSharing\_Partial</span></span>   | <span data-ttu-id="389c4-116">af6060ab-5197-11d2-b6af-00c04fd908e9</span><span class="sxs-lookup"><span data-stu-id="389c4-116">af6060ab-5197-11d2-b6af-00c04fd908e9</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="389c4-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="389c4-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="389c4-118">**GUID 值**</span><span class="sxs-lookup"><span data-stu-id="389c4-118">**GUID Values**</span></span>](guid-values.md)
</dt> </dl>

 

 




