---
description: 在六種預先定義的對應模式中，一個是裝置相依 (MM \_ 文字) ，其餘五個 (MM \_ HIENGLISH、mm \_ LOENGLISH、MM \_ HIMETRIC、mm \_ LOMETRIC 和 MM \_ 緹) 與裝置無關。
ms.assetid: 722df020-edf2-4763-b58c-3e29fa7007db
title: 預先定義的對應模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f252f587e98a739306a84450a1d9669ed21873cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972564"
---
# <a name="predefined-mapping-modes"></a><span data-ttu-id="2a300-103">預先定義的對應模式</span><span class="sxs-lookup"><span data-stu-id="2a300-103">Predefined Mapping Modes</span></span>

<span data-ttu-id="2a300-104">在六種預先定義的對應模式中，一個是裝置相依 (MM \_ 文字) ，其餘五個 (MM \_ HIENGLISH、mm \_ LOENGLISH、MM \_ HIMETRIC、mm \_ LOMETRIC 和 MM \_ 緹) 與裝置無關。</span><span class="sxs-lookup"><span data-stu-id="2a300-104">Of the six predefined mapping modes, one is device dependent (MM\_TEXT) and the remaining five (MM\_HIENGLISH, MM\_LOENGLISH, MM\_HIMETRIC, MM\_LOMETRIC, and MM\_TWIPS) are device independent.</span></span>

<span data-ttu-id="2a300-105">預設對應模式為 MM \_ TEXT。</span><span class="sxs-lookup"><span data-stu-id="2a300-105">The default mapping mode is MM\_TEXT.</span></span> <span data-ttu-id="2a300-106">一個邏輯單元等於一個圖元。</span><span class="sxs-lookup"><span data-stu-id="2a300-106">One logical unit equals one pixel.</span></span> <span data-ttu-id="2a300-107">正 x 向右，正 y 為關閉。</span><span class="sxs-lookup"><span data-stu-id="2a300-107">Positive x is to the right, and positive y is down.</span></span> <span data-ttu-id="2a300-108">此模式會直接對應至裝置的座標系統。</span><span class="sxs-lookup"><span data-stu-id="2a300-108">This mode maps directly to the device's coordinate system.</span></span> <span data-ttu-id="2a300-109">邏輯到實體的對應只會包含 x 和 y 中由應用程式控制的視窗和視口來源所定義的位移。</span><span class="sxs-lookup"><span data-stu-id="2a300-109">The logical-to-physical mapping involves only an offset in x and y that is defined by the application-controlled window and viewport origins.</span></span> <span data-ttu-id="2a300-110">此區和視窗範圍全都設定為1，建立一對一的對應。</span><span class="sxs-lookup"><span data-stu-id="2a300-110">The viewport and window extents are all set to 1, creating a one-to-one mapping.</span></span>

<span data-ttu-id="2a300-111">顯示幾何圖形 (圓形、正方形、多邊形等的應用程式) 使用其中一個裝置獨立的對應模式。</span><span class="sxs-lookup"><span data-stu-id="2a300-111">Applications that display geometric shapes (circles, squares, polygons, and so on) make use of one of the device-independent mapping modes.</span></span> <span data-ttu-id="2a300-112">例如，如果您要撰寫應用程式來提供試算表程式的圖表功能，並且想要保證每個圓形圖的直徑都是2英寸，請使用 MM \_ LOENGLISH 對應模式並呼叫適當的函式來繪製和填滿圖表。</span><span class="sxs-lookup"><span data-stu-id="2a300-112">For example, if you are writing an application to provide charting capabilities for a spreadsheet program and want to guarantee that the diameter of each pie chart is 2 inches, use the MM\_LOENGLISH mapping mode and call the appropriate functions to draw and fill the chart.</span></span> <span data-ttu-id="2a300-113">指定 MM \_ LOENGLISH 可保證圖表的直徑在任何顯示或印表機上都是一致的。</span><span class="sxs-lookup"><span data-stu-id="2a300-113">Specifying MM\_LOENGLISH, guarantees that the diameter of the chart is consistent on any display or printer.</span></span> <span data-ttu-id="2a300-114">如果 \_ 使用 mm 文字而不是 mm \_ LOENGLISH，則在 VGA 顯示器上顯示為圓形的圖表會在 EGA 顯示器上顯示為橢圓形，並在 300 DPI (每英寸) 雷射印表機的點上顯示為極小。</span><span class="sxs-lookup"><span data-stu-id="2a300-114">If MM\_TEXT is used instead of MM\_LOENGLISH, a chart that appears circular on a VGA display would appear elliptical on an EGA display and would appear very small on a 300 dpi (dots per inch) laser printer.</span></span>

 

 



