---
title: 使用 DRM 7 版或更新版本保護檔案
description: 使用 DRM 7 版或更新版本保護檔案
ms.assetid: 906f16c1-6573-47e9-8228-58dc126f6357
keywords:
- Windows Media Format SDK，建立受保護的檔案
- Windows Media Format SDK，受保護的檔案
- Advanced Systems Format (ASF) ，建立受保護的檔案
- ASF (Advanced Systems Format) ，建立受保護的檔案
- Advanced Systems Format (ASF) 、受保護的檔案
- ASF (Advanced 系統格式) 、受保護的檔案
- Advanced Systems Format (ASF) ，WMStubDRM .lib
- ASF (Advanced Systems Format) ，WMStubDRM .lib
- WMStubDRM .lib，建立受保護的檔案
- WMStubDRM .lib，受保護的檔案
- 數位版權管理 (DRM) ，WMStubDRM .lib
- DRM (數位版權管理) ，WMStubDRM .lib
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ee809ea73401f22e4554e74c2ecb8855a0384e0
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "106999792"
---
# <a name="protecting-files-with-drm-version-7-or-later"></a><span data-ttu-id="61c06-115">使用 DRM 7 版或更新版本保護檔案</span><span class="sxs-lookup"><span data-stu-id="61c06-115">Protecting Files with DRM Version 7 or Later</span></span>

<span data-ttu-id="61c06-116">若要使用 Windows Media DRM 7 版或更新版本保護檔案，請使用寫入器物件的 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) 方法來設定 DRM 屬性。</span><span class="sxs-lookup"><span data-stu-id="61c06-116">To protect files with Windows Media DRM version 7 or later, use the writer object's [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) method to set DRM attributes.</span></span> <span data-ttu-id="61c06-117">由於 DRM 7 版和更新版本為每個受保護的檔案或一組檔案啟用了唯一的授權，因此 **IWMDRMWriter** 介面也有建立金鑰的方法。</span><span class="sxs-lookup"><span data-stu-id="61c06-117">Because DRM version 7 and later versions enable unique licenses for each protected file or set of files, the **IWMDRMWriter** interface also has methods for creating keys.</span></span> <span data-ttu-id="61c06-118">只為了方便起見，提供這些方法。</span><span class="sxs-lookup"><span data-stu-id="61c06-118">These methods are provided for convenience only.</span></span>

<span data-ttu-id="61c06-119">若要使用 DRM 7 版或更新版本來保護 ASF 檔案，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="61c06-119">To protect ASF files using DRM version 7 or later, perform the following steps:</span></span>

