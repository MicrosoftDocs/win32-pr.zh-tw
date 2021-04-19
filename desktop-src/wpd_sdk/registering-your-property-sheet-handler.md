---
description: 註冊您的屬性工作表處理常式
ms.assetid: 6621529c-717b-4f36-8d9e-769d6b720b8a
title: 註冊您的屬性工作表處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6a59a03ebd13f5a541674012da7b07045e0a510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979907"
---
# <a name="registering-your-property-sheet-handler"></a><span data-ttu-id="4db52-103">註冊您的屬性工作表處理常式</span><span class="sxs-lookup"><span data-stu-id="4db52-103">Registering Your Property Sheet Handler</span></span>

<span data-ttu-id="4db52-104">為了讓 WPD 命名空間能夠辨識您的屬性工作表處理常式，您必須在 Windows 登錄中正確註冊。</span><span class="sxs-lookup"><span data-stu-id="4db52-104">In order for your property sheet handler to be recognized by the WPD namespace you must register it properly in the Windows registry.</span></span> <span data-ttu-id="4db52-105">WPD 屬性工作表處理常式的註冊專案類似于 shell 的註冊專案，但會將它們註冊為特殊檔案類型。</span><span class="sxs-lookup"><span data-stu-id="4db52-105">The registration entries for a WPD property sheet handler are similar to those for the shell, but they are registered as special file types.</span></span> <span data-ttu-id="4db52-106">WPD 屬性工作表處理常式是根據它們所代表的內容類型來註冊。</span><span class="sxs-lookup"><span data-stu-id="4db52-106">WPD property sheet handlers are registered according to the content type they represent.</span></span> <span data-ttu-id="4db52-107">以下是 WPD 內容功能表處理常式的範例註冊樹：</span><span class="sxs-lookup"><span data-stu-id="4db52-107">Below is a sample registration tree for a WPD context menu handler:</span></span>


```C++
HKEY_CLASSES_ROOT
 \-- WPDPropSheet.Image
      \-- shellex
           \-- PropertySheetHandlers
                \-- MyHandler (Default)  REG_SZ {0000000-0000-0000-0000-000000000000}

```



<span data-ttu-id="4db52-108">上述範例會使用 WPD 命名空間來註冊自訂處理常式。</span><span class="sxs-lookup"><span data-stu-id="4db52-108">The above example registers a custom handler with the WPD namespace.</span></span> <span data-ttu-id="4db52-109">當使用者透過 Windows Shell 以滑鼠右鍵按一下裝置上的影像檔案，並選取 [ **屬性**] 時，它會叫用這個屬性工作表處理常式。</span><span class="sxs-lookup"><span data-stu-id="4db52-109">When a user right-clicks an image file on a device through the Windows Shell and selects **Properties**, it invokes this property sheet handler.</span></span> <span data-ttu-id="4db52-110">WPD 命名空間會使用 WPD \_ 內容 \_ 類型來決定要載入的屬性工作表處理常式。</span><span class="sxs-lookup"><span data-stu-id="4db52-110">The WPD namespace uses the WPD\_CONTENT\_TYPE to determine which property sheet handlers to load.</span></span> <span data-ttu-id="4db52-111">如果內容類型並未提供有用的分類，則命名空間會將屬性工作表處理常式載入 **WPDPropSheet 一般** 登錄機碼底下。</span><span class="sxs-lookup"><span data-stu-id="4db52-111">If the content type does not provide a useful classification, then the namespace will load the property sheet handlers under the **WPDPropSheet.Generic registry** key.</span></span> <span data-ttu-id="4db52-112">下表列出可供內容功能表處理常式使用的所有檔案類別，以及它們所代表的內容類型和副檔名。</span><span class="sxs-lookup"><span data-stu-id="4db52-112">The following table lists all of the file classes available to a context menu handler and what content types and file extensions they represent.</span></span>



