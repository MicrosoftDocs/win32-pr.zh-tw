---
Description: KNOWNFOLDERID 常數代表 Guid，可識別以已知的資料夾向系統註冊的標準資料夾。
ms.assetid: f2c08ade-3083-44e4-82b0-dde45f0e3094
title: 'KNOWNFOLDERID (Knownfolders) '
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/27/2020
ms.openlocfilehash: 97748d074d6b0982708f51ea679f0629e8abfad6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104974801"
---
# <a name="knownfolderid"></a><span data-ttu-id="4139d-103">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="4139d-103">KNOWNFOLDERID</span></span>

<span data-ttu-id="4139d-104">**KNOWNFOLDERID** 常數代表 guid，可識別以 [已知的資料夾](known-folders.md)向系統註冊的標準資料夾。</span><span class="sxs-lookup"><span data-stu-id="4139d-104">The **KNOWNFOLDERID** constants represent GUIDs that identify standard folders registered with the system as [Known Folders](known-folders.md).</span></span> <span data-ttu-id="4139d-105">這些資料夾會與 Windows Vista 和更新版本的作業系統一起安裝，而電腦將只會有適合安裝的資料夾。</span><span class="sxs-lookup"><span data-stu-id="4139d-105">These folders are installed with Windows Vista and later operating systems, and a computer will have only folders appropriate to it installed.</span></span> <span data-ttu-id="4139d-106">如需這些資料夾的說明，請參閱 [**CSIDL**](csidl.md)。</span><span class="sxs-lookup"><span data-stu-id="4139d-106">For descriptions of these folders, see [**CSIDL**](csidl.md).</span></span>

## <a name="example"></a><span data-ttu-id="4139d-107">範例</span><span class="sxs-lookup"><span data-stu-id="4139d-107">Example</span></span>

```c
HRESULT CExplorerBrowserHostDialog::_FillViewWithKnownFolders(IResultsFolder *prf)
{
    IKnownFolderManager *pManager;
    HRESULT hr = CoCreateInstance(CLSID_KnownFolderManager, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pManager));
    if (SUCCEEDED(hr))
    {
        UINT cCount;
        KNOWNFOLDERID *pkfid;

        hr = pManager->GetFolderIds(&pkfid, &cCount);
        if (SUCCEEDED(hr))
        {
            for (UINT i = 0; i < cCount; i++)
            {
                IKnownFolder *pKnownFolder;
                hr = pManager->GetFolder(pkfid[i], &pKnownFolder);
                if (SUCCEEDED(hr))
                {
                    IShellItem *psi;
                    hr = pKnownFolder->GetShellItem(0, IID_PPV_ARGS(&psi));
                    if (SUCCEEDED(hr))
                    {
                        hr = prf->AddItem(psi);
                        psi->Release();
                    }
                    pKnownFolder->Release();
                }
            }
            CoTaskMemFree(pkfid);
        }
        pManager->Release();
    }
    return hr;
}

```

<span data-ttu-id="4139d-108">從 GitHub 上的 [Windows 傳統範例](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winui/shell/appplatform/ExplorerBrowserCustomContents/ExplorerBrowserCustomContents.cpp) 取得的範例。</span><span class="sxs-lookup"><span data-stu-id="4139d-108">Example from [Windows classic samples](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winui/shell/appplatform/ExplorerBrowserCustomContents/ExplorerBrowserCustomContents.cpp) on GitHub.</span></span>

