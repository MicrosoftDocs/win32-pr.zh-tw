---
description: Windows 影像處理元件 (WIC) 是 Windows Vista 和 Windows 7 作業系統上數位製作映射的可擴充平臺。
ms.assetid: ffcd5239-ae2d-436f-9402-8c10a79256c3
title: '簡介 (如何撰寫 WIC-Enabled 編解碼器) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776bf9f2c0cb5df8b45ce04d55f20d40d05a12a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106976931"
---
# <a name="introduction-how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="ee417-103">簡介 (如何撰寫 WIC-Enabled 編解碼器) </span><span class="sxs-lookup"><span data-stu-id="ee417-103">Introduction (How to Write a WIC-Enabled Codec)</span></span>

<span data-ttu-id="ee417-104">Windows 影像處理元件 (WIC) 是 Windows Vista 和 Windows 7 作業系統上數位製作映射的可擴充平臺。</span><span class="sxs-lookup"><span data-stu-id="ee417-104">The Windows Imaging Component (WIC) is an extensible platform for digital imaging on the Windows Vista and Windows 7 operating systems.</span></span> <span data-ttu-id="ee417-105">WIC 也可在 Windows XP 與 Windows Server 2003 上取得，可作為 Microsoft .NET Framework 3.0 或您可以重新發佈的個別元件。</span><span class="sxs-lookup"><span data-stu-id="ee417-105">WIC is also available on Windows XP and Windows Server 2003, either as part of Microsoft .NET Framework 3.0 or as a separate component that you can redistribute.</span></span> <span data-ttu-id="ee417-106">任何使用 WIC 的應用程式都可以使用任何影像格式來存取、顯示、處理及列印影像，以提供已啟用 WIC 的編解碼器，並使用一組一致的介面，免除特定格式的特殊知識需求。</span><span class="sxs-lookup"><span data-stu-id="ee417-106">Any application using the WIC can access, display, process, and print images in any image format that provides a WIC-enabled codec, using a single set of consistent interfaces that eliminate the need for specialized knowledge of specific formats.</span></span>

<span data-ttu-id="ee417-107">Windows Vista Explorer、Windows Vista 影像中心、Live 影像中心和 Windows 7 相片檢視器都是以 WIC 為基礎。</span><span class="sxs-lookup"><span data-stu-id="ee417-107">The Windows Vista Explorer, Windows Vista Photo Gallery, Live Photo Gallery, and Windows 7 Photo Viewer are built on WIC.</span></span> <span data-ttu-id="ee417-108">在 Windows Vista 或 Windows 7 系統上安裝已啟用 WIC 的編解碼器之後，作業系統會針對該平臺隨附的標準影像格式，提供相同的關聯影像格式支援層級。</span><span class="sxs-lookup"><span data-stu-id="ee417-108">After a WIC-enabled codec is installed on a Windows Vista or Windows 7 system, the operating system provides the same level of support for the associated image format as for the standard image formats that ship with the platform.</span></span> <span data-ttu-id="ee417-109">因為您為自己的影像格式撰寫編解碼器，所以您可以在使用影像格式的任何地方確保一致的品質，並獲得完整平臺支援的優點。</span><span class="sxs-lookup"><span data-stu-id="ee417-109">Because you write the codec for your own image format, you can ensure consistent quality wherever your image format is used, and you get the benefits of full platform support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee417-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="ee417-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="ee417-111">**概念**</span><span class="sxs-lookup"><span data-stu-id="ee417-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="ee417-112">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="ee417-112">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="ee417-113">Windows 影像處理元件的運作方式</span><span class="sxs-lookup"><span data-stu-id="ee417-113">How The Windows Imaging Component Works</span></span>](-wic-howwicworks.md)
</dt> <dt>

<span data-ttu-id="ee417-114">如何撰寫 WIC-Enabled 編解碼器</span><span class="sxs-lookup"><span data-stu-id="ee417-114">How to Write a WIC-Enabled CODEC</span></span>
</dt> <dt>

[<span data-ttu-id="ee417-115">Windows 影像處理元件總覽</span><span class="sxs-lookup"><span data-stu-id="ee417-115">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



