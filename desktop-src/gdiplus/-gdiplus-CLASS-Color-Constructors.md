---
description: 本主題列出 Color 類別的函式。 如需完整的類別清單，請參閱色彩類別。
ms.assetid: ebd68c22-9b00-4a8e-9954-e8b0eda764f8
title: Color： Color 函式
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 9d6fe2cdc790f87a69395cec5bfadaf653fc8acf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991491"
---
# <a name="colorcolor-constructors"></a><span data-ttu-id="a7d96-104">Color： Color 函式</span><span class="sxs-lookup"><span data-stu-id="a7d96-104">Color.Color constructors</span></span>

<span data-ttu-id="a7d96-105">本主題列出 [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) 類別的函式。</span><span class="sxs-lookup"><span data-stu-id="a7d96-105">This topic lists the constructors of the [**Color**](/windows/win32/api/gdipluscolor/nl-gdipluscolor-color) class.</span></span> <span data-ttu-id="a7d96-106">如需完整的類別清單，請參閱 **色彩類別**。</span><span class="sxs-lookup"><span data-stu-id="a7d96-106">For a complete class listing, see **Color Class**.</span></span>

### <a name="overload-list"></a><span data-ttu-id="a7d96-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="a7d96-107">Overload list</span></span>



| <span data-ttu-id="a7d96-108">建構函式</span><span class="sxs-lookup"><span data-stu-id="a7d96-108">Constructor</span></span>                                                               | <span data-ttu-id="a7d96-109">描述</span><span class="sxs-lookup"><span data-stu-id="a7d96-109">Description</span></span>                                                                                                                                                                                                         |
|:--------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d96-110">[**色彩 (ARGB)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inargb))</span><span class="sxs-lookup"><span data-stu-id="a7d96-110">[**Color(ARGB)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inargb))</span></span>                   | <span data-ttu-id="a7d96-111">使用 **ARGB** 值建立 [**Color：： color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inargb))物件。</span><span class="sxs-lookup"><span data-stu-id="a7d96-111">Creates a [**Color::Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inargb)) object by using an **ARGB** value.</span></span><br/>                                                                                                    |
| <span data-ttu-id="a7d96-112">[**色彩 (位元組、位元組、位元組)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte))</span><span class="sxs-lookup"><span data-stu-id="a7d96-112">[**Color(BYTE,BYTE,BYTE)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte))</span></span>        | <span data-ttu-id="a7d96-113">使用指定的紅色、綠色和藍色元件值，建立 [**color：： color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte)) 物件。</span><span class="sxs-lookup"><span data-stu-id="a7d96-113">Creates a [**Color::Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte)) object by using specified values for the red, green, and blue components.</span></span> <span data-ttu-id="a7d96-114">這個函式會將 Alpha 元件設為 255 (不透明) 。</span><span class="sxs-lookup"><span data-stu-id="a7d96-114">This constructor sets the alpha component to 255 (opaque).</span></span><br/> |
| <span data-ttu-id="a7d96-115">[**色彩 (位元組、位元組、位元組、位元組)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte_inbyte))</span><span class="sxs-lookup"><span data-stu-id="a7d96-115">[**Color(BYTE,BYTE,BYTE,BYTE)**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte_inbyte))</span></span> | <span data-ttu-id="a7d96-116">使用指定的 Alpha、紅色、綠色和藍色元件值，建立 [**color：： color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte_inbyte)) 物件。</span><span class="sxs-lookup"><span data-stu-id="a7d96-116">Creates a [**Color::Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color(inbyte_inbyte_inbyte_inbyte)) object by using specified values for the alpha, red, green, and blue components.</span></span><br/>                                                   |
| [<span data-ttu-id="a7d96-117">**色彩 ()**</span><span class="sxs-lookup"><span data-stu-id="a7d96-117">**Color()**</span></span>](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color)                            | <span data-ttu-id="a7d96-118">建立 [**color：： color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color) 物件，並將它初始化為不透明的黑色。</span><span class="sxs-lookup"><span data-stu-id="a7d96-118">Creates a [**Color::Color**](/windows/win32/api/gdipluscolor/nf-gdipluscolor-color-color) object and initializes it to opaque black.</span></span> <span data-ttu-id="a7d96-119">這是預設建構函式。</span><span class="sxs-lookup"><span data-stu-id="a7d96-119">This is the default constructor.</span></span><br/>                                                                |



 

 
