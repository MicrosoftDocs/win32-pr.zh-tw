---
title: Image. Source 屬性
description: 代表影像的目錄路徑。
ms.assetid: 174a518a-e9a3-4461-a9a3-d61b62d2b718
keywords:
- 影像。來源屬性視窗功能區
topic_type:
- apiref
api_name:
- Image.Source
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ace2a907280a11c54452b54bfb6172539980e38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685782"
---
# <a name="imagesource-property"></a><span data-ttu-id="d0e6d-104">Image. Source 屬性</span><span class="sxs-lookup"><span data-stu-id="d0e6d-104">Image.Source property</span></span>

<span data-ttu-id="d0e6d-105">代表影像的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="d0e6d-105">Represents the directory path of an image.</span></span>

## <a name="usage"></a><span data-ttu-id="d0e6d-106">使用方式</span><span class="sxs-lookup"><span data-stu-id="d0e6d-106">Usage</span></span>

``` syntax
<Image.Source/>
```

## <a name="attributes"></a><span data-ttu-id="d0e6d-107">屬性</span><span class="sxs-lookup"><span data-stu-id="d0e6d-107">Attributes</span></span>

<span data-ttu-id="d0e6d-108">沒有任何屬性。</span><span class="sxs-lookup"><span data-stu-id="d0e6d-108">There are no attributes.</span></span>

## <a name="child-elements"></a><span data-ttu-id="d0e6d-109">子元素</span><span class="sxs-lookup"><span data-stu-id="d0e6d-109">Child elements</span></span>

<span data-ttu-id="d0e6d-110">沒有任何子項目。</span><span class="sxs-lookup"><span data-stu-id="d0e6d-110">There are no child elements.</span></span>

## <a name="parent-elements"></a><span data-ttu-id="d0e6d-111">父元素</span><span class="sxs-lookup"><span data-stu-id="d0e6d-111">Parent elements</span></span>



| <span data-ttu-id="d0e6d-112">元素</span><span class="sxs-lookup"><span data-stu-id="d0e6d-112">Element</span></span>                                                 |
|---------------------------------------------------------|
| [<span data-ttu-id="d0e6d-113">**Image**</span><span class="sxs-lookup"><span data-stu-id="d0e6d-113">**Image**</span></span>](windowsribbon-element-image.md)<br/> |



## <a name="remarks"></a><span data-ttu-id="d0e6d-114">備註</span><span class="sxs-lookup"><span data-stu-id="d0e6d-114">Remarks</span></span>

<span data-ttu-id="d0e6d-115">選擇性。</span><span class="sxs-lookup"><span data-stu-id="d0e6d-115">Optional.</span></span>

<span data-ttu-id="d0e6d-116">每個 [**影像**](windowsribbon-element-image.md)最多可能會發生一次。</span><span class="sxs-lookup"><span data-stu-id="d0e6d-116">May occur at most once for each [**Image**](windowsribbon-element-image.md).</span></span>

<span data-ttu-id="d0e6d-117">這個元素包含型別 *xs： anyURI* 的值，或代表 (URI) 之統一資源識別項的任何字元序列。</span><span class="sxs-lookup"><span data-stu-id="d0e6d-117">This element contains a value of type *xs:anyURI* or any sequence of characters that represents a Uniform Resource Identifier (URI).</span></span> <span data-ttu-id="d0e6d-118">URI 值是功能區標記檔案的絕對或相對 (，) 點陣圖類型之影像資源的目錄路徑 (BMP) 。</span><span class="sxs-lookup"><span data-stu-id="d0e6d-118">The URI value is an absolute or relative (to the Ribbon markup file) directory path of an image resource of type bitmap (BMP).</span></span>

## <a name="examples"></a><span data-ttu-id="d0e6d-119">範例</span><span class="sxs-lookup"><span data-stu-id="d0e6d-119">Examples</span></span>

<span data-ttu-id="d0e6d-120">下列程式碼範例會示範透過一組 [**影像**](windowsribbon-element-image.md) 元素來宣告所需的標記，此集合是設計用來支援四個特定螢幕 DPI 設定的影像資源集合。</span><span class="sxs-lookup"><span data-stu-id="d0e6d-120">The following code example shows the markup required to declare, through a set of [**Image**](windowsribbon-element-image.md) elements, a collection of image resources that are designed to support four specific screen dpi settings.</span></span> <span data-ttu-id="d0e6d-121">**Image. Source** 屬性可用來指定影像資源的路徑。</span><span class="sxs-lookup"><span data-stu-id="d0e6d-121">The **Image.Source** property is used to specify the path to the image resource.</span></span>


```C++
<Command Name="cmdSizeAndColor" Symbol="IDR_CMD_SIZEANDCOLOR">
  <Command.LabelTitle>
    <String Id="250">Size and Color</String>
  </Command.LabelTitle>
  <Command.LargeImages>
    <Image Id="251" MinDPI="96">
      <Image.Source>res/sizeAndColor_96.bmp</Image.Source>
    </Image>
    <Image Id="252" MinDPI="120">
      <Image.Source>res/sizeAndColor_120.bmp</Image.Source>
    </Image>
    <Image Id="253" MinDPI="144">
      <Image.Source>res/sizeAndColor_144.bmp</Image.Source>
    </Image>
    <Image Id="254" MinDPI="192">
      <Image.Source>res/sizeAndColor_192.bmp</Image.Source>
    </Image>
  </Command.LargeImages>
</Command>
```



## <a name="requirements"></a><span data-ttu-id="d0e6d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0e6d-122">Requirements</span></span>



| <span data-ttu-id="d0e6d-123">需求</span><span class="sxs-lookup"><span data-stu-id="d0e6d-123">Requirement</span></span> | <span data-ttu-id="d0e6d-124">值</span><span class="sxs-lookup"><span data-stu-id="d0e6d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="d0e6d-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0e6d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="d0e6d-126">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0e6d-126">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="d0e6d-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0e6d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="d0e6d-128">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0e6d-128">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



 

 