1.  <span data-ttu-id="61c06-120">連結至 WMStubDRM .lib，如有必要，請將 wmvcore 取消連結。</span><span class="sxs-lookup"><span data-stu-id="61c06-120">Link to WMStubDRM.lib and, if necessary, unlink wmvcore.lib.</span></span>
2.  <span data-ttu-id="61c06-121">呼叫 [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) 函數來建立 DRM 寫入器。</span><span class="sxs-lookup"><span data-stu-id="61c06-121">Call the [**WMCreateWriter**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter) function to create the DRM writer.</span></span> <span data-ttu-id="61c06-122">第一個引數是保留的，而且必須設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="61c06-122">The first argument is reserved and must be set to **NULL**.</span></span>
3.  <span data-ttu-id="61c06-123">藉由呼叫 [**IWMWriter：： SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) 或 [**IWMWriter：： SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid)，設定要使用之寫入器的設定檔。</span><span class="sxs-lookup"><span data-stu-id="61c06-123">Set a profile for the writer to use by calling [**IWMWriter::SetProfile**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setprofile) or [**IWMWriter::SetProfileByID**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmwriter-setprofilebyid).</span></span> <span data-ttu-id="61c06-124">設定任何 DRM 屬性之前，您必須先在寫入器中設定設定檔。</span><span class="sxs-lookup"><span data-stu-id="61c06-124">You must set a profile in the writer before setting any DRM attributes.</span></span> <span data-ttu-id="61c06-125">只有使用 Windows Media 音訊或 Windows Media 視訊編解碼器的設定檔支援 DRM</span><span class="sxs-lookup"><span data-stu-id="61c06-125">DRM is supported only for profiles that use the Windows Media Audio or Windows Media Video codecs</span></span>
4.  <span data-ttu-id="61c06-126">取得寫入器物件的 [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) 介面。</span><span class="sxs-lookup"><span data-stu-id="61c06-126">Obtain the writer object's [**IWMDRMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter) interface.</span></span>
5.  <span data-ttu-id="61c06-127">呼叫 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) ，並將 [ [**使用 \_ Advanced \_ DRM**](use-advanced-drm.md) ] 設定為 [ **TRUE**]。</span><span class="sxs-lookup"><span data-stu-id="61c06-127">Call [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) and set [**Use\_Advanced\_DRM**](use-advanced-drm.md) to **TRUE**.</span></span>
6.  <span data-ttu-id="61c06-128">如果您需要產生新的金鑰種子，請呼叫 [**IWMDRMWriter：： GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed)。</span><span class="sxs-lookup"><span data-stu-id="61c06-128">If you need to generate a new key seed, call [**IWMDRMWriter::GenerateKeySeed**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyseed).</span></span> <span data-ttu-id="61c06-129">在大多數情況下，您將會重複使用先前產生的金鑰種子。</span><span class="sxs-lookup"><span data-stu-id="61c06-129">In most cases, you will be reusing a key seed that was generated previously.</span></span> <span data-ttu-id="61c06-130">此值必須保持秘密;它不會寫入檔案中。</span><span class="sxs-lookup"><span data-stu-id="61c06-130">This value must remain secret; it is not written into the file.</span></span>
7.  <span data-ttu-id="61c06-131">呼叫 [**IWMDRMWriter：： GenerateKeyID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyid) 來建立金鑰識別碼，這是用來建立實際金鑰的第二個值。</span><span class="sxs-lookup"><span data-stu-id="61c06-131">Call [**IWMDRMWriter::GenerateKeyID**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatekeyid) to create a key ID, which is the second value used to create the actual key.</span></span> <span data-ttu-id="61c06-132">與金鑰種子不同的是，金鑰識別碼是公用的，而且會以純文字方式寫入 DRM 標頭中的檔案。</span><span class="sxs-lookup"><span data-stu-id="61c06-132">Unlike the key seed, the key ID is public and is written to the file in the DRM header in the clear.</span></span> <span data-ttu-id="61c06-133">為您建立的每個新檔案建立新的金鑰識別碼。</span><span class="sxs-lookup"><span data-stu-id="61c06-133">Create a new key ID for each new file you create.</span></span>
8.  <span data-ttu-id="61c06-134">如有需要，請呼叫 **IWMDRMWriter：： GenerateSigningKeyPair** ，以產生將用來簽署 ADVANCED DRM ASF 標頭物件的公開和私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="61c06-134">Call **IWMDRMWriter::GenerateSigningKeyPair** if necessary to generate a public and private key that will be used to sign the advanced DRM ASF Header object.</span></span> <span data-ttu-id="61c06-135">如需這些金鑰的詳細資訊，請參閱 [**IWMDRMWriter：： GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair)。</span><span class="sxs-lookup"><span data-stu-id="61c06-135">For more information about these keys, see [**IWMDRMWriter::GenerateSigningKeyPair**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-generatesigningkeypair).</span></span>
9.  <span data-ttu-id="61c06-136">如有必要，請取得值以填入 DRM 標頭的數位簽章物件。</span><span class="sxs-lookup"><span data-stu-id="61c06-136">If necessary, obtain the values to populate the DRM header's digital signature object.</span></span> <span data-ttu-id="61c06-137">如果您的系統上沒有安裝 Windows Media Rights Manager 的工作版本，您必須指定下列四個屬性（全部都必須從 Microsoft 取得）來設定 ASF 檔案標頭的數位簽章物件：</span><span class="sxs-lookup"><span data-stu-id="61c06-137">If you do not have a working version of Windows Media Rights Manager installed on your system, you must configure the ASF file header's digital signature object by specifying the following four attributes, which all must be obtained from Microsoft:</span></span>

    -   [<span data-ttu-id="61c06-138">**DRM \_ LASignatureRootCert**</span><span class="sxs-lookup"><span data-stu-id="61c06-138">**DRM\_LASignatureRootCert**</span></span>](drm-lasignaturerootcert.md)
    -   [<span data-ttu-id="61c06-139">**DRM \_ LASignatureCert**</span><span class="sxs-lookup"><span data-stu-id="61c06-139">**DRM\_LASignatureCert**</span></span>](drm-lasignaturecert.md)
    -   [<span data-ttu-id="61c06-140">**DRM \_ LASignatureLicSrvCert**</span><span class="sxs-lookup"><span data-stu-id="61c06-140">**DRM\_LASignatureLicSrvCert**</span></span>](drm-lasignaturelicsrvcert.md)
    -   [<span data-ttu-id="61c06-141">**DRM \_ LASignaturePrivKey**</span><span class="sxs-lookup"><span data-stu-id="61c06-141">**DRM\_LASignaturePrivKey**</span></span>](drm-lasignatureprivkey.md)

    <span data-ttu-id="61c06-142">如果您已安裝 Windows Media Rights Manager，就不需要在應用程式中設定這些屬性。</span><span class="sxs-lookup"><span data-stu-id="61c06-142">If you do have Windows Media Rights Manager installed, there is no need to set these attributes in your application.</span></span> <span data-ttu-id="61c06-143">DRM 元件會取得這些屬性，並使用它們來自動簽署標頭。</span><span class="sxs-lookup"><span data-stu-id="61c06-143">The DRM component will retrieve these attributes and use them to sign the header automatically.</span></span> <span data-ttu-id="61c06-144">如果您在另一部電腦上有 Windows Media Rights Manager 的啟用版本，而且想要重複使用這些數位簽章物件值，您可以在登錄中找到它們。</span><span class="sxs-lookup"><span data-stu-id="61c06-144">If you have an activated version of Windows Media Rights Manager on another machine, and wish to reuse those digital signature object values, you can find them in the registry.</span></span> <span data-ttu-id="61c06-145">授權伺服器憑證會儲存在 HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ microsoft \\ wm rights manager \\ 授權伺服器憑證 \\ ： cert1，並將根憑證儲存在 HKEY \_ Local \_ machine \\ software \\ microsoft \\ wm rights manager \\ 授權伺服器 \\ 證書： cert2。</span><span class="sxs-lookup"><span data-stu-id="61c06-145">The license server certificate is stored under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WM Rights Manager\\License Server\\Certs:cert1, and the root certificate is stored under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WM Rights Manager\\License Server\\Certs:cert2.</span></span> <span data-ttu-id="61c06-146">使用 DRM 版本7保護檔案時，您必須使用這些登錄機碼中的值。</span><span class="sxs-lookup"><span data-stu-id="61c06-146">When protecting files with DRM version 7, you must use the values from these registry keys.</span></span> <span data-ttu-id="61c06-147">針對 **DRM \_ LASignaturePrivKey 屬性**，請使用 **GenerateSigningKeysEx** (透過 Windows media rights manager SDK) 或重複使用 WINDOWS media rights manager 在 HKEY \_ LOCAL \_ MACHINE \\ SOFTWARE \\ Microsoft \\ WM Rights manager \\ 授權伺服器： Info \_ Cert0 中所安裝的值。</span><span class="sxs-lookup"><span data-stu-id="61c06-147">For the **DRM\_LASignaturePrivKey property**, use either **GenerateSigningKeysEx** (through the Windows Media Rights Manager SDK) or else reuse the value installed by Windows Media Rights Manager under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WM Rights Manager\\License Server:Info\_Cert0.</span></span> <span data-ttu-id="61c06-148">針對 **DRM \_ LASignatureCert** 屬性，請使用 **GenerateSigningKeysEx** (透過 Windows media Rights manager SDK) ，或使用 WINDOWS media rights manager 在 HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ WM Rights manager \\ 授權伺服器憑證 \\ ： cert0 下安裝的值。</span><span class="sxs-lookup"><span data-stu-id="61c06-148">For the **DRM\_LASignatureCert** property, use either **GenerateSigningKeysEx** (through the Windows Media Rights Manager SDK) or else the value installed by Windows Media Rights Manager under HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\WM Rights Manager\\License Server\\Certs:cert0.</span></span>

