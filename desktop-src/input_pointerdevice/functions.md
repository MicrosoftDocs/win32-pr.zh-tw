---
description: 本節中的主題提供指標裝置輸入堆疊函數的參考規格。
ms.assetid: 44942954-3EA6-4C33-8CF1-E8BF72A914CB
title: '函數 (指標裝置輸入堆疊) '
ms.topic: article
ms.date: 02/05/2020
ms.openlocfilehash: cfba2a0011747402af81d1f1379076282b65ca74
ms.sourcegitcommit: 4570ac533e129ff88b23f2c2b69e0140ead3a4a4
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/26/2021
ms.locfileid: "106993691"
---
# <a name="pointer-device-input-stack-functions"></a><span data-ttu-id="ef0ca-103">指標裝置輸入堆疊函數</span><span class="sxs-lookup"><span data-stu-id="ef0ca-103">Pointer Device Input Stack functions</span></span>

<span data-ttu-id="ef0ca-104">本節中的主題提供 [指標裝置輸入堆疊](pointer-device-stack-portal.md) 函數的參考規格。</span><span class="sxs-lookup"><span data-stu-id="ef0ca-104">The topics in this section provide the reference specifications for [Pointer Device Input Stack](pointer-device-stack-portal.md) functions.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ef0ca-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="ef0ca-105">In this section</span></span>