| <span data-ttu-id="4db52-113">登錄金鑰</span><span class="sxs-lookup"><span data-stu-id="4db52-113">Registry Key</span></span>                   | <span data-ttu-id="4db52-114">WPD 內容類型</span><span class="sxs-lookup"><span data-stu-id="4db52-114">WPD Content Type</span></span>                                                                                                               |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4db52-115">**WPDCoNtextMenu 裝置**</span><span class="sxs-lookup"><span data-stu-id="4db52-115">**WPDContextMenu.Device**</span></span>      | <span data-ttu-id="4db52-116">在此機碼下註冊可在裝置層級啟用您的內容功能表處理常式。</span><span class="sxs-lookup"><span data-stu-id="4db52-116">Registering under this key enables your context menu handler at the device level.</span></span> <span data-ttu-id="4db52-117"> (在裝置上按一下滑鼠右鍵。 ) </span><span class="sxs-lookup"><span data-stu-id="4db52-117">(Right-click on a device.)</span></span>                   |
| <span data-ttu-id="4db52-118">**WPDCoNtextMenu**</span><span class="sxs-lookup"><span data-stu-id="4db52-118">**WPDContextMenu.Storage**</span></span>     | <span data-ttu-id="4db52-119">在此機碼下註冊可在儲存層級啟用您的內容功能表處理常式。</span><span class="sxs-lookup"><span data-stu-id="4db52-119">Registering under this key enables your context menu handler at the storage level.</span></span> <span data-ttu-id="4db52-120"> (以滑鼠右鍵按一下儲存體。 ) </span><span class="sxs-lookup"><span data-stu-id="4db52-120">(Right-click on a storage.)</span></span>                 |
| <span data-ttu-id="4db52-121">**WPDCoNtextMenu 資料夾**</span><span class="sxs-lookup"><span data-stu-id="4db52-121">**WPDContextMenu.Folder**</span></span>      | <span data-ttu-id="4db52-122">WPD \_ 內容 \_ 類型 \_ 資料夾</span><span class="sxs-lookup"><span data-stu-id="4db52-122">WPD\_CONTENT\_TYPE\_FOLDER</span></span>                                                                                                     |
| <span data-ttu-id="4db52-123">**WPDCoNtextMenu 影像**</span><span class="sxs-lookup"><span data-stu-id="4db52-123">**WPDContextMenu.Image**</span></span>       | <span data-ttu-id="4db52-124">WPD \_ 內容 \_ 類型 \_ 影像</span><span class="sxs-lookup"><span data-stu-id="4db52-124">WPD\_CONTENT\_TYPE\_IMAGE</span></span>                                                                                                      |
| <span data-ttu-id="4db52-125">**WPDCoNtextMenu 音訊**</span><span class="sxs-lookup"><span data-stu-id="4db52-125">**WPDContextMenu.Audio**</span></span>       | <span data-ttu-id="4db52-126">WPD \_ 內容 \_ 類型 \_ 音訊</span><span class="sxs-lookup"><span data-stu-id="4db52-126">WPD\_CONTENT\_TYPE\_AUDIO</span></span>                                                                                                      |
| <span data-ttu-id="4db52-127">**WPDCoNtextMenu 影片**</span><span class="sxs-lookup"><span data-stu-id="4db52-127">**WPDContextMenu.Video**</span></span>       | <span data-ttu-id="4db52-128">WPD \_ 內容 \_ 類型 \_ 影片</span><span class="sxs-lookup"><span data-stu-id="4db52-128">WPD\_CONTENT\_TYPE\_VIDEO</span></span>                                                                                                      |
| <span data-ttu-id="4db52-129">**WPDCoNtextMenu 播放清單**</span><span class="sxs-lookup"><span data-stu-id="4db52-129">**WPDContextMenu.Playlist**</span></span>    | <span data-ttu-id="4db52-130">WPD \_ 內容 \_ 類型 \_ 播放清單</span><span class="sxs-lookup"><span data-stu-id="4db52-130">WPD\_CONTENT\_TYPE\_PLAYLIST</span></span>                                                                                                   |
| <span data-ttu-id="4db52-131">**WPDContextMenu.Doc>ument**</span><span class="sxs-lookup"><span data-stu-id="4db52-131">**WPDContextMenu.Document**</span></span>    | <span data-ttu-id="4db52-132">WPD \_ 內容 \_ 類型 \_ 檔</span><span class="sxs-lookup"><span data-stu-id="4db52-132">WPD\_CONTENT\_TYPE\_DOCUMENT</span></span>                                                                                                   |
| <span data-ttu-id="4db52-133">**WPDCoNtextMenu。連絡人**</span><span class="sxs-lookup"><span data-stu-id="4db52-133">**WPDContextMenu.Contact**</span></span>     | <span data-ttu-id="4db52-134">WPD \_ 內容 \_ 類型 \_ 連絡人</span><span class="sxs-lookup"><span data-stu-id="4db52-134">WPD\_CONTENT\_TYPE\_CONTACT</span></span>                                                                                                    |
| <span data-ttu-id="4db52-135">**WPDCoNtextMenu.Email**</span><span class="sxs-lookup"><span data-stu-id="4db52-135">**WPDContextMenu.Email**</span></span>       | <span data-ttu-id="4db52-136">WPD \_ 內容 \_ 類型 \_ 電子郵件</span><span class="sxs-lookup"><span data-stu-id="4db52-136">WPD\_CONTENT\_TYPE\_EMAIL</span></span>                                                                                                      |
| <span data-ttu-id="4db52-137">**WPDCoNtextMenu 約會**</span><span class="sxs-lookup"><span data-stu-id="4db52-137">**WPDContextMenu.Appointment**</span></span> | <span data-ttu-id="4db52-138">WPD \_ 內容 \_ 類型 \_ 約會</span><span class="sxs-lookup"><span data-stu-id="4db52-138">WPD\_CONTENT\_TYPE\_APPOINTMENT</span></span>                                                                                                |
| <span data-ttu-id="4db52-139">**WPDCoNtextMenu。工作**</span><span class="sxs-lookup"><span data-stu-id="4db52-139">**WPDContextMenu.Task**</span></span>        | <span data-ttu-id="4db52-140">WPD \_ 內容 \_ 類型 \_ 工作</span><span class="sxs-lookup"><span data-stu-id="4db52-140">WPD\_CONTENT\_TYPE\_TASK</span></span>                                                                                                       |
| <span data-ttu-id="4db52-141">**WPDCoNtextMenu**</span><span class="sxs-lookup"><span data-stu-id="4db52-141">**WPDContextMenu.Memo**</span></span>        | <span data-ttu-id="4db52-142">WPD \_ 內容 \_ 類型 \_ 備忘錄</span><span class="sxs-lookup"><span data-stu-id="4db52-142">WPD\_CONTENT\_TYPE\_MEMO</span></span>                                                                                                       |
| <span data-ttu-id="4db52-143">**WPDCoNtextMenu.ImageAlbum**</span><span class="sxs-lookup"><span data-stu-id="4db52-143">**WPDContextMenu.ImageAlbum**</span></span>  | <span data-ttu-id="4db52-144">WPD \_ 內容 \_ 類型 \_ 影像 \_ 專輯</span><span class="sxs-lookup"><span data-stu-id="4db52-144">WPD\_CONTENT\_TYPE\_IMAGE\_ALBUM</span></span>                                                                                               |
| <span data-ttu-id="4db52-145">**WPDCoNtextMenu.AudioAlbum**</span><span class="sxs-lookup"><span data-stu-id="4db52-145">**WPDContextMenu.AudioAlbum**</span></span>  | <span data-ttu-id="4db52-146">WPD \_ 內容 \_ 類型 \_ 音訊 \_ 專輯</span><span class="sxs-lookup"><span data-stu-id="4db52-146">WPD\_CONTENT\_TYPE\_AUDIO\_ALBUM</span></span>                                                                                               |
| <span data-ttu-id="4db52-147">**WPDCoNtextMenu.VideoAlbum**</span><span class="sxs-lookup"><span data-stu-id="4db52-147">**WPDContextMenu.VideoAlbum**</span></span>  | <span data-ttu-id="4db52-148">WPD \_ 內容 \_ 類型 \_ 影片 \_ 專輯</span><span class="sxs-lookup"><span data-stu-id="4db52-148">WPD\_CONTENT\_TYPE\_VIDEO\_ALBUM</span></span>                                                                                               |
| <span data-ttu-id="4db52-149">**WPDCoNtextMenu.MixedAlbum**</span><span class="sxs-lookup"><span data-stu-id="4db52-149">**WPDContextMenu.MixedAlbum**</span></span>  | <span data-ttu-id="4db52-150">WPD \_ 內容 \_ 類型 \_ 混合式 \_ 內容 \_ 專輯</span><span class="sxs-lookup"><span data-stu-id="4db52-150">WPD\_CONTENT\_TYPE\_MIXED\_CONTENT\_ALBUM</span></span>                                                                                      |
| <span data-ttu-id="4db52-151">**WPDCoNtextMenu 泛型**</span><span class="sxs-lookup"><span data-stu-id="4db52-151">**WPDContextMenu.Generic**</span></span>     | <span data-ttu-id="4db52-152">\_ \_ 未指定 WPD 內容類型 \_</span><span class="sxs-lookup"><span data-stu-id="4db52-152">WPD\_CONTENT\_TYPE\_UNSPECIFIED</span></span><br/> <span data-ttu-id="4db52-153">WPD \_ 內容 \_ 類型 \_ 一般 \_ 檔案</span><span class="sxs-lookup"><span data-stu-id="4db52-153">WPD\_CONTENT\_TYPE\_GENERIC\_FILE</span></span><br/> <span data-ttu-id="4db52-154">WPD \_ 內容 \_ 類型 \_ 方案</span><span class="sxs-lookup"><span data-stu-id="4db52-154">WPD\_CONTENT\_TYPE\_PROGRAM</span></span><br/> |



 

 

 




