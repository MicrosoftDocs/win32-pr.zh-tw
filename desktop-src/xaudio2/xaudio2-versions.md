---
description: XAudio2 是一種跨平臺 API，隨附于 Xbox 360 及 Windows 版本，包括 Windows XP、Windows Vista、Windows 7 和 Windows 8。
ms.assetid: 875b44c4-30d6-8a6e-0cfc-9beb8c46f1b4
title: XAudio2 版本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5c9facfe357c323bd8f7b607460a8f59bd062fe
ms.sourcegitcommit: 010f524cd6098a5941de77907d4d6ae7871f8af1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/03/2021
ms.locfileid: "106982127"
---
# <a name="xaudio2-versions"></a><span data-ttu-id="a12c8-103">XAudio2 版本</span><span class="sxs-lookup"><span data-stu-id="a12c8-103">XAudio2 Versions</span></span>

<span data-ttu-id="a12c8-104">XAudio2 是一種跨平臺 API，隨附于 Xbox 360 及 Windows 版本，包括 Windows XP、Windows Vista、Windows 7 和 Windows 8。</span><span class="sxs-lookup"><span data-stu-id="a12c8-104">XAudio2 is a cross-platform API that has shipped for use on Xbox 360 as well as versions of Windows, including Windows XP, Windows Vista, Windows 7, and Windows 8.</span></span> <span data-ttu-id="a12c8-105">在 Xbox 360 上，XAudio2 會以靜態程式庫的形式提供，並編譯成主要的遊戲可執行檔。</span><span class="sxs-lookup"><span data-stu-id="a12c8-105">On Xbox 360, XAudio2 ships as a static library that is compiled into the main game executable.</span></span> <span data-ttu-id="a12c8-106">在 Windows 中，XAudio2 是以動態連結程式庫的形式提供， (DLL) 安裝到作業系統的系統資料夾中。</span><span class="sxs-lookup"><span data-stu-id="a12c8-106">On Windows, XAudio2 is provided as a Dynamic Link Library (DLL) installed into the system folders of the Operating System.</span></span>

## <a name="xaudio-29-windows-10-and-redistributable-for-windows-7-and-windows-8x"></a><span data-ttu-id="a12c8-107">適用于 Windows 7 和 Windows 8 x 的 XAudio 2.9 (Windows 10 和可轉散發套件) </span><span class="sxs-lookup"><span data-stu-id="a12c8-107">XAudio 2.9 (Windows 10 and redistributable for Windows 7 and Windows 8.x)</span></span>

<span data-ttu-id="a12c8-108">XAudio2 2.9 版隨附于 Windows 10、XAUDIO2 \_9.DLL，以及 XAudio 2.8 以支援較舊的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a12c8-108">XAudio2 version 2.9 ships as part of Windows 10, XAUDIO2\_9.DLL, alongside XAudio 2.8 to support older applications.</span></span> <span data-ttu-id="a12c8-109">[XAudio 2.9](xaudio2-redistributable.md)的可轉散發版本也適用于 WINDOWS 7 SP1、Windows 8 和 Windows 8.1。</span><span class="sxs-lookup"><span data-stu-id="a12c8-109">A [redistributable version of XAudio 2.9](xaudio2-redistributable.md) is also available for Windows 7 SP1, Windows 8 and Windows 8.1.</span></span>

<span data-ttu-id="a12c8-110">XAudio 2.9 已更新下列變更：</span><span class="sxs-lookup"><span data-stu-id="a12c8-110">XAudio2.9 has been updated with the following changes:</span></span>

-   <span data-ttu-id="a12c8-111">新建立旗標： XAUDIO2 \_ DEBUG \_ ENGINE、XAUDIO2 \_ STOP \_ ENGINE \_ WHEN \_ IDLE、XAUDIO2 \_ 1024 \_ 量子</span><span class="sxs-lookup"><span data-stu-id="a12c8-111">New creation flags: XAUDIO2\_DEBUG\_ENGINE, XAUDIO2\_STOP\_ENGINE\_WHEN\_IDLE, XAUDIO2\_1024\_QUANTUM</span></span>
-   <span data-ttu-id="a12c8-112">此版本的 XAudio2 提供 xWMA 支援。</span><span class="sxs-lookup"><span data-stu-id="a12c8-112">xWMA support is available in this version of XAudio2.</span></span>
-   <span data-ttu-id="a12c8-113">Windows 10 版本的 XAudio 2.9 支援 [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) 函數。</span><span class="sxs-lookup"><span data-stu-id="a12c8-113">The [**CreateHrtfApo**](/windows/desktop/api/HrtfApoApi/nf-hrtfapoapi-createhrtfapo) function is supported in the Windows 10 version of XAudio 2.9.</span></span>
-   <span data-ttu-id="a12c8-114">[**XAUDIO2FX \_立即的 \_ 參數**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) 現在包含7.1 系統的值 *SideDelay* 。</span><span class="sxs-lookup"><span data-stu-id="a12c8-114">[**XAUDIO2FX\_REVERB\_PARAMETERS**](/windows/desktop/api/xaudio2fx/ns-xaudio2fx-xaudio2fx_reverb_parameters) now includes the value *SideDelay* for 7.1 systems.</span></span>
-   <span data-ttu-id="a12c8-115">[**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative)函式現在包含啟用7.1 回音的布林 *sevenDotOneReverb* 參數。</span><span class="sxs-lookup"><span data-stu-id="a12c8-115">The [**ReverbConvertI3DL2ToNative**](/windows/desktop/api/xaudio2fx/nf-xaudio2fx-reverbconverti3dl2tonative) function now includes the boolean *sevenDotOneReverb* parameter enabling 7.1 reverb.</span></span>

