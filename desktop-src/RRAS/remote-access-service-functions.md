---
title: 遠端存取服務函式
description: 使用下列函式來執行 RAS 功能。
ms.assetid: 5883a77a-6af8-47a8-bb28-6ef60a5aa2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d272403c8cd485f5e9d3d1de0c7fe5ac1cac9442
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093091"
---
# <a name="remote-access-service-functions"></a><span data-ttu-id="f7abd-103">遠端存取服務函式</span><span class="sxs-lookup"><span data-stu-id="f7abd-103">Remote Access Service Functions</span></span>

<span data-ttu-id="f7abd-104">使用下列函式來執行 RAS 功能。</span><span class="sxs-lookup"><span data-stu-id="f7abd-104">Use the following functions to implement RAS functionality.</span></span>

<span data-ttu-id="f7abd-105">**CmFree**</span><span class="sxs-lookup"><span data-stu-id="f7abd-105">**CmFree**</span></span>

<span data-ttu-id="f7abd-106">**CmMalloc**</span><span class="sxs-lookup"><span data-stu-id="f7abd-106">**CmMalloc**</span></span>

[<span data-ttu-id="f7abd-107">**ORASADFunc**</span><span class="sxs-lookup"><span data-stu-id="f7abd-107">**ORASADFunc**</span></span>](/windows/desktop/api/Ras/nc-ras-orasadfunc)

[<span data-ttu-id="f7abd-108">**RASADFunc**</span><span class="sxs-lookup"><span data-stu-id="f7abd-108">**RASADFunc**</span></span>](/windows/desktop/api/Ras/nc-ras-rasadfunca)

[<span data-ttu-id="f7abd-109">**RasClearConnectionStatistics**</span><span class="sxs-lookup"><span data-stu-id="f7abd-109">**RasClearConnectionStatistics**</span></span>](/windows/desktop/api/Ras/nf-ras-rasclearconnectionstatistics)

[<span data-ttu-id="f7abd-110">**RasClearLinkStatistics**</span><span class="sxs-lookup"><span data-stu-id="f7abd-110">**RasClearLinkStatistics**</span></span>](/windows/desktop/api/Ras/nf-ras-rasclearlinkstatistics)

[<span data-ttu-id="f7abd-111">**RasConnectionNotification**</span><span class="sxs-lookup"><span data-stu-id="f7abd-111">**RasConnectionNotification**</span></span>](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa)

[<span data-ttu-id="f7abd-112">**RasCreatePhonebookEntry**</span><span class="sxs-lookup"><span data-stu-id="f7abd-112">**RasCreatePhonebookEntry**</span></span>](/windows/desktop/api/Ras/nf-ras-rascreatephonebookentrya)