10. <span data-ttu-id="61c06-149">視需要呼叫 [**IWMDRMWriter：： SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) ，以設定寫入器物件，此物件會視需要設定必要的 DRM 標頭屬性。</span><span class="sxs-lookup"><span data-stu-id="61c06-149">Call [**IWMDRMWriter::SetDRMAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmdrmwriter-setdrmattribute) as many times as necessary to configure the writer object, which will set the required DRM header attributes as necessary.</span></span> <span data-ttu-id="61c06-150">這些屬性會保存在寫入器物件的存留期內，或直到以新值重設為止。</span><span class="sxs-lookup"><span data-stu-id="61c06-150">These properties persist for the lifetime of the writer object or until they are reset with a new value.</span></span> <span data-ttu-id="61c06-151">您所建立的每個新檔案都不需要重設它們。</span><span class="sxs-lookup"><span data-stu-id="61c06-151">They do not need to be reset for each new file you create.</span></span>

    <span data-ttu-id="61c06-152">寫入器物件需要下列屬性：</span><span class="sxs-lookup"><span data-stu-id="61c06-152">The following properties are required by the writer object:</span></span>

    -   [<span data-ttu-id="61c06-153">**DRM \_ HeaderSignPrivKey**</span><span class="sxs-lookup"><span data-stu-id="61c06-153">**DRM\_HeaderSignPrivKey**</span></span>](drm-headersignprivkey.md)
    -   [<span data-ttu-id="61c06-154">**DRM \_ KeySeed**</span><span class="sxs-lookup"><span data-stu-id="61c06-154">**DRM\_KeySeed**</span></span>](drm-keyseed.md)
    -   [<span data-ttu-id="61c06-155">**DRM \_ V1LicenseAcqURL**</span><span class="sxs-lookup"><span data-stu-id="61c06-155">**DRM\_V1LicenseAcqURL**</span></span>](drm-v1licenseacqurl.md)
    -   [<span data-ttu-id="61c06-156">**DRM \_ KeyID**</span><span class="sxs-lookup"><span data-stu-id="61c06-156">**DRM\_KeyID**</span></span>](drm-keyid.md)
    -   [<span data-ttu-id="61c06-157">**DRM \_ LicenseAcqURL**</span><span class="sxs-lookup"><span data-stu-id="61c06-157">**DRM\_LicenseAcqURL**</span></span>](drm-licenseacqurl.md)

    <span data-ttu-id="61c06-158">以下是選擇性屬性：</span><span class="sxs-lookup"><span data-stu-id="61c06-158">The following properties are optional:</span></span>

    -   [<span data-ttu-id="61c06-159">**DRM \_ ContentID**</span><span class="sxs-lookup"><span data-stu-id="61c06-159">**DRM\_ContentID**</span></span>](drm-contentid.md)
    -   [<span data-ttu-id="61c06-160">**DRM \_ IndividualizedVersion**</span><span class="sxs-lookup"><span data-stu-id="61c06-160">**DRM\_IndividualizedVersion**</span></span>](drm-individualizedversion.md)

    <span data-ttu-id="61c06-161">此外，您也可以使用 [**DRM \_ DRMHeader**](drm-drmheader.md) 基底屬性，直接指定使用者定義的 DRM 檔案屬性。</span><span class="sxs-lookup"><span data-stu-id="61c06-161">In addition, you may specify user-defined DRM file attributes directly using the [**DRM\_DRMHeader**](drm-drmheader.md) base attribute.</span></span> <span data-ttu-id="61c06-162">您可以新增任何您想要的其他屬性，例如 "DRMHeader. RequireSAP"，以傳達授權伺服器將在建立授權時使用的其他資訊。</span><span class="sxs-lookup"><span data-stu-id="61c06-162">You can add any additional attribute you wish, such as "DRMHeader.RequireSAP" for example, as a way of communicating additional information that will be used by the license server in creating the license.</span></span> <span data-ttu-id="61c06-163">授權伺服器必須事先知道您新增的任何其他屬性。</span><span class="sxs-lookup"><span data-stu-id="61c06-163">The license server must be aware in advance of any additional properties you add.</span></span> <span data-ttu-id="61c06-164">無法以程式設計方式探索未知的屬性。</span><span class="sxs-lookup"><span data-stu-id="61c06-164">There is no way to discover unknown properties programmatically.</span></span>