| <span data-ttu-id="ef0ca-106">主題</span><span class="sxs-lookup"><span data-stu-id="ef0ca-106">Topic</span></span> | <span data-ttu-id="ef0ca-107">描述</span><span class="sxs-lookup"><span data-stu-id="ef0ca-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="ef0ca-108">**CreateSyntheticPointerDevice**</span><span class="sxs-lookup"><span data-stu-id="ef0ca-108">**CreateSyntheticPointerDevice**</span></span>](/windows/win32/api/winuser/nf-winuser-createsyntheticpointerdevice)<br/> | <span data-ttu-id="ef0ca-109">設定呼叫應用程式的指標插入裝置，並初始化應用程式可以插入的同時指標數目上限。</span><span class="sxs-lookup"><span data-stu-id="ef0ca-109">Configures the pointer injection device for the calling application, and initializes the maximum number of simultaneous pointers that the app can inject.</span></span><br/> |
| [<span data-ttu-id="ef0ca-110">**DestroySyntheticPointerDevice**</span><span class="sxs-lookup"><span data-stu-id="ef0ca-110">**DestroySyntheticPointerDevice**</span></span>](/windows/win32/api/winuser/nf-winuser-destroysyntheticpointerdevice)<br/> | <span data-ttu-id="ef0ca-111">終結指定的指標插入裝置。</span><span class="sxs-lookup"><span data-stu-id="ef0ca-111">Destroys the specified pointer injection device.</span></span><br/> |
| [<span data-ttu-id="ef0ca-112">**GetPointerDevice**</span><span class="sxs-lookup"><span data-stu-id="ef0ca-112">**GetPointerDevice**</span></span>](/windows/win32/api/winuser/nf-winuser-getpointerdevice)<br/> | <span data-ttu-id="ef0ca-113">取得指標裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ef0ca-113">Gets information about the pointer device.</span></span><br/> |
| [<span data-ttu-id="ef0ca-114">**GetPointerDeviceCursors**</span><span class="sxs-lookup"><span data-stu-id="ef0ca-114">**GetPointerDeviceCursors**</span></span>](/windows/win32/api/winuser/nf-winuser-getpointerdevicecursors)<br/> | <span data-ttu-id="ef0ca-115">取得對應至與指標裝置相關聯之資料指標的資料指標識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef0ca-115">Gets the cursor IDs that are mapped to the cursors associated with a pointer device.</span></span><br/> |
| [<span data-ttu-id="ef0ca-116">**GetPointerDeviceProperties**</span><span class="sxs-lookup"><span data-stu-id="ef0ca-116">**GetPointerDeviceProperties**</span></span>](/windows/win32/api/winuser/nf-winuser-getpointerdeviceproperties)<br/> | <span data-ttu-id="ef0ca-117">取得不包含在 [**指標 \_ 裝置 \_ 資訊**](/previous-versions/windows/desktop/api) 結構中的裝置屬性。</span><span class="sxs-lookup"><span data-stu-id="ef0ca-117">Gets device properties that aren't included in the [**POINTER\_DEVICE\_INFO**](/previous-versions/windows/desktop/api) structure.</span></span> <br/> |
| [<span data-ttu-id="ef0ca-118">**GetPointerDeviceRects**</span><span class="sxs-lookup"><span data-stu-id="ef0ca-118">**GetPointerDeviceRects**</span></span>](/windows/win32/api/winuser/nf-winuser-getpointerdevicerects)<br/> | <span data-ttu-id="ef0ca-119">取得指標裝置 (在 himetric) 中的 x 和 y 範圍，以及指標裝置所對應之顯示的 x 和 y 範圍 (目前的解析度) 。</span><span class="sxs-lookup"><span data-stu-id="ef0ca-119">Gets the x and y range for the pointer device (in himetric) and the x and y range (current resolution) for the display that the pointer device is mapped to.</span></span> <br/> |
| [<span data-ttu-id="ef0ca-120">**GetPointerDevices**</span><span class="sxs-lookup"><span data-stu-id="ef0ca-120">**GetPointerDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-getpointerdevices)<br/> | <span data-ttu-id="ef0ca-121">取得連接到系統之指標裝置的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ef0ca-121">Gets information about the pointer devices attached to the system.</span></span><br/> |
| [<span data-ttu-id="ef0ca-122">**GetRawPointerDeviceData**</span><span class="sxs-lookup"><span data-stu-id="ef0ca-122">**GetRawPointerDeviceData**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawpointerdevicedata)<br/> | <span data-ttu-id="ef0ca-123">從指標裝置取得原始輸入資料。</span><span class="sxs-lookup"><span data-stu-id="ef0ca-123">Gets the raw input data from the pointer device.</span></span> <br/> |
| [<span data-ttu-id="ef0ca-124">**InjectSyntheticPointerInput**</span><span class="sxs-lookup"><span data-stu-id="ef0ca-124">**InjectSyntheticPointerInput**</span></span>](/windows/win32/api/winuser/nf-winuser-injectsyntheticpointerinput)<br/> | <span data-ttu-id="ef0ca-125">模擬指標輸入 (畫筆或觸控) 。</span><span class="sxs-lookup"><span data-stu-id="ef0ca-125">Simulates pointer input (pen or touch).</span></span><br/> |
| [<span data-ttu-id="ef0ca-126">**RegisterPointerDeviceNotifications**</span><span class="sxs-lookup"><span data-stu-id="ef0ca-126">**RegisterPointerDeviceNotifications**</span></span>](/windows/win32/api/winuser/nf-winuser-registerpointerdevicenotifications)<br/> | <span data-ttu-id="ef0ca-127">註冊視窗，以處理 [**WM_POINTERDEVICECHANGE**](../inputmsg/wm-pointerdevicechange.md)、 [**WM_POINTERDEVICEINRANGE**](../inputmsg/wm-pointerdeviceinrange.md)和 [**WM_POINTERDEVICEOUTOFRANGE**](../inputmsg/wm-pointerdeviceoutofrange.md) 指標裝置通知。</span><span class="sxs-lookup"><span data-stu-id="ef0ca-127">Registers a window to process the [**WM_POINTERDEVICECHANGE**](../inputmsg/wm-pointerdevicechange.md), [**WM_POINTERDEVICEINRANGE**](../inputmsg/wm-pointerdeviceinrange.md), and [**WM_POINTERDEVICEOUTOFRANGE**](../inputmsg/wm-pointerdeviceoutofrange.md) pointer device notifications.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="ef0ca-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef0ca-128">Related topics</span></span>

[<span data-ttu-id="ef0ca-129">指標裝置輸入堆疊參考</span><span class="sxs-lookup"><span data-stu-id="ef0ca-129">Pointer Device Input Stack Reference</span></span>](unified-input-stack-reference.md)
