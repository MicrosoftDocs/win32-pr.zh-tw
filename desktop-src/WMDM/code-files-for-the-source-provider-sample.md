---
title: 來源提供者範例的程式碼檔案
description: 來源提供者範例的程式碼檔案
ms.assetid: bd6bfc98-a805-4e04-8a80-7af42ed3dbef
keywords:
- Windows Media 裝置管理員，範例
- 裝置管理員，範例
- Windows Media 裝置管理員、服務提供者範例
- 裝置管理員，服務提供者範例
- 服務提供者，範例
- 範例，服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64b8af4b34310ae183ce55b2e52d3dd346dc6665
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104092275"
---
# <a name="code-files-for-the-source-provider-sample"></a><span data-ttu-id="85e4f-109">來源提供者範例的程式碼檔案</span><span class="sxs-lookup"><span data-stu-id="85e4f-109">Code Files for the Source Provider Sample</span></span>

<span data-ttu-id="85e4f-110">範例來源提供者專案包含下列原始程式碼檔案，其中包含相關聯的標頭：</span><span class="sxs-lookup"><span data-stu-id="85e4f-110">The sample source provider project includes the following source code files, with associated headers:</span></span>



| <span data-ttu-id="85e4f-111">檔案</span><span class="sxs-lookup"><span data-stu-id="85e4f-111">File</span></span>                   | <span data-ttu-id="85e4f-112">描述</span><span class="sxs-lookup"><span data-stu-id="85e4f-112">Description</span></span>                                                                                                                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="85e4f-113">hdsppch .cpp</span><span class="sxs-lookup"><span data-stu-id="85e4f-113">hdsppch.cpp</span></span>            | <span data-ttu-id="85e4f-114">包含標準 ATL 檔案。</span><span class="sxs-lookup"><span data-stu-id="85e4f-114">Includes standard ATL files.</span></span>                                                                                                                                                                                    |
| <span data-ttu-id="85e4f-115">c。</span><span class="sxs-lookup"><span data-stu-id="85e4f-115">key.c</span></span>                  | <span data-ttu-id="85e4f-116">包含虛擬驗證金鑰。</span><span class="sxs-lookup"><span data-stu-id="85e4f-116">Contains a dummy authentication key.</span></span>                                                                                                                                                                            |
| <span data-ttu-id="85e4f-117">loghelp .cpp</span><span class="sxs-lookup"><span data-stu-id="85e4f-117">loghelp.cpp</span></span>            | <span data-ttu-id="85e4f-118">包含使用 **WMDMLogger** 類別記錄活動和錯誤的函式，該類別會在 WMDMLOG.dll 系統檔案中執行。</span><span class="sxs-lookup"><span data-stu-id="85e4f-118">Contains functions that log activity and errors by using the **WMDMLogger** class, which is implemented in the WMDMLOG.dll system file.</span></span>                                                                         |
| <span data-ttu-id="85e4f-119">MDServiceProvider .cpp</span><span class="sxs-lookup"><span data-stu-id="85e4f-119">MDServiceProvider.cpp</span></span>  | <span data-ttu-id="85e4f-120">實 CMDServiceProvider 類別，它會實 [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) 和 IComponentAuthenticate 介面。</span><span class="sxs-lookup"><span data-stu-id="85e4f-120">Implements a class, CMDServiceProvider, that implements the [**IMDServiceProvider**](/windows/desktop/api/mswmdm/nn-mswmdm-imdserviceprovider) and IComponentAuthenticate interfaces.</span></span>                                                             |
| <span data-ttu-id="85e4f-121">mdsp .cpp</span><span class="sxs-lookup"><span data-stu-id="85e4f-121">mdsp.cpp</span></span>               | <span data-ttu-id="85e4f-122">DLL 進入點和註冊碼。</span><span class="sxs-lookup"><span data-stu-id="85e4f-122">DLL entry point and registration code.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="85e4f-123">MDSPDevice .cpp</span><span class="sxs-lookup"><span data-stu-id="85e4f-123">MDSPDevice.cpp</span></span>         | <span data-ttu-id="85e4f-124">實 CMDSPDevice，這個類別會實 [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2)、 [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol)和 **ISpecifyPropertyPages** 介面。</span><span class="sxs-lookup"><span data-stu-id="85e4f-124">Implements a class, CMDSPDevice, that implements the [**IMDSPDevice2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevice2), [**IMDSPDeviceControl**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspdevicecontrol), and **ISpecifyPropertyPages** interfaces.</span></span>                          |
| <span data-ttu-id="85e4f-125">MDSPEnumDevice .cpp</span><span class="sxs-lookup"><span data-stu-id="85e4f-125">MDSPEnumDevice.cpp</span></span>     | <span data-ttu-id="85e4f-126">實 CMDSPEnumDevice，這個類別會實 [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) 介面。</span><span class="sxs-lookup"><span data-stu-id="85e4f-126">Implements a class, CMDSPEnumDevice, that implements the [**IMDSPEnumDevice**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumdevice) interface.</span></span>                                                                                                  |
| <span data-ttu-id="85e4f-127">MDSPEnumStorage .cpp</span><span class="sxs-lookup"><span data-stu-id="85e4f-127">MDSPEnumStorage.cpp</span></span>    | <span data-ttu-id="85e4f-128">實 CMDSPEnumStorage，這個類別會實 [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) 介面。</span><span class="sxs-lookup"><span data-stu-id="85e4f-128">Implements a class, CMDSPEnumStorage, that implements the [**IMDSPEnumStorage**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspenumstorage) interface.</span></span>                                                                                               |
| <span data-ttu-id="85e4f-129">MDSPStorage .cpp</span><span class="sxs-lookup"><span data-stu-id="85e4f-129">MDSPStorage.cpp</span></span>        | <span data-ttu-id="85e4f-130">實 CMDSPStorage，這個類別會實 [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2)、 [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo)和 [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) 介面。</span><span class="sxs-lookup"><span data-stu-id="85e4f-130">Implements a class, CMDSPStorage, that implements the [**IMDSPStorage2**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorage2), [**IMDSPObjectInfo**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobjectinfo), and [**IMDSPObject**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspobject) interfaces.</span></span>                    |
| <span data-ttu-id="85e4f-131">MDSPStorageGlobals .cpp</span><span class="sxs-lookup"><span data-stu-id="85e4f-131">MDSPStorageGlobals.cpp</span></span> | <span data-ttu-id="85e4f-132">實 CMDSPStorageGlobals，這個類別會實 [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) 介面。</span><span class="sxs-lookup"><span data-stu-id="85e4f-132">Implements a class, CMDSPStorageGlobals, that implements the [**IMDSPStorageGlobals**](/windows/desktop/api/mswmdm/nn-mswmdm-imdspstorageglobals) interface.</span></span>                                                                                      |
| <span data-ttu-id="85e4f-133">MDSPutil .cpp</span><span class="sxs-lookup"><span data-stu-id="85e4f-133">MDSPutil.cpp</span></span>           | <span data-ttu-id="85e4f-134">包含各種適用于裝置和檔案管理的公用程式功能。</span><span class="sxs-lookup"><span data-stu-id="85e4f-134">Contains various utility functions for device and file management.</span></span>                                                                                                                                              |
| <span data-ttu-id="85e4f-135">proppage .cpp</span><span class="sxs-lookup"><span data-stu-id="85e4f-135">proppage.cpp</span></span>           | <span data-ttu-id="85e4f-136">會 CPropPage 繼承 ATL 類別的類別，此類別會繼承 ATL 類別 **IPropertyPageImpl** (來執行 IPropertyPage) 和 **CDialogImpl**，這會繼承 atl 類別 CDialogImpl (來管理 windows 和) 的訊息。</span><span class="sxs-lookup"><span data-stu-id="85e4f-136">Implements a class, CPropPage, that inherits the ATL classes **IPropertyPageImpl** (to implement IPropertyPage) and **CDialogImpl**, which inherits the ATL class CDialogImpl (to manage windows and messages).</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="85e4f-137">相關主題</span><span class="sxs-lookup"><span data-stu-id="85e4f-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85e4f-138">**範例服務提供者**</span><span class="sxs-lookup"><span data-stu-id="85e4f-138">**Sample Service Provider**</span></span>](sample-service-provider.md)
</dt> </dl>

 

 




