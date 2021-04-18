---
title: Windows 封裝管理員 COM API
description: 適用于 Windows 10，並在行動裝置系列中實行。 如需 Windows 封裝管理員的詳細資訊，請與您的 Microsoft 帳戶小組代表合作。
ms.assetid: 4863EC42-413D-46E3-AE61-E29006708E39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82de491b2ceb7da7029a8db7fdf3e436a92d50a5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106976316"
---
# <a name="windows-package-manager-com-api"></a><span data-ttu-id="9b5e3-104">Windows 封裝管理員 COM API</span><span class="sxs-lookup"><span data-stu-id="9b5e3-104">Windows Package Manager COM API</span></span>

<span data-ttu-id="9b5e3-105">適用于 Windows 10，並在行動裝置系列中實行。</span><span class="sxs-lookup"><span data-stu-id="9b5e3-105">Applies to Windows 10, and implemented in the mobile device family.</span></span> <span data-ttu-id="9b5e3-106">如需 Windows 封裝管理員的詳細資訊，請與您的 Microsoft 帳戶小組代表合作。</span><span class="sxs-lookup"><span data-stu-id="9b5e3-106">For more information about Windows Package Manager, please work with your Microsoft Account Team representative.</span></span>

> [!Note]
>
> <span data-ttu-id="9b5e3-107">所有 Windows 應用程式都無法使用此 API。</span><span class="sxs-lookup"><span data-stu-id="9b5e3-107">This API is not available to all Windows apps.</span></span> <span data-ttu-id="9b5e3-108">除非您的開發人員帳戶是由 Microsoft 特別布建，否則這些 Api 的呼叫將會在執行時間失敗。</span><span class="sxs-lookup"><span data-stu-id="9b5e3-108">Unless your developer account is specially provisioned by Microsoft, calls to these APIs will fail at runtime.</span></span>

 

<span data-ttu-id="9b5e3-109">API 包含下列 coclass。</span><span class="sxs-lookup"><span data-stu-id="9b5e3-109">The API consists of the following coclass.</span></span>

-   <span data-ttu-id="9b5e3-110">PMSvc.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-110">PMSvc.</span></span> <span data-ttu-id="9b5e3-111">CLSID： {B9E511FC-E364-497A-A1-21-B7-B3-61-2C-ED-CE}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-111">CLSID: {B9E511FC-E364-497A-A1-21-B7-B3-61-2C-ED-CE}</span></span>

<span data-ttu-id="9b5e3-112">PMSvc 會執行下列介面。</span><span class="sxs-lookup"><span data-stu-id="9b5e3-112">PMSvc implements the following interfaces.</span></span>

