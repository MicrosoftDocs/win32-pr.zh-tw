---
title: HasAttachedImages
description: HasAttachedImages 屬性是檔案層級屬性，用來指定檔案是否為具有附加之 APIC ID3 框架的 MP3 檔案。
ms.assetid: 5c45f61c-3149-4b1b-b5de-f5817cc48c02
keywords:
- HasAttachedImages windows Media 格式
topic_type:
- apiref
api_name:
- HasAttachedImages
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b89c8e8260bac7fa22c50460c57a77d4b3033e6
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106999584"
---
# <a name="hasattachedimages"></a><span data-ttu-id="fd744-104">HasAttachedImages</span><span class="sxs-lookup"><span data-stu-id="fd744-104">HasAttachedImages</span></span>

<span data-ttu-id="fd744-105">**HasAttachedImages** 屬性是檔案層級屬性，用來指定檔案是否為具有附加之 APIC ID3 框架的 MP3 檔案。</span><span class="sxs-lookup"><span data-stu-id="fd744-105">The **HasAttachedImages** attribute is a file-level attribute specifying whether the file is an MP3 file with attached APIC ID3 frames.</span></span>

## <a name="global-constant"></a><span data-ttu-id="fd744-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="fd744-106">Global Constant</span></span>

<span data-ttu-id="fd744-107">g \_ wszWMHasAttachedImages</span><span class="sxs-lookup"><span data-stu-id="fd744-107">g\_wszWMHasAttachedImages</span></span>

## <a name="data-type"></a><span data-ttu-id="fd744-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="fd744-108">Data Type</span></span>

<span data-ttu-id="fd744-109">**WMT \_ 類型 \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="fd744-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="fd744-110">備註</span><span class="sxs-lookup"><span data-stu-id="fd744-110">Remarks</span></span>

<span data-ttu-id="fd744-111">這是程式碼屬性。</span><span class="sxs-lookup"><span data-stu-id="fd744-111">This is a coded attribute.</span></span>

<span data-ttu-id="fd744-112">這個屬性不能在檔案層級複製。</span><span class="sxs-lookup"><span data-stu-id="fd744-112">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="fd744-113">如果此屬性用於個別的資料流程，它會被視為自訂中繼資料，而且不會將其一般意義傳遞給 Windows Media 格式 SDK 的物件。</span><span class="sxs-lookup"><span data-stu-id="fd744-113">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="fd744-114">**HasAttachedImages** 的設計目的是要通知應用程式有映射存在，以便使用 [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) 介面來抓取影像。</span><span class="sxs-lookup"><span data-stu-id="fd744-114">**HasAttachedImages** was designed to inform an application that images were present so that they could be retrieved using the [**IWMImageInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmimageinfo) interface.</span></span> <span data-ttu-id="fd744-115">現在已使用 [**WM/Picture**](wmpicture.md) 屬性支援映射，因此不再需要 **HasAttachedImages** 。</span><span class="sxs-lookup"><span data-stu-id="fd744-115">Now that images are supported using the [**WM/Picture**](wmpicture.md) attribute, **HasAttachedImages** is no longer needed.</span></span>

<span data-ttu-id="fd744-116">若要判斷檔案是否包含影像，請呼叫 [**IWMHeaderInfo3：： GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) 來指定 **WM/圖片** 屬性。</span><span class="sxs-lookup"><span data-stu-id="fd744-116">To determine whether a file contains images, call [**IWMHeaderInfo3::GetAttributeIndices**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-getattributeindices) specifying the **WM/Picture** attribute.</span></span>

## <a name="see-also"></a><span data-ttu-id="fd744-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fd744-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd744-118">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="fd744-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




