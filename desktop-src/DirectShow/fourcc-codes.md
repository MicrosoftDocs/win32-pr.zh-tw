---
description: FOURCC 碼
ms.assetid: 7627b580-4119-48e2-88b7-51b714b5d5b2
title: FOURCC 碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb789bc16a1643ee737c1c1a63bdbc5704567931
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104108545"
---
# <a name="fourcc-codes"></a><span data-ttu-id="5c593-103">FOURCC 碼</span><span class="sxs-lookup"><span data-stu-id="5c593-103">FOURCC Codes</span></span>

<span data-ttu-id="5c593-104">許多數位媒體格式都有指派的 FOURCC 碼。</span><span class="sxs-lookup"><span data-stu-id="5c593-104">Many digital media formats have FOURCC codes assigned to them.</span></span> <span data-ttu-id="5c593-105">FOURCC 程式碼是串連四個 ASCII 字元所建立的32位不帶正負號的整數。</span><span class="sxs-lookup"><span data-stu-id="5c593-105">A FOURCC code is a 32-bit unsigned integer that is created by concatenating four ASCII characters.</span></span> <span data-ttu-id="5c593-106">例如，YUY2 video 的 FOURCC 程式碼為 ' YUY2 '。</span><span class="sxs-lookup"><span data-stu-id="5c593-106">For example, the FOURCC code for YUY2 video is 'YUY2'.</span></span> <span data-ttu-id="5c593-107">針對壓縮的影片格式和非 RGB 影片格式 (例如 YUV) ， [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader)結構的 **biCompression** 成員應設定為 FOURCC 程式碼。</span><span class="sxs-lookup"><span data-stu-id="5c593-107">For compressed video formats and non-RGB video formats (such as YUV), the **biCompression** member of the [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure should be set to the FOURCC code.</span></span>

<span data-ttu-id="5c593-108">有各種 C/c + + 宏，可讓您更輕鬆地在原始程式碼中宣告 FOURCC 值。</span><span class="sxs-lookup"><span data-stu-id="5c593-108">There are various C/C++ macros that make it easier to declare FOURCC values in source code.</span></span> <span data-ttu-id="5c593-109">例如， **MAKEFOURCC** 宏是在 Mmsystem 中宣告，而 **FCC** 宏則是在 Aviriff 中宣告。</span><span class="sxs-lookup"><span data-stu-id="5c593-109">For example, the **MAKEFOURCC** macro is declared in Mmsystem.h, and the **FCC** macro is declared in Aviriff.h.</span></span> <span data-ttu-id="5c593-110">使用方式如下：</span><span class="sxs-lookup"><span data-stu-id="5c593-110">Use them as follows:</span></span>


```C++
DWORD fccYUY2 = MAKEFOURCC('Y','U','Y','2');
DWORD fccYUY2 = FCC('YUY2');
```



<span data-ttu-id="5c593-111">您也可以藉由反轉字元順序，直接將 FOURCC 程式碼宣告為字串常值。</span><span class="sxs-lookup"><span data-stu-id="5c593-111">You can also declare a FOURCC code directly as a string literal simply by reversing the order of the characters.</span></span> <span data-ttu-id="5c593-112">例如：</span><span class="sxs-lookup"><span data-stu-id="5c593-112">For example:</span></span>


```C++
DWORD fccYUY2 = '2YUY';  // Declares the FOURCC 'YUY2'.
```



<span data-ttu-id="5c593-113">反轉順序是必要的，因為 Microsoft Windows 作業系統使用位元組由小到大的架構。</span><span class="sxs-lookup"><span data-stu-id="5c593-113">Reversing the order is necessary because the Microsoft Windows operating system uses a little-endian architecture.</span></span> <span data-ttu-id="5c593-114">' Y ' = 0x59，' U ' = 0x55，' 2 ' = 0x32，因此 ' 2YUY ' 為0x32595559。</span><span class="sxs-lookup"><span data-stu-id="5c593-114">'Y' = 0x59, 'U' = 0x55, and '2' = 0x32, so '2YUY' is 0x32595559.</span></span>

### <a name="converting-fourcc-codes-to-subtype-guids"></a><span data-ttu-id="5c593-115">將 FOURCC 碼轉換成子類型 Guid</span><span class="sxs-lookup"><span data-stu-id="5c593-115">Converting FOURCC Codes to Subtype GUIDs</span></span>

<span data-ttu-id="5c593-116">2 \* 32 guid 的範圍是保留來代表 FOURCCs。</span><span class="sxs-lookup"><span data-stu-id="5c593-116">A range of 2\*32 GUIDs is reserved for representing FOURCCs.</span></span> <span data-ttu-id="5c593-117">這些 Guid 全都是 `XXXXXXXX-0000-0010-8000-00AA00389B71` `XXXXXXXX` FOURCC 程式碼的形式。</span><span class="sxs-lookup"><span data-stu-id="5c593-117">These GUIDs are all of the form `XXXXXXXX-0000-0010-8000-00AA00389B71` where `XXXXXXXX` is the FOURCC code.</span></span> <span data-ttu-id="5c593-118">因此，YUY2 的子類型 GUID 為 `32595559-0000-0010-8000-00AA00389B71` 。</span><span class="sxs-lookup"><span data-stu-id="5c593-118">Thus, the subtype GUID for YUY2 is `32595559-0000-0010-8000-00AA00389B71`.</span></span>

<span data-ttu-id="5c593-119">其中有許多 Guid 已定義在標頭檔 Uuid 中。</span><span class="sxs-lookup"><span data-stu-id="5c593-119">Many of these GUIDs are defined already in the header file Uuids.h.</span></span> <span data-ttu-id="5c593-120">例如，YUY2 子類型定義為 MEDIASUBTYPE \_ YUY2。</span><span class="sxs-lookup"><span data-stu-id="5c593-120">For example, the YUY2 subtype is defined as MEDIASUBTYPE\_YUY2.</span></span> <span data-ttu-id="5c593-121">DirectShow 基類庫也提供 helper 類別 [**FOURCCMap**](fourccmap.md)，可用來將 FOURCC 碼轉換成 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="5c593-121">The DirectShow base class library also provides a helper class, [**FOURCCMap**](fourccmap.md), which can be used to convert FOURCC codes into GUID values.</span></span> <span data-ttu-id="5c593-122">**FOURCCMap** 函式會採用 FOURCC 程式碼作為輸入參數。</span><span class="sxs-lookup"><span data-stu-id="5c593-122">The **FOURCCMap** constructor takes a FOURCC code as an input parameter.</span></span> <span data-ttu-id="5c593-123">然後，您可以將 **FOURCCMap** 物件轉換成對應的 GUID：</span><span class="sxs-lookup"><span data-stu-id="5c593-123">You can then cast the **FOURCCMap** object to the corresponding GUID:</span></span>


```C++
FOURCCMap fccMap(FCC('YUY2'));
GUID g1 = (GUID)fccMap;

// Equivalent:
GUID g2 = (GUID)FOURCCMap(FCC('YUY2'));
```



## <a name="related-topics"></a><span data-ttu-id="5c593-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="5c593-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c593-125">**音訊子類型**</span><span class="sxs-lookup"><span data-stu-id="5c593-125">**Audio Subtypes**</span></span>](audio-subtypes.md)
</dt> <dt>

[<span data-ttu-id="5c593-126">影片子類型</span><span class="sxs-lookup"><span data-stu-id="5c593-126">Video Subtypes</span></span>](video-subtypes.md)
</dt> <dt>

[<span data-ttu-id="5c593-127">使用編解碼器</span><span class="sxs-lookup"><span data-stu-id="5c593-127">Working with Codecs</span></span>](working-with-codecs.md)
</dt> </dl>

 

 



