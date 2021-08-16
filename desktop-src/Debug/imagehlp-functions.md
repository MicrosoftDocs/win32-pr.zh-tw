---
description: 以下是 Imagehlp.dll 函數。
ms.assetid: 926f412e-25ba-4f9c-a118-b5a1bc723379
title: Imagehlp.dll 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2650d80dfb78f346a5fab22e0adfabdfb11c8e626ad3b5ea39930337feaebe8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118957106"
---
# <a name="imagehlp-functions"></a>Imagehlp.dll 函式

以下是 Imagehlp.dll 函數。

## <a name="image-access"></a>影像存取

影像存取功能可存取可執行映射中的資料。 這些函式可提供映射基底的高階存取，以及對影像資料最常見部分的非常特定存取。

<dl>

[**GetImageConfigInformation**](/windows/desktop/api/Imagehlp/nf-imagehlp-getimageconfiginformation)  
[**GetImageUnusedHeaderBytes**](/windows/desktop/api/Imagehlp/nf-imagehlp-getimageunusedheaderbytes)  
[**ImageLoad**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageload)  
[**ImageUnload**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageunload)  
[**MapAndLoad**](/windows/desktop/api/Imagehlp/nf-imagehlp-mapandload)  
[**SetImageConfigInformation**](/windows/desktop/api/Imagehlp/nf-imagehlp-setimageconfiginformation)  
[**UnMapAndLoad**](/windows/desktop/api/Imagehlp/nf-imagehlp-unmapandload)  
</dl>

## <a name="image-integrity"></a>映射完整性

映射完整性函式會管理影像檔案中的一組憑證。

<dl>

[**DigestFunction**](/windows/desktop/api/Imagehlp/nc-imagehlp-digest_function)  
[**ImageAddCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageaddcertificate)  
[**ImageEnumerateCertificates**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageenumeratecertificates)  
[**ImageGetCertificateData**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificatedata)  
[**ImageGetCertificateHeader**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetcertificateheader)  
[**ImageGetDigestStream**](/windows/desktop/api/Imagehlp/nf-imagehlp-imagegetdigeststream)  
[**ImageRemoveCertificate**](/windows/desktop/api/Imagehlp/nf-imagehlp-imageremovecertificate)  
</dl>

## <a name="image-modification"></a>影像修改

影像修改函式可讓您變更可執行檔映射。

<dl>

[**BindImage**](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimage)  
[**BindImageEx**](/windows/desktop/api/Imagehlp/nf-imagehlp-bindimageex)  
[**CheckSumMappedFile**](/windows/desktop/api/Imagehlp/nf-imagehlp-checksummappedfile)  
[**MapFileAndCheckSum**](/windows/desktop/api/Imagehlp/nf-imagehlp-mapfileandchecksuma)  
[**ReBaseImage**](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage)  
[**ReBaseImage64**](/windows/desktop/api/Imagehlp/nf-imagehlp-rebaseimage64)  
[**SplitSymbols**](/windows/desktop/api/Imagehlp/nf-imagehlp-splitsymbols)  
[**StatusRoutine**](/windows/desktop/api/Imagehlp/nc-imagehlp-pimagehlp_status_routine)  
[**TouchFileTimes**](/windows/desktop/api/Imagehlp/nf-imagehlp-touchfiletimes)  
[**UpdateDebugInfoFile**](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofile)  
[**UpdateDebugInfoFileEx**](/windows/desktop/api/Imagehlp/nf-imagehlp-updatedebuginfofileex)  
</dl>

 

 



