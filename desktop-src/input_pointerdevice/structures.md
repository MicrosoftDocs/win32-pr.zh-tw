---
description: 本節中的主題提供指標裝置輸入堆疊結構的參考規格。
ms.assetid: 33DCB172-8D95-4205-AE2E-ADD7F3BF988A
title: '結構 (指標裝置輸入) '
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: 988a66a65581cf97406ace5481f115b15a29329a
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2021
ms.locfileid: "106987995"
---
# <a name="pointer-device-input-stack-structures"></a><span data-ttu-id="50135-103">指標裝置輸入堆疊結構</span><span class="sxs-lookup"><span data-stu-id="50135-103">Pointer Device Input Stack structures</span></span>

<span data-ttu-id="50135-104">本節中的主題提供 [指標裝置輸入堆疊](pointer-device-stack-portal.md) 結構的參考規格。</span><span class="sxs-lookup"><span data-stu-id="50135-104">The topics in this section provide the reference specifications for [Pointer Device Input Stack](pointer-device-stack-portal.md) structures.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="50135-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="50135-105">In this section</span></span>

| <span data-ttu-id="50135-106">主題</span><span class="sxs-lookup"><span data-stu-id="50135-106">Topic</span></span> | <span data-ttu-id="50135-107">描述</span><span class="sxs-lookup"><span data-stu-id="50135-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="50135-108">**POINTER_DEVICE_CURSOR_INFO**</span><span class="sxs-lookup"><span data-stu-id="50135-108">**POINTER_DEVICE_CURSOR_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-pointer_device_cursor_info)<br/> | <span data-ttu-id="50135-109">包含指標裝置的資料指標識別碼對應。</span><span class="sxs-lookup"><span data-stu-id="50135-109">Contains cursor ID mappings for pointer devices.</span></span><br/> |
| [<span data-ttu-id="50135-110">**POINTER_DEVICE_INFO**</span><span class="sxs-lookup"><span data-stu-id="50135-110">**POINTER_DEVICE_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-pointer_device_info)<br/> | <span data-ttu-id="50135-111">包含指標裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="50135-111">Contains information about a pointer device.</span></span> <span data-ttu-id="50135-112">這些結構的陣列是從 [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices) 函式傳回。</span><span class="sxs-lookup"><span data-stu-id="50135-112">An array of these structures is returned from the [**GetPointerDevices**](/windows/win32/api/winuser/nf-winuser-getpointerdevices) function.</span></span> <span data-ttu-id="50135-113">從呼叫 [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice) 函數時，會傳回單一結構。</span><span class="sxs-lookup"><span data-stu-id="50135-113">A single structure is returned from a call to the [**GetPointerDevice**](/windows/win32/api/winuser/nf-winuser-getpointerdevice) function.</span></span> <br/> |
| [<span data-ttu-id="50135-114">**POINTER_DEVICE_PROPERTY**</span><span class="sxs-lookup"><span data-stu-id="50135-114">**POINTER_DEVICE_PROPERTY**</span></span>](/windows/win32/api/winuser/ns-winuser-pointer_device_property)<br/> | <span data-ttu-id="50135-115">包含裝置屬性 (人體介面裝置 (HID) 對應至的隱藏專案) 的全域專案。</span><span class="sxs-lookup"><span data-stu-id="50135-115">Contains device properties (Human Interface Device (HID) global items that correspond to HID usages).</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="50135-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="50135-116">Related topics</span></span>

[<span data-ttu-id="50135-117">指標裝置輸入堆疊參考</span><span class="sxs-lookup"><span data-stu-id="50135-117">Pointer Device Input Stack Reference</span></span>](unified-input-stack-reference.md)