11. <span data-ttu-id="61c06-165">使用 [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) 介面方法來寫入檔案，如本檔中的其他位置所述。</span><span class="sxs-lookup"><span data-stu-id="61c06-165">Write the file using the [**IWMWriter**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter) interface methods as described elsewhere in this documentation.</span></span> <span data-ttu-id="61c06-166">若要建立即時 DRM 串流，只要寫入網路接收即可。</span><span class="sxs-lookup"><span data-stu-id="61c06-166">To create a live-DRM stream, simply write to a network sink.</span></span> <span data-ttu-id="61c06-167">您也可以寫入至推送接收器。</span><span class="sxs-lookup"><span data-stu-id="61c06-167">You can also write to a push sink.</span></span>
12. <span data-ttu-id="61c06-168">如有必要，請使用 Windows Media Rights Manager 建立檔案的授權。</span><span class="sxs-lookup"><span data-stu-id="61c06-168">If necessary, create a license for the file using Windows Media Rights Manager.</span></span> <span data-ttu-id="61c06-169">這項工作也可以由協力廠商授權伺服器執行。</span><span class="sxs-lookup"><span data-stu-id="61c06-169">This task can also be performed by a third-party license server.</span></span> <span data-ttu-id="61c06-170">針對即時 DRM 案例，終端使用者必須在串流開始之前，或在第一次嘗試連接時取得授權。</span><span class="sxs-lookup"><span data-stu-id="61c06-170">For live-DRM scenarios, end users will need to obtain a license either before the stream begins, or else at the time they first attempt to connect to it.</span></span>

