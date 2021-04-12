---
UID: NN:dwrite_3.IDWriteBitmapRenderTarget2
title: 'IDWriteBitmapRenderTarget2 (dwrite_3 .h) '
description: 封裝可用於轉譯圖像的32位裝置獨立點陣圖和裝置內容。
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2
- dwrite_3/IDWriteBitmapRenderTarget2
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2
ms.openlocfilehash: edc1df695424eac0bbf0d5a4951b5e9fe4ec0809
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "104195687"
---
# <a name="idwritebitmaprendertarget2-interface-dwrite_3h"></a><span data-ttu-id="636c8-103">IDWriteBitmapRenderTarget2 介面 (dwrite_3 .h) </span><span class="sxs-lookup"><span data-stu-id="636c8-103">IDWriteBitmapRenderTarget2 interface (dwrite_3.h)</span></span>

<span data-ttu-id="636c8-104">封裝可用於轉譯圖像的32位裝置獨立點陣圖和裝置內容。</span><span class="sxs-lookup"><span data-stu-id="636c8-104">Encapsulates a 32-bit device independent bitmap and device context, which can be used for rendering glyphs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="636c8-105">此 API 可作為 [DirectWrite](../direct-write-portal.md)DWriteCore 執行的一部分。</span><span class="sxs-lookup"><span data-stu-id="636c8-105">This API is available as part of the DWriteCore implementation of [DirectWrite](../direct-write-portal.md).</span></span> <span data-ttu-id="636c8-106">DWriteCore 是 DirectWrite 的其中一種形式，可在低至 Windows 8 的 Windows 版本上執行，並讓您自由地跨平台使用。</span><span class="sxs-lookup"><span data-stu-id="636c8-106">DWriteCore is a form of DirectWrite that runs on versions of Windows down to Windows 8, and opens the door for you to use it cross-platform.</span></span> <span data-ttu-id="636c8-107">如需詳細資訊和程式碼範例，請參閱 [DWriteCore 總覽](/windows/win32/DirectWrite/dwrite/dwritecore-overview)。</span><span class="sxs-lookup"><span data-stu-id="636c8-107">For more info, and code examples, see [DWriteCore overview](/windows/win32/DirectWrite/dwrite/dwritecore-overview).</span></span>

## <a name="inheritance"></a><span data-ttu-id="636c8-108">繼承</span><span class="sxs-lookup"><span data-stu-id="636c8-108">Inheritance</span></span>

<span data-ttu-id="636c8-109">**IDWriteBitmapRenderTarget2** 介面繼承自 [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1)。</span><span class="sxs-lookup"><span data-stu-id="636c8-109">The **IDWriteBitmapRenderTarget2** interface inherits from [IDWriteBitmapRenderTarget1](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1).</span></span>

## <a name="methods"></a><span data-ttu-id="636c8-110">方法</span><span class="sxs-lookup"><span data-stu-id="636c8-110">Methods</span></span>

<span data-ttu-id="636c8-111">**IDWriteBitmapRenderTarget2** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="636c8-111">The **IDWriteBitmapRenderTarget2** interface has these methods.</span></span>

| <span data-ttu-id="636c8-112">方法</span><span class="sxs-lookup"><span data-stu-id="636c8-112">Method</span></span> | <span data-ttu-id="636c8-113">描述</span><span class="sxs-lookup"><span data-stu-id="636c8-113">Description</span></span> |
| ---- |:---- |
| [<span data-ttu-id="636c8-114">IDWriteBitmapRenderTarget2::GetBitmapData</span><span class="sxs-lookup"><span data-stu-id="636c8-114">IDWriteBitmapRenderTarget2::GetBitmapData</span></span>](./nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md) | <span data-ttu-id="636c8-115">從點陣圖呈現目標抓取圖元資料。</span><span class="sxs-lookup"><span data-stu-id="636c8-115">Retrieves the pixel data from a bitmap render target.</span></span> |

## <a name="requirements"></a><span data-ttu-id="636c8-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="636c8-116">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="636c8-117">**最低支援的用戶端**</span><span class="sxs-lookup"><span data-stu-id="636c8-117">**Minimum supported client**</span></span> | <span data-ttu-id="636c8-118">Windows 10，Project 留尼旺島0.1 發行前版本 [Win32 應用程式]</span><span class="sxs-lookup"><span data-stu-id="636c8-118">Windows 10, Project Reunion 0.1 Prerelease [Win32 apps]</span></span> |
| <span data-ttu-id="636c8-119">**標頭**</span><span class="sxs-lookup"><span data-stu-id="636c8-119">**Header**</span></span> | <span data-ttu-id="636c8-120">dwrite_3 .h (包含 dwrite_core .h) </span><span class="sxs-lookup"><span data-stu-id="636c8-120">dwrite_3.h (include dwrite_core.h)</span></span> |