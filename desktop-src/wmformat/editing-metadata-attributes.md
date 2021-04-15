---
title: 編輯中繼資料屬性
description: 編輯中繼資料屬性
ms.assetid: 96c979e2-c616-45e3-9c60-a24f03e29dc4
keywords:
- Windows Media Format SDK，編輯中繼資料屬性
- Advanced Systems Format (ASF) 、編輯中繼資料屬性
- ASF (Advanced Systems Format) 、編輯中繼資料屬性
- 中繼資料，編輯屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a52990e5366da178e9ed5021af93a9f6403b80c4
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104374543"
---
# <a name="editing-metadata-attributes"></a><span data-ttu-id="0ca6e-107">編輯中繼資料屬性</span><span class="sxs-lookup"><span data-stu-id="0ca6e-107">Editing Metadata Attributes</span></span>

<span data-ttu-id="0ca6e-108">編輯中繼資料屬性與設定新屬性非常類似。</span><span class="sxs-lookup"><span data-stu-id="0ca6e-108">Editing metadata attributes is very similar to setting new ones.</span></span> <span data-ttu-id="0ca6e-109">請勿使用 [**IWMHeaderInfo3：： AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute)，而是使用 [**IWMHeaderInfo3：： ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute)。</span><span class="sxs-lookup"><span data-stu-id="0ca6e-109">Instead of using [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute), use [**IWMHeaderInfo3::ModifyAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-modifyattribute).</span></span> <span data-ttu-id="0ca6e-110">**ModifyAttribute** 與 **AddAttribute** 相同，不同之處在于您未指定屬性名稱，而且索引編號是輸入參數，而不是輸出。</span><span class="sxs-lookup"><span data-stu-id="0ca6e-110">**ModifyAttribute** is identical to **AddAttribute** except that you do not specify an attribute name, and the index number is an input parameter instead of an output.</span></span>

<span data-ttu-id="0ca6e-111">您可以使用 stream number 0xFFFF 來指定要使用其全域索引來修改的屬性。</span><span class="sxs-lookup"><span data-stu-id="0ca6e-111">You can use stream number 0xFFFF to specify an attribute to modify using its global index.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0ca6e-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="0ca6e-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0ca6e-113">**使用中繼資料**</span><span class="sxs-lookup"><span data-stu-id="0ca6e-113">**Working with Metadata**</span></span>](working-with-metadata.md)
</dt> </dl>

 

 




