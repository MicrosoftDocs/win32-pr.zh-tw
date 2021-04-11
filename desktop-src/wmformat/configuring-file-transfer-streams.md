---
title: 設定檔案傳輸資料流程
description: 設定檔案傳輸資料流程
ms.assetid: faed54ae-9e80-492a-9602-e726bdb3b54a
keywords:
- 資料流程，設定檔案傳輸資料流程
- 編解碼器，設定檔案傳輸串流
- 檔案傳輸資料流程
- 資料流程，資料單位延伸
- 編解碼器，資料單位延伸
- 資料單位延伸模組，檔案傳輸資料流程
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fac7d2270da82f1f9e82ed9123611ae608dd3c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023079"
---
# <a name="configuring-file-transfer-streams"></a><span data-ttu-id="185fc-109">設定檔案傳輸資料流程</span><span class="sxs-lookup"><span data-stu-id="185fc-109">Configuring File Transfer Streams</span></span>

<span data-ttu-id="185fc-110">在 [**WM \_ 媒體 \_ 類型**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) 結構中，檔案傳輸資料流程不需要任何特殊設定。</span><span class="sxs-lookup"><span data-stu-id="185fc-110">File transfer streams do not require any special settings in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="185fc-111">它們需要資料單位延伸模組，才能將檔案名與每個範例產生關聯。</span><span class="sxs-lookup"><span data-stu-id="185fc-111">They do require a data unit extension to associate a file name with each sample.</span></span> <span data-ttu-id="185fc-112">若要使用檔案傳輸範例來傳送名稱，您必須為數據流執行資料單位延伸系統。</span><span class="sxs-lookup"><span data-stu-id="185fc-112">To send a name with file transfer samples, you must implement a data unit extension system for the stream.</span></span>

<span data-ttu-id="185fc-113">若要設定資料流程的資料單位延伸，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="185fc-113">To set a data unit extension for the stream, perform the following steps:</span></span>

1.  <span data-ttu-id="185fc-114">藉由呼叫 **IWMStreamConfig：： QueryInterface**，取得資料流程設定物件之 [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2)介面的指標。</span><span class="sxs-lookup"><span data-stu-id="185fc-114">Obtain a pointer to the [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
2.  <span data-ttu-id="185fc-115">藉由呼叫 [**IWMStreamConfig2：： AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) 來新增資料流程的資料單位延伸，如下所示：</span><span class="sxs-lookup"><span data-stu-id="185fc-115">Add a data unit extension for the stream by calling [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) as follows:</span></span>
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="185fc-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="185fc-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="185fc-117">**所有資料流程通用的設定**</span><span class="sxs-lookup"><span data-stu-id="185fc-117">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="185fc-118">**設定任意資料流程類型**</span><span class="sxs-lookup"><span data-stu-id="185fc-118">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="185fc-119">**檔案資料流程**</span><span class="sxs-lookup"><span data-stu-id="185fc-119">**File Streams**</span></span>](file-streams.md)
</dt> </dl>

 

 