<span data-ttu-id="61c06-171">**注意** 此 SDK 的 x64 版本不支援 DRM。</span><span class="sxs-lookup"><span data-stu-id="61c06-171">**Note** DRM is not supported by the x64-based version of this SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="61c06-172">相關主題</span><span class="sxs-lookup"><span data-stu-id="61c06-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="61c06-173">**屬性**</span><span class="sxs-lookup"><span data-stu-id="61c06-173">**Attributes**</span></span>](attributes.md)
</dt> <dt>

[<span data-ttu-id="61c06-174">**DRM 屬性清單**</span><span class="sxs-lookup"><span data-stu-id="61c06-174">**DRM Attribute List**</span></span>](drm-attribute-list.md)
</dt> <dt>

[<span data-ttu-id="61c06-175">**DRM 屬性**</span><span class="sxs-lookup"><span data-stu-id="61c06-175">**DRM Properties**</span></span>](drm-properties.md)
</dt> <dt>

[<span data-ttu-id="61c06-176">**IWMDRMWriter 介面**</span><span class="sxs-lookup"><span data-stu-id="61c06-176">**IWMDRMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmwriter)
</dt> <dt>

[<span data-ttu-id="61c06-177">**IWMHeaderInfo：： SetAttribute**</span><span class="sxs-lookup"><span data-stu-id="61c06-177">**IWMHeaderInfo::SetAttribute**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo-setattribute)
</dt> <dt>

[<span data-ttu-id="61c06-178">**IWMWriter 介面**</span><span class="sxs-lookup"><span data-stu-id="61c06-178">**IWMWriter Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[<span data-ttu-id="61c06-179">**讀取受保護的檔案**</span><span class="sxs-lookup"><span data-stu-id="61c06-179">**Reading Protected Files**</span></span>](reading-protected-files.md)
</dt> <dt>

[<span data-ttu-id="61c06-180">**WMCreateWriter**</span><span class="sxs-lookup"><span data-stu-id="61c06-180">**WMCreateWriter**</span></span>](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriter)
</dt> </dl>

 

 




