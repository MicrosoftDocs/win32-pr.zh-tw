---
title: IDWriteLocalFontFileLoader 介面
description: IDWriteFontFileLoader 介面的內建執行，可在本機字型檔案上運作，並公開字型檔案參考索引鍵的本機字型檔案資訊。
ms.assetid: acb777c8-24c6-452e-8f58-8fb2ad8c0b6c
keywords:
- IDWriteLocalFontFileLoader 介面直接寫入
- IDWriteLocalFontFileLoader 介面直接寫入，描述
topic_type:
- apiref
api_name:
- IDWriteLocalFontFileLoader
api_location:
- dwrite.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0c65f537dc2a4a96161a11d85ae0a4e1869a331e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999261"
---
# <a name="idwritelocalfontfileloader-interface"></a><span data-ttu-id="6be96-105">IDWriteLocalFontFileLoader 介面</span><span class="sxs-lookup"><span data-stu-id="6be96-105">IDWriteLocalFontFileLoader interface</span></span>

<span data-ttu-id="6be96-106">[**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader)介面的內建執行，可在本機字型檔案上運作，並公開字型檔案參考索引鍵的本機字型檔案資訊。</span><span class="sxs-lookup"><span data-stu-id="6be96-106">A built-in implementation of the [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) interface, that operates on local font files and exposes local font file information from the font file reference key.</span></span> <span data-ttu-id="6be96-107">使用 [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) 建立的字型檔案參考會使用這個字型檔案載入器。</span><span class="sxs-lookup"><span data-stu-id="6be96-107">Font file references created using [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) use this font file loader.</span></span>

## <a name="members"></a><span data-ttu-id="6be96-108">成員</span><span class="sxs-lookup"><span data-stu-id="6be96-108">Members</span></span>

<span data-ttu-id="6be96-109">**IDWriteLocalFontFileLoader** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="6be96-109">The **IDWriteLocalFontFileLoader** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="6be96-110">**IDWriteLocalFontFileLoader** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="6be96-110">**IDWriteLocalFontFileLoader** also has these types of members:</span></span>

-   [<span data-ttu-id="6be96-111">方法</span><span class="sxs-lookup"><span data-stu-id="6be96-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="6be96-112">方法</span><span class="sxs-lookup"><span data-stu-id="6be96-112">Methods</span></span>

<span data-ttu-id="6be96-113">**IDWriteLocalFontFileLoader** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="6be96-113">The **IDWriteLocalFontFileLoader** interface has these methods.</span></span>



| <span data-ttu-id="6be96-114">方法</span><span class="sxs-lookup"><span data-stu-id="6be96-114">Method</span></span>                                                                                  | <span data-ttu-id="6be96-115">描述</span><span class="sxs-lookup"><span data-stu-id="6be96-115">Description</span></span>                                                                               |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6be96-116">**GetFilePathFromKey**</span><span class="sxs-lookup"><span data-stu-id="6be96-116">**GetFilePathFromKey**</span></span>](idwritelocalfontfileloader-getfilepathfromkey.md)             | <span data-ttu-id="6be96-117">從字型檔案參考索引鍵取得絕對字型檔案路徑。</span><span class="sxs-lookup"><span data-stu-id="6be96-117">Obtains the absolute font file path from the font file reference key.</span></span><br/>          |
| [<span data-ttu-id="6be96-118">**GetFilePathLengthFromKey**</span><span class="sxs-lookup"><span data-stu-id="6be96-118">**GetFilePathLengthFromKey**</span></span>](idwritelocalfontfileloader-getfilepathlengthfromkey.md) | <span data-ttu-id="6be96-119">從字型檔案參考索引鍵取得絕對檔案路徑的長度。</span><span class="sxs-lookup"><span data-stu-id="6be96-119">Obtains the length of the absolute file path from the font file reference key.</span></span><br/> |
| [<span data-ttu-id="6be96-120">**GetLastWriteTimeFromKey**</span><span class="sxs-lookup"><span data-stu-id="6be96-120">**GetLastWriteTimeFromKey**</span></span>](idwritelocalfontfileloader-getlastwritetimefromkey.md)   | <span data-ttu-id="6be96-121">從字型檔案參考索引鍵取得檔案的上次寫入時間。</span><span class="sxs-lookup"><span data-stu-id="6be96-121">Obtains the last write time of the file from the font file reference key.</span></span><br/>      |



 

## <a name="requirements"></a><span data-ttu-id="6be96-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="6be96-122">Requirements</span></span>



| <span data-ttu-id="6be96-123">需求</span><span class="sxs-lookup"><span data-stu-id="6be96-123">Requirement</span></span> | <span data-ttu-id="6be96-124">值</span><span class="sxs-lookup"><span data-stu-id="6be96-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6be96-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="6be96-125">Library</span></span><br/> | <dl> <span data-ttu-id="6be96-126"><dt>Dwrite .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6be96-126"><dt>Dwrite.lib</dt></span></span> </dl> |
| <span data-ttu-id="6be96-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6be96-127">DLL</span></span><br/>     | <dl> <span data-ttu-id="6be96-128"><dt>Dwrite.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6be96-128"><dt>Dwrite.dll</dt></span></span> </dl> |



 

