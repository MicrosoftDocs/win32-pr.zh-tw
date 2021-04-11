---
description: ICE51 會檢查是否已提供字型資源檔的標題。
ms.assetid: 5a57ba6e-d1fe-44ab-b72d-52b1f212c322
title: ICE51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38082d754564eead6d60a62e3b4cdcf9b1f0f94f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194097"
---
# <a name="ice51"></a><span data-ttu-id="d1ce6-103">ICE51</span><span class="sxs-lookup"><span data-stu-id="d1ce6-103">ICE51</span></span>

<span data-ttu-id="d1ce6-104">ICE51 會檢查是否已提供字型資源檔的標題。</span><span class="sxs-lookup"><span data-stu-id="d1ce6-104">ICE51 checks that a title has been provided for font resource files.</span></span>

<span data-ttu-id="d1ce6-105">您必須提供沒有內嵌名稱之字型資源的標題。</span><span class="sxs-lookup"><span data-stu-id="d1ce6-105">You must provide a title for a font resource that does not have an embedded name.</span></span> <span data-ttu-id="d1ce6-106">只有 simsun18030.ttc、. ttf 和. otf 字型資源檔不需要標題，因為這些檔案包含內嵌名稱。</span><span class="sxs-lookup"><span data-stu-id="d1ce6-106">Only .ttc, .ttf, and .otf font resource files do not require a title, because these files contain an embedded name.</span></span> <span data-ttu-id="d1ce6-107">請勿提供包含內嵌名稱的字型資源標題，因為系統接著會註冊字型兩次。</span><span class="sxs-lookup"><span data-stu-id="d1ce6-107">Do not provide a title for a font resource that contains an embedded name because the system then registers the font twice.</span></span>

<span data-ttu-id="d1ce6-108">**[Windows Installer 4.5 及更早版本](not-supported-in-windows-installer-4-5.md)：** ICE51 不會檢查 otf 字型資源檔。</span><span class="sxs-lookup"><span data-stu-id="d1ce6-108">**[Windows Installer 4.5 and earlier](not-supported-in-windows-installer-4-5.md):** ICE51 does not check .otf font resource files.</span></span>

## <a name="result"></a><span data-ttu-id="d1ce6-109">結果</span><span class="sxs-lookup"><span data-stu-id="d1ce6-109">Result</span></span>

<span data-ttu-id="d1ce6-110">如果有任何 simsun18030.ttc、ttf 和 otf 字型資源檔具有標題，ICE51 會張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="d1ce6-110">ICE51 posts an error if there are any .ttc, .ttf, and .otf font resource files with titles.</span></span> <span data-ttu-id="d1ce6-111">如果有任何其他字型資源檔沒有標題，ICE51 會張貼警告。</span><span class="sxs-lookup"><span data-stu-id="d1ce6-111">ICE51 posts a warning if there are any other font resource files without a title.</span></span>

## <a name="example"></a><span data-ttu-id="d1ce6-112">範例</span><span class="sxs-lookup"><span data-stu-id="d1ce6-112">Example</span></span>

<span data-ttu-id="d1ce6-113">ICE51 會針對所顯示的範例報告下列警告。</span><span class="sxs-lookup"><span data-stu-id="d1ce6-113">ICE51 would report the following warning for the example shown.</span></span>

``` syntax
Font 'Font1' is a TTC\TTF\OTF font, but also has a title.
```

<span data-ttu-id="d1ce6-114">ICE51 會針對所顯示的範例報告下列錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="d1ce6-114">ICE51 would report the following error message for the example shown.</span></span>

``` syntax
Font 'Font2' does not have a title. Only TTC\TTF\OTF fonts do not need titles.
```

<span data-ttu-id="d1ce6-115">[檔資料表](file-table.md) (部分) </span><span class="sxs-lookup"><span data-stu-id="d1ce6-115">[File Table](file-table.md) (partial)</span></span>



| <span data-ttu-id="d1ce6-116">檔案</span><span class="sxs-lookup"><span data-stu-id="d1ce6-116">File</span></span>  | <span data-ttu-id="d1ce6-117">FileName</span><span class="sxs-lookup"><span data-stu-id="d1ce6-117">FileName</span></span>  |
|-------|-----------|
| <span data-ttu-id="d1ce6-118">Font1</span><span class="sxs-lookup"><span data-stu-id="d1ce6-118">Font1</span></span> | <span data-ttu-id="d1ce6-119">font1. ttf</span><span class="sxs-lookup"><span data-stu-id="d1ce6-119">font1.ttf</span></span> |
| <span data-ttu-id="d1ce6-120">Font2</span><span class="sxs-lookup"><span data-stu-id="d1ce6-120">Font2</span></span> | <span data-ttu-id="d1ce6-121">font2.fon</span><span class="sxs-lookup"><span data-stu-id="d1ce6-121">font2.fon</span></span> |



 

[<span data-ttu-id="d1ce6-122">字型資料表</span><span class="sxs-lookup"><span data-stu-id="d1ce6-122">Font Table</span></span>](font-table.md)



| <span data-ttu-id="d1ce6-123">檔案\_</span><span class="sxs-lookup"><span data-stu-id="d1ce6-123">File\_</span></span> | <span data-ttu-id="d1ce6-124">FontTitle</span><span class="sxs-lookup"><span data-stu-id="d1ce6-124">FontTitle</span></span>          |
|--------|--------------------|
| <span data-ttu-id="d1ce6-125">Font1</span><span class="sxs-lookup"><span data-stu-id="d1ce6-125">Font1</span></span>  | <span data-ttu-id="d1ce6-126">非常酷炫的字型</span><span class="sxs-lookup"><span data-stu-id="d1ce6-126">A Really Cool Font</span></span> |
| <span data-ttu-id="d1ce6-127">Font2</span><span class="sxs-lookup"><span data-stu-id="d1ce6-127">Font2</span></span>  |                    |



 

## <a name="related-topics"></a><span data-ttu-id="d1ce6-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="d1ce6-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d1ce6-129">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="d1ce6-129">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



