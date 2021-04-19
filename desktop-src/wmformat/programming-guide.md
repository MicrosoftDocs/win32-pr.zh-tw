---
title: Windows Media Format SDK 程式設計指南
description: Windows Media Format SDK 程式設計指南
ms.assetid: 9b382c88-e4a9-4aed-a250-250fabface44
keywords:
- Windows Media Format SDK，程式設計手冊
- 'Windows Media Format SDK、Advanced Systems Format (ASF) '
- Advanced Systems Format (ASF) ，程式設計手冊
- ASF (Advanced Systems Format) ，程式設計手冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f4ea4f6819a31693d7c9d149717324ef6dcc65a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106966902"
---
# <a name="windows-media-format-sdk-programming-guide"></a><span data-ttu-id="15b20-107">Windows Media Format SDK 程式設計指南</span><span class="sxs-lookup"><span data-stu-id="15b20-107">Windows Media Format SDK Programming Guide</span></span>

<span data-ttu-id="15b20-108">程式設計指南旨在協助您瞭解如何使用 Microsoft Windows Media Format 軟體發展工具組 (SDK) 來建立應用程式，以使用 Advanced Systems 格式的檔案 (ASF) 。</span><span class="sxs-lookup"><span data-stu-id="15b20-108">The Programming Guide is intended to help you learn how to use the Microsoft Windows Media Format Software Development Kit (SDK) to build applications that work with files using the Advanced Systems Format (ASF).</span></span>

<span data-ttu-id="15b20-109">您可以使用 Windows Media Format SDK 來建立應用程式，以將數位媒體串流寫入及讀取來自 ASF 檔案的資料流程。</span><span class="sxs-lookup"><span data-stu-id="15b20-109">You can use the Windows Media Format SDK to create applications that write digital media streams to and read streams from ASF files.</span></span> <span data-ttu-id="15b20-110">此 SDK 也支援在 ASF 檔案中編輯中繼資料。</span><span class="sxs-lookup"><span data-stu-id="15b20-110">This SDK also supports the editing of metadata in ASF files.</span></span> <span data-ttu-id="15b20-111">此外，此 SDK 可以用來讀取和操作 MP3 檔案中的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="15b20-111">In addition, this SDK can be used to read and manipulate metadata in MP3 files.</span></span>

<span data-ttu-id="15b20-112">下列各節詳細說明使用此 SDK 寫入、讀取和編輯 ASF 檔案時所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="15b20-112">The following sections explain in detail the steps required to write, read, and edit ASF files by using this SDK.</span></span>



