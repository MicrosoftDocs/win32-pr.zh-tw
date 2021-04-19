---
description: 深入瞭解：傳輸資料
ms.assetid: 34871ff4-7eb0-451b-a62b-85b632af9a47
title: 傳送資料
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05d94e9e09aad121720ca491864a23f3d2d38b16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972641"
---
# <a name="transferring-data"></a><span data-ttu-id="bb0e5-103">傳送資料</span><span class="sxs-lookup"><span data-stu-id="bb0e5-103">Transferring Data</span></span>

> [!Note]  
> <span data-ttu-id="bb0e5-104">此腳本系統已取代為 Windows 映像取得 (WIA) Automation 層。</span><span class="sxs-lookup"><span data-stu-id="bb0e5-104">This scripting system has been replaced with Windows Image Acquisition (WIA) Automation Layer.</span></span> <span data-ttu-id="bb0e5-105">請參閱 [Windows 映像取得自動化層](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)。</span><span class="sxs-lookup"><span data-stu-id="bb0e5-105">See [Windows Image Acquisition Automation Layer](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).</span></span>

 

<span data-ttu-id="bb0e5-106">使用 [**專案**](-wia-item.md)物件的 [**傳送**](-wia-iwiadispatchitem-transfer.md)方法，將影像或音訊資料從裝置傳送至檔案或剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="bb0e5-106">Use the [**Transfer**](-wia-iwiadispatchitem-transfer.md) method of an [**Item**](-wia-item.md) object to transfer image or audio data from a device to a file or the clipboard.</span></span>

<span data-ttu-id="bb0e5-107">傳遞路徑和檔案名做為第一個參數，以將資料儲存至磁片，或傳遞字串 "剪貼簿" 以將專案傳送至剪貼簿。</span><span class="sxs-lookup"><span data-stu-id="bb0e5-107">Pass a path and filename as the first parameter to save the data to disk, or pass the string "clipboard" to transfer the item to the clipboard.</span></span>

 

 
