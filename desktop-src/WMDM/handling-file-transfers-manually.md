---
title: 手動處理檔案傳輸
description: 手動處理檔案傳輸
ms.assetid: ff94191b-a0f2-4118-996c-d040f214fb9b
keywords:
- Windows Media 裝置管理員，手動檔案傳輸
- 裝置管理員，手動檔案傳輸
- 程式設計指南，手動檔案傳輸
- 桌面應用程式，手動檔案傳輸
- 建立 Windows Media 裝置管理員應用程式，手動檔案傳輸
- 手動檔案傳輸
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2bf12404e8cd83b6f0c0e4f1c8ec8b0b7bda205
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103682767"
---
# <a name="handling-file-transfers-manually"></a><span data-ttu-id="5dc9c-109">手動處理檔案傳輸</span><span class="sxs-lookup"><span data-stu-id="5dc9c-109">Handling File Transfers Manually</span></span>

<span data-ttu-id="5dc9c-110">您的應用程式可以執行 [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) 介面，以管理部分的讀取或寫入處理常式。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-110">Your application can implement the [**IWMDMOperation**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmoperation) interface to manage part of the reading or writing process.</span></span> <span data-ttu-id="5dc9c-111">在讀取裝置時，此實行可讓應用程式接收來自裝置檔案的原始資料區塊。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-111">On a read from device, the implementation enables the application to receive blocks of raw data from a device file.</span></span> <span data-ttu-id="5dc9c-112">在寫入裝置時，它會讓應用程式將原始資料的區區塊轉送到裝置上的檔案。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-112">On a write to device, it enables the application to send blocks of raw data to a file on the device.</span></span>

<span data-ttu-id="5dc9c-113">在讀取和寫入作業中， [**IWMDMOperation：： TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) 方法會在電腦與裝置之間傳遞資料。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-113">In both read and write operations, the [**IWMDMOperation::TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) method passes the data between the computer and the device.</span></span> <span data-ttu-id="5dc9c-114">若要知道資料傳輸的方向，當 Windows Media 裝置管理員呼叫 [**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) 或 [**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite)時，您的應用程式必須設定旗標。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-114">To know the direction of the data transfer, your application must set a flag when Windows Media Device Manager calls [**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) or [**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite).</span></span> <span data-ttu-id="5dc9c-115">當呼叫 [**End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) 方法時，應用程式應該重設此旗標。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-115">When the [**End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) method is called, the application should reset this flag.</span></span>

> [!Note]  
> <span data-ttu-id="5dc9c-116">如果服務提供者和裝置正確地執行 [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2)，它會先呼叫應用程式的 [IWMDMOperation3：： TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel) 方法（如果已執行）。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-116">If the service provider and device properly implement [**IMDSPObject2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject2), it will first call the application's [IWMDMOperation3::TransferObjectDataOnClearChannel](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation3-transferobjectdataonclearchannel) method, if implemented.</span></span> <span data-ttu-id="5dc9c-117">此方法是傳輸資料的更有效率方式。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-117">This method is a more efficient way of transferring data.</span></span> <span data-ttu-id="5dc9c-118">**TransferObjectDataOnClearChannel** 的處理方式與 **TransferObjectData** 相同，不同之處在于資料永遠不會加密，而且不會有 MAC 值可進行驗證。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-118">**TransferObjectDataOnClearChannel** is handled the same way as **TransferObjectData**, except that the data is never encrypted and has no MAC values to verify.</span></span>

 

<span data-ttu-id="5dc9c-119">下列各節描述當您的應用程式執行 **IWMDMOperation** 時的讀取和寫入程式。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-119">The following sections describe both the reading and the writing process, when your application implements **IWMDMOperation**.</span></span>

<span data-ttu-id="5dc9c-120">**從裝置讀取**</span><span class="sxs-lookup"><span data-stu-id="5dc9c-120">**Reading from a device**</span></span>

<span data-ttu-id="5dc9c-121">從裝置讀取檔案時，Windows Media 裝置管理員會依序呼叫下列 **IWMDMOperation** 方法：</span><span class="sxs-lookup"><span data-stu-id="5dc9c-121">When reading a file from a device, Windows Media Device Manager calls the following **IWMDMOperation** methods in order:</span></span>

