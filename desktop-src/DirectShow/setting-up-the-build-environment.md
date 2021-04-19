---
description: 打造 DirectShow 應用程式
ms.assetid: 2fbdbe49-0d4d-4dce-afc3-7049c793ace0
title: 打造 DirectShow 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56c6ab8a0731e93eece734abd4380b092414ff5f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972296"
---
# <a name="building-directshow-applications"></a><span data-ttu-id="9ad3d-103">打造 DirectShow 應用程式</span><span class="sxs-lookup"><span data-stu-id="9ad3d-103">Building DirectShow Applications</span></span>

<span data-ttu-id="9ad3d-104">本主題說明建立 DirectShow 應用程式所需的標頭和程式庫。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-104">This topic describes the headers and libraries needed to build DirectShow applications.</span></span>

<span data-ttu-id="9ad3d-105">[Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx)中提供最新的 DirectShow 標頭和程式庫。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-105">The latest DirectShow headers and libraries are available in the [Windows SDK](https://msdn.microsoft.com/windows/aa904949.aspx).</span></span>

## <a name="header-files"></a><span data-ttu-id="9ad3d-106">標頭檔</span><span class="sxs-lookup"><span data-stu-id="9ad3d-106">Header Files</span></span>

<span data-ttu-id="9ad3d-107">所有的 DirectShow 應用程式都會使用下表所示的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-107">All DirectShow applications use the header file shown in the following table.</span></span>



| <span data-ttu-id="9ad3d-108">標頭檔案</span><span class="sxs-lookup"><span data-stu-id="9ad3d-108">Header File</span></span> | <span data-ttu-id="9ad3d-109">需要</span><span class="sxs-lookup"><span data-stu-id="9ad3d-109">Required For</span></span>                 |
|-------------|------------------------------|
| <span data-ttu-id="9ad3d-110">Dshow。h</span><span class="sxs-lookup"><span data-stu-id="9ad3d-110">Dshow.h</span></span>     | <span data-ttu-id="9ad3d-111">所有的 DirectShow 應用程式。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-111">All DirectShow applications.</span></span> |



 

<span data-ttu-id="9ad3d-112">某些 DirectShow 介面需要額外的標頭檔。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-112">Some DirectShow interfaces require additional header files.</span></span> <span data-ttu-id="9ad3d-113">這些需求會在介面參考中注明。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-113">These requirements are noted in the interface reference.</span></span>

## <a name="library-files"></a><span data-ttu-id="9ad3d-114">程式庫檔案</span><span class="sxs-lookup"><span data-stu-id="9ad3d-114">Library Files</span></span>

<span data-ttu-id="9ad3d-115">DirectShow 使用下表所示的靜態程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-115">DirectShow uses the static library files shown in the following table.</span></span>



| <span data-ttu-id="9ad3d-116">程式庫檔案</span><span class="sxs-lookup"><span data-stu-id="9ad3d-116">Library File</span></span> | <span data-ttu-id="9ad3d-117">Description</span><span class="sxs-lookup"><span data-stu-id="9ad3d-117">Description</span></span>                                                                                                                    |
|--------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9ad3d-118">Strmiids .lib</span><span class="sxs-lookup"><span data-stu-id="9ad3d-118">Strmiids.lib</span></span> | <span data-ttu-id="9ad3d-119"> (Clsid) 和介面識別碼匯出類別識別碼 (Iid) 。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-119">Exports class identifiers (CLSIDs) and interface identifiers (IIDs).</span></span>                                                           |
| <span data-ttu-id="9ad3d-120">Quartz .lib</span><span class="sxs-lookup"><span data-stu-id="9ad3d-120">Quartz.lib</span></span>   | <span data-ttu-id="9ad3d-121">匯出 [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) 函數。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-121">Exports the [**AMGetErrorText**](/windows/win32/api/errors/nf-errors-amgeterrortexta) function.</span></span> <span data-ttu-id="9ad3d-122">如果您未呼叫此函式，則不需要此程式庫。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-122">If you do not call this function, this library is not required.</span></span> |



 

<span data-ttu-id="9ad3d-123">針對 debug 和 release 組建使用相同的 .lib 檔案。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-123">Use the same .lib files for debug and release builds.</span></span>

## <a name="filter-base-classes"></a><span data-ttu-id="9ad3d-124">篩選基類</span><span class="sxs-lookup"><span data-stu-id="9ad3d-124">Filter Base Classes</span></span>

