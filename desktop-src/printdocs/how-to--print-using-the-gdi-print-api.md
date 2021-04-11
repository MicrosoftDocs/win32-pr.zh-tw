---
description: 本主題將介紹如何使用 GDI&160，從原生 Windows 程式進行列印 \# ;列印&\# 160;Api。
ms.assetid: C212DD92-2B90-45BC-8746-29C193FBDF69
title: 如何：使用 GDI 列印 API 進行列印
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41d6351e228297b5378b54879548b823f81894b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852419"
---
# <a name="how-to-print-using-the-gdi-print-api"></a><span data-ttu-id="ab649-103">如何：使用 GDI 列印 API 進行列印</span><span class="sxs-lookup"><span data-stu-id="ab649-103">How To: Print Using the GDI Print API</span></span>

<span data-ttu-id="ab649-104">本主題將介紹如何使用 [GDI 列印 API](gdi-printing.md)，從原生 Windows 程式進行列印。</span><span class="sxs-lookup"><span data-stu-id="ab649-104">This topic introduces how to print from a native Windows program using the [GDI Print API](gdi-printing.md).</span></span>

## <a name="overview"></a><span data-ttu-id="ab649-105">概觀</span><span class="sxs-lookup"><span data-stu-id="ab649-105">Overview</span></span>

<span data-ttu-id="ab649-106">列印通常是原生 Windows 程式不可或缺的一部分，因此它不是您在撰寫程式之後可以輕鬆新增的功能。</span><span class="sxs-lookup"><span data-stu-id="ab649-106">Printing is usually an integral part of a native Windows program, so it is not a feature that you can add easily after you have written the program.</span></span> <span data-ttu-id="ab649-107">針對 Windows 7 設計程式時，您應該考慮使用 [XPS 列印 API](xps-printing.md) 來提供列印功能，因為它會為未來提供最高的相容性。</span><span class="sxs-lookup"><span data-stu-id="ab649-107">When designing a program for Windows 7, you should consider using the [XPS Print API](xps-printing.md) to provide the printing functionality because it provides the most compatibility for the future.</span></span> <span data-ttu-id="ab649-108">必須在 Windows Vista 和舊版 Windows 上執行的程式，很可能會使用 [GDI 列印 API](gdi-printing.md) 來提供列印功能。</span><span class="sxs-lookup"><span data-stu-id="ab649-108">Programs that must run on Windows Vista and earlier versions of Windows will most likely use the [GDI Print API](gdi-printing.md) to provide printing functionality.</span></span> <span data-ttu-id="ab649-109">Windows 7 也支援 GDI 列印 API，但它比 XPS 列印 API 更受限制。</span><span class="sxs-lookup"><span data-stu-id="ab649-109">The GDI Print API is also supported in Windows 7, but it is more limited than the XPS Print API.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ab649-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="ab649-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ab649-111">使用列印</span><span class="sxs-lookup"><span data-stu-id="ab649-111">Using Printing</span></span>](using-printing.md)
</dt> <dt>

[<span data-ttu-id="ab649-112">如何從 Windows 應用程式列印</span><span class="sxs-lookup"><span data-stu-id="ab649-112">How to print from a Windows application</span></span>](how-to--print-from-a-windows-application.md)
</dt> </dl>

 

 