[<span data-ttu-id="f7abd-113">**RasCustomDeleteEntryNotify**</span><span class="sxs-lookup"><span data-stu-id="f7abd-113">**RasCustomDeleteEntryNotify**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

[<span data-ttu-id="f7abd-114">**RasCustomDial**</span><span class="sxs-lookup"><span data-stu-id="f7abd-114">**RasCustomDial**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)

[<span data-ttu-id="f7abd-115">**RasCustomDialDlg**</span><span class="sxs-lookup"><span data-stu-id="f7abd-115">**RasCustomDialDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)

[<span data-ttu-id="f7abd-116">**RasCustomEntryDlg**</span><span class="sxs-lookup"><span data-stu-id="f7abd-116">**RasCustomEntryDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)

[<span data-ttu-id="f7abd-117">**RasCustomHangUp**</span><span class="sxs-lookup"><span data-stu-id="f7abd-117">**RasCustomHangUp**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)

[<span data-ttu-id="f7abd-118">**RasDeleteEntry**</span><span class="sxs-lookup"><span data-stu-id="f7abd-118">**RasDeleteEntry**</span></span>](/windows/desktop/api/Ras/nf-ras-rasdeleteentrya)

[<span data-ttu-id="f7abd-119">**RasDeleteSubEntry**</span><span class="sxs-lookup"><span data-stu-id="f7abd-119">**RasDeleteSubEntry**</span></span>](/windows/desktop/api/Ras/nf-ras-rasdeletesubentrya)

[<span data-ttu-id="f7abd-120">**RasDial**</span><span class="sxs-lookup"><span data-stu-id="f7abd-120">**RasDial**</span></span>](/windows/desktop/api/Ras/nf-ras-rasdiala)

[<span data-ttu-id="f7abd-121">**RasDialDlg**</span><span class="sxs-lookup"><span data-stu-id="f7abd-121">**RasDialDlg**</span></span>](/windows/desktop/api/Rasdlg/nf-rasdlg-rasdialdlga)

[<span data-ttu-id="f7abd-122">**RasDialFunc**</span><span class="sxs-lookup"><span data-stu-id="f7abd-122">**RasDialFunc**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc)

[<span data-ttu-id="f7abd-123">**RasDialFunc1**</span><span class="sxs-lookup"><span data-stu-id="f7abd-123">**RasDialFunc1**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc1)

[<span data-ttu-id="f7abd-124">**RasDialFunc2**</span><span class="sxs-lookup"><span data-stu-id="f7abd-124">**RasDialFunc2**</span></span>](/windows/desktop/api/Ras/nc-ras-rasdialfunc2)

[<span data-ttu-id="f7abd-125">**RasEditPhonebookEntry**</span><span class="sxs-lookup"><span data-stu-id="f7abd-125">**RasEditPhonebookEntry**</span></span>](/windows/desktop/api/Ras/nf-ras-raseditphonebookentrya)

[<span data-ttu-id="f7abd-126">**RasEntryDlg**</span><span class="sxs-lookup"><span data-stu-id="f7abd-126">**RasEntryDlg**</span></span>](/windows/desktop/api/Rasdlg/nf-rasdlg-rasentrydlga)

[<span data-ttu-id="f7abd-127">**RasEnumAutodialAddresses**</span><span class="sxs-lookup"><span data-stu-id="f7abd-127">**RasEnumAutodialAddresses**</span></span>](/windows/desktop/api/Ras/nf-ras-rasenumautodialaddressesa)

[<span data-ttu-id="f7abd-128">**RasEnumConnections**</span><span class="sxs-lookup"><span data-stu-id="f7abd-128">**RasEnumConnections**</span></span>](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa)

[<span data-ttu-id="f7abd-129">**RasEnumDevices**</span><span class="sxs-lookup"><span data-stu-id="f7abd-129">**RasEnumDevices**</span></span>](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa)

[<span data-ttu-id="f7abd-130">**RasEnumEntries**</span><span class="sxs-lookup"><span data-stu-id="f7abd-130">**RasEnumEntries**</span></span>](/windows/desktop/api/Ras/nf-ras-rasenumentriesa)

[<span data-ttu-id="f7abd-131">**RasFreeEapUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="f7abd-131">**RasFreeEapUserIdentity**</span></span>](/windows/desktop/api/Ras/nf-ras-rasfreeeapuseridentitya)

[<span data-ttu-id="f7abd-132">**RasGetAutodialAddress**</span><span class="sxs-lookup"><span data-stu-id="f7abd-132">**RasGetAutodialAddress**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetautodialaddressa)

[<span data-ttu-id="f7abd-133">**RasGetAutodialEnable**</span><span class="sxs-lookup"><span data-stu-id="f7abd-133">**RasGetAutodialEnable**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetautodialenablea)

[<span data-ttu-id="f7abd-134">**RasGetAutodialParam**</span><span class="sxs-lookup"><span data-stu-id="f7abd-134">**RasGetAutodialParam**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetautodialparama)

[<span data-ttu-id="f7abd-135">**RasGetConnectionStatistics**</span><span class="sxs-lookup"><span data-stu-id="f7abd-135">**RasGetConnectionStatistics**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetconnectionstatistics)

[<span data-ttu-id="f7abd-136">**RasGetConnectStatus**</span><span class="sxs-lookup"><span data-stu-id="f7abd-136">**RasGetConnectStatus**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa)

[<span data-ttu-id="f7abd-137">**RasGetCountryInfo**</span><span class="sxs-lookup"><span data-stu-id="f7abd-137">**RasGetCountryInfo**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetcountryinfoa)

[<span data-ttu-id="f7abd-138">**RasGetCredentials**</span><span class="sxs-lookup"><span data-stu-id="f7abd-138">**RasGetCredentials**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetcredentialsa)

[<span data-ttu-id="f7abd-139">**RasGetCustomAuthData**</span><span class="sxs-lookup"><span data-stu-id="f7abd-139">**RasGetCustomAuthData**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetcustomauthdataa)

[<span data-ttu-id="f7abd-140">**RasGetEapUserData**</span><span class="sxs-lookup"><span data-stu-id="f7abd-140">**RasGetEapUserData**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgeteapuserdataa)

[<span data-ttu-id="f7abd-141">**RasGetEapUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="f7abd-141">**RasGetEapUserIdentity**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgeteapuseridentitya)

[<span data-ttu-id="f7abd-142">**RasGetEntryDialParams**</span><span class="sxs-lookup"><span data-stu-id="f7abd-142">**RasGetEntryDialParams**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetentrydialparamsa)

[<span data-ttu-id="f7abd-143">**RasGetEntryProperties**</span><span class="sxs-lookup"><span data-stu-id="f7abd-143">**RasGetEntryProperties**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa)

[<span data-ttu-id="f7abd-144">**RasGetErrorString**</span><span class="sxs-lookup"><span data-stu-id="f7abd-144">**RasGetErrorString**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa)

[<span data-ttu-id="f7abd-145">**RasGetLinkStatistics**</span><span class="sxs-lookup"><span data-stu-id="f7abd-145">**RasGetLinkStatistics**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetlinkstatistics)

[<span data-ttu-id="f7abd-146">**RasGetNapStatus**</span><span class="sxs-lookup"><span data-stu-id="f7abd-146">**RasGetNapStatus**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetnapstatus)

<span data-ttu-id="f7abd-147">[**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="f7abd-147">[**RasGetProjectionInfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10))</span></span>

[<span data-ttu-id="f7abd-148">**RasGetProjectionInfoEx**</span><span class="sxs-lookup"><span data-stu-id="f7abd-148">**RasGetProjectionInfoEx**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetprojectioninfoex)

<span data-ttu-id="f7abd-149">[**RasGetQuarantineConnectionId**](/previous-versions/windows/desktop/legacy/aa377552(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f7abd-149">[**RasGetQuarantineConnectionId**](/previous-versions/windows/desktop/legacy/aa377552(v=vs.85))</span></span>

[<span data-ttu-id="f7abd-150">**RasGetSubEntryHandle**</span><span class="sxs-lookup"><span data-stu-id="f7abd-150">**RasGetSubEntryHandle**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetsubentryhandlea)

[<span data-ttu-id="f7abd-151">**RasGetSubEntryProperties**</span><span class="sxs-lookup"><span data-stu-id="f7abd-151">**RasGetSubEntryProperties**</span></span>](/windows/desktop/api/Ras/nf-ras-rasgetsubentrypropertiesa)

[<span data-ttu-id="f7abd-152">**RasHangUp**</span><span class="sxs-lookup"><span data-stu-id="f7abd-152">**RasHangUp**</span></span>](/windows/desktop/api/Ras/nf-ras-rashangupa)

[<span data-ttu-id="f7abd-153">**RasInvokeEapUI**</span><span class="sxs-lookup"><span data-stu-id="f7abd-153">**RasInvokeEapUI**</span></span>](/windows/desktop/api/Ras/nf-ras-rasinvokeeapui)

<span data-ttu-id="f7abd-154">[**RasMonitorDlg**](/previous-versions/windows/desktop/legacy/aa377584(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f7abd-154">[**RasMonitorDlg**](/previous-versions/windows/desktop/legacy/aa377584(v=vs.85))</span></span>

[<span data-ttu-id="f7abd-155">**RasPBDlgFunc**</span><span class="sxs-lookup"><span data-stu-id="f7abd-155">**RasPBDlgFunc**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-raspbdlgfunca)

[<span data-ttu-id="f7abd-156">**RasPhonebookDlg**</span><span class="sxs-lookup"><span data-stu-id="f7abd-156">**RasPhonebookDlg**</span></span>](/windows/desktop/api/Rasdlg/nf-rasdlg-rasphonebookdlga)

[<span data-ttu-id="f7abd-157">**RasRenameEntry**</span><span class="sxs-lookup"><span data-stu-id="f7abd-157">**RasRenameEntry**</span></span>](/windows/desktop/api/Ras/nf-ras-rasrenameentrya)

[<span data-ttu-id="f7abd-158">**RasSetAutodialAddress**</span><span class="sxs-lookup"><span data-stu-id="f7abd-158">**RasSetAutodialAddress**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetautodialaddressa)

[<span data-ttu-id="f7abd-159">**RasSetAutodialEnable**</span><span class="sxs-lookup"><span data-stu-id="f7abd-159">**RasSetAutodialEnable**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetautodialenablea)

[<span data-ttu-id="f7abd-160">**RasSetAutodialParam**</span><span class="sxs-lookup"><span data-stu-id="f7abd-160">**RasSetAutodialParam**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetautodialparama)

[<span data-ttu-id="f7abd-161">**RasSetCommSettings**</span><span class="sxs-lookup"><span data-stu-id="f7abd-161">**RasSetCommSettings**</span></span>](/windows/desktop/api/Ras/nc-ras-pfnrassetcommsettings)

[<span data-ttu-id="f7abd-162">**RasSetCredentials**</span><span class="sxs-lookup"><span data-stu-id="f7abd-162">**RasSetCredentials**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetcredentialsa)

[<span data-ttu-id="f7abd-163">**RasSetCustomAuthData**</span><span class="sxs-lookup"><span data-stu-id="f7abd-163">**RasSetCustomAuthData**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetcustomauthdataa)

[<span data-ttu-id="f7abd-164">**RasSetEapUserData**</span><span class="sxs-lookup"><span data-stu-id="f7abd-164">**RasSetEapUserData**</span></span>](/windows/desktop/api/Ras/nf-ras-rasseteapuserdataa)

[<span data-ttu-id="f7abd-165">**RasSetEntryDialParams**</span><span class="sxs-lookup"><span data-stu-id="f7abd-165">**RasSetEntryDialParams**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetentrydialparamsa)

[<span data-ttu-id="f7abd-166">**RasSetEntryProperties**</span><span class="sxs-lookup"><span data-stu-id="f7abd-166">**RasSetEntryProperties**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa)

[<span data-ttu-id="f7abd-167">**RasSetSubEntryProperties**</span><span class="sxs-lookup"><span data-stu-id="f7abd-167">**RasSetSubEntryProperties**</span></span>](/windows/desktop/api/Ras/nf-ras-rassetsubentrypropertiesa)

[<span data-ttu-id="f7abd-168">**RasUpdateConnection**</span><span class="sxs-lookup"><span data-stu-id="f7abd-168">**RasUpdateConnection**</span></span>](/windows/desktop/api/Ras/nf-ras-rasupdateconnection)

[<span data-ttu-id="f7abd-169">**RasValidateEntryName**</span><span class="sxs-lookup"><span data-stu-id="f7abd-169">**RasValidateEntryName**</span></span>](/windows/desktop/api/Ras/nf-ras-rasvalidateentrynamea)

[<span data-ttu-id="f7abd-170">RAS 自訂腳本 DLL 函式</span><span class="sxs-lookup"><span data-stu-id="f7abd-170">RAS Custom Scripting DLL Functions</span></span>](ras-custom-scripting-dll-functions.md)

 

 