## <a name="xaudio-28-windows-8x"></a><span data-ttu-id="a12c8-116">XAudio 2.8 (Windows 8 x) </span><span class="sxs-lookup"><span data-stu-id="a12c8-116">XAudio 2.8 (Windows 8.x)</span></span>

<span data-ttu-id="a12c8-117">XAudio2 2.8 版現在隨附于 Windows 8，XAUDIO28.DLL 的系統元件 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a12c8-117">XAudio2 version 2.8 ships today as a system component in Windows 8, XAUDIO2\_8.DLL.</span></span> <span data-ttu-id="a12c8-118">這是可用的「收件匣」，不需要與應用程式一起轉散發。</span><span class="sxs-lookup"><span data-stu-id="a12c8-118">It is available “inbox” and does not require redistribution with an app.</span></span> <span data-ttu-id="a12c8-119">建議您使用 Windows 軟體開發套件 (SDK) 進行 Windows 8，以針對 XAudio2 進行開發;Windows 8 的 Windows SDK 包含必要的標頭和匯入程式庫，以針對 XAUDIO28.DLL 進行靜態連結 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a12c8-119">We recommend to use the Windows Software Development Kit (SDK) for Windows 8 to develop against XAudio2; the Windows SDK for Windows 8 contains the necessary header and import library for statically linking against XAUDIO2\_8.DLL.</span></span>

<span data-ttu-id="a12c8-120">XAudio2 2.8 已更新下列變更：</span><span class="sxs-lookup"><span data-stu-id="a12c8-120">XAudio2 2.8 has been updated with the following changes:</span></span>

-   <span data-ttu-id="a12c8-121">此版本支援 Windows Store 應用程式開發;XAudio2 API 可以在 c + +/DirectX Windows Store 應用程式中使用。</span><span class="sxs-lookup"><span data-stu-id="a12c8-121">This version supports Windows Store app development; the XAudio2 API can be used in C++/DirectX Windows Store apps.</span></span>
-   <span data-ttu-id="a12c8-122">[**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) 是一般的 WIN32 API 呼叫，不再建立 XAudio2 CLSID。</span><span class="sxs-lookup"><span data-stu-id="a12c8-122">[**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) is a flat Win32 API call and no longer creates an XAudio2 CLSID.</span></span> <span data-ttu-id="a12c8-123">已移除由 CoCreateInstance 將 XAudio2 具現化的支援。</span><span class="sxs-lookup"><span data-stu-id="a12c8-123">Support for instantiating XAudio2 by CoCreateInstance has been removed.</span></span>
-   <span data-ttu-id="a12c8-124">初始化函式現在已由建立程式隱含呼叫，且已從 [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) 介面中移除。</span><span class="sxs-lookup"><span data-stu-id="a12c8-124">The Initialize function is now implicitly called by the creation process and has been removed from the [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) interface.</span></span>
-   <span data-ttu-id="a12c8-125">裝置列舉功能已從 XAudio2 中移除;GetDeviceDetails 和 GetDeviceCount 函數已從 [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) 介面中移除。</span><span class="sxs-lookup"><span data-stu-id="a12c8-125">Device enumeration functionality has been removed from XAudio2; the GetDeviceDetails and GetDeviceCount functions have been removed from the [**IXAudio2**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2) interface.</span></span> <span data-ttu-id="a12c8-126">想要轉譯至系統上其他音訊裝置的應用程式，必須將裝置識別碼字串傳遞至 [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) ，而不是裝置索引。</span><span class="sxs-lookup"><span data-stu-id="a12c8-126">Apps that want to render to other audio devices on the system must pass a device identifier string to [**CreateMasteringVoice**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-createmasteringvoice) instead of a device index.</span></span> <span data-ttu-id="a12c8-127">仍可建立預設音訊轉譯裝置，但不含列舉。</span><span class="sxs-lookup"><span data-stu-id="a12c8-127">The default audio render device can still be created without enumeration.</span></span>
-   <span data-ttu-id="a12c8-128">[**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) 具有新增的函式 [**IXAudio2MasteringVoice：： GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) ，會傳回目的地輸出裝置的通道遮罩。</span><span class="sxs-lookup"><span data-stu-id="a12c8-128">[**IXAudio2MasteringVoice**](/windows/desktop/api/xaudio2/nn-xaudio2-ixaudio2masteringvoice) has an added function [**IXAudio2MasteringVoice::GetChannelMask**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2masteringvoice-getchannelmask) for that returns the channel mask for the destination output device.</span></span>
-   <span data-ttu-id="a12c8-129">[X3DAudio](x3daudio.md)和[XAPOFX](xapofx-overview.md)程式庫會合並到 XAudio2。</span><span class="sxs-lookup"><span data-stu-id="a12c8-129">The [X3DAudio](x3daudio.md) and [XAPOFX](xapofx-overview.md) libraries are merged into XAudio2.</span></span> <span data-ttu-id="a12c8-130">應用程式程式碼仍會使用不同的標頭 X3DAUDIO。H 和 XPOFX。H，但現在會連結到單一的匯入程式庫，XAUDIO2 \_ 8.。</span><span class="sxs-lookup"><span data-stu-id="a12c8-130">App code still uses separate headers, X3DAUDIO.H and XPOFX.H, but now links to a single import library, XAUDIO2\_8.LIB.</span></span>
-   <span data-ttu-id="a12c8-131">此版本的 XAudio2 無法使用 xWMA 支援;呼叫 CreateSourceVoice 時，不會將 xWMA 支援為音訊緩衝區格式。</span><span class="sxs-lookup"><span data-stu-id="a12c8-131">xWMA support is not available in this version of XAudio2; xWMA will not be supported as an audio buffer format when calling CreateSourceVoice.</span></span> <span data-ttu-id="a12c8-132">我們現在建議媒體基礎的來源讀取器物件，將各種不同的媒體格式解碼成記憶體中的 PCM 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="a12c8-132">We now recommend the Media Foundation Source Reader object for decoding a wide variety of media formats into in-memory PCM buffers.</span></span>
-   <span data-ttu-id="a12c8-133">[**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) 現在採用四個參數，而不是兩個。</span><span class="sxs-lookup"><span data-stu-id="a12c8-133">[**CreateFX**](/windows/desktop/api/XAPOFX/nf-xapofx-createfx) now takes four parameters rather than two.</span></span> <span data-ttu-id="a12c8-134">較新的參數會在建立 [XAPOFX](xapofx-overview.md) 時指定初始資料。</span><span class="sxs-lookup"><span data-stu-id="a12c8-134">The newer parameters specify initial data as part of [XAPOFX](xapofx-overview.md) creation.</span></span>