-   <span data-ttu-id="5dc9c-122">[**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) 呼叫以通知應用程式正在開始讀取裝置。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-122">[**BeginRead**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginread) Called to notify the application that a read from device is beginning.</span></span>
-   <span data-ttu-id="5dc9c-123">[**TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) 呼叫一次或多次。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-123">[**TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) Called one or more times.</span></span> <span data-ttu-id="5dc9c-124">下列步驟說明資料的處理方式：</span><span class="sxs-lookup"><span data-stu-id="5dc9c-124">The processing of data is described in the following steps:</span></span>
    1.  <span data-ttu-id="5dc9c-125">**TransferObjectData** 會接收大小 *pdwSize* 位元組的緩衝區 *.pdata*、填入資料，以及使用 MAC 來確認傳入的資料。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-125">**TransferObjectData** receives a buffer, *pData*, of size *pdwSize* bytes, filled with data, and a MAC to verify the incoming data.</span></span>
    2.  <span data-ttu-id="5dc9c-126">應用程式會使用傳入的資料 MAC 來驗證傳入的參數。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-126">The application verifies the incoming parameters with the incoming data MAC.</span></span>
    3.  <span data-ttu-id="5dc9c-127">應用程式會盡可能解密和讀取 *.pdata* 中的資料量，並修改 *pdwSize* 的傳回值，以指出實際讀取的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-127">The application decrypts and reads as much of the data in *pData* as it can, and modifies the returned value of *pdwSize* to indicate how many bytes were actually read.</span></span>
    4.  <span data-ttu-id="5dc9c-128">應用程式會使用 [**CSecureChannelClient：:D ecryptparam**](/previous-versions/bb231586(v=vs.85))來解密資料，並視需要加以儲存或使用。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-128">The application decrypts the data, using [**CSecureChannelClient::DecryptParam**](/previous-versions/bb231586(v=vs.85)), and stores it or uses it, as needed.</span></span>
    5.  <span data-ttu-id="5dc9c-129">**TransferObjectData** 傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-129">**TransferObjectData** returns S\_OK.</span></span>
    6.  <span data-ttu-id="5dc9c-130">Windows Media 裝置管理員會繼續呼叫 **TransferObjectData** ，直到應用程式讀取檔案中的所有資料，或應用程式傳回 WMDM \_ E \_ 使用者取消 \_ 以取消作業 (在這種情況下，讀取會取消，而 Windows Media 裝置管理員會呼叫 **End**) 。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-130">Windows Media Device Manager continues to call **TransferObjectData** until the application has read all the data from the file, or the application returns WMDM\_E\_USER\_CANCELLED to cancel the operation (in which case the read is canceled, and Windows Media Device Manager calls **End**).</span></span>
-   <span data-ttu-id="5dc9c-131">[**結束**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) 呼叫以通知應用程式，讀取裝置已結束。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-131">[**End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) Called to notify the application that a read from device is ending.</span></span>

<span data-ttu-id="5dc9c-132">**寫入至裝置**</span><span class="sxs-lookup"><span data-stu-id="5dc9c-132">**Writing to a device**</span></span>

<span data-ttu-id="5dc9c-133">將檔案寫入裝置時，Windows Media 裝置管理員會依序呼叫下列 **IWMDMOperation** 方法：</span><span class="sxs-lookup"><span data-stu-id="5dc9c-133">When writing a file to the device, Windows Media Device Manager calls the following **IWMDMOperation** methods in order:</span></span>

