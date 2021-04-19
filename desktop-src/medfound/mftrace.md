---
description: MFTrace 是一種工具，可為媒體基礎應用程式產生追蹤記錄。
ms.assetid: 55b421c8-e87c-4dd2-8649-93832c93f999
title: MFTrace
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d4a216f225141ceccf3f1357025dd069afa494d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982527"
---
# <a name="mftrace"></a><span data-ttu-id="496fb-103">MFTrace</span><span class="sxs-lookup"><span data-stu-id="496fb-103">MFTrace</span></span>

<span data-ttu-id="496fb-104">MFTrace 是一種工具，可為媒體基礎應用程式產生追蹤記錄。</span><span class="sxs-lookup"><span data-stu-id="496fb-104">MFTrace is a tool for generating trace logs for Media Foundation applications.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="496fb-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="496fb-105">In this section</span></span>

-   [<span data-ttu-id="496fb-106">使用 MFTrace</span><span class="sxs-lookup"><span data-stu-id="496fb-106">Using MFTrace</span></span>](using-mftrace.md)
-   [<span data-ttu-id="496fb-107">MFTrace 關鍵字</span><span class="sxs-lookup"><span data-stu-id="496fb-107">MFTrace Keywords</span></span>](mftrace-keywords.md)
-   [<span data-ttu-id="496fb-108">MFTrace 設定檔</span><span class="sxs-lookup"><span data-stu-id="496fb-108">MFTrace Configuration File</span></span>](mftrace-configuration-file.md)

## <a name="requirements"></a><span data-ttu-id="496fb-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="496fb-109">Requirements</span></span>



| <span data-ttu-id="496fb-110">需求</span><span class="sxs-lookup"><span data-stu-id="496fb-110">Requirement</span></span> | <span data-ttu-id="496fb-111">值</span><span class="sxs-lookup"><span data-stu-id="496fb-111">Value</span></span> |
|--------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="496fb-112">最低 SDK 版本</span><span class="sxs-lookup"><span data-stu-id="496fb-112">Minimum SDK version</span></span>      | <span data-ttu-id="496fb-113">適用于 Windows 7 和 .NET Framework 4.0 的 Microsoft Windows 軟體開發套件 (SDK) </span><span class="sxs-lookup"><span data-stu-id="496fb-113">Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0</span></span> |
| <span data-ttu-id="496fb-114">最低作業系統</span><span class="sxs-lookup"><span data-stu-id="496fb-114">Minimum operating system</span></span> | <span data-ttu-id="496fb-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="496fb-115">Windows Vista</span></span>                                                                         |



 

<span data-ttu-id="496fb-116">MFTrace 需要下列 Dll，這些 Dll 也會在 SDK 中提供。</span><span class="sxs-lookup"><span data-stu-id="496fb-116">MFTrace requires the following DLLs, which are also provided in the SDK.</span></span>

-   <span data-ttu-id="496fb-117">detoured.dll</span><span class="sxs-lookup"><span data-stu-id="496fb-117">detoured.dll</span></span>
-   <span data-ttu-id="496fb-118">mfdetours.dll</span><span class="sxs-lookup"><span data-stu-id="496fb-118">mfdetours.dll</span></span>

<span data-ttu-id="496fb-119">SDK 提供32位和64位版本的 MFTrace。</span><span class="sxs-lookup"><span data-stu-id="496fb-119">The SDK provides both 32-bit and 64-bit versions of MFTrace.</span></span> <span data-ttu-id="496fb-120">MFTrace 不支援 WOW64;若要追蹤在64位 Windows 上執行的32位進程，請使用 MFTrace 的32位版本。</span><span class="sxs-lookup"><span data-stu-id="496fb-120">MFTrace does not support WOW64; to trace a 32-bit process running on 64-bit Windows, use the 32-bit version of MFTrace.</span></span>

<span data-ttu-id="496fb-121">sdk-32 位系統上的根目錄： \Program Files\Windows Kits\10 sdk-64 位系統上的根目錄： \Program 檔案 (x86) \Windows Kits\10 您會在 <sdk 根> \bin\mftrace.exe 找到 mftrace \<sdk-version> \<architecture></span><span class="sxs-lookup"><span data-stu-id="496fb-121">sdk-root on 32 bit systems: \Program Files\Windows Kits\10 sdk-root on 64 bit system: \Program Files (x86)\Windows Kits\10 You will find mftrace at <sdk-root>\bin\<sdk-version>\<architecture>\mftrace.exe</span></span>

## <a name="related-topics"></a><span data-ttu-id="496fb-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="496fb-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="496fb-123">媒體基礎工具</span><span class="sxs-lookup"><span data-stu-id="496fb-123">Media Foundation Tools</span></span>](media-foundation-tools.md)
</dt> </dl>

 

 



