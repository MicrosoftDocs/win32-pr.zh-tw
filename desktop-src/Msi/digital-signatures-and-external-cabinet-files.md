---
description: Windows Installer 可以使用數位簽章來偵測損毀的資源。
ms.assetid: 49f1c1f9-d342-47e0-8888-2eadc5dbd000
title: 數位簽章和外部封包檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f10e921b324a43a919a417f47953c0a44e4777ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850223"
---
# <a name="digital-signatures-and-external-cabinet-files"></a><span data-ttu-id="8290f-103">數位簽章和外部封包檔</span><span class="sxs-lookup"><span data-stu-id="8290f-103">Digital Signatures and External Cabinet Files</span></span>

<span data-ttu-id="8290f-104">Windows Installer 可以使用數位簽章來偵測損毀的資源。</span><span class="sxs-lookup"><span data-stu-id="8290f-104">Windows Installer can use digital signatures to detect corrupted resources.</span></span> <span data-ttu-id="8290f-105">安裝外部資源時，可能會根據在封裝中撰寫的參考簽署者憑證來驗證屬於資源的簽署者憑證。</span><span class="sxs-lookup"><span data-stu-id="8290f-105">When installing an external resource, the signer certificate belonging to the resource may be verified against a reference signer certificate authored in the package.</span></span> <span data-ttu-id="8290f-106">安裝程式無法驗證內部封包的簽章。</span><span class="sxs-lookup"><span data-stu-id="8290f-106">The installer cannot verify signatures for internal cabinets.</span></span> <span data-ttu-id="8290f-107">它只能使用 [MsiDigitalSignature 資料表](msidigitalsignature-table.md) 和 [MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)來驗證數位簽章。</span><span class="sxs-lookup"><span data-stu-id="8290f-107">It can only verify digital signatures by using the [MsiDigitalSignature table](msidigitalsignature-table.md) and [MsiDigitalCertificate table](msidigitalcertificate-table.md).</span></span>

<span data-ttu-id="8290f-108">安裝儲存在外部封包中的檔案時，Windows Installer 會執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="8290f-108">Windows Installer does the following when installing a file stored in an external cabinet:</span></span>

-   <span data-ttu-id="8290f-109">安裝程式會檢查該外部封包的媒體專案是否列在 [MsiDigitalSignature 資料表](msidigitalsignature-table.md)中。</span><span class="sxs-lookup"><span data-stu-id="8290f-109">The installer checks to see whether the media entry for that external cabinet is listed in the [MsiDigitalSignature table](msidigitalsignature-table.md).</span></span> <span data-ttu-id="8290f-110">儲存在外部封包中的檔案，其識別方式是在 [媒體資料表](media-table.md) 的 [封包] 資料行中，以 ' \# ' 字元為開頭的專案。</span><span class="sxs-lookup"><span data-stu-id="8290f-110">A file stored in an external cabinet is identified by having an entry in the Cabinet column of the [Media table](media-table.md) that is not prefixed by a '\#' character.</span></span>
-   <span data-ttu-id="8290f-111">開啟外部封包之前，安裝程式會呼叫 WinVerifyTrust 以解壓縮目前的憑證和雜湊資訊。</span><span class="sxs-lookup"><span data-stu-id="8290f-111">Before opening the external cabinet, the installer calls WinVerifyTrust to extract the current certificate and hash information.</span></span> <span data-ttu-id="8290f-112">如果封包上目前的簽章資訊與封裝中撰寫的簽章資訊不相符，則安裝會失敗。</span><span class="sxs-lookup"><span data-stu-id="8290f-112">If there is a mismatch between the current signature information on the cabinet and the signature information authored in the package, the installation fails.</span></span> <span data-ttu-id="8290f-113">安裝失敗，因為封包可能已遭入侵且無法信任。</span><span class="sxs-lookup"><span data-stu-id="8290f-113">The installation fails because the cabinet may have been compromised and cannot be trusted.</span></span>

<span data-ttu-id="8290f-114">如需有關使用數位簽章、數位憑證和 [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust)的詳細資訊，請參閱 Microsoft WINDOWS 軟體開發套件 (SDK) 的 [安全性](https://msdn.microsoft.com/library/cc527452.aspx) 一節。</span><span class="sxs-lookup"><span data-stu-id="8290f-114">For more information regarding the use of digital signatures, digital certificates, and [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust), see the [Security](https://msdn.microsoft.com/library/cc527452.aspx) section of the Microsoft Windows Software Development Kit (SDK).</span></span>

<span data-ttu-id="8290f-115">如需詳細資訊，請參閱 [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa)、 [MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)和 [MsiDigitalSignature 資料表](msidigitalsignature-table.md)。</span><span class="sxs-lookup"><span data-stu-id="8290f-115">For more information, see [**MsiGetFileSignatureInformation**](/windows/desktop/api/Msi/nf-msi-msigetfilesignatureinformationa), [MsiDigitalCertificate table](msidigitalcertificate-table.md), and [MsiDigitalSignature table](msidigitalsignature-table.md).</span></span>

 

 