## <a name="constants"></a><span data-ttu-id="4139d-109">常數</span><span class="sxs-lookup"><span data-stu-id="4139d-109">Constants</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="4139d-110">常數</span><span class="sxs-lookup"><span data-stu-id="4139d-110">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="4139d-111">描述</span><span class="sxs-lookup"><span data-stu-id="4139d-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AccountPictures"></span><span id="folderid_accountpictures"></span><span id="FOLDERID_ACCOUNTPICTURES"></span><dl> <span data-ttu-id="4139d-112"><dt><strong>FOLDERID_AccountPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-112"><dt><strong>FOLDERID_AccountPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-113">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-113">GUID</span></span></td>
<td><span data-ttu-id="4139d-114">{008ca0b1-55b4-4c56-b8a8-4de4b299d3be}</span><span class="sxs-lookup"><span data-stu-id="4139d-114">{008ca0b1-55b4-4c56-b8a8-4de4b299d3be}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-115">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-115">Display Name</span></span></td>
<td><span data-ttu-id="4139d-116">帳戶圖片</span><span class="sxs-lookup"><span data-stu-id="4139d-116">Account Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-117">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-117">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-118">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-118">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-119">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-119">Default Path</span></span></td>
<td><span data-ttu-id="4139d-120">%APPDATA%\Microsoft\Windows\AccountPictures</span><span class="sxs-lookup"><span data-stu-id="4139d-120">%APPDATA%\Microsoft\Windows\AccountPictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-121">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-121">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-122">無，Windows 8 中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-122">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-123">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-123">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-124">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-124">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-125">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-125">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-126">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-126">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AddNewPrograms"></span><span id="folderid_addnewprograms"></span><span id="FOLDERID_ADDNEWPROGRAMS"></span><dl> <span data-ttu-id="4139d-127"><dt><strong>FOLDERID_AddNewPrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-127"><dt><strong>FOLDERID_AddNewPrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-128">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-128">GUID</span></span></td>
<td><span data-ttu-id="4139d-129">{de61d971-5ebc-4f02-a3a9-6c82895e5c04}</span><span class="sxs-lookup"><span data-stu-id="4139d-129">{de61d971-5ebc-4f02-a3a9-6c82895e5c04}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-130">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-130">Display Name</span></span></td>
<td><span data-ttu-id="4139d-131">取得程式</span><span class="sxs-lookup"><span data-stu-id="4139d-131">Get Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-132">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-132">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-133">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-133">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-134">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-134">Default Path</span></span></td>
<td><span data-ttu-id="4139d-135">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-135">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-136">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-136">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-137">無</span><span class="sxs-lookup"><span data-stu-id="4139d-137">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-138">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-138">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-139">在主控台) 的 [新增 <strong>或移除程式</strong> ] 專案中，加入新的程式 (</span><span class="sxs-lookup"><span data-stu-id="4139d-139">Add New Programs (found in the <strong>Add or Remove Programs</strong> item in the Control Panel)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-140">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-140">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-141">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-141">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AdminTools"></span><span id="folderid_admintools"></span><span id="FOLDERID_ADMINTOOLS"></span><dl> <span data-ttu-id="4139d-142"><dt><strong>FOLDERID_AdminTools</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-142"><dt><strong>FOLDERID_AdminTools</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-143">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-143">GUID</span></span></td>
<td><span data-ttu-id="4139d-144">{724EF170-A42D-4FEF-9F26-B60E846FBA4F}</span><span class="sxs-lookup"><span data-stu-id="4139d-144">{724EF170-A42D-4FEF-9F26-B60E846FBA4F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-145">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-145">Display Name</span></span></td>
<td><span data-ttu-id="4139d-146">[系統管理工具]</span><span class="sxs-lookup"><span data-stu-id="4139d-146">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-147">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-147">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-148">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-148">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-149">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-149">Default Path</span></span></td>
<td><span data-ttu-id="4139d-150">%APPDATA%\Microsoft\Windows\Start Menu\Programs\Administrative 工具</span><span class="sxs-lookup"><span data-stu-id="4139d-150">%APPDATA%\Microsoft\Windows\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-151">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-151">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-152">CSIDL_ADMINTOOLS</span><span class="sxs-lookup"><span data-stu-id="4139d-152">CSIDL_ADMINTOOLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-153">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-153">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-154">[系統管理工具]</span><span class="sxs-lookup"><span data-stu-id="4139d-154">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-155">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-155">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-156">%USERPROFILE%\Start Menu\Programs\Administrative 工具</span><span class="sxs-lookup"><span data-stu-id="4139d-156">%USERPROFILE%\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppDataDesktop"></span><span id="folderid_appdatadesktop"></span><span id="FOLDERID_APPDATADESKTOP"></span><dl> <span data-ttu-id="4139d-157"><dt><strong>FOLDERID_AppDataDesktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-157"><dt><strong>FOLDERID_AppDataDesktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-158">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-158">GUID</span></span></td>
<td><span data-ttu-id="4139d-159">{B2C5E279-7ADD-439F-B28C-C41FE1BBF672}</span><span class="sxs-lookup"><span data-stu-id="4139d-159">{B2C5E279-7ADD-439F-B28C-C41FE1BBF672}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-160">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-160">Display Name</span></span></td>
<td><span data-ttu-id="4139d-161">AppDataDesktop</span><span class="sxs-lookup"><span data-stu-id="4139d-161">AppDataDesktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-162">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-162">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-163">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-163">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-164">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-164">Default Path</span></span></td>
<td><span data-ttu-id="4139d-165">%LOCALAPPDATA%\Desktop</span><span class="sxs-lookup"><span data-stu-id="4139d-165">%LOCALAPPDATA%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-166">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-166">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-167">無，Windows 10 1709 版中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-167">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-168">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-168">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-169">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-169">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-170">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-170">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-171">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-171">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="4139d-172">.NET 應用程式會在內部使用此 FOLDERID 來啟用跨平臺應用程式功能。</span><span class="sxs-lookup"><span data-stu-id="4139d-172">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="4139d-173">它不適合直接從應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="4139d-173">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppDataDocuments"></span><span id="folderid_appdatadocuments"></span><span id="FOLDERID_APPDATADOCUMENTS"></span><dl> <span data-ttu-id="4139d-174"><dt><strong>FOLDERID_AppDataDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-174"><dt><strong>FOLDERID_AppDataDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-175">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-175">GUID</span></span></td>
<td><span data-ttu-id="4139d-176">{7BE16610-1F7F-44AC-BFF0-83E15F2FFCA1}</span><span class="sxs-lookup"><span data-stu-id="4139d-176">{7BE16610-1F7F-44AC-BFF0-83E15F2FFCA1}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-177">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-177">Display Name</span></span></td>
<td><span data-ttu-id="4139d-178">AppDataDocuments</span><span class="sxs-lookup"><span data-stu-id="4139d-178">AppDataDocuments</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-179">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-179">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-180">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-180">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-181">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-181">Default Path</span></span></td>
<td><span data-ttu-id="4139d-182">%LOCALAPPDATA%\Documents</span><span class="sxs-lookup"><span data-stu-id="4139d-182">%LOCALAPPDATA%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-183">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-183">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-184">無，Windows 10 1709 版中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-184">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-185">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-185">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-186">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-186">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-187">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-187">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-188">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-188">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="4139d-189">.NET 應用程式會在內部使用此 FOLDERID 來啟用跨平臺應用程式功能。</span><span class="sxs-lookup"><span data-stu-id="4139d-189">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="4139d-190">它不適合直接從應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="4139d-190">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppDataFavorites"></span><span id="folderid_appdatafavorites"></span><span id="FOLDERID_APPDATAFAVORITES"></span><dl> <span data-ttu-id="4139d-191"><dt><strong>FOLDERID_AppDataFavorites</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-191"><dt><strong>FOLDERID_AppDataFavorites</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-192">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-192">GUID</span></span></td>
<td><span data-ttu-id="4139d-193">{7CFBEFBC-DE1F-45AA-B843-A542AC536CC9}</span><span class="sxs-lookup"><span data-stu-id="4139d-193">{7CFBEFBC-DE1F-45AA-B843-A542AC536CC9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-194">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-194">Display Name</span></span></td>
<td><span data-ttu-id="4139d-195">AppDataFavorites</span><span class="sxs-lookup"><span data-stu-id="4139d-195">AppDataFavorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-196">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-196">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-197">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-197">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-198">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-198">Default Path</span></span></td>
<td><span data-ttu-id="4139d-199">%LOCALAPPDATA%\Favorites</span><span class="sxs-lookup"><span data-stu-id="4139d-199">%LOCALAPPDATA%\Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-200">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-200">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-201">無，Windows 10 1709 版中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-201">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-202">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-202">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-203">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-203">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-204">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-204">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-205">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-205">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="4139d-206">.NET 應用程式會在內部使用此 FOLDERID 來啟用跨平臺應用程式功能。</span><span class="sxs-lookup"><span data-stu-id="4139d-206">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="4139d-207">它不適合直接從應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="4139d-207">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppDataProgramData"></span><span id="folderid_appdataprogramdata"></span><span id="FOLDERID_APPDATAPROGRAMDATA"></span><dl> <span data-ttu-id="4139d-208"><dt><strong>FOLDERID_AppDataProgramData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-208"><dt><strong>FOLDERID_AppDataProgramData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-209">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-209">GUID</span></span></td>
<td><span data-ttu-id="4139d-210">{559D40A3-A036-40FA-AF61-84CB430A4D34}</span><span class="sxs-lookup"><span data-stu-id="4139d-210">{559D40A3-A036-40FA-AF61-84CB430A4D34}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-211">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-211">Display Name</span></span></td>
<td><span data-ttu-id="4139d-212">AppDataProgramData</span><span class="sxs-lookup"><span data-stu-id="4139d-212">AppDataProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-213">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-213">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-214">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-214">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-215">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-215">Default Path</span></span></td>
<td><span data-ttu-id="4139d-216">%LOCALAPPDATA%\ProgramData</span><span class="sxs-lookup"><span data-stu-id="4139d-216">%LOCALAPPDATA%\ProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-217">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-217">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-218">無，Windows 10 1709 版中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-218">None, value introduced in Windows 10, version 1709</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-219">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-219">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-220">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-220">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-221">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-221">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-222">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-222">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p>
<p><span data-ttu-id="4139d-223">.NET 應用程式會在內部使用此 FOLDERID 來啟用跨平臺應用程式功能。</span><span class="sxs-lookup"><span data-stu-id="4139d-223">This FOLDERID is used internally by .NET applications to enable cross-platform app functionality.</span></span> <span data-ttu-id="4139d-224">它不適合直接從應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="4139d-224">It is not intended to be used directly from an application.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ApplicationShortcuts"></span><span id="folderid_applicationshortcuts"></span><span id="FOLDERID_APPLICATIONSHORTCUTS"></span><dl> <span data-ttu-id="4139d-225"><dt><strong>FOLDERID_ApplicationShortcuts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-225"><dt><strong>FOLDERID_ApplicationShortcuts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-226">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-226">GUID</span></span></td>
<td><span data-ttu-id="4139d-227">{A3918781-E5F2-4890-B3D9-A7E54332328C}</span><span class="sxs-lookup"><span data-stu-id="4139d-227">{A3918781-E5F2-4890-B3D9-A7E54332328C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-228">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-228">Display Name</span></span></td>
<td><span data-ttu-id="4139d-229">應用程式快捷方式</span><span class="sxs-lookup"><span data-stu-id="4139d-229">Application Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-230">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-230">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-231">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-231">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-232">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-232">Default Path</span></span></td>
<td><span data-ttu-id="4139d-233">%LOCALAPPDATA%\Microsoft\Windows\Application 快捷方式</span><span class="sxs-lookup"><span data-stu-id="4139d-233">%LOCALAPPDATA%\Microsoft\Windows\Application Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-234">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-234">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-235">無，Windows 8 中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-235">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-236">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-236">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-237">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-237">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-238">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-238">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-239">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-239">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_AppsFolder"></span><span id="folderid_appsfolder"></span><span id="FOLDERID_APPSFOLDER"></span><dl> <span data-ttu-id="4139d-240"><dt><strong>FOLDERID_AppsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-240"><dt><strong>FOLDERID_AppsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-241">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-241">GUID</span></span></td>
<td><span data-ttu-id="4139d-242">{1e87508d-89c2-42f0-8a7e-645a0f50ca58}</span><span class="sxs-lookup"><span data-stu-id="4139d-242">{1e87508d-89c2-42f0-8a7e-645a0f50ca58}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-243">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-243">Display Name</span></span></td>
<td><span data-ttu-id="4139d-244">應用程式</span><span class="sxs-lookup"><span data-stu-id="4139d-244">Applications</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-245">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-245">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-246">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-246">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-247">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-247">Default Path</span></span></td>
<td><span data-ttu-id="4139d-248">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-248">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-249">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-249">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-250">無，Windows 8 中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-250">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-251">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-251">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-252">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-252">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-253">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-253">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-254">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-254">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_AppUpdates"></span><span id="folderid_appupdates"></span><span id="FOLDERID_APPUPDATES"></span><dl> <span data-ttu-id="4139d-255"><dt><strong>FOLDERID_AppUpdates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-255"><dt><strong>FOLDERID_AppUpdates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-256">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-256">GUID</span></span></td>
<td><span data-ttu-id="4139d-257">{a305ce99-f527-492b-8b1a-7e76fa98d6e4}</span><span class="sxs-lookup"><span data-stu-id="4139d-257">{a305ce99-f527-492b-8b1a-7e76fa98d6e4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-258">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-258">Display Name</span></span></td>
<td><span data-ttu-id="4139d-259">已安裝的更新</span><span class="sxs-lookup"><span data-stu-id="4139d-259">Installed Updates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-260">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-260">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-261">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-261">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-262">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-262">Default Path</span></span></td>
<td><span data-ttu-id="4139d-263">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-263">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-264">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-264">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-265">無</span><span class="sxs-lookup"><span data-stu-id="4139d-265">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-266">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-266">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-267">無，在 Windows Vista 中引進的價值。</span><span class="sxs-lookup"><span data-stu-id="4139d-267">None, value introduced in Windows Vista.</span></span> <span data-ttu-id="4139d-268">在舊版的 Windows 中，如果已核取 [<strong>顯示更新</strong>] 方塊，這個頁面上的資訊就會包含在 [<strong>新增或移除程式</strong>] 中。</span><span class="sxs-lookup"><span data-stu-id="4139d-268">In earlier versions of Windows, the information on this page was included in <strong>Add or Remove Programs</strong> if the <strong>Show updates</strong> box was checked.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-269">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-269">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-270">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-270">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CameraRoll"></span><span id="folderid_cameraroll"></span><span id="FOLDERID_CAMERAROLL"></span><dl> <span data-ttu-id="4139d-271"><dt><strong>FOLDERID_CameraRoll</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-271"><dt><strong>FOLDERID_CameraRoll</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-272">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-272">GUID</span></span></td>
<td><span data-ttu-id="4139d-273">{AB5FB87B-7CE2-4F83-915D-550846C9537B}</span><span class="sxs-lookup"><span data-stu-id="4139d-273">{AB5FB87B-7CE2-4F83-915D-550846C9537B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-274">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-274">Display Name</span></span></td>
<td><span data-ttu-id="4139d-275">攝影機滾動</span><span class="sxs-lookup"><span data-stu-id="4139d-275">Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-276">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-276">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-277">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-277">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-278">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-278">Default Path</span></span></td>
<td><span data-ttu-id="4139d-279">%USERPROFILE%\Pictures\Camera 匯總</span><span class="sxs-lookup"><span data-stu-id="4139d-279">%USERPROFILE%\Pictures\Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-280">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-280">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-281">無，Windows 8.1 中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-281">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-282">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-282">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-283">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-283">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-284">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-284">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-285">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-285">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CDBurning"></span><span id="folderid_cdburning"></span><span id="FOLDERID_CDBURNING"></span><dl> <span data-ttu-id="4139d-286"><dt><strong>FOLDERID_CDBurning</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-286"><dt><strong>FOLDERID_CDBurning</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-287">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-287">GUID</span></span></td>
<td><span data-ttu-id="4139d-288">{9E52AB10-F80D-49DF-ACB8-4330F5687855}</span><span class="sxs-lookup"><span data-stu-id="4139d-288">{9E52AB10-F80D-49DF-ACB8-4330F5687855}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-289">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-289">Display Name</span></span></td>
<td><span data-ttu-id="4139d-290">暫存燒錄資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-290">Temporary Burn Folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-291">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-291">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-292">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-292">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-293">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-293">Default Path</span></span></td>
<td><span data-ttu-id="4139d-294">%LOCALAPPDATA%\Microsoft\Windows\Burn\Burn</span><span class="sxs-lookup"><span data-stu-id="4139d-294">%LOCALAPPDATA%\Microsoft\Windows\Burn\Burn</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-295">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-295">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-296">CSIDL_CDBURN_AREA</span><span class="sxs-lookup"><span data-stu-id="4139d-296">CSIDL_CDBURN_AREA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-297">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-297">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-298">CD 燒錄</span><span class="sxs-lookup"><span data-stu-id="4139d-298">CD Burning</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-299">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-299">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-300">%USERPROFILE%\Local Settings\Application Data\microsoft\cd burning 燒錄</span><span class="sxs-lookup"><span data-stu-id="4139d-300">%USERPROFILE%\Local Settings\Application Data\Microsoft\CD Burning</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ChangeRemovePrograms"></span><span id="folderid_changeremoveprograms"></span><span id="FOLDERID_CHANGEREMOVEPROGRAMS"></span><dl> <span data-ttu-id="4139d-301"><dt><strong>FOLDERID_ChangeRemovePrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-301"><dt><strong>FOLDERID_ChangeRemovePrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-302">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-302">GUID</span></span></td>
<td><span data-ttu-id="4139d-303">{df7266ac-9274-4867-8d55-3bd661de872d}</span><span class="sxs-lookup"><span data-stu-id="4139d-303">{df7266ac-9274-4867-8d55-3bd661de872d}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-304">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-304">Display Name</span></span></td>
<td><span data-ttu-id="4139d-305">[程式和功能]</span><span class="sxs-lookup"><span data-stu-id="4139d-305">Programs and Features</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-306">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-306">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-307">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-307">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-308">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-308">Default Path</span></span></td>
<td><span data-ttu-id="4139d-309">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-309">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-310">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-310">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-311">無</span><span class="sxs-lookup"><span data-stu-id="4139d-311">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-312">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-312">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-313">新增或移除程式</span><span class="sxs-lookup"><span data-stu-id="4139d-313">Add or Remove Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-314">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-314">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-315">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-315">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonAdminTools"></span><span id="folderid_commonadmintools"></span><span id="FOLDERID_COMMONADMINTOOLS"></span><dl> <span data-ttu-id="4139d-316"><dt><strong>FOLDERID_CommonAdminTools</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-316"><dt><strong>FOLDERID_CommonAdminTools</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-317">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-317">GUID</span></span></td>
<td><span data-ttu-id="4139d-318">{D0384E7D-BAC3-4797-8F14-CBA229B392B5}</span><span class="sxs-lookup"><span data-stu-id="4139d-318">{D0384E7D-BAC3-4797-8F14-CBA229B392B5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-319">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-319">Display Name</span></span></td>
<td><span data-ttu-id="4139d-320">[系統管理工具]</span><span class="sxs-lookup"><span data-stu-id="4139d-320">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-321">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-321">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-322">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-322">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-323">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-323">Default Path</span></span></td>
<td><span data-ttu-id="4139d-324">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\Administrative 工具</span><span class="sxs-lookup"><span data-stu-id="4139d-324">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-325">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-325">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-326">CSIDL_COMMON_ADMINTOOLS</span><span class="sxs-lookup"><span data-stu-id="4139d-326">CSIDL_COMMON_ADMINTOOLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-327">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-327">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-328">[系統管理工具]</span><span class="sxs-lookup"><span data-stu-id="4139d-328">Administrative Tools</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-329">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-329">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-330">%ALLUSERSPROFILE%\Start Menu\Programs\Administrative 工具</span><span class="sxs-lookup"><span data-stu-id="4139d-330">%ALLUSERSPROFILE%\Start Menu\Programs\Administrative Tools</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonOEMLinks"></span><span id="folderid_commonoemlinks"></span><span id="FOLDERID_COMMONOEMLINKS"></span><dl> <span data-ttu-id="4139d-331"><dt><strong>FOLDERID_CommonOEMLinks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-331"><dt><strong>FOLDERID_CommonOEMLinks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-332">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-332">GUID</span></span></td>
<td><span data-ttu-id="4139d-333">{C1BAE2D0-10DF-4334-BEDD-7AA20B227A9D}</span><span class="sxs-lookup"><span data-stu-id="4139d-333">{C1BAE2D0-10DF-4334-BEDD-7AA20B227A9D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-334">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-334">Display Name</span></span></td>
<td><span data-ttu-id="4139d-335">OEM 連結</span><span class="sxs-lookup"><span data-stu-id="4139d-335">OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-336">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-336">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-337">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-337">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-338">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-338">Default Path</span></span></td>
<td><span data-ttu-id="4139d-339">%ALLUSERSPROFILE%\OEM 連結</span><span class="sxs-lookup"><span data-stu-id="4139d-339">%ALLUSERSPROFILE%\OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-340">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-340">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-341">CSIDL_COMMON_OEM_LINKS</span><span class="sxs-lookup"><span data-stu-id="4139d-341">CSIDL_COMMON_OEM_LINKS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-342">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-342">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-343">OEM 連結</span><span class="sxs-lookup"><span data-stu-id="4139d-343">OEM Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-344">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-344">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-345">%ALLUSERSPROFILE%\OEM 連結</span><span class="sxs-lookup"><span data-stu-id="4139d-345">%ALLUSERSPROFILE%\OEM Links</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonPrograms"></span><span id="folderid_commonprograms"></span><span id="FOLDERID_COMMONPROGRAMS"></span><dl> <span data-ttu-id="4139d-346"><dt><strong>FOLDERID_CommonPrograms</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-346"><dt><strong>FOLDERID_CommonPrograms</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-347">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-347">GUID</span></span></td>
<td><span data-ttu-id="4139d-348">{0139D44E-6AFE-49F2-8690-3DAFCAE6FFB8}</span><span class="sxs-lookup"><span data-stu-id="4139d-348">{0139D44E-6AFE-49F2-8690-3DAFCAE6FFB8}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-349">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-349">Display Name</span></span></td>
<td><span data-ttu-id="4139d-350">程式</span><span class="sxs-lookup"><span data-stu-id="4139d-350">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-351">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-351">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-352">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-352">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-353">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-353">Default Path</span></span></td>
<td><span data-ttu-id="4139d-354">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs</span><span class="sxs-lookup"><span data-stu-id="4139d-354">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-355">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-355">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-356">CSIDL_COMMON_PROGRAMS</span><span class="sxs-lookup"><span data-stu-id="4139d-356">CSIDL_COMMON_PROGRAMS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-357">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-357">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-358">程式</span><span class="sxs-lookup"><span data-stu-id="4139d-358">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-359">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-359">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-360">%ALLUSERSPROFILE%\Start Menu\Programs</span><span class="sxs-lookup"><span data-stu-id="4139d-360">%ALLUSERSPROFILE%\Start Menu\Programs</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonStartMenu"></span><span id="folderid_commonstartmenu"></span><span id="FOLDERID_COMMONSTARTMENU"></span><dl> <span data-ttu-id="4139d-361"><dt><strong>FOLDERID_CommonStartMenu</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-361"><dt><strong>FOLDERID_CommonStartMenu</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-362">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-362">GUID</span></span></td>
<td><span data-ttu-id="4139d-363">{A4115719-D62E-491D-AA7C-E74B8BE3B067}</span><span class="sxs-lookup"><span data-stu-id="4139d-363">{A4115719-D62E-491D-AA7C-E74B8BE3B067}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-364">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-364">Display Name</span></span></td>
<td><span data-ttu-id="4139d-365">開始功能表</span><span class="sxs-lookup"><span data-stu-id="4139d-365">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-366">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-366">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-367">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-367">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-368">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-368">Default Path</span></span></td>
<td><span data-ttu-id="4139d-369">%ALLUSERSPROFILE%\Microsoft\Windows\Start 功能表</span><span class="sxs-lookup"><span data-stu-id="4139d-369">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-370">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-370">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-371">CSIDL_COMMON_STARTMENU</span><span class="sxs-lookup"><span data-stu-id="4139d-371">CSIDL_COMMON_STARTMENU</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-372">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-372">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-373">開始功能表</span><span class="sxs-lookup"><span data-stu-id="4139d-373">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-374">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-374">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-375">%ALLUSERSPROFILE%\Start 功能表</span><span class="sxs-lookup"><span data-stu-id="4139d-375">%ALLUSERSPROFILE%\Start Menu</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_CommonStartup"></span><span id="folderid_commonstartup"></span><span id="FOLDERID_COMMONSTARTUP"></span><dl> <span data-ttu-id="4139d-376"><dt><strong>FOLDERID_CommonStartup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-376"><dt><strong>FOLDERID_CommonStartup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-377">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-377">GUID</span></span></td>
<td><span data-ttu-id="4139d-378">{82A5EA35-D9CD-47C5-9629-E15D2F714E6E}</span><span class="sxs-lookup"><span data-stu-id="4139d-378">{82A5EA35-D9CD-47C5-9629-E15D2F714E6E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-379">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-379">Display Name</span></span></td>
<td><span data-ttu-id="4139d-380">啟動</span><span class="sxs-lookup"><span data-stu-id="4139d-380">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-381">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-381">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-382">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-382">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-383">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-383">Default Path</span></span></td>
<td><span data-ttu-id="4139d-384">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\StartUp</span><span class="sxs-lookup"><span data-stu-id="4139d-384">%ALLUSERSPROFILE%\Microsoft\Windows\Start Menu\Programs\StartUp</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-385">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-385">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-386">CSIDL_COMMON_STARTUP，CSIDL_COMMON_ALTSTARTUP</span><span class="sxs-lookup"><span data-stu-id="4139d-386">CSIDL_COMMON_STARTUP, CSIDL_COMMON_ALTSTARTUP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-387">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-387">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-388">啟動</span><span class="sxs-lookup"><span data-stu-id="4139d-388">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-389">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-389">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-390">%ALLUSERSPROFILE%\Start Menu\Programs\StartUp</span><span class="sxs-lookup"><span data-stu-id="4139d-390">%ALLUSERSPROFILE%\Start Menu\Programs\StartUp</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_CommonTemplates"></span><span id="folderid_commontemplates"></span><span id="FOLDERID_COMMONTEMPLATES"></span><dl> <span data-ttu-id="4139d-391"><dt><strong>FOLDERID_CommonTemplates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-391"><dt><strong>FOLDERID_CommonTemplates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-392">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-392">GUID</span></span></td>
<td><span data-ttu-id="4139d-393">{B94237E7-57AC-4347-9151-B08C6C32D1F7}</span><span class="sxs-lookup"><span data-stu-id="4139d-393">{B94237E7-57AC-4347-9151-B08C6C32D1F7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-394">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-394">Display Name</span></span></td>
<td><span data-ttu-id="4139d-395">範本</span><span class="sxs-lookup"><span data-stu-id="4139d-395">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-396">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-396">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-397">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-397">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-398">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-398">Default Path</span></span></td>
<td><span data-ttu-id="4139d-399">%ALLUSERSPROFILE%\Microsoft\Windows\Templates</span><span class="sxs-lookup"><span data-stu-id="4139d-399">%ALLUSERSPROFILE%\Microsoft\Windows\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-400">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-400">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-401">CSIDL_COMMON_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="4139d-401">CSIDL_COMMON_TEMPLATES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-402">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-402">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-403">範本</span><span class="sxs-lookup"><span data-stu-id="4139d-403">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-404">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-404">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-405">%ALLUSERSPROFILE%\Templates</span><span class="sxs-lookup"><span data-stu-id="4139d-405">%ALLUSERSPROFILE%\Templates</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ComputerFolder"></span><span id="folderid_computerfolder"></span><span id="FOLDERID_COMPUTERFOLDER"></span><dl> <span data-ttu-id="4139d-406"><dt><strong>FOLDERID_ComputerFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-406"><dt><strong>FOLDERID_ComputerFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-407">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-407">GUID</span></span></td>
<td><span data-ttu-id="4139d-408">{0AC0837C-BBF8-452A-850D-79D08E667CA7}</span><span class="sxs-lookup"><span data-stu-id="4139d-408">{0AC0837C-BBF8-452A-850D-79D08E667CA7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-409">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-409">Display Name</span></span></td>
<td><span data-ttu-id="4139d-410">電腦</span><span class="sxs-lookup"><span data-stu-id="4139d-410">Computer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-411">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-411">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-412">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-412">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-413">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-413">Default Path</span></span></td>
<td><span data-ttu-id="4139d-414">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-414">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-415">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-415">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-416">CSIDL_DRIVES</span><span class="sxs-lookup"><span data-stu-id="4139d-416">CSIDL_DRIVES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-417">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-417">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-418">我的電腦</span><span class="sxs-lookup"><span data-stu-id="4139d-418">My Computer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-419">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-419">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-420">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-420">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ConflictFolder"></span><span id="folderid_conflictfolder"></span><span id="FOLDERID_CONFLICTFOLDER"></span><dl> <span data-ttu-id="4139d-421"><dt><strong>FOLDERID_ConflictFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-421"><dt><strong>FOLDERID_ConflictFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-422">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-422">GUID</span></span></td>
<td><span data-ttu-id="4139d-423">{4bfefb45-347d-4006-a5be-ac0cb0567192}</span><span class="sxs-lookup"><span data-stu-id="4139d-423">{4bfefb45-347d-4006-a5be-ac0cb0567192}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-424">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-424">Display Name</span></span></td>
<td><span data-ttu-id="4139d-425">衝突</span><span class="sxs-lookup"><span data-stu-id="4139d-425">Conflicts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-426">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-426">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-427">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-427">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-428">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-428">Default Path</span></span></td>
<td><span data-ttu-id="4139d-429">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-429">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-430">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-430">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-431">無，在 Windows Vista 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-431">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-432">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-432">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-433">不適用。</span><span class="sxs-lookup"><span data-stu-id="4139d-433">Not applicable.</span></span> <span data-ttu-id="4139d-434">此 <strong>KNOWNFOLDERID</strong> 是指 Windows Vista 同步處理管理員。</span><span class="sxs-lookup"><span data-stu-id="4139d-434">This <strong>KNOWNFOLDERID</strong> refers to the Windows Vista Synchronization Manager.</span></span> <span data-ttu-id="4139d-435">它不是舊版 <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a>所參考的資料夾。</span><span class="sxs-lookup"><span data-stu-id="4139d-435">It is not the folder referenced by the older <a href="/windows/desktop/api/Syncmgr/nn-syncmgr-isyncmgrconflictfolder"><strong>ISyncMgrConflictFolder</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-436">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-436">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-437">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-437">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ConnectionsFolder"></span><span id="folderid_connectionsfolder"></span><span id="FOLDERID_CONNECTIONSFOLDER"></span><dl> <span data-ttu-id="4139d-438"><dt><strong>FOLDERID_ConnectionsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-438"><dt><strong>FOLDERID_ConnectionsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-439">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-439">GUID</span></span></td>
<td><span data-ttu-id="4139d-440">{6F0CD92B-2E97-45D1-88FF-B0D186B8DEDD}</span><span class="sxs-lookup"><span data-stu-id="4139d-440">{6F0CD92B-2E97-45D1-88FF-B0D186B8DEDD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-441">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-441">Display Name</span></span></td>
<td><span data-ttu-id="4139d-442">網路連線</span><span class="sxs-lookup"><span data-stu-id="4139d-442">Network Connections</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-443">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-443">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-444">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-444">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-445">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-445">Default Path</span></span></td>
<td><span data-ttu-id="4139d-446">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-446">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-447">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-447">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-448">CSIDL_CONNECTIONS</span><span class="sxs-lookup"><span data-stu-id="4139d-448">CSIDL_CONNECTIONS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-449">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-449">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-450">網路連線</span><span class="sxs-lookup"><span data-stu-id="4139d-450">Network Connections</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-451">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-451">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-452">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-452">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Contacts"></span><span id="folderid_contacts"></span><span id="FOLDERID_CONTACTS"></span><dl> <span data-ttu-id="4139d-453"><dt><strong>FOLDERID_Contacts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-453"><dt><strong>FOLDERID_Contacts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-454">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-454">GUID</span></span></td>
<td><span data-ttu-id="4139d-455">{56784854-C6CB-462b-8169-88E350ACB882}</span><span class="sxs-lookup"><span data-stu-id="4139d-455">{56784854-C6CB-462b-8169-88E350ACB882}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-456">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-456">Display Name</span></span></td>
<td><span data-ttu-id="4139d-457">連絡人</span><span class="sxs-lookup"><span data-stu-id="4139d-457">Contacts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-458">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-458">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-459">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-459">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-460">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-460">Default Path</span></span></td>
<td><span data-ttu-id="4139d-461">%USERPROFILE%\Contacts</span><span class="sxs-lookup"><span data-stu-id="4139d-461">%USERPROFILE%\Contacts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-462">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-462">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-463">無，在 Windows Vista 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-463">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-464">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-464">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-465">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-465">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-466">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-466">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-467">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-467">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ControlPanelFolder"></span><span id="folderid_controlpanelfolder"></span><span id="FOLDERID_CONTROLPANELFOLDER"></span><dl> <span data-ttu-id="4139d-468"><dt><strong>FOLDERID_ControlPanelFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-468"><dt><strong>FOLDERID_ControlPanelFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-469">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-469">GUID</span></span></td>
<td><span data-ttu-id="4139d-470">{82A74AEB-AEB4-465C-A014-D097EE346D63}</span><span class="sxs-lookup"><span data-stu-id="4139d-470">{82A74AEB-AEB4-465C-A014-D097EE346D63}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-471">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-471">Display Name</span></span></td>
<td><span data-ttu-id="4139d-472">控制台</span><span class="sxs-lookup"><span data-stu-id="4139d-472">Control Panel</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-473">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-473">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-474">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-474">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-475">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-475">Default Path</span></span></td>
<td><span data-ttu-id="4139d-476">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-476">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-477">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-477">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-478">CSIDL_CONTROLS</span><span class="sxs-lookup"><span data-stu-id="4139d-478">CSIDL_CONTROLS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-479">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-479">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-480">控制台</span><span class="sxs-lookup"><span data-stu-id="4139d-480">Control Panel</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-481">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-481">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-482">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-482">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Cookies"></span><span id="folderid_cookies"></span><span id="FOLDERID_COOKIES"></span><dl> <span data-ttu-id="4139d-483"><dt><strong>FOLDERID_Cookies</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-483"><dt><strong>FOLDERID_Cookies</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-484">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-484">GUID</span></span></td>
<td><span data-ttu-id="4139d-485">{2B0F765D-C0E9-4171-908E-08A611B84FF6}</span><span class="sxs-lookup"><span data-stu-id="4139d-485">{2B0F765D-C0E9-4171-908E-08A611B84FF6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-486">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-486">Display Name</span></span></td>
<td><span data-ttu-id="4139d-487">Cookie</span><span class="sxs-lookup"><span data-stu-id="4139d-487">Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-488">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-488">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-489">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-489">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-490">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-490">Default Path</span></span></td>
<td><span data-ttu-id="4139d-491">%APPDATA%\Microsoft\Windows\Cookies</span><span class="sxs-lookup"><span data-stu-id="4139d-491">%APPDATA%\Microsoft\Windows\Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-492">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-492">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-493">CSIDL_COOKIES</span><span class="sxs-lookup"><span data-stu-id="4139d-493">CSIDL_COOKIES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-494">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-494">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-495">Cookie</span><span class="sxs-lookup"><span data-stu-id="4139d-495">Cookies</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-496">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-496">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-497">%USERPROFILE%\Cookies</span><span class="sxs-lookup"><span data-stu-id="4139d-497">%USERPROFILE%\Cookies</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Desktop"></span><span id="folderid_desktop"></span><span id="FOLDERID_DESKTOP"></span><dl> <span data-ttu-id="4139d-498"><dt><strong>FOLDERID_Desktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-498"><dt><strong>FOLDERID_Desktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-499">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-499">GUID</span></span></td>
<td><span data-ttu-id="4139d-500">{B4BFCC3A-DB2C-424C-B029-7FE99A87C641}</span><span class="sxs-lookup"><span data-stu-id="4139d-500">{B4BFCC3A-DB2C-424C-B029-7FE99A87C641}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-501">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-501">Display Name</span></span></td>
<td><span data-ttu-id="4139d-502">桌面</span><span class="sxs-lookup"><span data-stu-id="4139d-502">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-503">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-503">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-504">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-504">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-505">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-505">Default Path</span></span></td>
<td><span data-ttu-id="4139d-506">%USERPROFILE%\Desktop</span><span class="sxs-lookup"><span data-stu-id="4139d-506">%USERPROFILE%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-507">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-507">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-508">CSIDL_DESKTOP，CSIDL_DESKTOPDIRECTORY</span><span class="sxs-lookup"><span data-stu-id="4139d-508">CSIDL_DESKTOP, CSIDL_DESKTOPDIRECTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-509">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-509">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-510">桌面</span><span class="sxs-lookup"><span data-stu-id="4139d-510">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-511">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-511">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-512">%USERPROFILE%\Desktop</span><span class="sxs-lookup"><span data-stu-id="4139d-512">%USERPROFILE%\Desktop</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_DeviceMetadataStore"></span><span id="folderid_devicemetadatastore"></span><span id="FOLDERID_DEVICEMETADATASTORE"></span><dl> <span data-ttu-id="4139d-513"><dt><strong>FOLDERID_DeviceMetadataStore</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-513"><dt><strong>FOLDERID_DeviceMetadataStore</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-514">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-514">GUID</span></span></td>
<td><span data-ttu-id="4139d-515">{5CE4A5E9-E4EB-479D-B89F-130C02886155}</span><span class="sxs-lookup"><span data-stu-id="4139d-515">{5CE4A5E9-E4EB-479D-B89F-130C02886155}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-516">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-516">Display Name</span></span></td>
<td><span data-ttu-id="4139d-517">DeviceMetadataStore</span><span class="sxs-lookup"><span data-stu-id="4139d-517">DeviceMetadataStore</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-518">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-518">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-519">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-519">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-520">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-520">Default Path</span></span></td>
<td><span data-ttu-id="4139d-521">%ALLUSERSPROFILE%\Microsoft\Windows\DeviceMetadataStore</span><span class="sxs-lookup"><span data-stu-id="4139d-521">%ALLUSERSPROFILE%\Microsoft\Windows\DeviceMetadataStore</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-522">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-522">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-523">無，在 Windows 7 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-523">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-524">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-524">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-525">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-525">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-526">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-526">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-527">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-527">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Documents"></span><span id="folderid_documents"></span><span id="FOLDERID_DOCUMENTS"></span><dl> <span data-ttu-id="4139d-528"><dt><strong>FOLDERID_Documents</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-528"><dt><strong>FOLDERID_Documents</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-529">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-529">GUID</span></span></td>
<td><span data-ttu-id="4139d-530">{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</span><span class="sxs-lookup"><span data-stu-id="4139d-530">{FDD39AD0-238F-46AF-ADB4-6C85480369C7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-531">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-531">Display Name</span></span></td>
<td><span data-ttu-id="4139d-532">文件</span><span class="sxs-lookup"><span data-stu-id="4139d-532">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-533">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-533">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-534">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-534">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-535">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-535">Default Path</span></span></td>
<td><span data-ttu-id="4139d-536">%USERPROFILE%\Documents</span><span class="sxs-lookup"><span data-stu-id="4139d-536">%USERPROFILE%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-537">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-537">CSIDL Equivalents</span></span></td>
<td><span data-ttu-id="4139d-538">CSIDL_MYDOCUMENTS，CSIDL_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="4139d-538">CSIDL_MYDOCUMENTS, CSIDL_PERSONAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-539">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-539">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-540">我的文件</span><span class="sxs-lookup"><span data-stu-id="4139d-540">My Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-541">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-541">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-542">%USERPROFILE%\My 檔</span><span class="sxs-lookup"><span data-stu-id="4139d-542">%USERPROFILE%\My Documents</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_DocumentsLibrary"></span><span id="folderid_documentslibrary"></span><span id="FOLDERID_DOCUMENTSLIBRARY"></span><dl> <span data-ttu-id="4139d-543"><dt><strong>FOLDERID_DocumentsLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-543"><dt><strong>FOLDERID_DocumentsLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-544">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-544">GUID</span></span></td>
<td><span data-ttu-id="4139d-545">{7B0DB17D-9CD2-4A93-9733-46CC89022E7C}</span><span class="sxs-lookup"><span data-stu-id="4139d-545">{7B0DB17D-9CD2-4A93-9733-46CC89022E7C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-546">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-546">Display Name</span></span></td>
<td><span data-ttu-id="4139d-547">文件</span><span class="sxs-lookup"><span data-stu-id="4139d-547">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-548">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-548">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-549">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-549">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-550">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-550">Default Path</span></span></td>
<td><span data-ttu-id="4139d-551">%APPDATA%\Microsoft\Windows\Libraries\Documents.library-ms</span><span class="sxs-lookup"><span data-stu-id="4139d-551">%APPDATA%\Microsoft\Windows\Libraries\Documents.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-552">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-552">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-553">無，在 Windows 7 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-553">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-554">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-554">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-555">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-555">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-556">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-556">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-557">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-557">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Downloads"></span><span id="folderid_downloads"></span><span id="FOLDERID_DOWNLOADS"></span><dl> <span data-ttu-id="4139d-558"><dt><strong>FOLDERID_Downloads</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-558"><dt><strong>FOLDERID_Downloads</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-559">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-559">GUID</span></span></td>
<td><span data-ttu-id="4139d-560">{374DE290-123F-4565-9164-39C4925E467B}</span><span class="sxs-lookup"><span data-stu-id="4139d-560">{374DE290-123F-4565-9164-39C4925E467B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-561">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-561">Display Name</span></span></td>
<td><span data-ttu-id="4139d-562">下載</span><span class="sxs-lookup"><span data-stu-id="4139d-562">Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-563">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-563">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-564">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-564">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-565">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-565">Default Path</span></span></td>
<td><span data-ttu-id="4139d-566">%USERPROFILE%\Downloads</span><span class="sxs-lookup"><span data-stu-id="4139d-566">%USERPROFILE%\Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-567">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-567">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-568">無</span><span class="sxs-lookup"><span data-stu-id="4139d-568">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-569">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-569">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-570">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-570">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-571">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-571">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-572">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-572">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Favorites"></span><span id="folderid_favorites"></span><span id="FOLDERID_FAVORITES"></span><dl> <span data-ttu-id="4139d-573"><dt><strong>FOLDERID_Favorites</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-573"><dt><strong>FOLDERID_Favorites</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-574">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-574">GUID</span></span></td>
<td><span data-ttu-id="4139d-575">{1777F761-68AD-4D8A-87BD-30B759FA33DD}</span><span class="sxs-lookup"><span data-stu-id="4139d-575">{1777F761-68AD-4D8A-87BD-30B759FA33DD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-576">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-576">Display Name</span></span></td>
<td><span data-ttu-id="4139d-577">我的最愛</span><span class="sxs-lookup"><span data-stu-id="4139d-577">Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-578">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-578">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-579">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-579">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-580">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-580">Default Path</span></span></td>
<td><span data-ttu-id="4139d-581">%USERPROFILE%\Favorites</span><span class="sxs-lookup"><span data-stu-id="4139d-581">%USERPROFILE%\Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-582">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-582">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-583">CSIDL_FAVORITES，CSIDL_COMMON_FAVORITES</span><span class="sxs-lookup"><span data-stu-id="4139d-583">CSIDL_FAVORITES, CSIDL_COMMON_FAVORITES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-584">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-584">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-585">我的最愛</span><span class="sxs-lookup"><span data-stu-id="4139d-585">Favorites</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-586">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-586">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-587">%USERPROFILE%\Favorites</span><span class="sxs-lookup"><span data-stu-id="4139d-587">%USERPROFILE%\Favorites</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Fonts"></span><span id="folderid_fonts"></span><span id="FOLDERID_FONTS"></span><dl> <span data-ttu-id="4139d-588"><dt><strong>FOLDERID_Fonts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-588"><dt><strong>FOLDERID_Fonts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-589">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-589">GUID</span></span></td>
<td><span data-ttu-id="4139d-590">{FD228CB7-AE11-4AE3-864C-16F3910AB8FE}</span><span class="sxs-lookup"><span data-stu-id="4139d-590">{FD228CB7-AE11-4AE3-864C-16F3910AB8FE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-591">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-591">Display Name</span></span></td>
<td><span data-ttu-id="4139d-592">字型</span><span class="sxs-lookup"><span data-stu-id="4139d-592">Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-593">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-593">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-594">FIXED</span><span class="sxs-lookup"><span data-stu-id="4139d-594">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-595">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-595">Default Path</span></span></td>
<td><span data-ttu-id="4139d-596">%windir%\Fonts</span><span class="sxs-lookup"><span data-stu-id="4139d-596">%windir%\Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-597">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-597">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-598">CSIDL_FONTS</span><span class="sxs-lookup"><span data-stu-id="4139d-598">CSIDL_FONTS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-599">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-599">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-600">字型</span><span class="sxs-lookup"><span data-stu-id="4139d-600">Fonts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-601">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-601">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-602">%windir%\Fonts</span><span class="sxs-lookup"><span data-stu-id="4139d-602">%windir%\Fonts</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Games"></span><span id="folderid_games"></span><span id="FOLDERID_GAMES"></span><dl> <span data-ttu-id="4139d-603"><dt><strong>FOLDERID_Games</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-603"><dt><strong>FOLDERID_Games</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><div class="alert">
<blockquote>
[!Note]<br />
<span data-ttu-id="4139d-604">此 FOLDERID 已在 Windows 10 1803 版和更新版本中淘汰。</span><span class="sxs-lookup"><span data-stu-id="4139d-604">This FOLDERID is deprecated in Windows 10, version 1803 and later versions.</span></span> <span data-ttu-id="4139d-605">在這些版本中，它會傳回 <strong>0x80070057-E_INVALIDARG</strong>
</span><span class="sxs-lookup"><span data-stu-id="4139d-605">In these versions, it returns <strong>0x80070057 - E_INVALIDARG</strong>
</span></span></blockquote>
</div>
<div>
 
</div>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-606">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-606">GUID</span></span></td>
<td><span data-ttu-id="4139d-607">{CAC52C1A-B53D-4edc-92D7-6B2E8AC19434}</span><span class="sxs-lookup"><span data-stu-id="4139d-607">{CAC52C1A-B53D-4edc-92D7-6B2E8AC19434}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-608">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-608">Display Name</span></span></td>
<td><span data-ttu-id="4139d-609">遊戲</span><span class="sxs-lookup"><span data-stu-id="4139d-609">Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-610">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-610">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-611">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-611">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-612">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-612">Default Path</span></span></td>
<td><span data-ttu-id="4139d-613">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-613">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-614">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-614">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-615">無</span><span class="sxs-lookup"><span data-stu-id="4139d-615">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-616">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-616">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-617">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-617">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-618">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-618">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-619">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-619">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_GameTasks"></span><span id="folderid_gametasks"></span><span id="FOLDERID_GAMETASKS"></span><dl> <span data-ttu-id="4139d-620"><dt><strong>FOLDERID_GameTasks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-620"><dt><strong>FOLDERID_GameTasks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-621">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-621">GUID</span></span></td>
<td><span data-ttu-id="4139d-622">{054FAE61-4DD8-4787-80B6-090220C4B700}</span><span class="sxs-lookup"><span data-stu-id="4139d-622">{054FAE61-4DD8-4787-80B6-090220C4B700}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-623">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-623">Display Name</span></span></td>
<td><span data-ttu-id="4139d-624">GameExplorer</span><span class="sxs-lookup"><span data-stu-id="4139d-624">GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-625">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-625">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-626">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-626">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-627">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-627">Default Path</span></span></td>
<td><span data-ttu-id="4139d-628">%LOCALAPPDATA%\Microsoft\Windows\GameExplorer</span><span class="sxs-lookup"><span data-stu-id="4139d-628">%LOCALAPPDATA%\Microsoft\Windows\GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-629">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-629">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-630">無，在 Windows Vista 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-630">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-631">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-631">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-632">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-632">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-633">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-633">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-634">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-634">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_History"></span><span id="folderid_history"></span><span id="FOLDERID_HISTORY"></span><dl> <span data-ttu-id="4139d-635"><dt><strong>FOLDERID_History</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-635"><dt><strong>FOLDERID_History</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-636">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-636">GUID</span></span></td>
<td><span data-ttu-id="4139d-637">{D9DC8A3B-B784-432E-A781-5A1130A75963}</span><span class="sxs-lookup"><span data-stu-id="4139d-637">{D9DC8A3B-B784-432E-A781-5A1130A75963}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-638">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-638">Display Name</span></span></td>
<td><span data-ttu-id="4139d-639">記錄</span><span class="sxs-lookup"><span data-stu-id="4139d-639">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-640">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-640">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-641">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-641">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-642">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-642">Default Path</span></span></td>
<td><span data-ttu-id="4139d-643">%LOCALAPPDATA%\Microsoft\Windows\History</span><span class="sxs-lookup"><span data-stu-id="4139d-643">%LOCALAPPDATA%\Microsoft\Windows\History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-644">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-644">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-645">CSIDL_HISTORY</span><span class="sxs-lookup"><span data-stu-id="4139d-645">CSIDL_HISTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-646">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-646">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-647">記錄</span><span class="sxs-lookup"><span data-stu-id="4139d-647">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-648">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-648">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-649">%USERPROFILE%\Local Settings\History</span><span class="sxs-lookup"><span data-stu-id="4139d-649">%USERPROFILE%\Local Settings\History</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_HomeGroup"></span><span id="folderid_homegroup"></span><span id="FOLDERID_HOMEGROUP"></span><dl> <span data-ttu-id="4139d-650"><dt><strong>FOLDERID_HomeGroup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-650"><dt><strong>FOLDERID_HomeGroup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-651">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-651">GUID</span></span></td>
<td><span data-ttu-id="4139d-652">{52528A6B-B9E3-4ADD-B60D-588C2DBA842D}</span><span class="sxs-lookup"><span data-stu-id="4139d-652">{52528A6B-B9E3-4ADD-B60D-588C2DBA842D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-653">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-653">Display Name</span></span></td>
<td><span data-ttu-id="4139d-654">家用群組</span><span class="sxs-lookup"><span data-stu-id="4139d-654">Homegroup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-655">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-655">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-656">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-656">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-657">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-657">Default Path</span></span></td>
<td><span data-ttu-id="4139d-658">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-658">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-659">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-659">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-660">無，在 Windows 7 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-660">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-661">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-661">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-662">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-662">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-663">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-663">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-664">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-664">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_HomeGroupCurrentUser"></span><span id="folderid_homegroupcurrentuser"></span><span id="FOLDERID_HOMEGROUPCURRENTUSER"></span><dl> <span data-ttu-id="4139d-665"><dt><strong>FOLDERID_HomeGroupCurrentUser</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-665"><dt><strong>FOLDERID_HomeGroupCurrentUser</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-666">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-666">GUID</span></span></td>
<td><span data-ttu-id="4139d-667">{9B74B6A3-0DFD-4f11-9E78-5F7800F2E772}</span><span class="sxs-lookup"><span data-stu-id="4139d-667">{9B74B6A3-0DFD-4f11-9E78-5F7800F2E772}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-668">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-668">Display Name</span></span></td>
<td><span data-ttu-id="4139d-669">使用者的使用者名稱 (% USERNAME% ) </span><span class="sxs-lookup"><span data-stu-id="4139d-669">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-670">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-670">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-671">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-671">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-672">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-672">Default Path</span></span></td>
<td><span data-ttu-id="4139d-673">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-673">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-674">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-674">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-675">無，Windows 8 中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-675">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-676">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-676">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-677">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-677">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-678">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-678">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-679">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-679">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ImplicitAppShortcuts"></span><span id="folderid_implicitappshortcuts"></span><span id="FOLDERID_IMPLICITAPPSHORTCUTS"></span><dl> <span data-ttu-id="4139d-680"><dt><strong>FOLDERID_ImplicitAppShortcuts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-680"><dt><strong>FOLDERID_ImplicitAppShortcuts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-681">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-681">GUID</span></span></td>
<td><span data-ttu-id="4139d-682">{BCB5256F-79F6-4CEE-B725-DC34E402FD46}</span><span class="sxs-lookup"><span data-stu-id="4139d-682">{BCB5256F-79F6-4CEE-B725-DC34E402FD46}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-683">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-683">Display Name</span></span></td>
<td><span data-ttu-id="4139d-684">ImplicitAppShortcuts</span><span class="sxs-lookup"><span data-stu-id="4139d-684">ImplicitAppShortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-685">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-685">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-686">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-686">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-687">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-687">Default Path</span></span></td>
<td><span data-ttu-id="4139d-688">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned\ImplicitAppShortcuts</span><span class="sxs-lookup"><span data-stu-id="4139d-688">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned\ImplicitAppShortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-689">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-689">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-690">無，在 Windows 7 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-690">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-691">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-691">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-692">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-692">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-693">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-693">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-694">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-694">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_InternetCache"></span><span id="folderid_internetcache"></span><span id="FOLDERID_INTERNETCACHE"></span><dl> <span data-ttu-id="4139d-695"><dt><strong>FOLDERID_InternetCache</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-695"><dt><strong>FOLDERID_InternetCache</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-696">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-696">GUID</span></span></td>
<td><span data-ttu-id="4139d-697">{352481E8-33BE-4251-BA85-6007CAEDCF9D}</span><span class="sxs-lookup"><span data-stu-id="4139d-697">{352481E8-33BE-4251-BA85-6007CAEDCF9D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-698">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-698">Display Name</span></span></td>
<td><span data-ttu-id="4139d-699">Temporary Internet Files</span><span class="sxs-lookup"><span data-stu-id="4139d-699">Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-700">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-700">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-701">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-701">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-702">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-702">Default Path</span></span></td>
<td><span data-ttu-id="4139d-703">%LOCALAPPDATA%\Microsoft\Windows\Temporary 網際網路檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-703">%LOCALAPPDATA%\Microsoft\Windows\Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-704">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-704">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-705">CSIDL_INTERNET_CACHE</span><span class="sxs-lookup"><span data-stu-id="4139d-705">CSIDL_INTERNET_CACHE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-706">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-706">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-707">Temporary Internet Files</span><span class="sxs-lookup"><span data-stu-id="4139d-707">Temporary Internet Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-708">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-708">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-709">%USERPROFILE%\Local Settings\Temporary Internet Files</span><span class="sxs-lookup"><span data-stu-id="4139d-709">%USERPROFILE%\Local Settings\Temporary Internet Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_InternetFolder"></span><span id="folderid_internetfolder"></span><span id="FOLDERID_INTERNETFOLDER"></span><dl> <span data-ttu-id="4139d-710"><dt><strong>FOLDERID_InternetFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-710"><dt><strong>FOLDERID_InternetFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-711">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-711">GUID</span></span></td>
<td><span data-ttu-id="4139d-712">{4D9F7874-4E0C-4904-967B-40B0D20C3E4B}</span><span class="sxs-lookup"><span data-stu-id="4139d-712">{4D9F7874-4E0C-4904-967B-40B0D20C3E4B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-713">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-713">Display Name</span></span></td>
<td><span data-ttu-id="4139d-714">網際網路</span><span class="sxs-lookup"><span data-stu-id="4139d-714">The Internet</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-715">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-715">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-716">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-716">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-717">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-717">Default Path</span></span></td>
<td><span data-ttu-id="4139d-718">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-718">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-719">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-719">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-720">CSIDL_INTERNET</span><span class="sxs-lookup"><span data-stu-id="4139d-720">CSIDL_INTERNET</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-721">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-721">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-722">Internet Explorer</span><span class="sxs-lookup"><span data-stu-id="4139d-722">Internet Explorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-723">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-723">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-724">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-724">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Libraries"></span><span id="folderid_libraries"></span><span id="FOLDERID_LIBRARIES"></span><dl> <span data-ttu-id="4139d-725"><dt><strong>FOLDERID_Libraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-725"><dt><strong>FOLDERID_Libraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-726">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-726">GUID</span></span></td>
<td><span data-ttu-id="4139d-727">{1B3EA5DC-B587-4786-B4EF-BD1DC332AEAE}</span><span class="sxs-lookup"><span data-stu-id="4139d-727">{1B3EA5DC-B587-4786-B4EF-BD1DC332AEAE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-728">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-728">Display Name</span></span></td>
<td><span data-ttu-id="4139d-729">程式庫</span><span class="sxs-lookup"><span data-stu-id="4139d-729">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-730">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-730">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-731">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-731">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-732">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-732">Default Path</span></span></td>
<td><span data-ttu-id="4139d-733">%APPDATA%\Microsoft\Windows\Libraries</span><span class="sxs-lookup"><span data-stu-id="4139d-733">%APPDATA%\Microsoft\Windows\Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-734">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-734">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-735">無，在 Windows 7 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-735">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-736">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-736">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-737">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-737">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-738">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-738">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-739">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-739">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Links"></span><span id="folderid_links"></span><span id="FOLDERID_LINKS"></span><dl> <span data-ttu-id="4139d-740"><dt><strong>FOLDERID_Links</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-740"><dt><strong>FOLDERID_Links</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-741">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-741">GUID</span></span></td>
<td><span data-ttu-id="4139d-742">{bfb9d5e0-c6a9-404c-b2b2-ae6db6af4968}</span><span class="sxs-lookup"><span data-stu-id="4139d-742">{bfb9d5e0-c6a9-404c-b2b2-ae6db6af4968}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-743">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-743">Display Name</span></span></td>
<td><span data-ttu-id="4139d-744">連結</span><span class="sxs-lookup"><span data-stu-id="4139d-744">Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-745">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-745">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-746">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-746">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-747">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-747">Default Path</span></span></td>
<td><span data-ttu-id="4139d-748">%USERPROFILE%\Links</span><span class="sxs-lookup"><span data-stu-id="4139d-748">%USERPROFILE%\Links</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-749">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-749">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-750">無</span><span class="sxs-lookup"><span data-stu-id="4139d-750">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-751">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-751">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-752">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-752">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-753">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-753">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-754">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-754">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_LocalAppData"></span><span id="folderid_localappdata"></span><span id="FOLDERID_LOCALAPPDATA"></span><dl> <span data-ttu-id="4139d-755"><dt><strong>FOLDERID_LocalAppData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-755"><dt><strong>FOLDERID_LocalAppData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-756">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-756">GUID</span></span></td>
<td><span data-ttu-id="4139d-757">{F1B32785-6FBA-4FCF-9D55-7B8E7F157091}</span><span class="sxs-lookup"><span data-stu-id="4139d-757">{F1B32785-6FBA-4FCF-9D55-7B8E7F157091}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-758">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-758">Display Name</span></span></td>
<td><span data-ttu-id="4139d-759">本機</span><span class="sxs-lookup"><span data-stu-id="4139d-759">Local</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-760">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-760">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-761">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-761">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-762">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-762">Default Path</span></span></td>
<td><span data-ttu-id="4139d-763">% LOCALAPPDATA% (%USERPROFILE%\AppData\Local) </span><span class="sxs-lookup"><span data-stu-id="4139d-763">%LOCALAPPDATA% (%USERPROFILE%\AppData\Local)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-764">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-764">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-765">CSIDL_LOCAL_APPDATA</span><span class="sxs-lookup"><span data-stu-id="4139d-765">CSIDL_LOCAL_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-766">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-766">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-767">應用程式資料</span><span class="sxs-lookup"><span data-stu-id="4139d-767">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-768">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-768">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-769">%USERPROFILE%\Local Settings\Application 資料</span><span class="sxs-lookup"><span data-stu-id="4139d-769">%USERPROFILE%\Local Settings\Application Data</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_LocalAppDataLow"></span><span id="folderid_localappdatalow"></span><span id="FOLDERID_LOCALAPPDATALOW"></span><dl> <span data-ttu-id="4139d-770"><dt><strong>FOLDERID_LocalAppDataLow</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-770"><dt><strong>FOLDERID_LocalAppDataLow</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-771">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-771">GUID</span></span></td>
<td><span data-ttu-id="4139d-772">{A520A1A4-1780-4FF6-BD18-167343C5AF16}</span><span class="sxs-lookup"><span data-stu-id="4139d-772">{A520A1A4-1780-4FF6-BD18-167343C5AF16}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-773">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-773">Display Name</span></span></td>
<td><span data-ttu-id="4139d-774">LocalLow</span><span class="sxs-lookup"><span data-stu-id="4139d-774">LocalLow</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-775">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-775">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-776">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-776">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-777">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-777">Default Path</span></span></td>
<td><span data-ttu-id="4139d-778">%USERPROFILE%\AppData\LocalLow</span><span class="sxs-lookup"><span data-stu-id="4139d-778">%USERPROFILE%\AppData\LocalLow</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-779">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-779">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-780">無</span><span class="sxs-lookup"><span data-stu-id="4139d-780">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-781">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-781">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-782">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-782">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-783">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-783">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-784">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-784">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_LocalizedResourcesDir"></span><span id="folderid_localizedresourcesdir"></span><span id="FOLDERID_LOCALIZEDRESOURCESDIR"></span><dl> <span data-ttu-id="4139d-785"><dt><strong>FOLDERID_LocalizedResourcesDir</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-785"><dt><strong>FOLDERID_LocalizedResourcesDir</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-786">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-786">GUID</span></span></td>
<td><span data-ttu-id="4139d-787">{2A00375E-224C-49DE-B8D1-440DF7EF3DDC}</span><span class="sxs-lookup"><span data-stu-id="4139d-787">{2A00375E-224C-49DE-B8D1-440DF7EF3DDC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-788">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-788">Display Name</span></span></td>
<td><span data-ttu-id="4139d-789">無</span><span class="sxs-lookup"><span data-stu-id="4139d-789">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-790">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-790">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-791">FIXED</span><span class="sxs-lookup"><span data-stu-id="4139d-791">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-792">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-792">Default Path</span></span></td>
<td><span data-ttu-id="4139d-793">%windir%\resources\0409 (字碼頁) </span><span class="sxs-lookup"><span data-stu-id="4139d-793">%windir%\resources\0409 (code page)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-794">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-794">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-795">CSIDL_RESOURCES_LOCALIZED</span><span class="sxs-lookup"><span data-stu-id="4139d-795">CSIDL_RESOURCES_LOCALIZED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-796">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-796">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-797">無</span><span class="sxs-lookup"><span data-stu-id="4139d-797">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-798">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-798">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-799">%windir%\resources\0409 (字碼頁) </span><span class="sxs-lookup"><span data-stu-id="4139d-799">%windir%\resources\0409 (code page)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Music"></span><span id="folderid_music"></span><span id="FOLDERID_MUSIC"></span><dl> <span data-ttu-id="4139d-800"><dt><strong>FOLDERID_Music</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-800"><dt><strong>FOLDERID_Music</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-801">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-801">GUID</span></span></td>
<td><span data-ttu-id="4139d-802">{4BD8D571-6D19-48D3-BE97-422220080E43}</span><span class="sxs-lookup"><span data-stu-id="4139d-802">{4BD8D571-6D19-48D3-BE97-422220080E43}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-803">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-803">Display Name</span></span></td>
<td><span data-ttu-id="4139d-804">音樂</span><span class="sxs-lookup"><span data-stu-id="4139d-804">Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-805">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-805">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-806">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-806">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-807">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-807">Default Path</span></span></td>
<td><span data-ttu-id="4139d-808">%USERPROFILE%\Music</span><span class="sxs-lookup"><span data-stu-id="4139d-808">%USERPROFILE%\Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-809">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-809">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-810">CSIDL_MYMUSIC</span><span class="sxs-lookup"><span data-stu-id="4139d-810">CSIDL_MYMUSIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-811">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-811">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-812">我的音樂</span><span class="sxs-lookup"><span data-stu-id="4139d-812">My Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-813">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-813">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-814">%USERPROFILE%\My Documents\ 我音樂</span><span class="sxs-lookup"><span data-stu-id="4139d-814">%USERPROFILE%\My Documents\My Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_MusicLibrary"></span><span id="folderid_musiclibrary"></span><span id="FOLDERID_MUSICLIBRARY"></span><dl> <span data-ttu-id="4139d-815"><dt><strong>FOLDERID_MusicLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-815"><dt><strong>FOLDERID_MusicLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-816">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-816">GUID</span></span></td>
<td><span data-ttu-id="4139d-817">{2112AB0A-C86A-4FFE-A368-0DE96E47012E}</span><span class="sxs-lookup"><span data-stu-id="4139d-817">{2112AB0A-C86A-4FFE-A368-0DE96E47012E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-818">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-818">Display Name</span></span></td>
<td><span data-ttu-id="4139d-819">音樂</span><span class="sxs-lookup"><span data-stu-id="4139d-819">Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-820">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-820">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-821">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-821">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-822">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-822">Default Path</span></span></td>
<td><span data-ttu-id="4139d-823">%APPDATA%\Microsoft\Windows\Libraries\Music.library-ms</span><span class="sxs-lookup"><span data-stu-id="4139d-823">%APPDATA%\Microsoft\Windows\Libraries\Music.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-824">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-824">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-825">無，在 Windows 7 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-825">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-826">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-826">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-827">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-827">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-828">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-828">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-829">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-829">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_NetHood"></span><span id="folderid_nethood"></span><span id="FOLDERID_NETHOOD"></span><dl> <span data-ttu-id="4139d-830"><dt><strong>FOLDERID_NetHood</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-830"><dt><strong>FOLDERID_NetHood</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-831">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-831">GUID</span></span></td>
<td><span data-ttu-id="4139d-832">{C5ABBF53-E17F-4121-8900-86626FC2C973}</span><span class="sxs-lookup"><span data-stu-id="4139d-832">{C5ABBF53-E17F-4121-8900-86626FC2C973}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-833">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-833">Display Name</span></span></td>
<td><span data-ttu-id="4139d-834">網路快速鍵</span><span class="sxs-lookup"><span data-stu-id="4139d-834">Network Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-835">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-835">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-836">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-836">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-837">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-837">Default Path</span></span></td>
<td><span data-ttu-id="4139d-838">%APPDATA%\Microsoft\Windows\Network 快捷方式</span><span class="sxs-lookup"><span data-stu-id="4139d-838">%APPDATA%\Microsoft\Windows\Network Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-839">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-839">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-840">CSIDL_NETHOOD</span><span class="sxs-lookup"><span data-stu-id="4139d-840">CSIDL_NETHOOD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-841">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-841">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-842">NetHood</span><span class="sxs-lookup"><span data-stu-id="4139d-842">NetHood</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-843">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-843">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-844">%USERPROFILE%\NetHood</span><span class="sxs-lookup"><span data-stu-id="4139d-844">%USERPROFILE%\NetHood</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_NetworkFolder"></span><span id="folderid_networkfolder"></span><span id="FOLDERID_NETWORKFOLDER"></span><dl> <span data-ttu-id="4139d-845"><dt><strong>FOLDERID_NetworkFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-845"><dt><strong>FOLDERID_NetworkFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-846">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-846">GUID</span></span></td>
<td><span data-ttu-id="4139d-847">{D20BEEC4-5CA8-4905-AE3B-BF251EA09B53}</span><span class="sxs-lookup"><span data-stu-id="4139d-847">{D20BEEC4-5CA8-4905-AE3B-BF251EA09B53}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-848">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-848">Display Name</span></span></td>
<td><span data-ttu-id="4139d-849">網路</span><span class="sxs-lookup"><span data-stu-id="4139d-849">Network</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-850">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-850">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-851">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-851">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-852">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-852">Default Path</span></span></td>
<td><span data-ttu-id="4139d-853">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-853">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-854">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-854">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-855">CSIDL_NETWORK，CSIDL_COMPUTERSNEARME</span><span class="sxs-lookup"><span data-stu-id="4139d-855">CSIDL_NETWORK, CSIDL_COMPUTERSNEARME</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-856">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-856">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-857">網路上的芳鄰</span><span class="sxs-lookup"><span data-stu-id="4139d-857">My Network Places</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-858">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-858">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-859">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-859">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Objects3D"></span><span id="folderid_objects3d"></span><span id="FOLDERID_OBJECTS3D"></span><dl> <span data-ttu-id="4139d-860"><dt><strong>FOLDERID_Objects3D</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-860"><dt><strong>FOLDERID_Objects3D</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-861">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-861">GUID</span></span></td>
<td><span data-ttu-id="4139d-862">{31C0DD25-9439-4F12-BF41-7FF4EDA38722}</span><span class="sxs-lookup"><span data-stu-id="4139d-862">{31C0DD25-9439-4F12-BF41-7FF4EDA38722}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-863">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-863">Display Name</span></span></td>
<td><span data-ttu-id="4139d-864">3D 物件</span><span class="sxs-lookup"><span data-stu-id="4139d-864">3D Objects</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-865">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-865">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-866">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-866">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-867">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-867">Default Path</span></span></td>
<td><span data-ttu-id="4139d-868">%USERPROFILE%\3D 物件</span><span class="sxs-lookup"><span data-stu-id="4139d-868">%USERPROFILE%\3D Objects</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-869">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-869">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-870">無，Windows 10 1703 版中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-870">None, value introduced in Windows 10, version 1703</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-871">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-871">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-872">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-872">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-873">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-873">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-874">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-874">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_OriginalImages"></span><span id="folderid_originalimages"></span><span id="FOLDERID_ORIGINALIMAGES"></span><dl> <span data-ttu-id="4139d-875"><dt><strong>FOLDERID_OriginalImages</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-875"><dt><strong>FOLDERID_OriginalImages</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-876">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-876">GUID</span></span></td>
<td><span data-ttu-id="4139d-877">{2C36C0AA-5812-4b87-BFD0-4CD0DFB19B39}</span><span class="sxs-lookup"><span data-stu-id="4139d-877">{2C36C0AA-5812-4b87-BFD0-4CD0DFB19B39}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-878">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-878">Display Name</span></span></td>
<td><span data-ttu-id="4139d-879">原始影像</span><span class="sxs-lookup"><span data-stu-id="4139d-879">Original Images</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-880">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-880">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-881">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-881">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-882">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-882">Default Path</span></span></td>
<td><span data-ttu-id="4139d-883">%LOCALAPPDATA%\Microsoft\Windows 相片 Gallery\Original 影像</span><span class="sxs-lookup"><span data-stu-id="4139d-883">%LOCALAPPDATA%\Microsoft\Windows Photo Gallery\Original Images</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-884">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-884">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-885">無，在 Windows Vista 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-885">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-886">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-886">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-887">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-887">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-888">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-888">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-889">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-889">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PhotoAlbums"></span><span id="folderid_photoalbums"></span><span id="FOLDERID_PHOTOALBUMS"></span><dl> <span data-ttu-id="4139d-890"><dt><strong>FOLDERID_PhotoAlbums</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-890"><dt><strong>FOLDERID_PhotoAlbums</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-891">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-891">GUID</span></span></td>
<td><span data-ttu-id="4139d-892">{69D2CF90-FC33-4FB7-9A0C-EBB0F0FCB43C}</span><span class="sxs-lookup"><span data-stu-id="4139d-892">{69D2CF90-FC33-4FB7-9A0C-EBB0F0FCB43C}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-893">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-893">Display Name</span></span></td>
<td><span data-ttu-id="4139d-894">幻燈片</span><span class="sxs-lookup"><span data-stu-id="4139d-894">Slide Shows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-895">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-895">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-896">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-896">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-897">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-897">Default Path</span></span></td>
<td><span data-ttu-id="4139d-898">%USERPROFILE%\Pictures\Slide 顯示</span><span class="sxs-lookup"><span data-stu-id="4139d-898">%USERPROFILE%\Pictures\Slide Shows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-899">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-899">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-900">無，在 Windows Vista 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-900">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-901">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-901">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-902">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-902">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-903">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-903">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-904">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-904">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PicturesLibrary"></span><span id="folderid_pictureslibrary"></span><span id="FOLDERID_PICTURESLIBRARY"></span><dl> <span data-ttu-id="4139d-905"><dt><strong>FOLDERID_PicturesLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-905"><dt><strong>FOLDERID_PicturesLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-906">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-906">GUID</span></span></td>
<td><span data-ttu-id="4139d-907">{A990AE9F-A03B-4E80-94BC-9912D7504104}</span><span class="sxs-lookup"><span data-stu-id="4139d-907">{A990AE9F-A03B-4E80-94BC-9912D7504104}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-908">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-908">Display Name</span></span></td>
<td><span data-ttu-id="4139d-909">圖片</span><span class="sxs-lookup"><span data-stu-id="4139d-909">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-910">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-910">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-911">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-911">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-912">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-912">Default Path</span></span></td>
<td><span data-ttu-id="4139d-913">%APPDATA%\Microsoft\Windows\Libraries\Pictures.library-ms</span><span class="sxs-lookup"><span data-stu-id="4139d-913">%APPDATA%\Microsoft\Windows\Libraries\Pictures.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-914">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-914">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-915">無，在 Windows 7 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-915">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-916">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-916">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-917">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-917">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-918">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-918">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-919">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-919">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Pictures"></span><span id="folderid_pictures"></span><span id="FOLDERID_PICTURES"></span><dl> <span data-ttu-id="4139d-920"><dt><strong>FOLDERID_Pictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-920"><dt><strong>FOLDERID_Pictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-921">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-921">GUID</span></span></td>
<td><span data-ttu-id="4139d-922">{33E28130-4E1E-4676-835A-98395C3BC3BB}</span><span class="sxs-lookup"><span data-stu-id="4139d-922">{33E28130-4E1E-4676-835A-98395C3BC3BB}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-923">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-923">Display Name</span></span></td>
<td><span data-ttu-id="4139d-924">圖片</span><span class="sxs-lookup"><span data-stu-id="4139d-924">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-925">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-925">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-926">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-926">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-927">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-927">Default Path</span></span></td>
<td><span data-ttu-id="4139d-928">%USERPROFILE%\Pictures</span><span class="sxs-lookup"><span data-stu-id="4139d-928">%USERPROFILE%\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-929">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-929">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-930">CSIDL_MYPICTURES</span><span class="sxs-lookup"><span data-stu-id="4139d-930">CSIDL_MYPICTURES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-931">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-931">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-932">我的圖片</span><span class="sxs-lookup"><span data-stu-id="4139d-932">My Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-933">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-933">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-934">%USERPROFILE%\My Documents\ 我圖片</span><span class="sxs-lookup"><span data-stu-id="4139d-934">%USERPROFILE%\My Documents\My Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Playlists"></span><span id="folderid_playlists"></span><span id="FOLDERID_PLAYLISTS"></span><dl> <span data-ttu-id="4139d-935"><dt><strong>FOLDERID_Playlists</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-935"><dt><strong>FOLDERID_Playlists</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-936">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-936">GUID</span></span></td>
<td><span data-ttu-id="4139d-937">{DE92C1C7-837F-4F69-A3BB-86E631204A23}</span><span class="sxs-lookup"><span data-stu-id="4139d-937">{DE92C1C7-837F-4F69-A3BB-86E631204A23}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-938">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-938">Display Name</span></span></td>
<td><span data-ttu-id="4139d-939">播放清單</span><span class="sxs-lookup"><span data-stu-id="4139d-939">Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-940">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-940">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-941">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-941">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-942">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-942">Default Path</span></span></td>
<td><span data-ttu-id="4139d-943">%USERPROFILE%\Music\Playlists</span><span class="sxs-lookup"><span data-stu-id="4139d-943">%USERPROFILE%\Music\Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-944">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-944">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-945">無</span><span class="sxs-lookup"><span data-stu-id="4139d-945">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-946">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-946">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-947">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-947">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-948">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-948">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-949">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-949">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PrintersFolder"></span><span id="folderid_printersfolder"></span><span id="FOLDERID_PRINTERSFOLDER"></span><dl> <span data-ttu-id="4139d-950"><dt><strong>FOLDERID_PrintersFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-950"><dt><strong>FOLDERID_PrintersFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-951">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-951">GUID</span></span></td>
<td><span data-ttu-id="4139d-952">{76FC4E2D-D6AD-4519-A663-37BD56068185}</span><span class="sxs-lookup"><span data-stu-id="4139d-952">{76FC4E2D-D6AD-4519-A663-37BD56068185}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-953">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-953">Display Name</span></span></td>
<td><span data-ttu-id="4139d-954">印表機</span><span class="sxs-lookup"><span data-stu-id="4139d-954">Printers</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-955">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-955">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-956">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-956">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-957">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-957">Default Path</span></span></td>
<td><span data-ttu-id="4139d-958">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-958">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-959">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-959">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-960">CSIDL_PRINTERS</span><span class="sxs-lookup"><span data-stu-id="4139d-960">CSIDL_PRINTERS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-961">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-961">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-962">印表機和傳真</span><span class="sxs-lookup"><span data-stu-id="4139d-962">Printers and Faxes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-963">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-963">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-964">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-964">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PrintHood"></span><span id="folderid_printhood"></span><span id="FOLDERID_PRINTHOOD"></span><dl> <span data-ttu-id="4139d-965"><dt><strong>FOLDERID_PrintHood</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-965"><dt><strong>FOLDERID_PrintHood</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-966">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-966">GUID</span></span></td>
<td><span data-ttu-id="4139d-967">{9274BD8D-CFD1-41C3-B35E-B13F55A758F4}</span><span class="sxs-lookup"><span data-stu-id="4139d-967">{9274BD8D-CFD1-41C3-B35E-B13F55A758F4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-968">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-968">Display Name</span></span></td>
<td><span data-ttu-id="4139d-969">印表機快捷方式</span><span class="sxs-lookup"><span data-stu-id="4139d-969">Printer Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-970">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-970">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-971">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-971">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-972">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-972">Default Path</span></span></td>
<td><span data-ttu-id="4139d-973">%APPDATA%\Microsoft\Windows\Printer 快捷方式</span><span class="sxs-lookup"><span data-stu-id="4139d-973">%APPDATA%\Microsoft\Windows\Printer Shortcuts</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-974">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-974">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-975">CSIDL_PRINTHOOD</span><span class="sxs-lookup"><span data-stu-id="4139d-975">CSIDL_PRINTHOOD</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-976">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-976">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-977">PrintHood</span><span class="sxs-lookup"><span data-stu-id="4139d-977">PrintHood</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-978">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-978">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-979">%USERPROFILE%\PrintHood</span><span class="sxs-lookup"><span data-stu-id="4139d-979">%USERPROFILE%\PrintHood</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Profile"></span><span id="folderid_profile"></span><span id="FOLDERID_PROFILE"></span><dl> <span data-ttu-id="4139d-980"><dt><strong>FOLDERID_Profile</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-980"><dt><strong>FOLDERID_Profile</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-981">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-981">GUID</span></span></td>
<td><span data-ttu-id="4139d-982">{5E6C858F-0E22-4760-9AFE-EA3317B67173}</span><span class="sxs-lookup"><span data-stu-id="4139d-982">{5E6C858F-0E22-4760-9AFE-EA3317B67173}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-983">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-983">Display Name</span></span></td>
<td><span data-ttu-id="4139d-984">使用者的使用者名稱 (% USERNAME% ) </span><span class="sxs-lookup"><span data-stu-id="4139d-984">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-985">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-985">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-986">FIXED</span><span class="sxs-lookup"><span data-stu-id="4139d-986">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-987">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-987">Default Path</span></span></td>
<td><span data-ttu-id="4139d-988">% USERPROFILE% (%SystemDrive%\Users \% USERNAME% ) </span><span class="sxs-lookup"><span data-stu-id="4139d-988">%USERPROFILE% (%SystemDrive%\Users\%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-989">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-989">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-990">CSIDL_PROFILE</span><span class="sxs-lookup"><span data-stu-id="4139d-990">CSIDL_PROFILE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-991">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-991">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-992">使用者的使用者名稱 (% USERNAME% ) </span><span class="sxs-lookup"><span data-stu-id="4139d-992">The user's username (%USERNAME%)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-993">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-993">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-994">% USERPROFILE% (%Systemdrive%\documents and 和設定 \% USERNAME% ) </span><span class="sxs-lookup"><span data-stu-id="4139d-994">%USERPROFILE% (%SystemDrive%\Documents and Settings\%USERNAME%)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramData"></span><span id="folderid_programdata"></span><span id="FOLDERID_PROGRAMDATA"></span><dl> <span data-ttu-id="4139d-995"><dt><strong>FOLDERID_ProgramData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-995"><dt><strong>FOLDERID_ProgramData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-996">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-996">GUID</span></span></td>
<td><span data-ttu-id="4139d-997">{62AB5D82-FDC1-4DC3-A9DD-070D1D495D97}</span><span class="sxs-lookup"><span data-stu-id="4139d-997">{62AB5D82-FDC1-4DC3-A9DD-070D1D495D97}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-998">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-998">Display Name</span></span></td>
<td><span data-ttu-id="4139d-999">ProgramData</span><span class="sxs-lookup"><span data-stu-id="4139d-999">ProgramData</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1000">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1000">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1001">FIXED</span><span class="sxs-lookup"><span data-stu-id="4139d-1001">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1002">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1002">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1003">% ALLUSERSPROFILE% (% ProgramData%，%SystemDrive%\ProgramData) </span><span class="sxs-lookup"><span data-stu-id="4139d-1003">%ALLUSERSPROFILE% (%ProgramData%, %SystemDrive%\ProgramData)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1004">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1004">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1005">CSIDL_COMMON_APPDATA</span><span class="sxs-lookup"><span data-stu-id="4139d-1005">CSIDL_COMMON_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1006">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1006">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1007">應用程式資料</span><span class="sxs-lookup"><span data-stu-id="4139d-1007">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1008">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1008">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1009">%ALLUSERSPROFILE%\Application 資料</span><span class="sxs-lookup"><span data-stu-id="4139d-1009">%ALLUSERSPROFILE%\Application Data</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFiles"></span><span id="folderid_programfiles"></span><span id="FOLDERID_PROGRAMFILES"></span><dl> <span data-ttu-id="4139d-1010"><dt><strong>FOLDERID_ProgramFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1010"><dt><strong>FOLDERID_ProgramFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4139d-1011">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="4139d-1011">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1012">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1012">GUID</span></span></td>
<td><span data-ttu-id="4139d-1013">{905e63b6-c1bf-494e-b29c-65b732d3d21a}</span><span class="sxs-lookup"><span data-stu-id="4139d-1013">{905e63b6-c1bf-494e-b29c-65b732d3d21a}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1014">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1014">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1015">Program Files</span><span class="sxs-lookup"><span data-stu-id="4139d-1015">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1016">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1016">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1017">FIXED</span><span class="sxs-lookup"><span data-stu-id="4139d-1017">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1018">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1018">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1019">% ProgramFiles% (%SystemDrive%\Program 檔) </span><span class="sxs-lookup"><span data-stu-id="4139d-1019">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1020">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1020">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1021">CSIDL_PROGRAM_FILES</span><span class="sxs-lookup"><span data-stu-id="4139d-1021">CSIDL_PROGRAM_FILES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1022">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1022">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1023">Program Files</span><span class="sxs-lookup"><span data-stu-id="4139d-1023">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1024">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1024">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1025">% ProgramFiles% (%SystemDrive%\Program 檔) </span><span class="sxs-lookup"><span data-stu-id="4139d-1025">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesX64"></span><span id="folderid_programfilesx64"></span><span id="FOLDERID_PROGRAMFILESX64"></span><dl> <span data-ttu-id="4139d-1026"><dt><strong>FOLDERID_ProgramFilesX64</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1026"><dt><strong>FOLDERID_ProgramFilesX64</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4139d-1027">32位的作業系統不支援此值。</span><span class="sxs-lookup"><span data-stu-id="4139d-1027">This value is not supported on 32-bit operating systems.</span></span> <span data-ttu-id="4139d-1028">在64位作業系統上執行的32位應用程式也不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="4139d-1028">It also is not supported for 32-bit applications running on 64-bit operating systems.</span></span> <span data-ttu-id="4139d-1029">在任一種情況下嘗試使用 FOLDERID_ProgramFilesX64 都會導致錯誤。</span><span class="sxs-lookup"><span data-stu-id="4139d-1029">Attempting to use FOLDERID_ProgramFilesX64 in either situation results in an error.</span></span> <span data-ttu-id="4139d-1030">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="4139d-1030">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1031">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1031">GUID</span></span></td>
<td><span data-ttu-id="4139d-1032">{6D809377-6AF0-444b-8957-A3773F02200E}</span><span class="sxs-lookup"><span data-stu-id="4139d-1032">{6D809377-6AF0-444b-8957-A3773F02200E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1033">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1033">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1034">Program Files</span><span class="sxs-lookup"><span data-stu-id="4139d-1034">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1035">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1035">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1036">FIXED</span><span class="sxs-lookup"><span data-stu-id="4139d-1036">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1037">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1037">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1038">% ProgramFiles% (%SystemDrive%\Program 檔) </span><span class="sxs-lookup"><span data-stu-id="4139d-1038">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1039">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1039">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1040">無</span><span class="sxs-lookup"><span data-stu-id="4139d-1040">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1041">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1041">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1042">Program Files</span><span class="sxs-lookup"><span data-stu-id="4139d-1042">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1043">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1043">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1044">% ProgramFiles% (%SystemDrive%\Program 檔) </span><span class="sxs-lookup"><span data-stu-id="4139d-1044">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesX86"></span><span id="folderid_programfilesx86"></span><span id="FOLDERID_PROGRAMFILESX86"></span><dl> <span data-ttu-id="4139d-1045"><dt><strong>FOLDERID_ProgramFilesX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1045"><dt><strong>FOLDERID_ProgramFilesX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4139d-1046">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="4139d-1046">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1047">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1047">GUID</span></span></td>
<td><span data-ttu-id="4139d-1048">{7C5A40EF-A0FB-4BFC-874A-C0F2E0B9FA8E}</span><span class="sxs-lookup"><span data-stu-id="4139d-1048">{7C5A40EF-A0FB-4BFC-874A-C0F2E0B9FA8E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1049">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1049">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1050">Program Files</span><span class="sxs-lookup"><span data-stu-id="4139d-1050">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1051">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1051">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1052">FIXED</span><span class="sxs-lookup"><span data-stu-id="4139d-1052">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1053">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1053">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1054">% ProgramFiles% (%SystemDrive%\Program 檔) </span><span class="sxs-lookup"><span data-stu-id="4139d-1054">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1055">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1055">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1056">CSIDL_PROGRAM_FILESX86</span><span class="sxs-lookup"><span data-stu-id="4139d-1056">CSIDL_PROGRAM_FILESX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1057">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1057">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1058">Program Files</span><span class="sxs-lookup"><span data-stu-id="4139d-1058">Program Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1059">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1059">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1060">% ProgramFiles% (%SystemDrive%\Program 檔) </span><span class="sxs-lookup"><span data-stu-id="4139d-1060">%ProgramFiles% (%SystemDrive%\Program Files)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommon"></span><span id="folderid_programfilescommon"></span><span id="FOLDERID_PROGRAMFILESCOMMON"></span><dl> <span data-ttu-id="4139d-1061"><dt><strong>FOLDERID_ProgramFilesCommon</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1061"><dt><strong>FOLDERID_ProgramFilesCommon</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4139d-1062">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="4139d-1062">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1063">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1063">GUID</span></span></td>
<td><span data-ttu-id="4139d-1064">{F7F1ED05-9F6D-47A2-AAAE-29D317C6F066}</span><span class="sxs-lookup"><span data-stu-id="4139d-1064">{F7F1ED05-9F6D-47A2-AAAE-29D317C6F066}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1065">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1065">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1066">一般檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-1066">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1067">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1067">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1068">FIXED</span><span class="sxs-lookup"><span data-stu-id="4139d-1068">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1069">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1069">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1070">%ProgramFiles%\Common 檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-1070">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1071">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1071">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1072">CSIDL_PROGRAM_FILES_COMMON</span><span class="sxs-lookup"><span data-stu-id="4139d-1072">CSIDL_PROGRAM_FILES_COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1073">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1073">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1074">一般檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-1074">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1075">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1075">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1076">%ProgramFiles%\Common 檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-1076">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommonX64"></span><span id="folderid_programfilescommonx64"></span><span id="FOLDERID_PROGRAMFILESCOMMONX64"></span><dl> <span data-ttu-id="4139d-1077"><dt><strong>FOLDERID_ProgramFilesCommonX64</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1077"><dt><strong>FOLDERID_ProgramFilesCommonX64</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4139d-1078">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="4139d-1078">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1079">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1079">GUID</span></span></td>
<td><span data-ttu-id="4139d-1080">{6365D5A7-0F0D-45E5-87F6-0DA56B6A4F7D}</span><span class="sxs-lookup"><span data-stu-id="4139d-1080">{6365D5A7-0F0D-45E5-87F6-0DA56B6A4F7D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1081">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1081">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1082">一般檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-1082">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1083">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1083">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1084">FIXED</span><span class="sxs-lookup"><span data-stu-id="4139d-1084">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1085">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1085">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1086">%ProgramFiles%\Common 檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-1086">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1087">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1087">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1088">無</span><span class="sxs-lookup"><span data-stu-id="4139d-1088">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1089">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1089">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1090">一般檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-1090">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1091">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1091">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1092">%ProgramFiles%\Common 檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-1092">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ProgramFilesCommonX86"></span><span id="folderid_programfilescommonx86"></span><span id="FOLDERID_PROGRAMFILESCOMMONX86"></span><dl> <span data-ttu-id="4139d-1093"><dt><strong>FOLDERID_ProgramFilesCommonX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1093"><dt><strong>FOLDERID_ProgramFilesCommonX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4139d-1094">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="4139d-1094">See Remarks for more information.</span></span></p>

<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1095">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1095">GUID</span></span></td>
<td><span data-ttu-id="4139d-1096">{DE974D24-D9C6-4D3E-BF91-F4455120B917}</span><span class="sxs-lookup"><span data-stu-id="4139d-1096">{DE974D24-D9C6-4D3E-BF91-F4455120B917}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1097">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1097">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1098">一般檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-1098">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1099">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1099">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1100">FIXED</span><span class="sxs-lookup"><span data-stu-id="4139d-1100">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1101">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1101">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1102">%ProgramFiles%\Common 檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-1102">%ProgramFiles%\Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1103">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1103">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1104">CSIDL_PROGRAM_FILES_COMMONX86</span><span class="sxs-lookup"><span data-stu-id="4139d-1104">CSIDL_PROGRAM_FILES_COMMONX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1105">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1105">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1106">一般檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-1106">Common Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1107">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1107">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1108">%ProgramFiles%\Common 檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-1108">%ProgramFiles%\Common Files</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Programs"></span><span id="folderid_programs"></span><span id="FOLDERID_PROGRAMS"></span><dl> <span data-ttu-id="4139d-1109"><dt><strong>FOLDERID_Programs</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1109"><dt><strong>FOLDERID_Programs</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1110">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1110">GUID</span></span></td>
<td><span data-ttu-id="4139d-1111">{A77F5D77-2E2B-44C3-A6A2-ABA601054A51}</span><span class="sxs-lookup"><span data-stu-id="4139d-1111">{A77F5D77-2E2B-44C3-A6A2-ABA601054A51}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1112">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1112">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1113">程式</span><span class="sxs-lookup"><span data-stu-id="4139d-1113">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1114">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1114">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1115">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1115">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1116">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1116">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1117">%APPDATA%\Microsoft\Windows\Start Menu\Programs</span><span class="sxs-lookup"><span data-stu-id="4139d-1117">%APPDATA%\Microsoft\Windows\Start Menu\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1118">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1118">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1119">CSIDL_PROGRAMS</span><span class="sxs-lookup"><span data-stu-id="4139d-1119">CSIDL_PROGRAMS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1120">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1120">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1121">程式</span><span class="sxs-lookup"><span data-stu-id="4139d-1121">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1122">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1122">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1123">%USERPROFILE%\Start Menu\Programs</span><span class="sxs-lookup"><span data-stu-id="4139d-1123">%USERPROFILE%\Start Menu\Programs</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Public"></span><span id="folderid_public"></span><span id="FOLDERID_PUBLIC"></span><dl> <span data-ttu-id="4139d-1124"><dt><strong>FOLDERID_Public</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1124"><dt><strong>FOLDERID_Public</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1125">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1125">GUID</span></span></td>
<td><span data-ttu-id="4139d-1126">{DFDF76A2-C82A-4D63-906A-5644AC457385}</span><span class="sxs-lookup"><span data-stu-id="4139d-1126">{DFDF76A2-C82A-4D63-906A-5644AC457385}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1127">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1127">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1128">公開</span><span class="sxs-lookup"><span data-stu-id="4139d-1128">Public</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1129">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1129">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1130">FIXED</span><span class="sxs-lookup"><span data-stu-id="4139d-1130">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1131">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1131">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1132">% PUBLIC% (%SystemDrive%\Users\Public) </span><span class="sxs-lookup"><span data-stu-id="4139d-1132">%PUBLIC% (%SystemDrive%\Users\Public)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1133">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1133">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1134">無，Windows Vista 的新內容</span><span class="sxs-lookup"><span data-stu-id="4139d-1134">None, new for Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1135">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1135">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1136">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1136">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1137">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1137">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1138">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1138">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicDesktop"></span><span id="folderid_publicdesktop"></span><span id="FOLDERID_PUBLICDESKTOP"></span><dl> <span data-ttu-id="4139d-1139"><dt><strong>FOLDERID_PublicDesktop</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1139"><dt><strong>FOLDERID_PublicDesktop</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1140">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1140">GUID</span></span></td>
<td><span data-ttu-id="4139d-1141">{C4AA340D-F20F-4863-AFEF-F87EF2E6BA25}</span><span class="sxs-lookup"><span data-stu-id="4139d-1141">{C4AA340D-F20F-4863-AFEF-F87EF2E6BA25}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1142">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1142">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1143">公用桌面</span><span class="sxs-lookup"><span data-stu-id="4139d-1143">Public Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1144">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1144">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1145">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-1145">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1146">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1146">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1147">%PUBLIC%\Desktop</span><span class="sxs-lookup"><span data-stu-id="4139d-1147">%PUBLIC%\Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1148">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1148">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1149">CSIDL_COMMON_DESKTOPDIRECTORY</span><span class="sxs-lookup"><span data-stu-id="4139d-1149">CSIDL_COMMON_DESKTOPDIRECTORY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1150">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1150">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1151">桌面</span><span class="sxs-lookup"><span data-stu-id="4139d-1151">Desktop</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1152">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1152">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1153">%ALLUSERSPROFILE%\Desktop</span><span class="sxs-lookup"><span data-stu-id="4139d-1153">%ALLUSERSPROFILE%\Desktop</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicDocuments"></span><span id="folderid_publicdocuments"></span><span id="FOLDERID_PUBLICDOCUMENTS"></span><dl> <span data-ttu-id="4139d-1154"><dt><strong>FOLDERID_PublicDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1154"><dt><strong>FOLDERID_PublicDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1155">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1155">GUID</span></span></td>
<td><span data-ttu-id="4139d-1156">{ED4824AF-DCE4-45A8-81E2-FC7965083634}</span><span class="sxs-lookup"><span data-stu-id="4139d-1156">{ED4824AF-DCE4-45A8-81E2-FC7965083634}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1157">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1157">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1158">公開文件</span><span class="sxs-lookup"><span data-stu-id="4139d-1158">Public Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1159">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1159">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1160">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-1160">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1161">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1161">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1162">%PUBLIC%\Documents</span><span class="sxs-lookup"><span data-stu-id="4139d-1162">%PUBLIC%\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1163">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1163">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1164">CSIDL_COMMON_DOCUMENTS</span><span class="sxs-lookup"><span data-stu-id="4139d-1164">CSIDL_COMMON_DOCUMENTS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1165">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1165">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1166">共用文件</span><span class="sxs-lookup"><span data-stu-id="4139d-1166">Shared Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1167">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1167">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1168">%ALLUSERSPROFILE%\Documents</span><span class="sxs-lookup"><span data-stu-id="4139d-1168">%ALLUSERSPROFILE%\Documents</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicDownloads"></span><span id="folderid_publicdownloads"></span><span id="FOLDERID_PUBLICDOWNLOADS"></span><dl> <span data-ttu-id="4139d-1169"><dt><strong>FOLDERID_PublicDownloads</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1169"><dt><strong>FOLDERID_PublicDownloads</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1170">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1170">GUID</span></span></td>
<td><span data-ttu-id="4139d-1171">{3D644C9B-1FB8-4f30-9B45-F670235F79C0}</span><span class="sxs-lookup"><span data-stu-id="4139d-1171">{3D644C9B-1FB8-4f30-9B45-F670235F79C0}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1172">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1172">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1173">公用下載</span><span class="sxs-lookup"><span data-stu-id="4139d-1173">Public Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1174">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1174">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1175">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-1175">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1176">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1176">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1177">%PUBLIC%\Downloads</span><span class="sxs-lookup"><span data-stu-id="4139d-1177">%PUBLIC%\Downloads</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1178">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1178">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1179">無，在 Windows Vista 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-1179">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1180">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1180">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1181">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1181">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1182">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1182">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1183">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1183">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicGameTasks"></span><span id="folderid_publicgametasks"></span><span id="FOLDERID_PUBLICGAMETASKS"></span><dl> <span data-ttu-id="4139d-1184"><dt><strong>FOLDERID_PublicGameTasks</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1184"><dt><strong>FOLDERID_PublicGameTasks</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1185">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1185">GUID</span></span></td>
<td><span data-ttu-id="4139d-1186">{DEBF2536-E1A8-4c59-B6A2-414586476AEA}</span><span class="sxs-lookup"><span data-stu-id="4139d-1186">{DEBF2536-E1A8-4c59-B6A2-414586476AEA}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1187">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1187">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1188">GameExplorer</span><span class="sxs-lookup"><span data-stu-id="4139d-1188">GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1189">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1189">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1190">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-1190">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1191">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1191">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1192">%ALLUSERSPROFILE%\Microsoft\Windows\GameExplorer</span><span class="sxs-lookup"><span data-stu-id="4139d-1192">%ALLUSERSPROFILE%\Microsoft\Windows\GameExplorer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1193">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1193">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1194">無，在 Windows Vista 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-1194">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1195">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1195">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1196">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1196">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1197">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1197">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1198">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1198">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicLibraries"></span><span id="folderid_publiclibraries"></span><span id="FOLDERID_PUBLICLIBRARIES"></span><dl> <span data-ttu-id="4139d-1199"><dt><strong>FOLDERID_PublicLibraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1199"><dt><strong>FOLDERID_PublicLibraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1200">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1200">GUID</span></span></td>
<td><span data-ttu-id="4139d-1201">{48DAF80B-E6CF-4F4E-B800-0E69D84EE384}</span><span class="sxs-lookup"><span data-stu-id="4139d-1201">{48DAF80B-E6CF-4F4E-B800-0E69D84EE384}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1202">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1202">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1203">程式庫</span><span class="sxs-lookup"><span data-stu-id="4139d-1203">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1204">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1204">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1205">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-1205">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1206">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1206">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1207">%ALLUSERSPROFILE%\Microsoft\Windows\Libraries</span><span class="sxs-lookup"><span data-stu-id="4139d-1207">%ALLUSERSPROFILE%\Microsoft\Windows\Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1208">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1208">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1209">無，在 Windows 7 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-1209">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1210">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1210">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1211">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1211">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1212">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1212">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1213">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1213">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicMusic"></span><span id="folderid_publicmusic"></span><span id="FOLDERID_PUBLICMUSIC"></span><dl> <span data-ttu-id="4139d-1214"><dt><strong>FOLDERID_PublicMusic</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1214"><dt><strong>FOLDERID_PublicMusic</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1215">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1215">GUID</span></span></td>
<td><span data-ttu-id="4139d-1216">{3214FAB5-9757-4298-BB61-92A9DEAA44FF}</span><span class="sxs-lookup"><span data-stu-id="4139d-1216">{3214FAB5-9757-4298-BB61-92A9DEAA44FF}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1217">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1217">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1218">公用音樂</span><span class="sxs-lookup"><span data-stu-id="4139d-1218">Public Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1219">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1219">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1220">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-1220">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1221">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1221">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1222">%PUBLIC%\Music</span><span class="sxs-lookup"><span data-stu-id="4139d-1222">%PUBLIC%\Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1223">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1223">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1224">CSIDL_COMMON_MUSIC</span><span class="sxs-lookup"><span data-stu-id="4139d-1224">CSIDL_COMMON_MUSIC</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1225">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1225">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1226">共用音樂</span><span class="sxs-lookup"><span data-stu-id="4139d-1226">Shared Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1227">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1227">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1228">%ALLUSERSPROFILE%\Documents\My 音樂</span><span class="sxs-lookup"><span data-stu-id="4139d-1228">%ALLUSERSPROFILE%\Documents\My Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicPictures"></span><span id="folderid_publicpictures"></span><span id="FOLDERID_PUBLICPICTURES"></span><dl> <span data-ttu-id="4139d-1229"><dt><strong>FOLDERID_PublicPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1229"><dt><strong>FOLDERID_PublicPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1230">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1230">GUID</span></span></td>
<td><span data-ttu-id="4139d-1231">{B6EBFB86-6907-413C-9AF7-4FC2ABF07CC5}</span><span class="sxs-lookup"><span data-stu-id="4139d-1231">{B6EBFB86-6907-413C-9AF7-4FC2ABF07CC5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1232">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1232">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1233">公用圖片</span><span class="sxs-lookup"><span data-stu-id="4139d-1233">Public Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1234">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1234">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1235">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-1235">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1236">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1236">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1237">%PUBLIC%\Pictures</span><span class="sxs-lookup"><span data-stu-id="4139d-1237">%PUBLIC%\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1238">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1238">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1239">CSIDL_COMMON_PICTURES</span><span class="sxs-lookup"><span data-stu-id="4139d-1239">CSIDL_COMMON_PICTURES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1240">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1240">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1241">共用圖片</span><span class="sxs-lookup"><span data-stu-id="4139d-1241">Shared Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1242">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1242">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1243">%ALLUSERSPROFILE%\Documents\My 圖片</span><span class="sxs-lookup"><span data-stu-id="4139d-1243">%ALLUSERSPROFILE%\Documents\My Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicRingtones"></span><span id="folderid_publicringtones"></span><span id="FOLDERID_PUBLICRINGTONES"></span><dl> <span data-ttu-id="4139d-1244"><dt><strong>FOLDERID_PublicRingtones</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1244"><dt><strong>FOLDERID_PublicRingtones</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1245">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1245">GUID</span></span></td>
<td><span data-ttu-id="4139d-1246">{E555AB60-153B-4D17-9F04-A5FE99FC15EC}</span><span class="sxs-lookup"><span data-stu-id="4139d-1246">{E555AB60-153B-4D17-9F04-A5FE99FC15EC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1247">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1247">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1248">鈴聲</span><span class="sxs-lookup"><span data-stu-id="4139d-1248">Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1249">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1249">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1250">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-1250">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1251">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1251">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1252">%ALLUSERSPROFILE%\Microsoft\Windows\Ringtones</span><span class="sxs-lookup"><span data-stu-id="4139d-1252">%ALLUSERSPROFILE%\Microsoft\Windows\Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1253">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1253">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1254">無，在 Windows 7 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-1254">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1255">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1255">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1256">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1256">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1257">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1257">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1258">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1258">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_PublicUserTiles"></span><span id="folderid_publicusertiles"></span><span id="FOLDERID_PUBLICUSERTILES"></span><dl> <span data-ttu-id="4139d-1259"><dt><strong>FOLDERID_PublicUserTiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1259"><dt><strong>FOLDERID_PublicUserTiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1260">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1260">GUID</span></span></td>
<td><span data-ttu-id="4139d-1261">{0482af6c-08f1-4c34-8c90-e17ec98b1e17}</span><span class="sxs-lookup"><span data-stu-id="4139d-1261">{0482af6c-08f1-4c34-8c90-e17ec98b1e17}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1262">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1262">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1263">公用帳戶圖片</span><span class="sxs-lookup"><span data-stu-id="4139d-1263">Public Account Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1264">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1264">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1265">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-1265">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1266">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1266">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1267">%PUBLIC%\AccountPictures</span><span class="sxs-lookup"><span data-stu-id="4139d-1267">%PUBLIC%\AccountPictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1268">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1268">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1269">無，Windows 8 中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-1269">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1270">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1270">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1271">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1271">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1272">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1272">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1273">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1273">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_PublicVideos"></span><span id="folderid_publicvideos"></span><span id="FOLDERID_PUBLICVIDEOS"></span><dl> <span data-ttu-id="4139d-1274"><dt><strong>FOLDERID_PublicVideos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1274"><dt><strong>FOLDERID_PublicVideos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1275">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1275">GUID</span></span></td>
<td><span data-ttu-id="4139d-1276">{2400183A-6185-49FB-A2D8-4A392A602BA3}</span><span class="sxs-lookup"><span data-stu-id="4139d-1276">{2400183A-6185-49FB-A2D8-4A392A602BA3}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1277">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1277">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1278">公用影片</span><span class="sxs-lookup"><span data-stu-id="4139d-1278">Public Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1279">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1279">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1280">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-1280">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1281">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1281">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1282">%PUBLIC%\Videos</span><span class="sxs-lookup"><span data-stu-id="4139d-1282">%PUBLIC%\Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1283">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1283">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1284">CSIDL_COMMON_VIDEO</span><span class="sxs-lookup"><span data-stu-id="4139d-1284">CSIDL_COMMON_VIDEO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1285">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1285">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1286">共用影片</span><span class="sxs-lookup"><span data-stu-id="4139d-1286">Shared Video</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1287">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1287">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1288">%ALLUSERSPROFILE%\Documents\My 影片</span><span class="sxs-lookup"><span data-stu-id="4139d-1288">%ALLUSERSPROFILE%\Documents\My Videos</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_QuickLaunch"></span><span id="folderid_quicklaunch"></span><span id="FOLDERID_QUICKLAUNCH"></span><dl> <span data-ttu-id="4139d-1289"><dt><strong>FOLDERID_QuickLaunch</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1289"><dt><strong>FOLDERID_QuickLaunch</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1290">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1290">GUID</span></span></td>
<td><span data-ttu-id="4139d-1291">{52a4f021-7b75-48a9-9f6b-4b87a210bc8f}</span><span class="sxs-lookup"><span data-stu-id="4139d-1291">{52a4f021-7b75-48a9-9f6b-4b87a210bc8f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1292">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1292">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1293">快速啟動</span><span class="sxs-lookup"><span data-stu-id="4139d-1293">Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1294">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1294">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1295">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1295">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1296">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1296">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1297">%APPDATA%\Microsoft\Internet Explorer\Quick 啟動</span><span class="sxs-lookup"><span data-stu-id="4139d-1297">%APPDATA%\Microsoft\Internet Explorer\Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1298">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1298">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1299">無</span><span class="sxs-lookup"><span data-stu-id="4139d-1299">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1300">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1300">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1301">快速啟動</span><span class="sxs-lookup"><span data-stu-id="4139d-1301">Quick Launch</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1302">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1302">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1303">%APPDATA%\Microsoft\Internet Explorer\Quick 啟動</span><span class="sxs-lookup"><span data-stu-id="4139d-1303">%APPDATA%\Microsoft\Internet Explorer\Quick Launch</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_Recent"></span><span id="folderid_recent"></span><span id="FOLDERID_RECENT"></span><dl> <span data-ttu-id="4139d-1304"><dt><strong>FOLDERID_Recent</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1304"><dt><strong>FOLDERID_Recent</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1305">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1305">GUID</span></span></td>
<td><span data-ttu-id="4139d-1306">{AE50C081-EBD2-438A-8655-8A092E34987A}</span><span class="sxs-lookup"><span data-stu-id="4139d-1306">{AE50C081-EBD2-438A-8655-8A092E34987A}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1307">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1307">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1308">最近的項目</span><span class="sxs-lookup"><span data-stu-id="4139d-1308">Recent Items</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1309">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1309">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1310">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1310">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1311">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1311">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1312">%APPDATA%\Microsoft\Windows\Recent</span><span class="sxs-lookup"><span data-stu-id="4139d-1312">%APPDATA%\Microsoft\Windows\Recent</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1313">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1313">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1314">CSIDL_RECENT</span><span class="sxs-lookup"><span data-stu-id="4139d-1314">CSIDL_RECENT</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1315">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1315">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1316">最近使用的檔</span><span class="sxs-lookup"><span data-stu-id="4139d-1316">My Recent Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1317">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1317">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1318">%USERPROFILE%\Recent</span><span class="sxs-lookup"><span data-stu-id="4139d-1318">%USERPROFILE%\Recent</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RecordedTV"></span><span id="folderid_recordedtv"></span><span id="FOLDERID_RECORDEDTV"></span><dl> <span data-ttu-id="4139d-1319"><dt><strong>FOLDERID_RecordedTV</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1319"><dt><strong>FOLDERID_RecordedTV</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4139d-1320">未使用。</span><span class="sxs-lookup"><span data-stu-id="4139d-1320">Not used.</span></span> <span data-ttu-id="4139d-1321">在 Windows 7 中，此值未定義。</span><span class="sxs-lookup"><span data-stu-id="4139d-1321">This value is undefined as of Windows 7.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RecordedTVLibrary"></span><span id="folderid_recordedtvlibrary"></span><span id="FOLDERID_RECORDEDTVLIBRARY"></span><dl> <span data-ttu-id="4139d-1322"><dt><strong>FOLDERID_RecordedTVLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1322"><dt><strong>FOLDERID_RecordedTVLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1323">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1323">GUID</span></span></td>
<td><span data-ttu-id="4139d-1324">{1A6FDBA2-F42D-4358-A798-B74D745926C5}</span><span class="sxs-lookup"><span data-stu-id="4139d-1324">{1A6FDBA2-F42D-4358-A798-B74D745926C5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1325">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1325">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1326">錄製的節目</span><span class="sxs-lookup"><span data-stu-id="4139d-1326">Recorded TV</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1327">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1327">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1328">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-1328">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1329">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1329">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1330">%PUBLIC%\RecordedTV.library-ms</span><span class="sxs-lookup"><span data-stu-id="4139d-1330">%PUBLIC%\RecordedTV.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1331">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1331">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1332">無，在 Windows 7 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-1332">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1333">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1333">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1334">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1334">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1335">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1335">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1336">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1336">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RecycleBinFolder"></span><span id="folderid_recyclebinfolder"></span><span id="FOLDERID_RECYCLEBINFOLDER"></span><dl> <span data-ttu-id="4139d-1337"><dt><strong>FOLDERID_RecycleBinFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1337"><dt><strong>FOLDERID_RecycleBinFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1338">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1338">GUID</span></span></td>
<td><span data-ttu-id="4139d-1339">{B7534046-3ECB-4C18-BE4E-64CD4CB7D6AC}</span><span class="sxs-lookup"><span data-stu-id="4139d-1339">{B7534046-3ECB-4C18-BE4E-64CD4CB7D6AC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1340">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1340">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1341">資源回收筒</span><span class="sxs-lookup"><span data-stu-id="4139d-1341">Recycle Bin</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1342">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1342">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1343">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-1343">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1344">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1344">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1345">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-1345">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1346">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1346">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1347">CSIDL_BITBUCKET</span><span class="sxs-lookup"><span data-stu-id="4139d-1347">CSIDL_BITBUCKET</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1348">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1348">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1349">資源回收筒</span><span class="sxs-lookup"><span data-stu-id="4139d-1349">Recycle Bin</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1350">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1350">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1351">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-1351">Not applicable—virtual folder</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_ResourceDir"></span><span id="folderid_resourcedir"></span><span id="FOLDERID_RESOURCEDIR"></span><dl> <span data-ttu-id="4139d-1352"><dt><strong>FOLDERID_ResourceDir</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1352"><dt><strong>FOLDERID_ResourceDir</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1353">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1353">GUID</span></span></td>
<td><span data-ttu-id="4139d-1354">{8AD10C31-2ADB-4296-A8F7-E4701232C972}</span><span class="sxs-lookup"><span data-stu-id="4139d-1354">{8AD10C31-2ADB-4296-A8F7-E4701232C972}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1355">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1355">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1356">資源</span><span class="sxs-lookup"><span data-stu-id="4139d-1356">Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1357">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1357">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1358">FIXED</span><span class="sxs-lookup"><span data-stu-id="4139d-1358">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1359">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1359">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1360">%windir%\Resources</span><span class="sxs-lookup"><span data-stu-id="4139d-1360">%windir%\Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1361">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1361">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1362">CSIDL_RESOURCES</span><span class="sxs-lookup"><span data-stu-id="4139d-1362">CSIDL_RESOURCES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1363">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1363">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1364">資源</span><span class="sxs-lookup"><span data-stu-id="4139d-1364">Resources</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1365">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1365">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1366">%windir%\Resources</span><span class="sxs-lookup"><span data-stu-id="4139d-1366">%windir%\Resources</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Ringtones"></span><span id="folderid_ringtones"></span><span id="FOLDERID_RINGTONES"></span><dl> <span data-ttu-id="4139d-1367"><dt><strong>FOLDERID_Ringtones</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1367"><dt><strong>FOLDERID_Ringtones</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1368">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1368">GUID</span></span></td>
<td><span data-ttu-id="4139d-1369">{C870044B-F49E-4126-A9C3-B52A1FF411E8}</span><span class="sxs-lookup"><span data-stu-id="4139d-1369">{C870044B-F49E-4126-A9C3-B52A1FF411E8}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1370">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1370">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1371">鈴聲</span><span class="sxs-lookup"><span data-stu-id="4139d-1371">Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1372">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1372">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1373">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1373">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1374">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1374">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1375">%LOCALAPPDATA%\Microsoft\Windows\Ringtones</span><span class="sxs-lookup"><span data-stu-id="4139d-1375">%LOCALAPPDATA%\Microsoft\Windows\Ringtones</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1376">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1376">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1377">無，在 Windows 7 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-1377">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1378">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1378">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1379">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1379">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1380">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1380">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1381">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1381">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RoamingAppData"></span><span id="folderid_roamingappdata"></span><span id="FOLDERID_ROAMINGAPPDATA"></span><dl> <span data-ttu-id="4139d-1382"><dt><strong>FOLDERID_RoamingAppData</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1382"><dt><strong>FOLDERID_RoamingAppData</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1383">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1383">GUID</span></span></td>
<td><span data-ttu-id="4139d-1384">{3EB685DB-65F9-4CF6-A03A-E3EF65729F3D}</span><span class="sxs-lookup"><span data-stu-id="4139d-1384">{3EB685DB-65F9-4CF6-A03A-E3EF65729F3D}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1385">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1385">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1386">漫遊</span><span class="sxs-lookup"><span data-stu-id="4139d-1386">Roaming</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1387">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1387">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1388">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1388">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1389">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1389">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1390">% APPDATA% (%USERPROFILE%\AppData\Roaming) </span><span class="sxs-lookup"><span data-stu-id="4139d-1390">%APPDATA% (%USERPROFILE%\AppData\Roaming)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1391">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1391">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1392">CSIDL_APPDATA</span><span class="sxs-lookup"><span data-stu-id="4139d-1392">CSIDL_APPDATA</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1393">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1393">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1394">應用程式資料</span><span class="sxs-lookup"><span data-stu-id="4139d-1394">Application Data</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1395">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1395">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1396">% APPDATA% (%USERPROFILE%\Application 資料) </span><span class="sxs-lookup"><span data-stu-id="4139d-1396">%APPDATA% (%USERPROFILE%\Application Data)</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_RoamedTileImages"></span><span id="folderid_roamedtileimages"></span><span id="FOLDERID_ROAMEDTILEIMAGES"></span><dl> <span data-ttu-id="4139d-1397"><dt><strong>FOLDERID_RoamedTileImages</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1397"><dt><strong>FOLDERID_RoamedTileImages</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1398">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1398">GUID</span></span></td>
<td><span data-ttu-id="4139d-1399">{AAA8D5A5-F1D6-4259-BAA8-78E7EF60835E}</span><span class="sxs-lookup"><span data-stu-id="4139d-1399">{AAA8D5A5-F1D6-4259-BAA8-78E7EF60835E}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1400">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1400">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1401">RoamedTileImages</span><span class="sxs-lookup"><span data-stu-id="4139d-1401">RoamedTileImages</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1402">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1402">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1403">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1403">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1404">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1404">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1405">%LOCALAPPDATA%\Microsoft\Windows\RoamedTileImages</span><span class="sxs-lookup"><span data-stu-id="4139d-1405">%LOCALAPPDATA%\Microsoft\Windows\RoamedTileImages</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1406">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1406">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1407">無，Windows 8 中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-1407">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1408">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1408">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1409">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1409">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1410">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1410">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1411">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1411">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_RoamingTiles"></span><span id="folderid_roamingtiles"></span><span id="FOLDERID_ROAMINGTILES"></span><dl> <span data-ttu-id="4139d-1412"><dt><strong>FOLDERID_RoamingTiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1412"><dt><strong>FOLDERID_RoamingTiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1413">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1413">GUID</span></span></td>
<td><span data-ttu-id="4139d-1414">{00BCFC5A-ED94-4e48-96A1-3F6217F21990}</span><span class="sxs-lookup"><span data-stu-id="4139d-1414">{00BCFC5A-ED94-4e48-96A1-3F6217F21990}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1415">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1415">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1416">RoamingTiles</span><span class="sxs-lookup"><span data-stu-id="4139d-1416">RoamingTiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1417">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1417">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1418">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1418">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1419">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1419">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1420">%LOCALAPPDATA%\Microsoft\Windows\RoamingTiles</span><span class="sxs-lookup"><span data-stu-id="4139d-1420">%LOCALAPPDATA%\Microsoft\Windows\RoamingTiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1421">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1421">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1422">無，Windows 8 中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-1422">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1423">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1423">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1424">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1424">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1425">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1425">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1426">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1426">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SampleMusic"></span><span id="folderid_samplemusic"></span><span id="FOLDERID_SAMPLEMUSIC"></span><dl> <span data-ttu-id="4139d-1427"><dt><strong>FOLDERID_SampleMusic</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1427"><dt><strong>FOLDERID_SampleMusic</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1428">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1428">GUID</span></span></td>
<td><span data-ttu-id="4139d-1429">{B250C668-F57D-4EE1-A63C-290EE7D1AA1F}</span><span class="sxs-lookup"><span data-stu-id="4139d-1429">{B250C668-F57D-4EE1-A63C-290EE7D1AA1F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1430">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1430">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1431">範例音樂</span><span class="sxs-lookup"><span data-stu-id="4139d-1431">Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1432">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1432">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1433">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-1433">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1434">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1434">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1435">%PUBLIC%\Music\Sample 音樂</span><span class="sxs-lookup"><span data-stu-id="4139d-1435">%PUBLIC%\Music\Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1436">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1436">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1437">無</span><span class="sxs-lookup"><span data-stu-id="4139d-1437">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1438">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1438">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1439">範例音樂</span><span class="sxs-lookup"><span data-stu-id="4139d-1439">Sample Music</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1440">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1440">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1441">%ALLUSERSPROFILE%\Documents\My Music\Sample 音樂</span><span class="sxs-lookup"><span data-stu-id="4139d-1441">%ALLUSERSPROFILE%\Documents\My Music\Sample Music</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SamplePictures"></span><span id="folderid_samplepictures"></span><span id="FOLDERID_SAMPLEPICTURES"></span><dl> <span data-ttu-id="4139d-1442"><dt><strong>FOLDERID_SamplePictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1442"><dt><strong>FOLDERID_SamplePictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1443">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1443">GUID</span></span></td>
<td><span data-ttu-id="4139d-1444">{C4900540-2379-4C75-844B-64E6FAF8716B}</span><span class="sxs-lookup"><span data-stu-id="4139d-1444">{C4900540-2379-4C75-844B-64E6FAF8716B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1445">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1445">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1446">範例圖片</span><span class="sxs-lookup"><span data-stu-id="4139d-1446">Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1447">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1447">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1448">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-1448">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1449">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1449">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1450">%PUBLIC%\Pictures\Sample 圖片</span><span class="sxs-lookup"><span data-stu-id="4139d-1450">%PUBLIC%\Pictures\Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1451">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1451">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1452">無</span><span class="sxs-lookup"><span data-stu-id="4139d-1452">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1453">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1453">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1454">範例圖片</span><span class="sxs-lookup"><span data-stu-id="4139d-1454">Sample Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1455">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1455">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1456">%ALLUSERSPROFILE%\Documents\My 圖片 \ 範例圖片</span><span class="sxs-lookup"><span data-stu-id="4139d-1456">%ALLUSERSPROFILE%\Documents\My Pictures\Sample Pictures</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SamplePlaylists"></span><span id="folderid_sampleplaylists"></span><span id="FOLDERID_SAMPLEPLAYLISTS"></span><dl> <span data-ttu-id="4139d-1457"><dt><strong>FOLDERID_SamplePlaylists</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1457"><dt><strong>FOLDERID_SamplePlaylists</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1458">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1458">GUID</span></span></td>
<td><span data-ttu-id="4139d-1459">{15CA69B3-30EE-49C1-ACE1-6B5EC372AFB5}</span><span class="sxs-lookup"><span data-stu-id="4139d-1459">{15CA69B3-30EE-49C1-ACE1-6B5EC372AFB5}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1460">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1460">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1461">範例播放清單</span><span class="sxs-lookup"><span data-stu-id="4139d-1461">Sample Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1462">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1462">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1463">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-1463">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1464">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1464">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1465">%PUBLIC%\Music\Sample 播放清單</span><span class="sxs-lookup"><span data-stu-id="4139d-1465">%PUBLIC%\Music\Sample Playlists</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1466">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1466">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1467">無，在 Windows Vista 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-1467">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1468">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1468">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1469">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1469">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1470">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1470">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1471">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1471">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SampleVideos"></span><span id="folderid_samplevideos"></span><span id="FOLDERID_SAMPLEVIDEOS"></span><dl> <span data-ttu-id="4139d-1472"><dt><strong>FOLDERID_SampleVideos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1472"><dt><strong>FOLDERID_SampleVideos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1473">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1473">GUID</span></span></td>
<td><span data-ttu-id="4139d-1474">{859EAD94-2E85-48AD-A71A-0969CB56A6CD}</span><span class="sxs-lookup"><span data-stu-id="4139d-1474">{859EAD94-2E85-48AD-A71A-0969CB56A6CD}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1475">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1475">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1476">範例影片</span><span class="sxs-lookup"><span data-stu-id="4139d-1476">Sample Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1477">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1477">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1478">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-1478">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1479">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1479">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1480">%PUBLIC%\Videos\Sample 影片</span><span class="sxs-lookup"><span data-stu-id="4139d-1480">%PUBLIC%\Videos\Sample Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1481">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1481">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1482">無</span><span class="sxs-lookup"><span data-stu-id="4139d-1482">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1483">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1483">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1484">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1484">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1485">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1485">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1486">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1486">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SavedGames"></span><span id="folderid_savedgames"></span><span id="FOLDERID_SAVEDGAMES"></span><dl> <span data-ttu-id="4139d-1487"><dt><strong>FOLDERID_SavedGames</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1487"><dt><strong>FOLDERID_SavedGames</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1488">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1488">GUID</span></span></td>
<td><span data-ttu-id="4139d-1489">{4C5C32FF-BB9D-43b0-B5B4-2D72E54EAAA4}</span><span class="sxs-lookup"><span data-stu-id="4139d-1489">{4C5C32FF-BB9D-43b0-B5B4-2D72E54EAAA4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1490">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1490">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1491">儲存的遊戲</span><span class="sxs-lookup"><span data-stu-id="4139d-1491">Saved Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1492">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1492">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1493">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1493">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1494">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1494">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1495">%USERPROFILE%\Saved 遊戲</span><span class="sxs-lookup"><span data-stu-id="4139d-1495">%USERPROFILE%\Saved Games</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1496">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1496">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1497">無，在 Windows Vista 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-1497">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1498">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1498">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1499">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1499">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1500">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1500">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1501">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1501">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SavedPictures"></span><span id="folderid_savedpictures"></span><span id="FOLDERID_SAVEDPICTURES"></span><dl> <span data-ttu-id="4139d-1502"><dt><strong>FOLDERID_SavedPictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1502"><dt><strong>FOLDERID_SavedPictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1503">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1503">GUID</span></span></td>
<td><span data-ttu-id="4139d-1504">{3B193882-D3AD-4eab-965A-69829D1FB59F}</span><span class="sxs-lookup"><span data-stu-id="4139d-1504">{3B193882-D3AD-4eab-965A-69829D1FB59F}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1505">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1505">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1506">儲存的圖片</span><span class="sxs-lookup"><span data-stu-id="4139d-1506">Saved Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1507">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1507">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1508">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1508">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1509">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1509">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1510">%USERPROFILE%\Pictures\Saved 圖片</span><span class="sxs-lookup"><span data-stu-id="4139d-1510">%USERPROFILE%\Pictures\Saved Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1511">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1511">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1512">無</span><span class="sxs-lookup"><span data-stu-id="4139d-1512">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1513">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1513">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1514">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1514">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1515">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1515">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1516">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1516">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SavedPicturesLibrary"></span><span id="folderid_savedpictureslibrary"></span><span id="FOLDERID_SAVEDPICTURESLIBRARY"></span><dl> <span data-ttu-id="4139d-1517"><dt><strong>FOLDERID_SavedPicturesLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1517"><dt><strong>FOLDERID_SavedPicturesLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1518">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1518">GUID</span></span></td>
<td><span data-ttu-id="4139d-1519">{E25B5812-BE88-4bd9-94B0-29233477B6C3}</span><span class="sxs-lookup"><span data-stu-id="4139d-1519">{E25B5812-BE88-4bd9-94B0-29233477B6C3}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1520">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1520">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1521">儲存的圖片媒體櫃</span><span class="sxs-lookup"><span data-stu-id="4139d-1521">Saved Pictures Library</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1522">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1522">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1523">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1523">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1524">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1524">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1525">%APPDATE%\Microsoft\Windows\Libraries\SavedPictures.library-ms</span><span class="sxs-lookup"><span data-stu-id="4139d-1525">%APPDATE%\Microsoft\Windows\Libraries\SavedPictures.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1526">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1526">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1527">無</span><span class="sxs-lookup"><span data-stu-id="4139d-1527">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1528">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1528">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1529">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1529">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1530">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1530">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1531">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1531">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SavedSearches"></span><span id="folderid_savedsearches"></span><span id="FOLDERID_SAVEDSEARCHES"></span><dl> <span data-ttu-id="4139d-1532"><dt><strong>FOLDERID_SavedSearches</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1532"><dt><strong>FOLDERID_SavedSearches</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1533">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1533">GUID</span></span></td>
<td><span data-ttu-id="4139d-1534">{7d1d3a04-debb-4115-95cf-2f29da2920da}</span><span class="sxs-lookup"><span data-stu-id="4139d-1534">{7d1d3a04-debb-4115-95cf-2f29da2920da}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1535">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1535">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1536">搜尋</span><span class="sxs-lookup"><span data-stu-id="4139d-1536">Searches</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1537">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1537">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1538">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1538">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1539">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1539">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1540">%USERPROFILE%\Searches</span><span class="sxs-lookup"><span data-stu-id="4139d-1540">%USERPROFILE%\Searches</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1541">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1541">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1542">無</span><span class="sxs-lookup"><span data-stu-id="4139d-1542">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1543">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1543">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1544">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1544">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1545">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1545">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1546">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1546">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Screenshots"></span><span id="folderid_screenshots"></span><span id="FOLDERID_SCREENSHOTS"></span><dl> <span data-ttu-id="4139d-1547"><dt><strong>FOLDERID_Screenshots</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1547"><dt><strong>FOLDERID_Screenshots</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1548">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1548">GUID</span></span></td>
<td><span data-ttu-id="4139d-1549">{b7bede81-df94-4682-a7d8-57a52620b86f}</span><span class="sxs-lookup"><span data-stu-id="4139d-1549">{b7bede81-df94-4682-a7d8-57a52620b86f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1550">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1550">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1551">螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="4139d-1551">Screenshots</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1552">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1552">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1553">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1553">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1554">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1554">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1555">%USERPROFILE%\Pictures\Screenshots</span><span class="sxs-lookup"><span data-stu-id="4139d-1555">%USERPROFILE%\Pictures\Screenshots</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1556">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1556">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1557">無，Windows 8 中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-1557">None, value introduced in Windows 8</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1558">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1558">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1559">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1559">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1560">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1560">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1561">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1561">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SEARCH_CSC"></span><span id="folderid_search_csc"></span><dl> <span data-ttu-id="4139d-1562"><dt><strong>FOLDERID_SEARCH_CSC</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1562"><dt><strong>FOLDERID_SEARCH_CSC</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1563">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1563">GUID</span></span></td>
<td><span data-ttu-id="4139d-1564">{ee32e446-31ca-4aba-814f-a5ebd2fd6d5e}</span><span class="sxs-lookup"><span data-stu-id="4139d-1564">{ee32e446-31ca-4aba-814f-a5ebd2fd6d5e}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1565">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1565">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1566">離線檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-1566">Offline Files</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1567">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1567">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1568">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-1568">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1569">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1569">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1570">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-1570">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1571">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1571">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1572">無</span><span class="sxs-lookup"><span data-stu-id="4139d-1572">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1573">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1573">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1574">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1574">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1575">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1575">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1576">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1576">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SearchHistory"></span><span id="folderid_searchhistory"></span><span id="FOLDERID_SEARCHHISTORY"></span><dl> <span data-ttu-id="4139d-1577"><dt><strong>FOLDERID_SearchHistory</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1577"><dt><strong>FOLDERID_SearchHistory</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1578">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1578">GUID</span></span></td>
<td><span data-ttu-id="4139d-1579">{0D4C3DB6-03A3-462F-A0E6-08924C41B5D4}</span><span class="sxs-lookup"><span data-stu-id="4139d-1579">{0D4C3DB6-03A3-462F-A0E6-08924C41B5D4}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1580">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1580">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1581">記錄</span><span class="sxs-lookup"><span data-stu-id="4139d-1581">History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1582">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1582">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1583">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1583">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1584">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1584">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1585">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\History</span><span class="sxs-lookup"><span data-stu-id="4139d-1585">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\History</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1586">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1586">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1587">無，Windows 8.1 中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-1587">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1588">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1588">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1589">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1589">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1590">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1590">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1591">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1591">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SearchHome"></span><span id="folderid_searchhome"></span><span id="FOLDERID_SEARCHHOME"></span><dl> <span data-ttu-id="4139d-1592"><dt><strong>FOLDERID_SearchHome</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1592"><dt><strong>FOLDERID_SearchHome</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1593">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1593">GUID</span></span></td>
<td><span data-ttu-id="4139d-1594">{190337d1-b8ca-4121-a639-6d472d16972a}</span><span class="sxs-lookup"><span data-stu-id="4139d-1594">{190337d1-b8ca-4121-a639-6d472d16972a}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1595">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1595">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1596">搜尋結果</span><span class="sxs-lookup"><span data-stu-id="4139d-1596">Search Results</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1597">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1597">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1598">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-1598">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1599">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1599">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1600">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-1600">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1601">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1601">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1602">無</span><span class="sxs-lookup"><span data-stu-id="4139d-1602">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1603">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1603">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1604">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1604">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1605">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1605">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1606">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1606">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SEARCH_MAPI"></span><span id="folderid_search_mapi"></span><dl> <span data-ttu-id="4139d-1607"><dt><strong>FOLDERID_SEARCH_MAPI</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1607"><dt><strong>FOLDERID_SEARCH_MAPI</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1608">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1608">GUID</span></span></td>
<td><span data-ttu-id="4139d-1609">{98ec0e18-2098-4d44-8644-66979315a281}</span><span class="sxs-lookup"><span data-stu-id="4139d-1609">{98ec0e18-2098-4d44-8644-66979315a281}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1610">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1610">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1611">Microsoft Office Outlook</span><span class="sxs-lookup"><span data-stu-id="4139d-1611">Microsoft Office Outlook</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1612">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1612">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1613">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-1613">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1614">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1614">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1615">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-1615">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1616">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1616">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1617">無</span><span class="sxs-lookup"><span data-stu-id="4139d-1617">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1618">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1618">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1619">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1619">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1620">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1620">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1621">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1621">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SearchTemplates"></span><span id="folderid_searchtemplates"></span><span id="FOLDERID_SEARCHTEMPLATES"></span><dl> <span data-ttu-id="4139d-1622"><dt><strong>FOLDERID_SearchTemplates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1622"><dt><strong>FOLDERID_SearchTemplates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1623">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1623">GUID</span></span></td>
<td><span data-ttu-id="4139d-1624">{7E636BFE-DFA9-4D5E-B456-D7B39851D8A9}</span><span class="sxs-lookup"><span data-stu-id="4139d-1624">{7E636BFE-DFA9-4D5E-B456-D7B39851D8A9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1625">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1625">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1626">範本</span><span class="sxs-lookup"><span data-stu-id="4139d-1626">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1627">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1627">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1628">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1628">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1629">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1629">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1630">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\Templates</span><span class="sxs-lookup"><span data-stu-id="4139d-1630">%LOCALAPPDATA%\Microsoft\Windows\ConnectedSearch\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1631">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1631">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1632">無，Windows 8.1 中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-1632">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1633">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1633">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1634">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1634">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1635">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1635">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1636">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1636">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SendTo"></span><span id="folderid_sendto"></span><span id="FOLDERID_SENDTO"></span><dl> <span data-ttu-id="4139d-1637"><dt><strong>FOLDERID_SendTo</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1637"><dt><strong>FOLDERID_SendTo</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1638">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1638">GUID</span></span></td>
<td><span data-ttu-id="4139d-1639">{8983036C-27C0-404B-8F08-102D10DCFD74}</span><span class="sxs-lookup"><span data-stu-id="4139d-1639">{8983036C-27C0-404B-8F08-102D10DCFD74}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1640">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1640">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1641">SendTo</span><span class="sxs-lookup"><span data-stu-id="4139d-1641">SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1642">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1642">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1643">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1643">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1644">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1644">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1645">%APPDATA%\Microsoft\Windows\SendTo</span><span class="sxs-lookup"><span data-stu-id="4139d-1645">%APPDATA%\Microsoft\Windows\SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1646">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1646">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1647">CSIDL_SENDTO</span><span class="sxs-lookup"><span data-stu-id="4139d-1647">CSIDL_SENDTO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1648">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1648">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1649">SendTo</span><span class="sxs-lookup"><span data-stu-id="4139d-1649">SendTo</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1650">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1650">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1651">%USERPROFILE%\SendTo</span><span class="sxs-lookup"><span data-stu-id="4139d-1651">%USERPROFILE%\SendTo</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SidebarDefaultParts"></span><span id="folderid_sidebardefaultparts"></span><span id="FOLDERID_SIDEBARDEFAULTPARTS"></span><dl> <span data-ttu-id="4139d-1652"><dt><strong>FOLDERID_SidebarDefaultParts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1652"><dt><strong>FOLDERID_SidebarDefaultParts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1653">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1653">GUID</span></span></td>
<td><span data-ttu-id="4139d-1654">{7B396E54-9EC5-4300-BE0A-2482EBAE1A26}</span><span class="sxs-lookup"><span data-stu-id="4139d-1654">{7B396E54-9EC5-4300-BE0A-2482EBAE1A26}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1655">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1655">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1656">小工具</span><span class="sxs-lookup"><span data-stu-id="4139d-1656">Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1657">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1657">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1658">常見</span><span class="sxs-lookup"><span data-stu-id="4139d-1658">COMMON</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1659">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1659">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1660">%ProgramFiles%\Windows Sidebar\Gadgets</span><span class="sxs-lookup"><span data-stu-id="4139d-1660">%ProgramFiles%\Windows Sidebar\Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1661">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1661">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1662">無，Windows 7 的新內容</span><span class="sxs-lookup"><span data-stu-id="4139d-1662">None, new for Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1663">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1663">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1664">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1664">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1665">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1665">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1666">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1666">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SidebarParts"></span><span id="folderid_sidebarparts"></span><span id="FOLDERID_SIDEBARPARTS"></span><dl> <span data-ttu-id="4139d-1667"><dt><strong>FOLDERID_SidebarParts</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1667"><dt><strong>FOLDERID_SidebarParts</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1668">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1668">GUID</span></span></td>
<td><span data-ttu-id="4139d-1669">{A75D362E-50FC-4fb7-AC2C-A8BEAA314493}</span><span class="sxs-lookup"><span data-stu-id="4139d-1669">{A75D362E-50FC-4fb7-AC2C-A8BEAA314493}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1670">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1670">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1671">小工具</span><span class="sxs-lookup"><span data-stu-id="4139d-1671">Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1672">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1672">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1673">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1673">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1674">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1674">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1675">%LOCALAPPDATA%\Microsoft\Windows Sidebar\Gadgets</span><span class="sxs-lookup"><span data-stu-id="4139d-1675">%LOCALAPPDATA%\Microsoft\Windows Sidebar\Gadgets</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1676">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1676">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1677">無，Windows 7 的新內容</span><span class="sxs-lookup"><span data-stu-id="4139d-1677">None, new for Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1678">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1678">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1679">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1679">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1680">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1680">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1681">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1681">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SkyDrive"></span><span id="folderid_skydrive"></span><span id="FOLDERID_SKYDRIVE"></span><dl> <span data-ttu-id="4139d-1682"><dt><strong>FOLDERID_SkyDrive</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1682"><dt><strong>FOLDERID_SkyDrive</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1683">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1683">GUID</span></span></td>
<td><span data-ttu-id="4139d-1684">{A52BBA46-E9E1-435f-B3D9-28DAA648C0F6}</span><span class="sxs-lookup"><span data-stu-id="4139d-1684">{A52BBA46-E9E1-435f-B3D9-28DAA648C0F6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1685">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1685">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1686">OneDrive</span><span class="sxs-lookup"><span data-stu-id="4139d-1686">OneDrive</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1687">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1687">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1688">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1688">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1689">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1689">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1690">%USERPROFILE%\OneDrive</span><span class="sxs-lookup"><span data-stu-id="4139d-1690">%USERPROFILE%\OneDrive</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1691">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1691">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1692">無，Windows 8.1 中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-1692">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1693">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1693">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1694">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1694">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1695">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1695">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1696">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1696">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SkyDriveCameraRoll"></span><span id="folderid_skydrivecameraroll"></span><span id="FOLDERID_SKYDRIVECAMERAROLL"></span><dl> <span data-ttu-id="4139d-1697"><dt><strong>FOLDERID_SkyDriveCameraRoll</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1697"><dt><strong>FOLDERID_SkyDriveCameraRoll</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1698">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1698">GUID</span></span></td>
<td><span data-ttu-id="4139d-1699">{767E6811-49CB-4273-87C2-20F355E1085B}</span><span class="sxs-lookup"><span data-stu-id="4139d-1699">{767E6811-49CB-4273-87C2-20F355E1085B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1700">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1700">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1701">攝影機滾動</span><span class="sxs-lookup"><span data-stu-id="4139d-1701">Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1702">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1702">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1703">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1703">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1704">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1704">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1705">%USERPROFILE%\OneDrive\Pictures\Camera 匯總</span><span class="sxs-lookup"><span data-stu-id="4139d-1705">%USERPROFILE%\OneDrive\Pictures\Camera Roll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1706">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1706">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1707">無，Windows 8.1 中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-1707">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1708">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1708">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1709">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1709">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1710">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1710">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1711">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1711">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SkyDriveDocuments"></span><span id="folderid_skydrivedocuments"></span><span id="FOLDERID_SKYDRIVEDOCUMENTS"></span><dl> <span data-ttu-id="4139d-1712"><dt><strong>FOLDERID_SkyDriveDocuments</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1712"><dt><strong>FOLDERID_SkyDriveDocuments</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1713">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1713">GUID</span></span></td>
<td><span data-ttu-id="4139d-1714">{24D89E24-2F19-4534-9DDE-6A6671FBB8FE}</span><span class="sxs-lookup"><span data-stu-id="4139d-1714">{24D89E24-2F19-4534-9DDE-6A6671FBB8FE}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1715">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1715">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1716">文件</span><span class="sxs-lookup"><span data-stu-id="4139d-1716">Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1717">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1717">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1718">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1718">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1719">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1719">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1720">%USERPROFILE%\OneDrive\Documents</span><span class="sxs-lookup"><span data-stu-id="4139d-1720">%USERPROFILE%\OneDrive\Documents</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1721">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1721">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1722">無，Windows 8.1 中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-1722">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1723">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1723">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1724">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1724">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1725">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1725">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1726">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1726">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SkyDrivePictures"></span><span id="folderid_skydrivepictures"></span><span id="FOLDERID_SKYDRIVEPICTURES"></span><dl> <span data-ttu-id="4139d-1727"><dt><strong>FOLDERID_SkyDrivePictures</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1727"><dt><strong>FOLDERID_SkyDrivePictures</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1728">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1728">GUID</span></span></td>
<td><span data-ttu-id="4139d-1729">{339719B5-8C47-4894-94C2-D8F77ADD44A6}</span><span class="sxs-lookup"><span data-stu-id="4139d-1729">{339719B5-8C47-4894-94C2-D8F77ADD44A6}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1730">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1730">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1731">圖片</span><span class="sxs-lookup"><span data-stu-id="4139d-1731">Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1732">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1732">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1733">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1733">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1734">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1734">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1735">%USERPROFILE%\OneDrive\Pictures</span><span class="sxs-lookup"><span data-stu-id="4139d-1735">%USERPROFILE%\OneDrive\Pictures</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1736">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1736">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1737">無，Windows 8.1 中引進的值</span><span class="sxs-lookup"><span data-stu-id="4139d-1737">None, value introduced in Windows 8.1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1738">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1738">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1739">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1739">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1740">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1740">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1741">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1741">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_StartMenu"></span><span id="folderid_startmenu"></span><span id="FOLDERID_STARTMENU"></span><dl> <span data-ttu-id="4139d-1742"><dt><strong>FOLDERID_StartMenu</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1742"><dt><strong>FOLDERID_StartMenu</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1743">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1743">GUID</span></span></td>
<td><span data-ttu-id="4139d-1744">{625B53C3-AB48-4EC1-BA1F-A1EF4146FC19}</span><span class="sxs-lookup"><span data-stu-id="4139d-1744">{625B53C3-AB48-4EC1-BA1F-A1EF4146FC19}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1745">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1745">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1746">開始功能表</span><span class="sxs-lookup"><span data-stu-id="4139d-1746">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1747">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1747">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1748">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1748">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1749">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1749">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1750">%APPDATA%\Microsoft\Windows\Start 功能表</span><span class="sxs-lookup"><span data-stu-id="4139d-1750">%APPDATA%\Microsoft\Windows\Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1751">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1751">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1752">CSIDL_STARTMENU</span><span class="sxs-lookup"><span data-stu-id="4139d-1752">CSIDL_STARTMENU</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1753">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1753">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1754">開始功能表</span><span class="sxs-lookup"><span data-stu-id="4139d-1754">Start Menu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1755">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1755">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1756">%USERPROFILE%\Start 功能表</span><span class="sxs-lookup"><span data-stu-id="4139d-1756">%USERPROFILE%\Start Menu</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Startup"></span><span id="folderid_startup"></span><span id="FOLDERID_STARTUP"></span><dl> <span data-ttu-id="4139d-1757"><dt><strong>FOLDERID_Startup</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1757"><dt><strong>FOLDERID_Startup</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1758">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1758">GUID</span></span></td>
<td><span data-ttu-id="4139d-1759">{B97D20BB-F46A-4C97-BA10-5E3608430854}</span><span class="sxs-lookup"><span data-stu-id="4139d-1759">{B97D20BB-F46A-4C97-BA10-5E3608430854}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1760">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1760">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1761">啟動</span><span class="sxs-lookup"><span data-stu-id="4139d-1761">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1762">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1762">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1763">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1763">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1764">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1764">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1765">%APPDATA%\Microsoft\Windows\Start Menu\Programs\StartUp</span><span class="sxs-lookup"><span data-stu-id="4139d-1765">%APPDATA%\Microsoft\Windows\Start Menu\Programs\StartUp</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1766">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1766">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1767">CSIDL_STARTUP，CSIDL_ALTSTARTUP</span><span class="sxs-lookup"><span data-stu-id="4139d-1767">CSIDL_STARTUP, CSIDL_ALTSTARTUP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1768">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1768">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1769">啟動</span><span class="sxs-lookup"><span data-stu-id="4139d-1769">Startup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1770">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1770">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1771">%USERPROFILE%\Start Menu\Programs\StartUp</span><span class="sxs-lookup"><span data-stu-id="4139d-1771">%USERPROFILE%\Start Menu\Programs\StartUp</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SyncManagerFolder"></span><span id="folderid_syncmanagerfolder"></span><span id="FOLDERID_SYNCMANAGERFOLDER"></span><dl> <span data-ttu-id="4139d-1772"><dt><strong>FOLDERID_SyncManagerFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1772"><dt><strong>FOLDERID_SyncManagerFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1773">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1773">GUID</span></span></td>
<td><span data-ttu-id="4139d-1774">{43668BF8-C14E-49B2-97C9-747784D784B7}</span><span class="sxs-lookup"><span data-stu-id="4139d-1774">{43668BF8-C14E-49B2-97C9-747784D784B7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1775">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1775">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1776">同步中心</span><span class="sxs-lookup"><span data-stu-id="4139d-1776">Sync Center</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1777">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1777">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1778">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-1778">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1779">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1779">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1780">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-1780">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1781">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1781">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1782">無，在 Windows Vista 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-1782">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1783">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1783">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1784">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1784">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1785">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1785">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1786">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1786">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_SyncResultsFolder"></span><span id="folderid_syncresultsfolder"></span><span id="FOLDERID_SYNCRESULTSFOLDER"></span><dl> <span data-ttu-id="4139d-1787"><dt><strong>FOLDERID_SyncResultsFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1787"><dt><strong>FOLDERID_SyncResultsFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1788">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1788">GUID</span></span></td>
<td><span data-ttu-id="4139d-1789">{289a9a43-be44-4057-a41b-587a76d7e7f9}</span><span class="sxs-lookup"><span data-stu-id="4139d-1789">{289a9a43-be44-4057-a41b-587a76d7e7f9}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1790">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1790">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1791">同步結果</span><span class="sxs-lookup"><span data-stu-id="4139d-1791">Sync Results</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1792">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1792">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1793">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-1793">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1794">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1794">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1795">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-1795">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1796">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1796">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1797">無，在 Windows Vista 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-1797">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1798">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1798">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1799">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1799">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1800">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1800">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1801">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1801">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SyncSetupFolder"></span><span id="folderid_syncsetupfolder"></span><span id="FOLDERID_SYNCSETUPFOLDER"></span><dl> <span data-ttu-id="4139d-1802"><dt><strong>FOLDERID_SyncSetupFolder</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1802"><dt><strong>FOLDERID_SyncSetupFolder</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1803">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1803">GUID</span></span></td>
<td><span data-ttu-id="4139d-1804">{0F214138-B1D3-4a90-BBA9-27CBC0C5389A}</span><span class="sxs-lookup"><span data-stu-id="4139d-1804">{0F214138-B1D3-4a90-BBA9-27CBC0C5389A}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1805">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1805">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1806">同步設定</span><span class="sxs-lookup"><span data-stu-id="4139d-1806">Sync Setup</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1807">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1807">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1808">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-1808">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1809">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1809">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1810">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-1810">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1811">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1811">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1812">無，在 Windows Vista 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-1812">None, value introduced in Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1813">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1813">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1814">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1814">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1815">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1815">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1816">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1816">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_System"></span><span id="folderid_system"></span><span id="FOLDERID_SYSTEM"></span><dl> <span data-ttu-id="4139d-1817"><dt><strong>FOLDERID_System</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1817"><dt><strong>FOLDERID_System</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1818">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1818">GUID</span></span></td>
<td><span data-ttu-id="4139d-1819">{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}</span><span class="sxs-lookup"><span data-stu-id="4139d-1819">{1AC14E77-02E7-4E5D-B744-2EB1AE5198B7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1820">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1820">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1821">System32</span><span class="sxs-lookup"><span data-stu-id="4139d-1821">System32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1822">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1822">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1823">FIXED</span><span class="sxs-lookup"><span data-stu-id="4139d-1823">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1824">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1824">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1825">%windir%\system32</span><span class="sxs-lookup"><span data-stu-id="4139d-1825">%windir%\system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1826">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1826">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1827">CSIDL_SYSTEM</span><span class="sxs-lookup"><span data-stu-id="4139d-1827">CSIDL_SYSTEM</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1828">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1828">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1829">system32</span><span class="sxs-lookup"><span data-stu-id="4139d-1829">system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1830">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1830">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1831">%windir%\system32</span><span class="sxs-lookup"><span data-stu-id="4139d-1831">%windir%\system32</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_SystemX86"></span><span id="folderid_systemx86"></span><span id="FOLDERID_SYSTEMX86"></span><dl> <span data-ttu-id="4139d-1832"><dt><strong>FOLDERID_SystemX86</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1832"><dt><strong>FOLDERID_SystemX86</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1833">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1833">GUID</span></span></td>
<td><span data-ttu-id="4139d-1834">{D65231B0-B2F1-4857-A4CE-A8E7C6EA7D27}</span><span class="sxs-lookup"><span data-stu-id="4139d-1834">{D65231B0-B2F1-4857-A4CE-A8E7C6EA7D27}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1835">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1835">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1836">System32</span><span class="sxs-lookup"><span data-stu-id="4139d-1836">System32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1837">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1837">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1838">FIXED</span><span class="sxs-lookup"><span data-stu-id="4139d-1838">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1839">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1839">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1840">%windir%\system32</span><span class="sxs-lookup"><span data-stu-id="4139d-1840">%windir%\system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1841">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1841">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1842">CSIDL_SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="4139d-1842">CSIDL_SYSTEMX86</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1843">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1843">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1844">system32</span><span class="sxs-lookup"><span data-stu-id="4139d-1844">system32</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1845">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1845">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1846">%windir%\system32</span><span class="sxs-lookup"><span data-stu-id="4139d-1846">%windir%\system32</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Templates"></span><span id="folderid_templates"></span><span id="FOLDERID_TEMPLATES"></span><dl> <span data-ttu-id="4139d-1847"><dt><strong>FOLDERID_Templates</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1847"><dt><strong>FOLDERID_Templates</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1848">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1848">GUID</span></span></td>
<td><span data-ttu-id="4139d-1849">{A63293E8-664E-48DB-A079-DF759E0509F7}</span><span class="sxs-lookup"><span data-stu-id="4139d-1849">{A63293E8-664E-48DB-A079-DF759E0509F7}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1850">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1850">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1851">範本</span><span class="sxs-lookup"><span data-stu-id="4139d-1851">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1852">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1852">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1853">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1853">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1854">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1854">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1855">%APPDATA%\Microsoft\Windows\Templates</span><span class="sxs-lookup"><span data-stu-id="4139d-1855">%APPDATA%\Microsoft\Windows\Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1856">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1856">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1857">CSIDL_TEMPLATES</span><span class="sxs-lookup"><span data-stu-id="4139d-1857">CSIDL_TEMPLATES</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1858">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1858">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1859">範本</span><span class="sxs-lookup"><span data-stu-id="4139d-1859">Templates</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1860">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1860">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1861">%USERPROFILE%\Templates</span><span class="sxs-lookup"><span data-stu-id="4139d-1861">%USERPROFILE%\Templates</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_TreeProperties"></span><span id="folderid_treeproperties"></span><span id="FOLDERID_TREEPROPERTIES"></span><dl> <span data-ttu-id="4139d-1862"><dt><strong>FOLDERID_TreeProperties</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1862"><dt><strong>FOLDERID_TreeProperties</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="4139d-1863">不是在 Windows Vista 中使用。</span><span class="sxs-lookup"><span data-stu-id="4139d-1863">Not used in Windows Vista.</span></span> <span data-ttu-id="4139d-1864">不支援 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="4139d-1864">Unsupported as of Windows 7.</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UserPinned"></span><span id="folderid_userpinned"></span><span id="FOLDERID_USERPINNED"></span><dl> <span data-ttu-id="4139d-1865"><dt><strong>FOLDERID_UserPinned</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1865"><dt><strong>FOLDERID_UserPinned</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1866">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1866">GUID</span></span></td>
<td><span data-ttu-id="4139d-1867">{9E3995AB-1F9C-4F13-B827-48B24B6C7174}</span><span class="sxs-lookup"><span data-stu-id="4139d-1867">{9E3995AB-1F9C-4F13-B827-48B24B6C7174}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1868">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1868">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1869">使用者釘選</span><span class="sxs-lookup"><span data-stu-id="4139d-1869">User Pinned</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1870">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1870">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1871">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1871">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1872">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1872">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1873">已釘選%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User</span><span class="sxs-lookup"><span data-stu-id="4139d-1873">%APPDATA%\Microsoft\Internet Explorer\Quick Launch\User Pinned</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1874">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1874">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1875">無，在 Windows 7 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-1875">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1876">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1876">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1877">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1877">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1878">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1878">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1879">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1879">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UserProfiles"></span><span id="folderid_userprofiles"></span><span id="FOLDERID_USERPROFILES"></span><dl> <span data-ttu-id="4139d-1880"><dt><strong>FOLDERID_UserProfiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1880"><dt><strong>FOLDERID_UserProfiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1881">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1881">GUID</span></span></td>
<td><span data-ttu-id="4139d-1882">{0762D272-C50A-4BB0-A382-697DCD729B80}</span><span class="sxs-lookup"><span data-stu-id="4139d-1882">{0762D272-C50A-4BB0-A382-697DCD729B80}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1883">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1883">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1884">使用者</span><span class="sxs-lookup"><span data-stu-id="4139d-1884">Users</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1885">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1885">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1886">FIXED</span><span class="sxs-lookup"><span data-stu-id="4139d-1886">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1887">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1887">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1888">%SystemDrive%\Users</span><span class="sxs-lookup"><span data-stu-id="4139d-1888">%SystemDrive%\Users</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1889">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1889">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1890">無，Windows Vista 的新內容</span><span class="sxs-lookup"><span data-stu-id="4139d-1890">None, new for Windows Vista</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1891">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1891">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1892">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1892">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1893">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1893">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1894">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1894">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UserProgramFiles"></span><span id="folderid_userprogramfiles"></span><span id="FOLDERID_USERPROGRAMFILES"></span><dl> <span data-ttu-id="4139d-1895"><dt><strong>FOLDERID_UserProgramFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1895"><dt><strong>FOLDERID_UserProgramFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1896">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1896">GUID</span></span></td>
<td><span data-ttu-id="4139d-1897">{5CD7AEE2-2219-4A67-B85D-6C9CE15660CB}</span><span class="sxs-lookup"><span data-stu-id="4139d-1897">{5CD7AEE2-2219-4A67-B85D-6C9CE15660CB}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1898">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1898">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1899">程式</span><span class="sxs-lookup"><span data-stu-id="4139d-1899">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1900">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1900">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1901">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1901">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1902">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1902">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1903">%LOCALAPPDATA%\Programs</span><span class="sxs-lookup"><span data-stu-id="4139d-1903">%LOCALAPPDATA%\Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1904">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1904">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1905">無，在 Windows 7 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-1905">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1906">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1906">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1907">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1907">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1908">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1908">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1909">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1909">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UserProgramFilesCommon"></span><span id="folderid_userprogramfilescommon"></span><span id="FOLDERID_USERPROGRAMFILESCOMMON"></span><dl> <span data-ttu-id="4139d-1910"><dt><strong>FOLDERID_UserProgramFilesCommon</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1910"><dt><strong>FOLDERID_UserProgramFilesCommon</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1911">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1911">GUID</span></span></td>
<td><span data-ttu-id="4139d-1912">{BCBD3057-CA5C-4622-B42D-BC56DB0AE516}</span><span class="sxs-lookup"><span data-stu-id="4139d-1912">{BCBD3057-CA5C-4622-B42D-BC56DB0AE516}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1913">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1913">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1914">程式</span><span class="sxs-lookup"><span data-stu-id="4139d-1914">Programs</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1915">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1915">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1916">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1916">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1917">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1917">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1918">%LOCALAPPDATA%\Programs\Common</span><span class="sxs-lookup"><span data-stu-id="4139d-1918">%LOCALAPPDATA%\Programs\Common</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1919">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1919">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1920">無，在 Windows 7 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-1920">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1921">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1921">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1922">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1922">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1923">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1923">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1924">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1924">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_UsersFiles"></span><span id="folderid_usersfiles"></span><span id="FOLDERID_USERSFILES"></span><dl> <span data-ttu-id="4139d-1925"><dt><strong>FOLDERID_UsersFiles</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1925"><dt><strong>FOLDERID_UsersFiles</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1926">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1926">GUID</span></span></td>
<td><span data-ttu-id="4139d-1927">{f3ce0f7c-4901-4acc-8648-d5d44b04ef8f}</span><span class="sxs-lookup"><span data-stu-id="4139d-1927">{f3ce0f7c-4901-4acc-8648-d5d44b04ef8f}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1928">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1928">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1929">使用者的完整名稱 (例如，建立使用者帳戶時輸入的 Jean Jean-philippe Bagel) 。</span><span class="sxs-lookup"><span data-stu-id="4139d-1929">The user's full name (for instance, Jean Philippe Bagel) entered when the user account was created.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1930">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1930">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1931">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-1931">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1932">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1932">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1933">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-1933">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1934">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1934">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1935">無</span><span class="sxs-lookup"><span data-stu-id="4139d-1935">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1936">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1936">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1937">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1937">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1938">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1938">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1939">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1939">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_UsersLibraries"></span><span id="folderid_userslibraries"></span><span id="FOLDERID_USERSLIBRARIES"></span><dl> <span data-ttu-id="4139d-1940"><dt><strong>FOLDERID_UsersLibraries</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1940"><dt><strong>FOLDERID_UsersLibraries</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1941">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1941">GUID</span></span></td>
<td><span data-ttu-id="4139d-1942">{A302545D-DEFF-464b-ABE8-61C8648D939B}</span><span class="sxs-lookup"><span data-stu-id="4139d-1942">{A302545D-DEFF-464b-ABE8-61C8648D939B}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1943">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1943">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1944">程式庫</span><span class="sxs-lookup"><span data-stu-id="4139d-1944">Libraries</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1945">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1945">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1946">機器</span><span class="sxs-lookup"><span data-stu-id="4139d-1946">VIRTUAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1947">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1947">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1948">不適用—虛擬資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-1948">Not applicable—virtual folder</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1949">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1949">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1950">無，在 Windows 7 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-1950">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1951">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1951">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1952">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1952">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1953">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1953">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1954">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1954">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Videos"></span><span id="folderid_videos"></span><span id="FOLDERID_VIDEOS"></span><dl> <span data-ttu-id="4139d-1955"><dt><strong>FOLDERID_Videos</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1955"><dt><strong>FOLDERID_Videos</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1956">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1956">GUID</span></span></td>
<td><span data-ttu-id="4139d-1957">{18989B1D-99B5-455B-841C-AB7C74E4DDFC}</span><span class="sxs-lookup"><span data-stu-id="4139d-1957">{18989B1D-99B5-455B-841C-AB7C74E4DDFC}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1958">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1958">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1959">影片</span><span class="sxs-lookup"><span data-stu-id="4139d-1959">Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1960">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1960">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1961">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1961">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1962">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1962">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1963">%USERPROFILE%\Videos</span><span class="sxs-lookup"><span data-stu-id="4139d-1963">%USERPROFILE%\Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1964">CSIDL</span><span class="sxs-lookup"><span data-stu-id="4139d-1964">CSIDL</span></span></td>
<td><span data-ttu-id="4139d-1965">CSIDL_MYVIDEO</span><span class="sxs-lookup"><span data-stu-id="4139d-1965">CSIDL_MYVIDEO</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1966">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1966">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1967">我的影片</span><span class="sxs-lookup"><span data-stu-id="4139d-1967">My Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1968">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1968">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1969">%USERPROFILE%\My Documents\ 我影片</span><span class="sxs-lookup"><span data-stu-id="4139d-1969">%USERPROFILE%\My Documents\My Videos</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FOLDERID_VideosLibrary"></span><span id="folderid_videoslibrary"></span><span id="FOLDERID_VIDEOSLIBRARY"></span><dl> <span data-ttu-id="4139d-1970"><dt><strong>FOLDERID_VideosLibrary</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1970"><dt><strong>FOLDERID_VideosLibrary</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1971">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1971">GUID</span></span></td>
<td><span data-ttu-id="4139d-1972">{491E922F-5643-4AF4-A7EB-4E7A138D8174}</span><span class="sxs-lookup"><span data-stu-id="4139d-1972">{491E922F-5643-4AF4-A7EB-4E7A138D8174}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1973">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1973">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1974">影片</span><span class="sxs-lookup"><span data-stu-id="4139d-1974">Videos</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1975">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1975">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1976">PERUSER</span><span class="sxs-lookup"><span data-stu-id="4139d-1976">PERUSER</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1977">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1977">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1978">%APPDATA%\Microsoft\Windows\Libraries\Videos.library-ms</span><span class="sxs-lookup"><span data-stu-id="4139d-1978">%APPDATA%\Microsoft\Windows\Libraries\Videos.library-ms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1979">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1979">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1980">無，在 Windows 7 中引進的價值</span><span class="sxs-lookup"><span data-stu-id="4139d-1980">None, value introduced in Windows 7</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1981">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1981">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1982">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1982">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1983">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1983">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1984">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-1984">Not applicable</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FOLDERID_Windows"></span><span id="folderid_windows"></span><span id="FOLDERID_WINDOWS"></span><dl> <span data-ttu-id="4139d-1985"><dt><strong>FOLDERID_Windows</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="4139d-1985"><dt><strong>FOLDERID_Windows</strong></dt> </span></span></dl></td>
<td style="text-align: left;">
<table>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4139d-1986">GUID</span><span class="sxs-lookup"><span data-stu-id="4139d-1986">GUID</span></span></td>
<td><span data-ttu-id="4139d-1987">{F38BF404-1D43-42F2-9305-67DE0B28FC23}</span><span class="sxs-lookup"><span data-stu-id="4139d-1987">{F38BF404-1D43-42F2-9305-67DE0B28FC23}</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1988">顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1988">Display Name</span></span></td>
<td><span data-ttu-id="4139d-1989">Windows</span><span class="sxs-lookup"><span data-stu-id="4139d-1989">Windows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1990">資料夾類型</span><span class="sxs-lookup"><span data-stu-id="4139d-1990">Folder Type</span></span></td>
<td><span data-ttu-id="4139d-1991">FIXED</span><span class="sxs-lookup"><span data-stu-id="4139d-1991">FIXED</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1992">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-1992">Default Path</span></span></td>
<td><span data-ttu-id="4139d-1993">windir</span><span class="sxs-lookup"><span data-stu-id="4139d-1993">%windir%</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1994">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-1994">CSIDL Equivalent</span></span></td>
<td><span data-ttu-id="4139d-1995">CSIDL_WINDOWS</span><span class="sxs-lookup"><span data-stu-id="4139d-1995">CSIDL_WINDOWS</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4139d-1996">舊版顯示名稱</span><span class="sxs-lookup"><span data-stu-id="4139d-1996">Legacy Display Name</span></span></td>
<td><span data-ttu-id="4139d-1997">WINDOWS</span><span class="sxs-lookup"><span data-stu-id="4139d-1997">WINDOWS</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4139d-1998">舊版預設路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-1998">Legacy Default Path</span></span></td>
<td><span data-ttu-id="4139d-1999">windir</span><span class="sxs-lookup"><span data-stu-id="4139d-1999">%windir%</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="4139d-2000">備註</span><span class="sxs-lookup"><span data-stu-id="4139d-2000">Remarks</span></span>

<span data-ttu-id="4139d-2001">某些 **KNOWNFOLDERID** 值的解釋取決於資料夾是否為32位或64位應用程式的一部分，以及該應用程式是在32位或64位作業系統上執行。</span><span class="sxs-lookup"><span data-stu-id="4139d-2001">The interpretation of certain **KNOWNFOLDERID** values depends on whether the folder is part of a 32-bit or 64-bit application and whether that application is running on a 32-bit or 64-bit operating system.</span></span> <span data-ttu-id="4139d-2002">如果您的應用程式需要區分 **程式** 檔和 **程式檔 (x86)**，您必須針對此情況使用正確的 **KNOWNFOLDERID** 。</span><span class="sxs-lookup"><span data-stu-id="4139d-2002">If your application needs to distinguish between, for example, **Program Files** and **Program Files (x86)**, you must use the right **KNOWNFOLDERID** for the situation.</span></span>

<span data-ttu-id="4139d-2003">下表摘要說明這些情況下的 **KNOWNFOLDERID** 用法。</span><span class="sxs-lookup"><span data-stu-id="4139d-2003">The following tables summarize the **KNOWNFOLDERID** use in those cases.</span></span>


<span data-ttu-id="4139d-2004">**FOLDERID \_ ProgramFiles**</span><span class="sxs-lookup"><span data-stu-id="4139d-2004">**FOLDERID\_ProgramFiles**</span></span> 

| <span data-ttu-id="4139d-2005">作業系統</span><span class="sxs-lookup"><span data-stu-id="4139d-2005">Operating System</span></span> | <span data-ttu-id="4139d-2006">應用程式</span><span class="sxs-lookup"><span data-stu-id="4139d-2006">Application</span></span> | <span data-ttu-id="4139d-2007">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="4139d-2007">KNOWNFOLDERID</span></span> | <span data-ttu-id="4139d-2008">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-2008">Default Path</span></span> | <span data-ttu-id="4139d-2009">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-2009">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="4139d-2010">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2010">32 bit</span></span> | <span data-ttu-id="4139d-2011">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2011">32 bit</span></span> | <span data-ttu-id="4139d-2012">FOLDERID \_ ProgramFiles</span><span class="sxs-lookup"><span data-stu-id="4139d-2012">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="4139d-2013">% SystemDrive% \\ Program Files</span><span class="sxs-lookup"><span data-stu-id="4139d-2013">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="4139d-2014">CSIDL \_ PROGRAM \_ FILES</span><span class="sxs-lookup"><span data-stu-id="4139d-2014">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="4139d-2015">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2015">32 bit</span></span> | <span data-ttu-id="4139d-2016">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2016">32 bit</span></span> | <span data-ttu-id="4139d-2017">FOLDERID \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2017">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="4139d-2018">% SystemDrive% \\ Program Files</span><span class="sxs-lookup"><span data-stu-id="4139d-2018">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="4139d-2019">CSIDL \_ PROGRAM \_ FILESX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2019">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="4139d-2020">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2020">32 bit</span></span> | <span data-ttu-id="4139d-2021">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2021">32 bit</span></span> | <span data-ttu-id="4139d-2022">\_32 位作業系統下不支援 FOLDERID ProgramFilesX64 () </span><span class="sxs-lookup"><span data-stu-id="4139d-2022">FOLDERID\_ProgramFilesX64 (not supported under 32-bit operating systems)</span></span> | <span data-ttu-id="4139d-2023">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-2023">Not applicable</span></span> | <span data-ttu-id="4139d-2024">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-2024">Not applicable</span></span> |
| <span data-ttu-id="4139d-2025">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2025">64 bit</span></span> | <span data-ttu-id="4139d-2026">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2026">64 bit</span></span> | <span data-ttu-id="4139d-2027">FOLDERID \_ ProgramFiles</span><span class="sxs-lookup"><span data-stu-id="4139d-2027">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="4139d-2028">% SystemDrive% \\ Program Files</span><span class="sxs-lookup"><span data-stu-id="4139d-2028">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="4139d-2029">CSIDL \_ PROGRAM \_ FILES</span><span class="sxs-lookup"><span data-stu-id="4139d-2029">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="4139d-2030">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2030">64 bit</span></span> | <span data-ttu-id="4139d-2031">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2031">64 bit</span></span> | <span data-ttu-id="4139d-2032">FOLDERID \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2032">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="4139d-2033">% SystemDrive% \\ Program Files (x86) </span><span class="sxs-lookup"><span data-stu-id="4139d-2033">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="4139d-2034">CSIDL \_ PROGRAM \_ FILESX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2034">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="4139d-2035">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2035">64 bit</span></span> | <span data-ttu-id="4139d-2036">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2036">64 bit</span></span> | <span data-ttu-id="4139d-2037">FOLDERID \_ ProgramFilesX64</span><span class="sxs-lookup"><span data-stu-id="4139d-2037">FOLDERID\_ProgramFilesX64</span></span> | <span data-ttu-id="4139d-2038">% SystemDrive% \\ Program Files</span><span class="sxs-lookup"><span data-stu-id="4139d-2038">%SystemDrive%\\Program Files</span></span> | <span data-ttu-id="4139d-2039">無</span><span class="sxs-lookup"><span data-stu-id="4139d-2039">None</span></span> |
| <span data-ttu-id="4139d-2040">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2040">64 bit</span></span> | <span data-ttu-id="4139d-2041">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2041">32 bit</span></span> | <span data-ttu-id="4139d-2042">FOLDERID \_ ProgramFiles</span><span class="sxs-lookup"><span data-stu-id="4139d-2042">FOLDERID\_ProgramFiles</span></span> | <span data-ttu-id="4139d-2043">% SystemDrive% \\ Program Files (x86) </span><span class="sxs-lookup"><span data-stu-id="4139d-2043">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="4139d-2044">CSIDL \_ PROGRAM \_ FILES</span><span class="sxs-lookup"><span data-stu-id="4139d-2044">CSIDL\_PROGRAM\_FILES</span></span> |
| <span data-ttu-id="4139d-2045">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2045">64 bit</span></span> | <span data-ttu-id="4139d-2046">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2046">32 bit</span></span> | <span data-ttu-id="4139d-2047">FOLDERID \_ ProgramFilesX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2047">FOLDERID\_ProgramFilesX86</span></span> | <span data-ttu-id="4139d-2048">% SystemDrive% \\ Program Files (x86) </span><span class="sxs-lookup"><span data-stu-id="4139d-2048">%SystemDrive%\\Program Files (x86)</span></span> | <span data-ttu-id="4139d-2049">CSIDL \_ PROGRAM \_ FILESX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2049">CSIDL\_PROGRAM\_FILESX86</span></span> |
| <span data-ttu-id="4139d-2050">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2050">64 bit</span></span> | <span data-ttu-id="4139d-2051">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2051">32 bit</span></span> | <span data-ttu-id="4139d-2052">\_32 位應用程式不支援的 FOLDERID ProgramFilesX64 () </span><span class="sxs-lookup"><span data-stu-id="4139d-2052">FOLDERID\_ProgramFilesX64 (not supported for 32-bit applications)</span></span> | <span data-ttu-id="4139d-2053">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-2053">Not applicable</span></span> | <span data-ttu-id="4139d-2054">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-2054">Not applicable</span></span> |


<span data-ttu-id="4139d-2055">**FOLDERID \_ ProgramFilesCommon**</span><span class="sxs-lookup"><span data-stu-id="4139d-2055">**FOLDERID\_ProgramFilesCommon**</span></span>

| <span data-ttu-id="4139d-2056">作業系統</span><span class="sxs-lookup"><span data-stu-id="4139d-2056">Operating System</span></span> | <span data-ttu-id="4139d-2057">應用程式</span><span class="sxs-lookup"><span data-stu-id="4139d-2057">Application</span></span> | <span data-ttu-id="4139d-2058">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="4139d-2058">KNOWNFOLDERID</span></span> | <span data-ttu-id="4139d-2059">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-2059">Default Path</span></span> | <span data-ttu-id="4139d-2060">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-2060">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="4139d-2061">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2061">32 bit</span></span> | <span data-ttu-id="4139d-2062">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2062">32 bit</span></span> | <span data-ttu-id="4139d-2063">FOLDERID \_ ProgramFilesCommon</span><span class="sxs-lookup"><span data-stu-id="4139d-2063">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="4139d-2064">% ProgramFiles% \\ 一般檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-2064">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="4139d-2065">常見的 CSIDL \_ 程式檔案 \_ \_</span><span class="sxs-lookup"><span data-stu-id="4139d-2065">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="4139d-2066">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2066">32 bit</span></span> | <span data-ttu-id="4139d-2067">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2067">32 bit</span></span> | <span data-ttu-id="4139d-2068">FOLDERID \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2068">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="4139d-2069">% ProgramFiles% \\ 一般檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-2069">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="4139d-2070">CSIDL \_ PROGRAM \_ FILES \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2070">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="4139d-2071">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2071">32 bit</span></span> | <span data-ttu-id="4139d-2072">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2072">32 bit</span></span> | <span data-ttu-id="4139d-2073">FOLDERID \_ ProgramFilesCommonX64 (未定義) </span><span class="sxs-lookup"><span data-stu-id="4139d-2073">FOLDERID\_ProgramFilesCommonX64 (undefined)</span></span> | <span data-ttu-id="4139d-2074">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-2074">Not applicable</span></span> | <span data-ttu-id="4139d-2075">不適用</span><span class="sxs-lookup"><span data-stu-id="4139d-2075">Not applicable</span></span> |
| <span data-ttu-id="4139d-2076">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2076">64 bit</span></span> | <span data-ttu-id="4139d-2077">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2077">64 bit</span></span> | <span data-ttu-id="4139d-2078">FOLDERID \_ ProgramFilesCommon</span><span class="sxs-lookup"><span data-stu-id="4139d-2078">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="4139d-2079">% ProgramFiles% \\ 一般檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-2079">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="4139d-2080">常見的 CSIDL \_ 程式檔案 \_ \_</span><span class="sxs-lookup"><span data-stu-id="4139d-2080">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="4139d-2081">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2081">64 bit</span></span> | <span data-ttu-id="4139d-2082">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2082">64 bit</span></span> | <span data-ttu-id="4139d-2083">FOLDERID \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2083">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="4139d-2084">% ProgramFiles (x86) % \\ 一般檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-2084">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="4139d-2085">CSIDL \_ PROGRAM \_ FILES \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2085">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="4139d-2086">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2086">64 bit</span></span> | <span data-ttu-id="4139d-2087">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2087">64 bit</span></span> | <span data-ttu-id="4139d-2088">FOLDERID \_ ProgramFilesCommonX64</span><span class="sxs-lookup"><span data-stu-id="4139d-2088">FOLDERID\_ProgramFilesCommonX64</span></span> | <span data-ttu-id="4139d-2089">% ProgramFiles% \\ 一般檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-2089">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="4139d-2090">無</span><span class="sxs-lookup"><span data-stu-id="4139d-2090">None</span></span> |
| <span data-ttu-id="4139d-2091">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2091">64 bit</span></span> | <span data-ttu-id="4139d-2092">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2092">32 bit</span></span> | <span data-ttu-id="4139d-2093">FOLDERID \_ ProgramFilesCommon</span><span class="sxs-lookup"><span data-stu-id="4139d-2093">FOLDERID\_ProgramFilesCommon</span></span> | <span data-ttu-id="4139d-2094">% ProgramFiles (x86) % \\ 一般檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-2094">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="4139d-2095">常見的 CSIDL \_ 程式檔案 \_ \_</span><span class="sxs-lookup"><span data-stu-id="4139d-2095">CSIDL\_PROGRAM\_FILES\_COMMON</span></span> |
| <span data-ttu-id="4139d-2096">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2096">64 bit</span></span> | <span data-ttu-id="4139d-2097">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2097">32 bit</span></span> | <span data-ttu-id="4139d-2098">FOLDERID \_ ProgramFilesCommonX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2098">FOLDERID\_ProgramFilesCommonX86</span></span> | <span data-ttu-id="4139d-2099">% ProgramFiles (x86) % \\ 一般檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-2099">%ProgramFiles(x86)%\\Common Files</span></span> | <span data-ttu-id="4139d-2100">CSIDL \_ PROGRAM \_ FILES \_ COMMONX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2100">CSIDL\_PROGRAM\_FILES\_COMMONX86</span></span> |
| <span data-ttu-id="4139d-2101">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2101">64 bit</span></span> | <span data-ttu-id="4139d-2102">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2102">32 bit</span></span> | <span data-ttu-id="4139d-2103">FOLDERID \_ ProgramFilesCommonX64</span><span class="sxs-lookup"><span data-stu-id="4139d-2103">FOLDERID\_ProgramFilesCommonX64</span></span> | <span data-ttu-id="4139d-2104">% ProgramFiles% \\ 一般檔案</span><span class="sxs-lookup"><span data-stu-id="4139d-2104">%ProgramFiles%\\Common Files</span></span> | <span data-ttu-id="4139d-2105">無</span><span class="sxs-lookup"><span data-stu-id="4139d-2105">None</span></span> |


<span data-ttu-id="4139d-2106">**FOLDERID \_ 系統**</span><span class="sxs-lookup"><span data-stu-id="4139d-2106">**FOLDERID\_System**</span></span>

| <span data-ttu-id="4139d-2107">作業系統</span><span class="sxs-lookup"><span data-stu-id="4139d-2107">Operating System</span></span> | <span data-ttu-id="4139d-2108">應用程式</span><span class="sxs-lookup"><span data-stu-id="4139d-2108">Application</span></span> | <span data-ttu-id="4139d-2109">KNOWNFOLDERID</span><span class="sxs-lookup"><span data-stu-id="4139d-2109">KNOWNFOLDERID</span></span> | <span data-ttu-id="4139d-2110">Default Path</span><span class="sxs-lookup"><span data-stu-id="4139d-2110">Default Path</span></span> | <span data-ttu-id="4139d-2111">CSIDL 對等專案</span><span class="sxs-lookup"><span data-stu-id="4139d-2111">CSIDL Equivalent</span></span> |
|------------------|-------------|---------------|--------------|------------------|  
| <span data-ttu-id="4139d-2112">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2112">32 bit</span></span> | <span data-ttu-id="4139d-2113">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2113">32 bit</span></span> | <span data-ttu-id="4139d-2114">FOLDERID \_ 系統</span><span class="sxs-lookup"><span data-stu-id="4139d-2114">FOLDERID\_System</span></span> | <span data-ttu-id="4139d-2115">% windir% \\ system32</span><span class="sxs-lookup"><span data-stu-id="4139d-2115">%windir%\\system32</span></span> | <span data-ttu-id="4139d-2116">CSIDL \_ 系統</span><span class="sxs-lookup"><span data-stu-id="4139d-2116">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="4139d-2117">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2117">32 bit</span></span> | <span data-ttu-id="4139d-2118">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2118">32 bit</span></span> | <span data-ttu-id="4139d-2119">FOLDERID \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2119">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="4139d-2120">% windir% \\ system32</span><span class="sxs-lookup"><span data-stu-id="4139d-2120">%windir%\\system32</span></span> | <span data-ttu-id="4139d-2121">CSIDL \_ SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2121">CSIDL\_SYSTEMX86</span></span> |
| <span data-ttu-id="4139d-2122">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2122">64 bit</span></span> | <span data-ttu-id="4139d-2123">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2123">64 bit</span></span> | <span data-ttu-id="4139d-2124">FOLDERID \_ 系統</span><span class="sxs-lookup"><span data-stu-id="4139d-2124">FOLDERID\_System</span></span> | <span data-ttu-id="4139d-2125">% windir% \\ system32</span><span class="sxs-lookup"><span data-stu-id="4139d-2125">%windir%\\system32</span></span> | <span data-ttu-id="4139d-2126">CSIDL \_ 系統</span><span class="sxs-lookup"><span data-stu-id="4139d-2126">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="4139d-2127">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2127">64 bit</span></span> | <span data-ttu-id="4139d-2128">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2128">64 bit</span></span> | <span data-ttu-id="4139d-2129">FOLDERID \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2129">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="4139d-2130">% windir% \\ syswow64</span><span class="sxs-lookup"><span data-stu-id="4139d-2130">%windir%\\syswow64</span></span> | <span data-ttu-id="4139d-2131">CSIDL \_ SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2131">CSIDL\_SYSTEMX86</span></span> |
| <span data-ttu-id="4139d-2132">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2132">64 bit</span></span> | <span data-ttu-id="4139d-2133">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2133">32 bit</span></span> | <span data-ttu-id="4139d-2134">FOLDERID \_ 系統</span><span class="sxs-lookup"><span data-stu-id="4139d-2134">FOLDERID\_System</span></span> | <span data-ttu-id="4139d-2135">% windir% \\ system32</span><span class="sxs-lookup"><span data-stu-id="4139d-2135">%windir%\\system32</span></span> | <span data-ttu-id="4139d-2136">CSIDL \_ 系統</span><span class="sxs-lookup"><span data-stu-id="4139d-2136">CSIDL\_SYSTEM</span></span> |
| <span data-ttu-id="4139d-2137">64 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2137">64 bit</span></span> | <span data-ttu-id="4139d-2138">32 位元</span><span class="sxs-lookup"><span data-stu-id="4139d-2138">32 bit</span></span> | <span data-ttu-id="4139d-2139">FOLDERID \_ SystemX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2139">FOLDERID\_SystemX86</span></span> | <span data-ttu-id="4139d-2140">% windir% \\ syswow64</span><span class="sxs-lookup"><span data-stu-id="4139d-2140">%windir%\\syswow64</span></span> | <span data-ttu-id="4139d-2141">CSIDL \_ SYSTEMX86</span><span class="sxs-lookup"><span data-stu-id="4139d-2141">CSIDL\_SYSTEMX86</span></span> |


<span data-ttu-id="4139d-2142">我們已使用環境字串來提供整個主題的一般路徑。</span><span class="sxs-lookup"><span data-stu-id="4139d-2142">We have used environment strings to provide generic paths throughout this topic.</span></span> <span data-ttu-id="4139d-2143">下表提供這些環境字串所代表路徑的範例。</span><span class="sxs-lookup"><span data-stu-id="4139d-2143">The following tables give examples of the paths those environment strings represent.</span></span> <span data-ttu-id="4139d-2144">在某些情況下，這些路徑可能不符合特定電腦上的路徑，因為在安裝或稍後的資料夾重新導向期間所做的選擇。</span><span class="sxs-lookup"><span data-stu-id="4139d-2144">In some cases, these paths might not match those on a particular computer because of choices made during installation or later folder redirection.</span></span> <span data-ttu-id="4139d-2145">請注意，Windows Vista 的某些路徑已變更。</span><span class="sxs-lookup"><span data-stu-id="4139d-2145">Note that some paths have changed for Windows Vista.</span></span>


<span data-ttu-id="4139d-2146">**Windows Vista 和更新版本**</span><span class="sxs-lookup"><span data-stu-id="4139d-2146">**Windows Vista and later**</span></span>

| <span data-ttu-id="4139d-2147">環境字串</span><span class="sxs-lookup"><span data-stu-id="4139d-2147">Environment String</span></span> | <span data-ttu-id="4139d-2148">範例路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-2148">Example Path</span></span> |
|--------------------|--------------|
| <span data-ttu-id="4139d-2149">ALLUSERSPROFILE</span><span class="sxs-lookup"><span data-stu-id="4139d-2149">%ALLUSERSPROFILE%</span></span> | <span data-ttu-id="4139d-2150">C： \\ ProgramData</span><span class="sxs-lookup"><span data-stu-id="4139d-2150">C:\\ProgramData</span></span> |
| <span data-ttu-id="4139d-2151">%APPDATA%</span><span class="sxs-lookup"><span data-stu-id="4139d-2151">%APPDATA%</span></span> | <span data-ttu-id="4139d-2152">C： \\ 使用者使用者 \\ *名稱* \\ AppData \\ 漫遊</span><span class="sxs-lookup"><span data-stu-id="4139d-2152">C:\\Users\\*username*\\AppData\\Roaming</span></span> |
| <span data-ttu-id="4139d-2153">LOCALAPPDATA</span><span class="sxs-lookup"><span data-stu-id="4139d-2153">%LOCALAPPDATA%</span></span> | <span data-ttu-id="4139d-2154">C： \\ Users \\ *username* \\ AppData \\ Local</span><span class="sxs-lookup"><span data-stu-id="4139d-2154">C:\\Users\\*username*\\AppData\\Local</span></span> |
| <span data-ttu-id="4139d-2155">%ProgramData%</span><span class="sxs-lookup"><span data-stu-id="4139d-2155">%ProgramData%</span></span> | <span data-ttu-id="4139d-2156">C： \\ ProgramData</span><span class="sxs-lookup"><span data-stu-id="4139d-2156">C:\\ProgramData</span></span> |
| <span data-ttu-id="4139d-2157">%ProgramFiles%</span><span class="sxs-lookup"><span data-stu-id="4139d-2157">%ProgramFiles%</span></span> | <span data-ttu-id="4139d-2158">C： \\ Program Files</span><span class="sxs-lookup"><span data-stu-id="4139d-2158">C:\\Program Files</span></span> |
| <span data-ttu-id="4139d-2159">%ProgramFiles(x86)%</span><span class="sxs-lookup"><span data-stu-id="4139d-2159">%ProgramFiles(x86)%</span></span> | <span data-ttu-id="4139d-2160">C： \\ Program Files (x86) </span><span class="sxs-lookup"><span data-stu-id="4139d-2160">C:\\Program Files (x86)</span></span> |
| <span data-ttu-id="4139d-2161">公共</span><span class="sxs-lookup"><span data-stu-id="4139d-2161">%PUBLIC%</span></span> | <span data-ttu-id="4139d-2162">C： \\ 使用者 \\ 公用</span><span class="sxs-lookup"><span data-stu-id="4139d-2162">C:\\Users\\Public</span></span> |
| <span data-ttu-id="4139d-2163">%SystemDrive%</span><span class="sxs-lookup"><span data-stu-id="4139d-2163">%SystemDrive%</span></span> | <span data-ttu-id="4139d-2164">C.</span><span class="sxs-lookup"><span data-stu-id="4139d-2164">C:</span></span> |
| <span data-ttu-id="4139d-2165">USERPROFILE</span><span class="sxs-lookup"><span data-stu-id="4139d-2165">%USERPROFILE%</span></span> | <span data-ttu-id="4139d-2166">C： \\ 使用者使用者 \\ *名稱*</span><span class="sxs-lookup"><span data-stu-id="4139d-2166">C:\\Users\\*username*</span></span> |
| <span data-ttu-id="4139d-2167">windir</span><span class="sxs-lookup"><span data-stu-id="4139d-2167">%windir%</span></span> | <span data-ttu-id="4139d-2168">C： \\ Windows</span><span class="sxs-lookup"><span data-stu-id="4139d-2168">C:\\Windows</span></span> |


<span data-ttu-id="4139d-2169">**Windows XP 及更早版本**</span><span class="sxs-lookup"><span data-stu-id="4139d-2169">**Windows XP and earlier**</span></span>

| <span data-ttu-id="4139d-2170">環境字串</span><span class="sxs-lookup"><span data-stu-id="4139d-2170">Environment String</span></span> | <span data-ttu-id="4139d-2171">範例路徑</span><span class="sxs-lookup"><span data-stu-id="4139d-2171">Example Path</span></span> |
|--------------------|--------------|
| <span data-ttu-id="4139d-2172">ALLUSERSPROFILE</span><span class="sxs-lookup"><span data-stu-id="4139d-2172">%ALLUSERSPROFILE%</span></span> | <span data-ttu-id="4139d-2173">C： \\ 檔和設定 \\ 所有使用者</span><span class="sxs-lookup"><span data-stu-id="4139d-2173">C:\\Documents and Settings\\All Users</span></span> |
| <span data-ttu-id="4139d-2174">%APPDATA%</span><span class="sxs-lookup"><span data-stu-id="4139d-2174">%APPDATA%</span></span> | <span data-ttu-id="4139d-2175">C： \\ 檔和設定使用者名稱使用者的 \\  \\ 應用程式資料</span><span class="sxs-lookup"><span data-stu-id="4139d-2175">C:\\Documents and Settings\\*username*\\Application Data</span></span> |
| <span data-ttu-id="4139d-2176">%ProgramFiles%</span><span class="sxs-lookup"><span data-stu-id="4139d-2176">%ProgramFiles%</span></span> | <span data-ttu-id="4139d-2177">C： \\ Program Files</span><span class="sxs-lookup"><span data-stu-id="4139d-2177">C:\\Program Files</span></span> |
| <span data-ttu-id="4139d-2178">%SystemDrive%</span><span class="sxs-lookup"><span data-stu-id="4139d-2178">%SystemDrive%</span></span> | <span data-ttu-id="4139d-2179">C.</span><span class="sxs-lookup"><span data-stu-id="4139d-2179">C:</span></span> |
| <span data-ttu-id="4139d-2180">USERPROFILE</span><span class="sxs-lookup"><span data-stu-id="4139d-2180">%USERPROFILE%</span></span> | <span data-ttu-id="4139d-2181">C： \\ 檔和設定使用者 \\ *名稱*</span><span class="sxs-lookup"><span data-stu-id="4139d-2181">C:\\Documents and Settings\\*username*</span></span> |
| <span data-ttu-id="4139d-2182">windir</span><span class="sxs-lookup"><span data-stu-id="4139d-2182">%windir%</span></span> | <span data-ttu-id="4139d-2183">C： \\ Windows</span><span class="sxs-lookup"><span data-stu-id="4139d-2183">C:\\Windows</span></span> |


## <a name="requirements"></a><span data-ttu-id="4139d-2184">規格需求</span><span class="sxs-lookup"><span data-stu-id="4139d-2184">Requirements</span></span>


| <span data-ttu-id="4139d-2185">需求</span><span class="sxs-lookup"><span data-stu-id="4139d-2185">Requirement</span></span> | <span data-ttu-id="4139d-2186">值</span><span class="sxs-lookup"><span data-stu-id="4139d-2186">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4139d-2187">標頭</span><span class="sxs-lookup"><span data-stu-id="4139d-2187">Header</span></span><br/> | <dl> <span data-ttu-id="4139d-2188"><dt>Knownfolders。h</dt></span><span class="sxs-lookup"><span data-stu-id="4139d-2188"><dt>Knownfolders.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4139d-2189">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4139d-2189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4139d-2190">**CSIDL**</span><span class="sxs-lookup"><span data-stu-id="4139d-2190">**CSIDL**</span></span>](csidl.md)
</dt> <dt>

[<span data-ttu-id="4139d-2191">已知的資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-2191">Known Folders</span></span>](known-folders.md)
</dt> <dt>

[<span data-ttu-id="4139d-2192">使用應用程式中的已知資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-2192">Working with Known Folders in Applications</span></span>](working-with-known-folders.md)
</dt> <dt>

[<span data-ttu-id="4139d-2193">如何使用自訂資料夾擴充已知資料夾</span><span class="sxs-lookup"><span data-stu-id="4139d-2193">How to Extend Known Folders with Custom Folders</span></span>](how-to-extend-known-folders-with-custom-folders.md)
</dt> <dt>

<span data-ttu-id="4139d-2194">[已知資料夾範例](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="4139d-2194">[Known Folders Sample](/previous-versions/windows/desktop/legacy/dd940364(v=vs.85))</span></span>
</dt> </dl>

 

 
