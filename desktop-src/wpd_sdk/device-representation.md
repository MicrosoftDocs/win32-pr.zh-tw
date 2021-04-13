---
description: 裝置標記法
ms.assetid: bf8b9c67-b023-40ed-97c6-9ca030de610a
title: 裝置標記法
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c95352c191d3e2d34392f4236b926b81cf65fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468956"
---
# <a name="device-representation"></a><span data-ttu-id="3941f-103">裝置標記法</span><span class="sxs-lookup"><span data-stu-id="3941f-103">Device Representation</span></span>

<span data-ttu-id="3941f-104">裝置有兩個主要的行為，可由 Windows 可攜式裝置 (WPD) 架構來解決：</span><span class="sxs-lookup"><span data-stu-id="3941f-104">Devices have two main behaviors that are addressed by the Windows Portable Devices (WPD) architecture:</span></span>

-   <span data-ttu-id="3941f-105">存取和儲存內容。</span><span class="sxs-lookup"><span data-stu-id="3941f-105">Accessing and storing content.</span></span> <span data-ttu-id="3941f-106">例如，應用程式必須能夠將音樂檔新增到便攜音樂播放機。</span><span class="sxs-lookup"><span data-stu-id="3941f-106">For example, applications must be able to add music files to a portable music player.</span></span>
-   <span data-ttu-id="3941f-107">裝置的程式設計。</span><span class="sxs-lookup"><span data-stu-id="3941f-107">Programming the device.</span></span> <span data-ttu-id="3941f-108">這包括簡單的作業，例如變更設定和準備裝置以進行資料捕獲，或更複雜的作業，例如上傳固件。</span><span class="sxs-lookup"><span data-stu-id="3941f-108">This includes simple operations such as changing settings and preparing the device for data capture, or more complex operations such as uploading firmware.</span></span> <span data-ttu-id="3941f-109">範例包括將「拍攝」命令發出至數位的靜止相機。</span><span class="sxs-lookup"><span data-stu-id="3941f-109">Examples include issuing a "Take Picture" command to a digital still camera.</span></span>

<span data-ttu-id="3941f-110">在 WPD 中，這些行為的描述方式是將裝置表示為物件的階層。</span><span class="sxs-lookup"><span data-stu-id="3941f-110">In WPD, these behaviors are described by representing the device as a hierarchy of objects.</span></span> <span data-ttu-id="3941f-111">下圖顯示多函式裝置的 WPD 物件標記法，在此案例中為行動電話。</span><span class="sxs-lookup"><span data-stu-id="3941f-111">The following illustration shows a WPD object representation for a multi-function device, which in this case is a mobile phone.</span></span>

![顯示行動電話物件階層的圖例](images/wpd-overview-figure3.gif)

<span data-ttu-id="3941f-113">此階層說明下列功能和內容。</span><span class="sxs-lookup"><span data-stu-id="3941f-113">This hierarchy illustrates the following functionality and contents.</span></span>

<span data-ttu-id="3941f-114">功能：</span><span class="sxs-lookup"><span data-stu-id="3941f-114">Functionality:</span></span>

-   <span data-ttu-id="3941f-115">儲存體物件。</span><span class="sxs-lookup"><span data-stu-id="3941f-115">Storage object.</span></span> <span data-ttu-id="3941f-116">此裝置具有資料存放區。</span><span class="sxs-lookup"><span data-stu-id="3941f-116">This device has data storage.</span></span>
-   <span data-ttu-id="3941f-117">連絡人服務。</span><span class="sxs-lookup"><span data-stu-id="3941f-117">Contacts Service.</span></span> <span data-ttu-id="3941f-118">這項服務是一個功能物件，可用來同步處理和儲存手機上的連絡人。</span><span class="sxs-lookup"><span data-stu-id="3941f-118">This service is a functional object that can be used to synchronize and store contacts on the phone.</span></span>
-   <span data-ttu-id="3941f-119">SMS 服務。</span><span class="sxs-lookup"><span data-stu-id="3941f-119">SMS Service.</span></span> <span data-ttu-id="3941f-120">這項服務是一個功能物件，可用來傳送、接收和儲存 SMS 訊息。</span><span class="sxs-lookup"><span data-stu-id="3941f-120">This service is a functional object that can be used to send, receive, and store SMS messages.</span></span>

<span data-ttu-id="3941f-121">內容: </span><span class="sxs-lookup"><span data-stu-id="3941f-121">Contents:</span></span>

-   <span data-ttu-id="3941f-122">媒體物件。</span><span class="sxs-lookup"><span data-stu-id="3941f-122">Media objects.</span></span> <span data-ttu-id="3941f-123">此裝置會將影像、音樂和影片檔案儲存在儲存物件上的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="3941f-123">This device stores images, music, and video files in folders on the Storage object.</span></span> <span data-ttu-id="3941f-124">雖然圖中顯示的檔案是儲存在一個資料夾下，裝置也可以將內容細分為依儲存的媒體類型組織的資料夾;例如，[影像資料夾]、[音樂] 資料夾和 [影片] 資料夾。</span><span class="sxs-lookup"><span data-stu-id="3941f-124">While the files shown in the illustration are stored under one folder, a device can subdivide content into folders organized by the type of media stored; for example, image folders, music folders, and video folders.</span></span>
-   <span data-ttu-id="3941f-125">Contact 物件。</span><span class="sxs-lookup"><span data-stu-id="3941f-125">Contact objects.</span></span> <span data-ttu-id="3941f-126">此裝置會將連絡人資訊儲存 (例如姓名、電話號碼和位址) 作為連絡人服務的子系</span><span class="sxs-lookup"><span data-stu-id="3941f-126">This device stores contact information (such as name, phone number, and address) as children of the Contacts Service</span></span>
-   <span data-ttu-id="3941f-127">Message 物件。</span><span class="sxs-lookup"><span data-stu-id="3941f-127">Message objects.</span></span> <span data-ttu-id="3941f-128">此裝置會將 SMS 訊息儲存為 SMS 服務的子系。</span><span class="sxs-lookup"><span data-stu-id="3941f-128">This device stores SMS messages as children of the SMS Service.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3941f-129">相關主題</span><span class="sxs-lookup"><span data-stu-id="3941f-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3941f-130">**應用程式總覽**</span><span class="sxs-lookup"><span data-stu-id="3941f-130">**Application Overview**</span></span>](application-overview.md)
</dt> </dl>

 

 



