---
title: WM/ContainerFormat
description: WM/ContainerFormat 屬性會指定在呼叫物件中載入的檔案類型。
ms.assetid: fea5b2e4-f10d-4482-a7b3-7dabf58df085
keywords:
- WM/ContainerFormat windows Media 格式
topic_type:
- apiref
api_name:
- WM/ContainerFormat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9394fca14c3e07eb1f867c7b8ac473b2b61a9a2
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "103678595"
---
# <a name="wmcontainerformat"></a><span data-ttu-id="88024-104">WM/ContainerFormat</span><span class="sxs-lookup"><span data-stu-id="88024-104">WM/ContainerFormat</span></span>

<span data-ttu-id="88024-105">**WM/ContainerFormat** 屬性會指定在呼叫物件中載入的檔案類型。</span><span class="sxs-lookup"><span data-stu-id="88024-105">The **WM/ContainerFormat** attribute specifies the type of file that is loaded in the calling object.</span></span>

## <a name="global-constant"></a><span data-ttu-id="88024-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="88024-106">Global Constant</span></span>

<span data-ttu-id="88024-107">g \_ wszWMContainerFormat</span><span class="sxs-lookup"><span data-stu-id="88024-107">g\_wszWMContainerFormat</span></span>

## <a name="data-type"></a><span data-ttu-id="88024-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="88024-108">Data Type</span></span>

<span data-ttu-id="88024-109">[**WMT \_ (\_**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) **WMT \_ 類型 \_ 二進位**) 的儲存格式</span><span class="sxs-lookup"><span data-stu-id="88024-109">[**WMT\_STORAGE\_FORMAT**](/previous-versions/windows/desktop/api/wmsdkidl/ne-wmsdkidl-wmt_storage_format) (**WMT\_TYPE\_BINARY**)</span></span>

## <a name="remarks"></a><span data-ttu-id="88024-110">備註</span><span class="sxs-lookup"><span data-stu-id="88024-110">Remarks</span></span>

<span data-ttu-id="88024-111">這個屬性是用來取代不再支援的 **IWMProfile3：： GetStorageFormat** 和 **IWMProfile3：： SetStorageFormat**。</span><span class="sxs-lookup"><span data-stu-id="88024-111">This attribute is used in place of **IWMProfile3::GetStorageFormat** and **IWMProfile3::SetStorageFormat**, which are no longer supported.</span></span>

<span data-ttu-id="88024-112">這是程式碼屬性。</span><span class="sxs-lookup"><span data-stu-id="88024-112">This is a coded attribute.</span></span>

<span data-ttu-id="88024-113">這個屬性不能在檔案層級複製。</span><span class="sxs-lookup"><span data-stu-id="88024-113">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="88024-114">如果此屬性用於個別的資料流程，它會被視為自訂中繼資料，而且不會將其一般意義傳遞給 Windows Media 格式 SDK 的物件。</span><span class="sxs-lookup"><span data-stu-id="88024-114">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

## <a name="see-also"></a><span data-ttu-id="88024-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="88024-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88024-116">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="88024-116">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