-   <span data-ttu-id="9b5e3-113">IPMApplicationInfo.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-113">IPMApplicationInfo.</span></span> <span data-ttu-id="9b5e3-114">IID： {50AFB58A-438C-4088-97-89-F8-C4-89-98-29-C7}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-114">IID: {50AFB58A-438C-4088-97-89-F8-C4-89-98-29-C7}</span></span>
-   <span data-ttu-id="9b5e3-115">IPMTilePropertyInfo.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-115">IPMTilePropertyInfo.</span></span> <span data-ttu-id="9b5e3-116">IID： {6C2B8017-1EFA-42a7-86-C0-6D-4B-64-0B-F5-28}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-116">IID: {6C2B8017-1EFA-42a7-86-C0-6D-4B-64-0B-F5-28}</span></span>
-   <span data-ttu-id="9b5e3-117">IPMTilePropertyEnumerator.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-117">IPMTilePropertyEnumerator.</span></span> <span data-ttu-id="9b5e3-118">IID： {CC4CD629-9047-4250-AA-C8-93-0E-47-81-24-21}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-118">IID: {CC4CD629-9047-4250-AA-C8-93-0E-47-81-24-21}</span></span>
-   <span data-ttu-id="9b5e3-119">IPMTileInfo.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-119">IPMTileInfo.</span></span> <span data-ttu-id="9b5e3-120">IID： {D1604833-2B08-4001-82-CD-18-3A-D7-34-F7-52}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-120">IID: {D1604833-2B08-4001-82-CD-18-3A-D7-34-F7-52}</span></span>
-   <span data-ttu-id="9b5e3-121">IPMTileInfoEnumerator.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-121">IPMTileInfoEnumerator.</span></span> <span data-ttu-id="9b5e3-122">IID： {DED83065-E462-4b2c-AC-B5-E3-9C-EA-61-C8-74}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-122">IID: {DED83065-E462-4b2c-AC-B5-E3-9C-EA-61-C8-74}</span></span>
-   <span data-ttu-id="9b5e3-123">IPMApplicationInfoEnumerator.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-123">IPMApplicationInfoEnumerator.</span></span> <span data-ttu-id="9b5e3-124">IID： {0EC42A96-4D46-4dc6-A3-D9-A7-AC-AA-C0-F5-FA}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-124">IID: {0EC42A96-4D46-4dc6-A3-D9-A7-AC-AA-C0-F5-FA}</span></span>
-   <span data-ttu-id="9b5e3-125">IPMLiveTileJobInfo.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-125">IPMLiveTileJobInfo.</span></span> <span data-ttu-id="9b5e3-126">IID： {6009A81F-4710-4697-B5-F6-22-08-F6-05-7B-8E}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-126">IID: {6009A81F-4710-4697-B5-F6-22-08-F6-05-7B-8E}</span></span>
-   <span data-ttu-id="9b5e3-127">IPMLiveTileJobInfoEnumerator.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-127">IPMLiveTileJobInfoEnumerator.</span></span> <span data-ttu-id="9b5e3-128">IID： {BC042582-9415-4f36-9F-99-06-F1-04-C0-7C-03}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-128">IID: {BC042582-9415-4f36-9F-99-06-F1-04-C0-7C-03}</span></span>
-   <span data-ttu-id="9b5e3-129">IPMDeploymentManager.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-129">IPMDeploymentManager.</span></span> <span data-ttu-id="9b5e3-130">IID： {35F785FA-1979 年-4A8B-BC-8F-FD-70-EB-0D-15-44}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-130">IID: {35F785FA-1979-4A8B-BC-8F-FD-70-EB-0D-15-44}</span></span>
-   <span data-ttu-id="9b5e3-131">IPMEnumerationManager.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-131">IPMEnumerationManager.</span></span> <span data-ttu-id="9b5e3-132">IID： {698D57C2-292D-4CF3-B7-3C-D9-5A-69-22-ED-9A}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-132">IID: {698D57C2-292D-4CF3-B7-3C-D9-5A-69-22-ED-9A}</span></span>
-   <span data-ttu-id="9b5e3-133">IPMTaskInfo.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-133">IPMTaskInfo.</span></span> <span data-ttu-id="9b5e3-134">IID： {BF1D8C33-1BF5-4ee0-B5-49-6B-9D-D3-83-49-42}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-134">IID: {BF1D8C33-1BF5-4ee0-B5-49-6B-9D-D3-83-49-42}</span></span>
-   <span data-ttu-id="9b5e3-135">IPMTaskInfoEnumerator.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-135">IPMTaskInfoEnumerator.</span></span> <span data-ttu-id="9b5e3-136">IID： {0630B0F8-0BBC-4821-A-74-C7-99-51-66-ED-2A}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-136">IID: {0630B0F8-0BBC-4821-BE-74-C7-99-51-66-ED-2A}</span></span>
-   <span data-ttu-id="9b5e3-137">IPMExtensionInfo.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-137">IPMExtensionInfo.</span></span> <span data-ttu-id="9b5e3-138">IID： {49ACDE79-9788-4d0a-8A-A0-17-46-AF-DB-9E-9D}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-138">IID: {49ACDE79-9788-4d0a-8A-A0-17-46-AF-DB-9E-9D}</span></span>
-   <span data-ttu-id="9b5e3-139">IPMExtensionFileExtensionInfo.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-139">IPMExtensionFileExtensionInfo.</span></span> <span data-ttu-id="9b5e3-140">IID： {6B87CB6C-0B88-4989-A4-EC-03-37-14-F7-10-D4}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-140">IID: {6B87CB6C-0B88-4989-A4-EC-03-37-14-F7-10-D4}</span></span>
-   <span data-ttu-id="9b5e3-141">IPMExtensionProtocolInfo.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-141">IPMExtensionProtocolInfo.</span></span> <span data-ttu-id="9b5e3-142">IID： {1E3FA036-51EB-4453-BA-FF-B8-D8-E4-B4-6C-8E}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-142">IID: {1E3FA036-51EB-4453-BA-FF-B8-D8-E4-B4-6C-8E}</span></span>
-   <span data-ttu-id="9b5e3-143">IPMExtensionShareTargetInfo.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-143">IPMExtensionShareTargetInfo.</span></span> <span data-ttu-id="9b5e3-144">IID： {5471F48B-C65C-4656-8C-70-24-2E-31-19-5F-EA}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-144">IID: {5471F48B-C65C-4656-8C-70-24-2E-31-19-5F-EA}</span></span>
-   <span data-ttu-id="9b5e3-145">IPMExtensionContractInfo.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-145">IPMExtensionContractInfo.</span></span> <span data-ttu-id="9b5e3-146">IID： {E5666373-7BA1-467C-B8-19-B1-75-DB-1C-29-5B}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-146">IID: {E5666373-7BA1-467C-B8-19-B1-75-DB-1C-29-5B}</span></span>
-   <span data-ttu-id="9b5e3-147">IPMExtensionFileOpenPickerInfo.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-147">IPMExtensionFileOpenPickerInfo.</span></span> <span data-ttu-id="9b5e3-148">IID： {6DC91D25-9606-420C-9A-78-E0-34-A3-41-83-45}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-148">IID: {6DC91D25-9606-420C-9A-78-E0-34-A3-41-83-45}</span></span>
-   <span data-ttu-id="9b5e3-149">IPMExtensionFileSavePickerInfo.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-149">IPMExtensionFileSavePickerInfo.</span></span> <span data-ttu-id="9b5e3-150">IID： {38005CBA-F81A-493E-A0-F8-92-2C-86-80-DA-43}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-150">IID: {38005CBA-F81A-493E-A0-F8-92-2C-86-80-DA-43}</span></span>
-   <span data-ttu-id="9b5e3-151">IPMExtensionCachedFileUpdaterInfo.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-151">IPMExtensionCachedFileUpdaterInfo.</span></span> <span data-ttu-id="9b5e3-152">IID： {E2D77509-4E58-4BA9-AF-7E-B6-42-E3-70-E1-B0}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-152">IID: {E2D77509-4E58-4BA9-AF-7E-B6-42-E3-70-E1-B0}</span></span>
-   <span data-ttu-id="9b5e3-153">IPMExtensionInfoEnumerator.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-153">IPMExtensionInfoEnumerator.</span></span> <span data-ttu-id="9b5e3-154">IID： {403B9E82-1171-4573-8E-6F-6F-33-F3-9B-83-DD}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-154">IID: {403B9E82-1171-4573-8E-6F-6F-33-F3-9B-83-DD}</span></span>
-   <span data-ttu-id="9b5e3-155">IPMBackgroundServiceAgentInfo.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-155">IPMBackgroundServiceAgentInfo.</span></span> <span data-ttu-id="9b5e3-156">IID： {3A8B46DA-928C-A177-C5DD61D9C242-99-8C-09-DC-96-F3-D4-90}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-156">IID: {3A8B46DA-928C-4879-99-8C-09-DC-96-F3-D4-90}</span></span>
-   <span data-ttu-id="9b5e3-157">IPMBackgroundWorkerInfo.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-157">IPMBackgroundWorkerInfo.</span></span> <span data-ttu-id="9b5e3-158">IID： {7DD4531B-D3BF-4B6B-94-F3-69-C0-98-B1-49-7D}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-158">IID: {7DD4531B-D3BF-4B6B-94-F3-69-C0-98-B1-49-7D}</span></span>
-   <span data-ttu-id="9b5e3-159">IPMBackgroundServiceAgentInfoEnumerator.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-159">IPMBackgroundServiceAgentInfoEnumerator.</span></span> <span data-ttu-id="9b5e3-160">IID： {18EB2072-AB56-43B3-87-2C-A-AF-B7-A6-B3-91}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-160">IID: {18EB2072-AB56-43B3-87-2C-BE-AF-B7-A6-B3-91}</span></span>
-   <span data-ttu-id="9b5e3-161">IPMBackgroundWorkerInfoEnumerator.</span><span class="sxs-lookup"><span data-stu-id="9b5e3-161">IPMBackgroundWorkerInfoEnumerator.</span></span> <span data-ttu-id="9b5e3-162">IID： {87F479F8-90D8-4EC7-92-B9-72-78-7E-2F-63-6B}</span><span class="sxs-lookup"><span data-stu-id="9b5e3-162">IID: {87F479F8-90D8-4EC7-92-B9-72-78-7E-2F-63-6B}</span></span>

 

 




