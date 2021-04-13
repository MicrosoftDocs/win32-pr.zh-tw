---
title: 查找
description: 可搜尋的屬性是檔案層級屬性，可指定應用程式是否可以搜尋內容中的點。
ms.assetid: 9653e368-4782-4506-9c44-54c9406b61b5
keywords:
- 能搜尋的 windows 媒體格式
topic_type:
- apiref
api_name:
- Seekable
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4db701be363c194c75bd698062d79a0c0c407cc
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104314499"
---
# <a name="seekable"></a><span data-ttu-id="53c7a-104">查找</span><span class="sxs-lookup"><span data-stu-id="53c7a-104">Seekable</span></span>

<span data-ttu-id="53c7a-105">可搜尋的屬性是檔案層級 **屬性，可** 指定應用程式是否可以搜尋內容中的點。</span><span class="sxs-lookup"><span data-stu-id="53c7a-105">The **Seekable** attribute is a file-level attribute specifying whether an application can seek to points within the content.</span></span>

## <a name="global-constant"></a><span data-ttu-id="53c7a-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="53c7a-106">Global Constant</span></span>

<span data-ttu-id="53c7a-107">g \_ wszWMSeekable</span><span class="sxs-lookup"><span data-stu-id="53c7a-107">g\_wszWMSeekable</span></span>

## <a name="data-type"></a><span data-ttu-id="53c7a-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="53c7a-108">Data Type</span></span>

<span data-ttu-id="53c7a-109">**WMT \_ 類型 \_ BOOL**</span><span class="sxs-lookup"><span data-stu-id="53c7a-109">**WMT\_TYPE\_BOOL**</span></span>

## <a name="remarks"></a><span data-ttu-id="53c7a-110">備註</span><span class="sxs-lookup"><span data-stu-id="53c7a-110">Remarks</span></span>

<span data-ttu-id="53c7a-111">這是程式碼屬性。</span><span class="sxs-lookup"><span data-stu-id="53c7a-111">This is a coded attribute.</span></span>

<span data-ttu-id="53c7a-112">這個屬性不能在檔案層級複製。</span><span class="sxs-lookup"><span data-stu-id="53c7a-112">This attribute cannot be duplicated at the file level.</span></span> <span data-ttu-id="53c7a-113">如果此屬性用於個別的資料流程，它會被視為自訂中繼資料，而且不會將其一般意義傳遞給 Windows Media 格式 SDK 的物件。</span><span class="sxs-lookup"><span data-stu-id="53c7a-113">If this attribute is used for an individual stream, it will be treated as custom metadata and will not convey its normal meaning to the objects of the Windows Media Format SDK.</span></span>

<span data-ttu-id="53c7a-114">檔案的這個屬性值可能會根據公開用來抓取 [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) 或 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) 介面的物件而有所不同。</span><span class="sxs-lookup"><span data-stu-id="53c7a-114">The value of this attribute for a file may vary depending upon the object exposing the [**IWMHeaderInfo**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo) or [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface used to retrieve it.</span></span> <span data-ttu-id="53c7a-115">這是因為「讀取器」物件 (同步和非同步) 執行比「中繼資料編輯器」物件更完整的檢查，以確定您是否可以搜尋檔案中的某個點。</span><span class="sxs-lookup"><span data-stu-id="53c7a-115">This is because the reader objects (both synchronous and asynchronous) perform a more thorough check than the metadata editor object does, to ascertain whether you can seek to a point in a file.</span></span> <span data-ttu-id="53c7a-116">讀取器物件所傳回的可 **搜尋屬性值** 比較精確。</span><span class="sxs-lookup"><span data-stu-id="53c7a-116">The **Seekable** attribute value returned by a reader object is more accurate.</span></span>

## <a name="see-also"></a><span data-ttu-id="53c7a-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="53c7a-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53c7a-118">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="53c7a-118">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




