---
description: XAudio2 引擎的 debug 版本會驗證參數，並提供詳細的警告和錯誤訊息。
ms.assetid: a7aaebf9-98d4-e96c-993d-b0d0b7074788
title: XAudio2 調試功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc50e710f30969e024078eeaf2660545e1da45c8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690883"
---
# <a name="xaudio2-debugging-facilities"></a><span data-ttu-id="90e8f-103">XAudio2 調試功能</span><span class="sxs-lookup"><span data-stu-id="90e8f-103">XAudio2 Debugging Facilities</span></span>

<span data-ttu-id="90e8f-104">XAudio2 引擎的 debug 版本會驗證參數，並提供詳細的警告和錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="90e8f-104">The debug version of the XAudio2 engine validates parameters, and provides detailed warning and error messages.</span></span>

## <a name="setting-the-debug-logging-level-at-run-time"></a><span data-ttu-id="90e8f-105">在執行時間設定 Debug 記錄層級</span><span class="sxs-lookup"><span data-stu-id="90e8f-105">Setting the Debug Logging Level at Run Time</span></span>

<span data-ttu-id="90e8f-106">您可以使用所需的記錄層級的旗標填入 [**XAudio2 \_ DEBUG \_**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) 設定結構，然後將結構傳遞給 [**IXAudio2：： SetDebugConfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) 方法，隨時設定 XAudio2 所顯示的偵錯工具的層級。</span><span class="sxs-lookup"><span data-stu-id="90e8f-106">You can set the level of debugging information shown by XAudio2 at any time by filling out an [**XAUDIO2\_DEBUG\_CONFIGURATION**](/windows/desktop/api/xaudio2/ns-xaudio2-xaudio2_debug_configuration) structure with the flags for the desired logging level, and then pass the structure to the [**IXAudio2::SetDebugConfiguration**](/windows/win32/api/xaudio2/nf-xaudio2-ixaudio2-setdebugconfiguration) method.</span></span> <span data-ttu-id="90e8f-107">傳遞給 **IXAudio2：： SetDebugConfiguration** 方法的值一律會覆寫在 Windows 登錄中設定的所有預設值。</span><span class="sxs-lookup"><span data-stu-id="90e8f-107">Values passed to the **IXAudio2::SetDebugConfiguration** method always override any default values that were set in the Windows registry.</span></span>

## <a name="debug-support"></a><span data-ttu-id="90e8f-108">Debug 支援</span><span class="sxs-lookup"><span data-stu-id="90e8f-108">Debug Support</span></span>

<span data-ttu-id="90e8f-109">在 Windows 8 中，偵錯工具一律可供 XAUDIO2。</span><span class="sxs-lookup"><span data-stu-id="90e8f-109">The debugging facilities are always available for XAUDIO2 in Windows 8.</span></span>

<span data-ttu-id="90e8f-110">針對 DirectX SDK 版本的 XAUDIO2，您必須在使用 [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create)建立 XAUDIO2 物件時使用 **XAUDIO2 \_ DEBUG \_ ENGINE** ，而且系統必須安裝 DirectX SDK Developer Runtime，才能支援偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="90e8f-110">For the DirectX SDK versions of XAUDIO2, you must use **XAUDIO2\_DEBUG\_ENGINE** when creating the XAUDIO2 object with [**XAudio2Create**](/windows/desktop/api/xaudio2/nf-xaudio2-xaudio2create) and the system must have the DirectX SDK Developer Runtime installed for debugging to be supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="90e8f-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="90e8f-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="90e8f-112">調試功能</span><span class="sxs-lookup"><span data-stu-id="90e8f-112">Debugging Facilities</span></span>](debugging-facilities.md)
</dt> <dt>

[<span data-ttu-id="90e8f-113">XAudio2 程式設計參考</span><span class="sxs-lookup"><span data-stu-id="90e8f-113">XAudio2 Programming Reference</span></span>](programming-reference.md)
</dt> </dl>

 

 