-   <span data-ttu-id="5dc9c-134">[**GetObjectName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectname) 呼叫以允許應用程式指定新儲存體的名稱。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-134">[**GetObjectName**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectname) Called to allow the application to specify a name for the new storage.</span></span> <span data-ttu-id="5dc9c-135">只有當應用程式未在 **Insert** 方法中指定名稱時，才會呼叫這個方法。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-135">This method is only called if the application did not specify a name in the **Insert** method.</span></span>
-   <span data-ttu-id="5dc9c-136">[**GetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes) 呼叫以允許應用程式在裝置上指定新儲存體的屬性。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-136">[**GetObjectAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjectattributes) Called to allow the application to specify attributes for the new storage on the device.</span></span>
-   <span data-ttu-id="5dc9c-137">[**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite) 呼叫以通知裝置的寫入即將開始。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-137">[**BeginWrite**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-beginwrite) Called to notify that that a write to device is beginning.</span></span>
-   <span data-ttu-id="5dc9c-138">[**GetObjectTotalSize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjecttotalsize) 呼叫以抓取要寫入至裝置的物件大小總計，以啟用傳輸的優化，以及提供 Windows Media 裝置管理員有機會在檔案對裝置而言太大時，取消傳輸。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-138">[**GetObjectTotalSize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-getobjecttotalsize) Called to retrieve the total size of the object being written to the device, to enable optimization of the transfer, and also to give Windows Media Device Manager an opportunity to cancel the transfer if the file is too large for the device.</span></span>
-   <span data-ttu-id="5dc9c-139">[**TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) 呼叫一次或多次。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-139">[**TransferObjectData**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-transferobjectdata) Called one or more times.</span></span> <span data-ttu-id="5dc9c-140">下列步驟說明資料的處理方式：</span><span class="sxs-lookup"><span data-stu-id="5dc9c-140">The processing of data is described in the following steps:</span></span>
    1.  <span data-ttu-id="5dc9c-141">**TransferObjectData** 會接收大小 *pdwSize* 位元組緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-141">**TransferObjectData** receives a pointer to a buffer of size *pdwSize* bytes.</span></span>
    2.  <span data-ttu-id="5dc9c-142">應用程式會取得要傳送至裝置的資料區塊，通常是從檔案讀取資料，並以最多 *pdwSize* 的位元組填滿接收的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-142">The application gets a block of data to send to the device, usually by reading data from a file, and fills the received buffer with up to *pdwSize* bytes.</span></span> <span data-ttu-id="5dc9c-143">如果有需要，它應該修改 *pdwSize* (，) 以反映已新增至緩衝區的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-143">It should modify *pdwSize* (if necessary) to reflect how many bytes were added to the buffer.</span></span>
    3.  <span data-ttu-id="5dc9c-144">應用程式會建立所有方法參數的 MAC。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-144">The application creates a MAC of all the method parameters.</span></span>
    4.  <span data-ttu-id="5dc9c-145">應用程式會使用 [**CSecureChannelClient：： EncryptParam**](/previous-versions/bb231587(v=vs.85))來加密緩衝區中的資料。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-145">The application encrypts the data in the buffer, using [**CSecureChannelClient::EncryptParam**](/previous-versions/bb231587(v=vs.85)).</span></span>
    5.  <span data-ttu-id="5dc9c-146">**TransferObjectData** 會傳回 \_ [確定] 以表示有更多資料，或 \_ 指定 FALSE 表示沒有其他資料。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-146">**TransferObjectData** returns S\_OK to indicate that there is more data, or S\_FALSE to indicate that there is no more data.</span></span> <span data-ttu-id="5dc9c-147">如果應用程式傳回 WMDM \_ E \_ 使用者已 \_ 取消，則會取消寫入作業，而且 Windows Media 裝置管理員會呼叫 **End**。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-147">If the application returns WMDM\_E\_USER\_CANCELLED, the write operation is canceled and Windows Media Device Manager will call **End**.</span></span>
    6.  <span data-ttu-id="5dc9c-148">只要應用程式傳回 [確定]，Windows Media 裝置管理員就會繼續呼叫 **TransferObjectData** \_ 。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-148">Windows Media Device Manager continues to call **TransferObjectData** as long as the application returns S\_OK.</span></span>
-   <span data-ttu-id="5dc9c-149">[**結束**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) 呼叫以通知裝置寫入正在結束。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-149">[**End**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmoperation-end) Called to notify that a write to device is ending.</span></span>

<span data-ttu-id="5dc9c-150">如需程式碼範例，請參閱 [加密和解密](encryption-and-decryption.md)。</span><span class="sxs-lookup"><span data-stu-id="5dc9c-150">For a code example, see [Encryption and Decryption](encryption-and-decryption.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="5dc9c-151">相關主題</span><span class="sxs-lookup"><span data-stu-id="5dc9c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5dc9c-152">**建立 Windows Media 裝置管理員應用程式**</span><span class="sxs-lookup"><span data-stu-id="5dc9c-152">**Creating a Windows Media Device Manager Application**</span></span>](creating-a-windows-media-device-manager-application.md)
</dt> </dl>

 

 