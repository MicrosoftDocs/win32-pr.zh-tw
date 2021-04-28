---
description: 壓縮 API
ms.assetid: 3ef35cd0-3742-4fc2-9c06-e0485d3538f2
title: 壓縮 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e088b37bbe2ba652379a2d90e6e1e21f87a2e68
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108087986"
---
# <a name="compression-api"></a><span data-ttu-id="9b72e-103">壓縮 API</span><span class="sxs-lookup"><span data-stu-id="9b72e-103">Compression API</span></span>

## <a name="purpose"></a><span data-ttu-id="9b72e-104">目的</span><span class="sxs-lookup"><span data-stu-id="9b72e-104">Purpose</span></span>

<span data-ttu-id="9b72e-105">壓縮 API 會公開 Windows MSZIP、XPRESS、XPRESS \_ HUFF 和 LZMS 壓縮演算法。</span><span class="sxs-lookup"><span data-stu-id="9b72e-105">The Compression API exposes the Windows MSZIP, XPRESS, XPRESS\_HUFF, and LZMS compression algorithms.</span></span> <span data-ttu-id="9b72e-106">這可讓 Windows 應用程式的開發人員管理版本、服務，以及擴充公開的壓縮演算法。</span><span class="sxs-lookup"><span data-stu-id="9b72e-106">This enables developers of Windows applications to manage versions, service, and extend the exposed compression algorithms.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="9b72e-107">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="9b72e-107">Developer audience</span></span>

<span data-ttu-id="9b72e-108">壓縮 API 是專為 Windows 應用程式的專業 C/c + + 開發人員所使用。</span><span class="sxs-lookup"><span data-stu-id="9b72e-108">The Compression API is designed for use by professional C/C++ developers of Windows applications.</span></span> <span data-ttu-id="9b72e-109">壓縮 API 會透過公用介面和使用者模式 API 來公開 Windows 所使用的非失真壓縮演算法。</span><span class="sxs-lookup"><span data-stu-id="9b72e-109">The Compression API exposes the lossless compression algorithms used by Windows though a public interface and user-mode API.</span></span> <span data-ttu-id="9b72e-110">壓縮 API 是 Windows 開發人員用來控制壓縮演算法的建議方法。</span><span class="sxs-lookup"><span data-stu-id="9b72e-110">The Compression API is the recommended method for Windows developers to control the compression algorithms.</span></span> <span data-ttu-id="9b72e-111">這項功能是64位 Windows 上的64位，以及32位 Windows 上的32位。</span><span class="sxs-lookup"><span data-stu-id="9b72e-111">This feature is 64-bit on 64-bit Windows and 32-bit on 32-bit Windows.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="9b72e-112">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="9b72e-112">Run-time requirements</span></span>

<span data-ttu-id="9b72e-113">從 Windows 8 或 Windows Server 2012 開始，可以使用壓縮 API。</span><span class="sxs-lookup"><span data-stu-id="9b72e-113">The Compression API is available beginning with the Windows 8 or Windows Server 2012.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9b72e-114">本節內容</span><span class="sxs-lookup"><span data-stu-id="9b72e-114">In this section</span></span>

-   [<span data-ttu-id="9b72e-115">使用壓縮 API</span><span class="sxs-lookup"><span data-stu-id="9b72e-115">Using the Compression API</span></span>](using-the-compression-api.md)
-   [<span data-ttu-id="9b72e-116">壓縮 API 函數</span><span class="sxs-lookup"><span data-stu-id="9b72e-116">Compression API Functions</span></span>](compression-api-functions.md)
-   [<span data-ttu-id="9b72e-117">壓縮 API 結構</span><span class="sxs-lookup"><span data-stu-id="9b72e-117">Compression API Structures</span></span>](compression-api-structures.md)
-   [<span data-ttu-id="9b72e-118">壓縮 API 列舉</span><span class="sxs-lookup"><span data-stu-id="9b72e-118">Compression API Enumerations</span></span>](compression-api-enumerations.md)

 

 