## <a name="xaudio-27-and-earlier-windows-7"></a><span data-ttu-id="a12c8-135">XAudio 2.7 和舊版 (Windows 7) </span><span class="sxs-lookup"><span data-stu-id="a12c8-135">XAudio 2.7 and earlier (Windows 7)</span></span>

<span data-ttu-id="a12c8-136">在應用程式中使用的所有舊版 XAudio2 都已提供為 DirectX SDK 中的可轉散發 Dll。</span><span class="sxs-lookup"><span data-stu-id="a12c8-136">All previous versions of XAudio2 for use in apps have been provided as redistributable DLLs in the DirectX SDK.</span></span> <span data-ttu-id="a12c8-137">第一版的 XAudio2 （XAudio2 2.0）隨附于年3月2008版的 DirectX SDK。</span><span class="sxs-lookup"><span data-stu-id="a12c8-137">The first version of XAudio2, XAudio2 2.0, shipped in the March 2008 release of the DirectX SDK.</span></span> <span data-ttu-id="a12c8-138">DirectX SDK 中所提供的最後一個版本是 XAudio2 2.7，在2010年6月的 DirectX SDK 最後一版中提供。</span><span class="sxs-lookup"><span data-stu-id="a12c8-138">The last version to ship in the DirectX SDK was XAudio2 2.7, available in the last release of the DirectX SDK in June 2010.</span></span>

<span data-ttu-id="a12c8-139">由於已淘汰所有 SHA-1 簽署的內容，因此 Microsoft 下載不再提供舊版 DirectX SDK。</span><span class="sxs-lookup"><span data-stu-id="a12c8-139">The legacy DirectX SDK is no longer available on Microsoft Downloads due to the retirement of all SHA-1 signed content.</span></span> <span data-ttu-id="a12c8-140">2010年6月是生命週期結束的版本。</span><span class="sxs-lookup"><span data-stu-id="a12c8-140">June 2010 was the end-of-life release.</span></span>

<span data-ttu-id="a12c8-141">舊版的 XAudio2 無法用來建立適用于 Windows 8 的 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="a12c8-141">Previous versions of XAudio2 cannot be used to build Windows Store apps for Windows 8.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a12c8-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="a12c8-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a12c8-143">快速入門</span><span class="sxs-lookup"><span data-stu-id="a12c8-143">Getting Started</span></span>](getting-started.md)
</dt> <dt>

[<span data-ttu-id="a12c8-144">XAudio2 重要概念</span><span class="sxs-lookup"><span data-stu-id="a12c8-144">XAudio2 Key Concepts</span></span>](xaudio2-key-concepts.md)
</dt> </dl>

[<span data-ttu-id="a12c8-145">XAudio 2.9 的可轉散發版本開發人員指南</span><span class="sxs-lookup"><span data-stu-id="a12c8-145">Developer guide for redistributable version of XAudio 2.9</span></span>](xaudio2-redistributable.md)
</dt> </dl>
 

 
