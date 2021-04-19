---
description: 選取映射之後，應用程式會針對在 Windows XP 或) 舊版中執行的應用程式使用 IWiaDataTransfer 介面 (，或針對在 Windows Vista 或更新版本中執行的應用程式使用 IWiaTransfer 介面 () 從映射裝置傳輸影像資料。 如需詳細資訊，請參閱 WIA 1.0 中的傳送影像資料，或傳輸 WIA 2.0 中的影像資料。
ms.assetid: cf76e526-d63b-4ee5-ba3c-871f2051a82c
title: 取得映射
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d062cb370327311ad0c7d4f883344c05bb776f6a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106988811"
---
# <a name="acquiring-images"></a><span data-ttu-id="dfd28-104">取得映射</span><span class="sxs-lookup"><span data-stu-id="dfd28-104">Acquiring Images</span></span>

<span data-ttu-id="dfd28-105">選取映射之後，應用程式會針對在 Windows XP 或) 舊版中執行的應用程式使用 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) 介面 (，或針對在 windows Vista 或更新版本中執行的應用程式使用 [**IWiaTransfer**](-wia-iwiatransfer.md) 介面 () 從映射裝置傳輸影像資料。</span><span class="sxs-lookup"><span data-stu-id="dfd28-105">After an image has been selected, an application uses the [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface (for applications running in Windows XP or earlier) or the [**IWiaTransfer**](-wia-iwiatransfer.md) interface (for applications running in Windows Vista or later) to transfer image data from imaging devices.</span></span> <span data-ttu-id="dfd28-106">如需詳細資訊，請參閱 [wia 1.0 中的傳送影像資料](-wia-transferring-image-data.md) ，或 [傳輸 wia 2.0 中的影像資料](-wia-transferring-image-data-in-wia2.md) 。</span><span class="sxs-lookup"><span data-stu-id="dfd28-106">See either [Transfering Image Data in WIA 1.0](-wia-transferring-image-data.md) or [Transferring Image Data in WIA 2.0](-wia-transferring-image-data-in-wia2.md) for details.</span></span>

<span data-ttu-id="dfd28-107">選取裝置之後，應用程式會使用裝置的 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem)或 [**IWiaItem2**](-wia-iwiaitem2.md)介面的 [**IWiaItem：:D evicedlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg)方法， (根項目) 從指定的 Windows 映像取得 (WIA) 裝置選取影像。</span><span class="sxs-lookup"><span data-stu-id="dfd28-107">After a device has been selected, an application uses the [**IWiaItem::DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) method of the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interface of the device (the root item) to select an image from a specified Windows Image Acquisition (WIA) device.</span></span> <span data-ttu-id="dfd28-108">[**IWiaDevMgr：： GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg)方法會顯示一個對話方塊，讓使用者可以從指定的裝置選取影像，並將影像傳送到使用者所選取的檔案名。</span><span class="sxs-lookup"><span data-stu-id="dfd28-108">The [**IWiaDevMgr::GetImageDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-getimagedlg) method displays a dialog box that allows a user to select an image from a specified device, and transfers the image to a file name selected by the user.</span></span> <span data-ttu-id="dfd28-109">它也可讓使用者在必要時指定裝置。</span><span class="sxs-lookup"><span data-stu-id="dfd28-109">It also allows the user to specify a device if necessary.</span></span> <span data-ttu-id="dfd28-110">如需詳細資訊，請參閱 [選取裝置](-wia-selecting-a-device.md)</span><span class="sxs-lookup"><span data-stu-id="dfd28-110">For more information, see [Selecting a Device](-wia-selecting-a-device.md)</span></span>

<span data-ttu-id="dfd28-111">請注意，使用者不需要使用上述方法來選取影像。</span><span class="sxs-lookup"><span data-stu-id="dfd28-111">Note that it is not necessary for a user to select an image using the above method.</span></span> <span data-ttu-id="dfd28-112">應用程式可以直接從裝置的專案樹狀結構取得影像專案的指標。</span><span class="sxs-lookup"><span data-stu-id="dfd28-112">An application can obtain a pointer to an image item directly from a device's item tree.</span></span> <span data-ttu-id="dfd28-113">如需相關指示，請參閱 [導覽專案樹狀結構](-wia-navigating-an-item-tree.md)。</span><span class="sxs-lookup"><span data-stu-id="dfd28-113">For instructions, see [Navigating an Item Tree](-wia-navigating-an-item-tree.md).</span></span>

<span data-ttu-id="dfd28-114">選取代表所需影像的 WIA 專案之後，在 Windows XP 或更早版本上執行的應用程式會查詢該專案的 [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) 介面，以取得其 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) 介面的指標。</span><span class="sxs-lookup"><span data-stu-id="dfd28-114">Once the WIA item that represents the desired image has been selected, an application running on Windows XP or earlier queries the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface of that item for a pointer to its [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface.</span></span> <span data-ttu-id="dfd28-115">在 Windows Vista 或更新版本上執行的應用程式會查詢其 [**IWiaTransfer**](-wia-iwiatransfer.md)介面指標的 [**IWiaItem2**](-wia-iwiaitem2.md)介面。</span><span class="sxs-lookup"><span data-stu-id="dfd28-115">An application running on Windows Vista or later queries the [**IWiaItem2**](-wia-iwiaitem2.md) interface for a pointer to its [**IWiaTransfer**](-wia-iwiatransfer.md) interface.</span></span>

<span data-ttu-id="dfd28-116">然後，應用程式可以使用 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) (或 [**IWiaTransfer**](-wia-iwiatransfer.md)) 介面的方法，將影像資料傳輸至應用程式。</span><span class="sxs-lookup"><span data-stu-id="dfd28-116">The application can then uses the methods of the [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) (or [**IWiaTransfer**](-wia-iwiatransfer.md)) interface to transfer the image data to the application.</span></span>

<span data-ttu-id="dfd28-117">如果映射裝置是掃描器、 [**IWiaDataTransfer：： idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata)或 [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) 介面的其他方法，則會觸發掃描工作，然後傳送產生的影像資料。</span><span class="sxs-lookup"><span data-stu-id="dfd28-117">If the imaging device is a scanner, [**IWiaDataTransfer::idtGetData**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatatransfer-idtgetdata), or other methods of the [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer) interface, triggers a scan operation, and then transfers the resulting image data.</span></span> <span data-ttu-id="dfd28-118">如果裝置是相機，則影像資料只會從相機傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="dfd28-118">If the device is a camera, the image data is simply transferred from the camera to the application.</span></span>

 

 



