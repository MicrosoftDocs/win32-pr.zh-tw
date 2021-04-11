---
title: 通用控制項的 Unicode 支援
description: 本主題說明如何支援一般控制項通知的 Unicode。
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb029d6e1c018f1793c749aefb2f88104559cae
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933736"
---
# <a name="unicode-support-for-common-controls"></a><span data-ttu-id="9de60-103">通用控制項的 Unicode 支援</span><span class="sxs-lookup"><span data-stu-id="9de60-103">Unicode Support for Common Controls</span></span>

<span data-ttu-id="9de60-104">本主題說明如何支援一般控制項通知的 Unicode。</span><span class="sxs-lookup"><span data-stu-id="9de60-104">This topic describes how to support Unicode for common control notifications.</span></span>


<span data-ttu-id="9de60-105">針對 comctl32.dll 5.80 版和更新版本，通用控制項通知支援 Windows 95 系統或更新版本上的 ANSI 和 Unicode 格式。</span><span class="sxs-lookup"><span data-stu-id="9de60-105">For versions 5.80 and later of comctl32.dll, common controls notifications support both ANSI and Unicode formats on Windows 95 systems or later.</span></span> <span data-ttu-id="9de60-106">系統會將您的視窗傳送至 [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) 訊息，以決定要使用的格式。</span><span class="sxs-lookup"><span data-stu-id="9de60-106">The system determines which format to use by sending your window a [**WM\_NOTIFYFORMAT**](wm-notifyformat.md) message.</span></span> <span data-ttu-id="9de60-107">若要指定格式，請傳回 \_ ansi 通知的 NFR ansi，或 \_ unicode 通知的 NFR unicode。</span><span class="sxs-lookup"><span data-stu-id="9de60-107">To specify a format, return NFR\_ANSI for ANSI notifications or NFR\_UNICODE for Unicode notifications.</span></span> <span data-ttu-id="9de60-108">如果您未處理此訊息，系統會呼叫 [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) 來判斷格式。</span><span class="sxs-lookup"><span data-stu-id="9de60-108">If you do not handle this message, the system calls [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) to determine the format.</span></span> <span data-ttu-id="9de60-109">由於 Windows 95 和 Windows 98 一律會傳回 **FALSE** 給此函式呼叫，因此預設會使用 ANSI 通知。</span><span class="sxs-lookup"><span data-stu-id="9de60-109">Since Windows 95 and Windows 98 always return **FALSE** to this function call, they use ANSI notifications by default.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9de60-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="9de60-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9de60-111">關於通用控制項</span><span class="sxs-lookup"><span data-stu-id="9de60-111">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 