| <span data-ttu-id="15b20-113">區段</span><span class="sxs-lookup"><span data-stu-id="15b20-113">Section</span></span>                                                                            | <span data-ttu-id="15b20-114">描述</span><span class="sxs-lookup"><span data-stu-id="15b20-114">Description</span></span>                                                                                                       |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="15b20-115">快速入門</span><span class="sxs-lookup"><span data-stu-id="15b20-115">Getting Started</span></span>](getting-started.md)                                             | <span data-ttu-id="15b20-116">提供開始使用此 SDK 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="15b20-116">Provides general information about getting ready to use this SDK.</span></span>                                                 |
| [<span data-ttu-id="15b20-117">使用回呼方法</span><span class="sxs-lookup"><span data-stu-id="15b20-117">Using the Callback Methods</span></span>](using-the-callback-methods.md)                       | <span data-ttu-id="15b20-118">描述許多不同工作中使用的回呼方法。</span><span class="sxs-lookup"><span data-stu-id="15b20-118">Describes the callback methods used in many different tasks.</span></span>                                                      |
| [<span data-ttu-id="15b20-119">使用設定檔</span><span class="sxs-lookup"><span data-stu-id="15b20-119">Working with Profiles</span></span>](working-with-profiles.md)                                 | <span data-ttu-id="15b20-120">說明如何使用、編輯和建立設定檔。</span><span class="sxs-lookup"><span data-stu-id="15b20-120">Describes how to use, edit, and create profiles.</span></span>                                                                  |
| [<span data-ttu-id="15b20-121">寫入 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="15b20-121">Writing ASF Files</span></span>](writing-asf-files.md)                                         | <span data-ttu-id="15b20-122">描述如何使用 writer 物件來建立 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="15b20-122">Describes how to use the writer object to create ASF files.</span></span>                                                       |
| [<span data-ttu-id="15b20-123">讀取 ASF 檔案</span><span class="sxs-lookup"><span data-stu-id="15b20-123">Reading ASF Files</span></span>](reading-asf-files.md)                                         | <span data-ttu-id="15b20-124">說明如何接收來自 ASF 檔案的內容。</span><span class="sxs-lookup"><span data-stu-id="15b20-124">Describes how to receive content from ASF files.</span></span>                                                                  |
| [<span data-ttu-id="15b20-125">使用中繼資料</span><span class="sxs-lookup"><span data-stu-id="15b20-125">Working with Metadata</span></span>](working-with-metadata.md)                                 | <span data-ttu-id="15b20-126">說明如何管理 ASF 檔案標頭區段的內容。</span><span class="sxs-lookup"><span data-stu-id="15b20-126">Describes how to manage the contents of the header section of an ASF file.</span></span>                                        |
| [<span data-ttu-id="15b20-127">使用索引</span><span class="sxs-lookup"><span data-stu-id="15b20-127">Working with Indexes</span></span>](working-with-indexes.md)                                   | <span data-ttu-id="15b20-128">說明如何使用索引。</span><span class="sxs-lookup"><span data-stu-id="15b20-128">Describes how to work with indexes.</span></span>                                                                               |
| [<span data-ttu-id="15b20-129">使用設定檔</span><span class="sxs-lookup"><span data-stu-id="15b20-129">Working with Profiles</span></span>](working-with-profiles.md)                                 | <span data-ttu-id="15b20-130">說明如何使用、編輯和建立設定檔。</span><span class="sxs-lookup"><span data-stu-id="15b20-130">Describes how to use, edit, and create profiles.</span></span>                                                                  |
| [<span data-ttu-id="15b20-131">使用指令碼命令</span><span class="sxs-lookup"><span data-stu-id="15b20-131">Using Script Commands</span></span>](using-script-commands.md)                                 | <span data-ttu-id="15b20-132">描述如何在您的 ASF 檔案中使用指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="15b20-132">Describes how to use script commands in your ASF files.</span></span>                                                           |
| [<span data-ttu-id="15b20-133">將資料從一個檔案複製到另一個檔案</span><span class="sxs-lookup"><span data-stu-id="15b20-133">Copying Data from One File to Another</span></span>](copying-data-from-one-file-to-another.md) | <span data-ttu-id="15b20-134">說明如何將資料從一個 ASF 檔案複製到另一個，而不需要解碼和編碼。</span><span class="sxs-lookup"><span data-stu-id="15b20-134">Describes how to copy data from one ASF file to another, with without decoding and encoding.</span></span>                      |
| [<span data-ttu-id="15b20-135">啟用 DRM 支援</span><span class="sxs-lookup"><span data-stu-id="15b20-135">Enabling DRM Support</span></span>](enabling-drm-support.md)                                   | <span data-ttu-id="15b20-136">說明如何啟用受 DRM 保護之 ASF 檔案的播放支援。</span><span class="sxs-lookup"><span data-stu-id="15b20-136">Describes how to enable support for playback of DRM-protected ASF files.</span></span>                                          |
| [<span data-ttu-id="15b20-137">執行網路功能</span><span class="sxs-lookup"><span data-stu-id="15b20-137">Implementing Network Functionality</span></span>](implementing-network-functionality.md)       | <span data-ttu-id="15b20-138">說明如何使用此 SDK 來執行成功串流處理媒體所不可或缺的網路作業。</span><span class="sxs-lookup"><span data-stu-id="15b20-138">Describes the use of this SDK to perform the network operations that are essential to successful streaming media.</span></span> |
| [<span data-ttu-id="15b20-139">Advanced 主題</span><span class="sxs-lookup"><span data-stu-id="15b20-139">Advanced Topics</span></span>](advanced-topics.md)                                             | <span data-ttu-id="15b20-140">描述如何在您的應用程式中使用此 SDK 的一些先進功能。</span><span class="sxs-lookup"><span data-stu-id="15b20-140">Describes how to use some of the advanced features of this SDK in your applications.</span></span>                              |
| [<span data-ttu-id="15b20-141">DirectShow 和 Windows Media</span><span class="sxs-lookup"><span data-stu-id="15b20-141">DirectShow and Windows Media</span></span>](directshow-and-windows-media.md)                   | <span data-ttu-id="15b20-142">說明如何使用 Microsoft DirectShow 來建立和讀取 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="15b20-142">Describes how you can use Microsoft DirectShow to create and read ASF files.</span></span>                                      |
| [<span data-ttu-id="15b20-143">專案考慮</span><span class="sxs-lookup"><span data-stu-id="15b20-143">Project Considerations</span></span>](project-considerations.md)                               | <span data-ttu-id="15b20-144">提供有關完成及散發應用程式的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="15b20-144">Provides details about finishing and distributing your applications.</span></span>                                              |



 

## <a name="related-topics"></a><span data-ttu-id="15b20-145">相關主題</span><span class="sxs-lookup"><span data-stu-id="15b20-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15b20-146">**關於 Windows Media Format SDK**</span><span class="sxs-lookup"><span data-stu-id="15b20-146">**About the Windows Media Format SDK**</span></span>](about-the-windows-media-format-sdk.md)
</dt> <dt>

[<span data-ttu-id="15b20-147">**Windows Media Format 11 SDK**</span><span class="sxs-lookup"><span data-stu-id="15b20-147">**Windows Media Format 11 SDK**</span></span>](windows-media-format-11-sdk.md)
</dt> </dl>

 

 




