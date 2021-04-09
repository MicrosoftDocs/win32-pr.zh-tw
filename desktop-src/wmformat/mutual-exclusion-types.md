---
title: 相互排除類型
description: 相互排除類型
ms.assetid: bfe6cfe6-3df4-49c4-8015-fe4479b693c1
keywords:
- Windows Media Format SDK，相互排除
- Advanced Systems Format (ASF) ，相互排除
- ASF (Advanced Systems Format) ，相互排除
- 相互排除，類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c425e69c2aa3eac012874837a6970dbc26d1a51
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023002"
---
# <a name="mutual-exclusion-types"></a><span data-ttu-id="d55e1-107">相互排除類型</span><span class="sxs-lookup"><span data-stu-id="d55e1-107">Mutual Exclusion Types</span></span>

<span data-ttu-id="d55e1-108">您可以使用相互排除類型來識別設定檔中互斥物件的本質。</span><span class="sxs-lookup"><span data-stu-id="d55e1-108">You can use mutual exclusion types to identify the nature of a mutual exclusion object in a profile.</span></span> <span data-ttu-id="d55e1-109">相互排除類型可做為 [**IWMMutualExclusion：： GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) 和 [**IWMMutualExclusion：： >advanced.field.settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype)的參數。</span><span class="sxs-lookup"><span data-stu-id="d55e1-109">Mutual exclusion types are used as parameters for [**IWMMutualExclusion::GetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-gettype) and [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype).</span></span>

<span data-ttu-id="d55e1-110">下表列出相互排除類型的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d55e1-110">The following table lists the identifiers for mutual exclusion types.</span></span>



| <span data-ttu-id="d55e1-111">相互排除類型常數</span><span class="sxs-lookup"><span data-stu-id="d55e1-111">Mutual exclusion type constant</span></span> | <span data-ttu-id="d55e1-112">GUID</span><span class="sxs-lookup"><span data-stu-id="d55e1-112">GUID</span></span>                                 |
|--------------------------------|--------------------------------------|
| <span data-ttu-id="d55e1-113">CLSID \_ WMMUTEX \_ 語言</span><span class="sxs-lookup"><span data-stu-id="d55e1-113">CLSID\_WMMUTEX\_Language</span></span>       | <span data-ttu-id="d55e1-114">D6E22A00-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="d55e1-114">D6E22A00-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="d55e1-115">CLSID \_ WMMUTEX \_ 位元速率</span><span class="sxs-lookup"><span data-stu-id="d55e1-115">CLSID\_WMMUTEX\_Bitrate</span></span>        | <span data-ttu-id="d55e1-116">D6E22A01-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="d55e1-116">D6E22A01-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="d55e1-117">CLSID \_ WMMUTEX \_ 簡報</span><span class="sxs-lookup"><span data-stu-id="d55e1-117">CLSID\_WMMUTEX\_Presentation</span></span>   | <span data-ttu-id="d55e1-118">D6E22A02-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="d55e1-118">D6E22A02-35DA-11D1-9034-00A0C90349BE</span></span> |
| <span data-ttu-id="d55e1-119">CLSID \_ WMMUTEX \_ 不明</span><span class="sxs-lookup"><span data-stu-id="d55e1-119">CLSID\_WMMUTEX\_Unknown</span></span>        | <span data-ttu-id="d55e1-120">D6E22A03-35DA-11D1-9034-00A0C90349BE</span><span class="sxs-lookup"><span data-stu-id="d55e1-120">D6E22A03-35DA-11D1-9034-00A0C90349BE</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="d55e1-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="d55e1-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d55e1-122">**GUID 值**</span><span class="sxs-lookup"><span data-stu-id="d55e1-122">**GUID Values**</span></span>](guid-values.md)
</dt> </dl>

 

 