<span data-ttu-id="9ad3d-125">Windows SDK 提供一組 c + + 類別，如果您要撰寫自訂的 DirectShow 篩選器，則建議使用這組類別。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-125">The Windows SDK provides a set of C++ classes that are recommended if you are writing a custom DirectShow filter.</span></span> <span data-ttu-id="9ad3d-126">這些類別會以範例程式碼的形式提供，您可以將其編譯成靜態程式庫。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-126">These classes are provided as sample code, which you can compile to a static library.</span></span> <span data-ttu-id="9ad3d-127">如需詳細資訊，請參閱 [DirectShow 基類](directshow-base-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-127">For more information, see [DirectShow Base Classes](directshow-base-classes.md).</span></span>

## <a name="redistributable-dlls"></a><span data-ttu-id="9ad3d-128">可轉散發 Dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-128">Redistributable DLLs</span></span>

<span data-ttu-id="9ad3d-129">針對 Windows XP Service Pack 2 (SP2) 和更新版本所撰寫的 DirectShow 應用程式不需要轉散發任何 DirectShow Dll。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-129">DirectShow applications written for Windows XP with Service Pack 2 (SP2) and later do not need to redistribute any DirectShow DLLs.</span></span>

<span data-ttu-id="9ad3d-130">若為 Windows XP Service Pack 1 (SP1) 及更早版本，可從 Microsoft DirectX SDK 取得可轉散發的 DirectShow Dll。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-130">For Windows XP with Service Pack 1 (SP1) and earlier, redistributable DirectShow DLLs are available from the Microsoft DirectX SDK.</span></span> <span data-ttu-id="9ad3d-131">這些 Dll 的最新版本是9.0 版 c。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-131">The latest version of these DLLs is version 9.0c.</span></span> <span data-ttu-id="9ad3d-132">不打算進一步開發這些可轉散發 Dll。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-132">No further development of these redistributable DLLs is planned.</span></span> <span data-ttu-id="9ad3d-133">Windows XP Service Pack 2 (SP2) 包含9.0 版的 c Dll。</span><span class="sxs-lookup"><span data-stu-id="9ad3d-133">Windows XP with Service Pack 2 (SP2) contains the version 9.0c DLLs.</span></span>

<span data-ttu-id="9ad3d-134">Redstributable 套件包含下列 Dll：</span><span class="sxs-lookup"><span data-stu-id="9ad3d-134">The redstributable packages contain the following DLLs:</span></span>

-   <span data-ttu-id="9ad3d-135">dxnt.cab</span><span class="sxs-lookup"><span data-stu-id="9ad3d-135">dxnt.cab</span></span>
    -   <span data-ttu-id="9ad3d-136">amstream.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-136">amstream.dll</span></span>
    -   <span data-ttu-id="9ad3d-137">devenum.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-137">devenum.dll</span></span>
    -   <span data-ttu-id="9ad3d-138">encapi.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-138">encapi.dll</span></span>
    -   <span data-ttu-id="9ad3d-139">ks.sys</span><span class="sxs-lookup"><span data-stu-id="9ad3d-139">ks.sys</span></span>
    -   <span data-ttu-id="9ad3d-140">ksolay.ax</span><span class="sxs-lookup"><span data-stu-id="9ad3d-140">ksolay.ax</span></span>
    -   <span data-ttu-id="9ad3d-141">ksproxy.ax</span><span class="sxs-lookup"><span data-stu-id="9ad3d-141">ksproxy.ax</span></span>
    -   <span data-ttu-id="9ad3d-142">ksuser.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-142">ksuser.dll</span></span>
    -   <span data-ttu-id="9ad3d-143">l3codecx.ax</span><span class="sxs-lookup"><span data-stu-id="9ad3d-143">l3codecx.ax</span></span>
    -   <span data-ttu-id="9ad3d-144">mciqtz32.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-144">mciqtz32.dll</span></span>
    -   <span data-ttu-id="9ad3d-145">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="9ad3d-145">mpg2splt.ax</span></span>
    -   <span data-ttu-id="9ad3d-146">msdmo.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-146">msdmo.dll</span></span>
    -   <span data-ttu-id="9ad3d-147">mskssrv.sys</span><span class="sxs-lookup"><span data-stu-id="9ad3d-147">mskssrv.sys</span></span>
    -   <span data-ttu-id="9ad3d-148">mspclock.sys</span><span class="sxs-lookup"><span data-stu-id="9ad3d-148">mspclock.sys</span></span>
    -   <span data-ttu-id="9ad3d-149">mspqm.sys</span><span class="sxs-lookup"><span data-stu-id="9ad3d-149">mspqm.sys</span></span>
    -   <span data-ttu-id="9ad3d-150">mstee.sys</span><span class="sxs-lookup"><span data-stu-id="9ad3d-150">mstee.sys</span></span>
    -   <span data-ttu-id="9ad3d-151">mswebdvd.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-151">mswebdvd.dll</span></span>
    -   <span data-ttu-id="9ad3d-152">qasf.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-152">qasf.dll</span></span>
    -   <span data-ttu-id="9ad3d-153">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-153">qcap.dll</span></span>
    -   <span data-ttu-id="9ad3d-154">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-154">qdv.dll</span></span>
    -   <span data-ttu-id="9ad3d-155">qdvd.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-155">qdvd.dll</span></span>
    -   <span data-ttu-id="9ad3d-156">qedit.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-156">qedit.dll</span></span>
    -   <span data-ttu-id="9ad3d-157">qedwipes.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-157">qedwipes.dll</span></span>
    -   <span data-ttu-id="9ad3d-158">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-158">quartz.dll</span></span>
    -   <span data-ttu-id="9ad3d-159">stream.sys</span><span class="sxs-lookup"><span data-stu-id="9ad3d-159">stream.sys</span></span>
    -   <span data-ttu-id="9ad3d-160">swenum.sys</span><span class="sxs-lookup"><span data-stu-id="9ad3d-160">swenum.sys</span></span>
-   <span data-ttu-id="9ad3d-161">bda.cab</span><span class="sxs-lookup"><span data-stu-id="9ad3d-161">bda.cab</span></span>
    -   <span data-ttu-id="9ad3d-162">bdaplgin.ax</span><span class="sxs-lookup"><span data-stu-id="9ad3d-162">bdaplgin.ax</span></span>
    -   <span data-ttu-id="9ad3d-163">bdasup.sys</span><span class="sxs-lookup"><span data-stu-id="9ad3d-163">bdasup.sys</span></span>
    -   <span data-ttu-id="9ad3d-164">ccdecode.sys</span><span class="sxs-lookup"><span data-stu-id="9ad3d-164">ccdecode.sys</span></span>
    -   <span data-ttu-id="9ad3d-165">ipsink.ax</span><span class="sxs-lookup"><span data-stu-id="9ad3d-165">ipsink.ax</span></span>
    -   <span data-ttu-id="9ad3d-166">kstvtune.ax</span><span class="sxs-lookup"><span data-stu-id="9ad3d-166">kstvtune.ax</span></span>
    -   <span data-ttu-id="9ad3d-167">kswdmcap.ax</span><span class="sxs-lookup"><span data-stu-id="9ad3d-167">kswdmcap.ax</span></span>
    -   <span data-ttu-id="9ad3d-168">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="9ad3d-168">ksxbar.ax</span></span>
    -   <span data-ttu-id="9ad3d-169">mpe.sys</span><span class="sxs-lookup"><span data-stu-id="9ad3d-169">mpe.sys</span></span>
    -   <span data-ttu-id="9ad3d-170">mpeg2data.ax</span><span class="sxs-lookup"><span data-stu-id="9ad3d-170">mpeg2data.ax</span></span>
    -   <span data-ttu-id="9ad3d-171">msdv.sys</span><span class="sxs-lookup"><span data-stu-id="9ad3d-171">msdv.sys</span></span>
    -   <span data-ttu-id="9ad3d-172">msdvbnp.ax</span><span class="sxs-lookup"><span data-stu-id="9ad3d-172">msdvbnp.ax</span></span>
    -   <span data-ttu-id="9ad3d-173">msvidctl.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-173">msvidctl.dll</span></span>
    -   <span data-ttu-id="9ad3d-174">msyuv.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-174">msyuv.dll</span></span>
    -   <span data-ttu-id="9ad3d-175">nabtsfec.sys</span><span class="sxs-lookup"><span data-stu-id="9ad3d-175">nabtsfec.sys</span></span>
    -   <span data-ttu-id="9ad3d-176">ndisip.sys</span><span class="sxs-lookup"><span data-stu-id="9ad3d-176">ndisip.sys</span></span>
    -   <span data-ttu-id="9ad3d-177">psisdecd.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-177">psisdecd.dll</span></span>
    -   <span data-ttu-id="9ad3d-178">psisrndr.ax</span><span class="sxs-lookup"><span data-stu-id="9ad3d-178">psisrndr.ax</span></span>
    -   <span data-ttu-id="9ad3d-179">slip.sys</span><span class="sxs-lookup"><span data-stu-id="9ad3d-179">slip.sys</span></span>
    -   <span data-ttu-id="9ad3d-180">streamip.sys</span><span class="sxs-lookup"><span data-stu-id="9ad3d-180">streamip.sys</span></span>
    -   <span data-ttu-id="9ad3d-181">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="9ad3d-181">vbisurf.ax</span></span>
    -   <span data-ttu-id="9ad3d-182">wstcodec.sys</span><span class="sxs-lookup"><span data-stu-id="9ad3d-182">wstcodec.sys</span></span>
    -   <span data-ttu-id="9ad3d-183">wstdecod.dll</span><span class="sxs-lookup"><span data-stu-id="9ad3d-183">wstdecod.dll</span></span>

## <a name="related-topics"></a><span data-ttu-id="9ad3d-184">相關主題</span><span class="sxs-lookup"><span data-stu-id="9ad3d-184">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9ad3d-185">建立 DirectShow 篩選器</span><span class="sxs-lookup"><span data-stu-id="9ad3d-185">Building DirectShow Filters</span></span>](building-directshow-filters.md)
</dt> </dl>

 

 
