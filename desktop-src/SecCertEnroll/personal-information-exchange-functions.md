---
description: 下列各節將討論 Xenroll.dll 所匯出的函式，以管理 (PFX) 訊息的個人資訊交換。
ms.assetid: f7e6b3a6-eae4-49f8-a624-609742741560
title: 個人資訊交換功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7dea1670e6017cd30ed8358d2670585727667068
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979265"
---
# <a name="personal-information-exchange-functions"></a><span data-ttu-id="4a26e-103">個人資訊交換功能</span><span class="sxs-lookup"><span data-stu-id="4a26e-103">Personal Information Exchange Functions</span></span>

<span data-ttu-id="4a26e-104">下列各節將討論 Xenroll.dll 所匯出的函式，以管理 (PFX) 訊息的個人資訊交換。</span><span class="sxs-lookup"><span data-stu-id="4a26e-104">Each of the following sections discusses a function exported by Xenroll.dll to manage Personal Information Exchange (PFX) messages.</span></span> <span data-ttu-id="4a26e-105">每個章節也會討論如何使用 CertEnroll.dll 來取代函式，或指出兩個程式庫之間沒有任何對應存在。</span><span class="sxs-lookup"><span data-stu-id="4a26e-105">Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists.</span></span>

## <a name="createfilepfxwstr"></a><span data-ttu-id="4a26e-106">createFilePFXWStr</span><span class="sxs-lookup"><span data-stu-id="4a26e-106">createFilePFXWStr</span></span>

<span data-ttu-id="4a26e-107">Xenroll.dll 中的 [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) 函數會使用 PFX 格式，將憑證鏈和 [*私密金鑰*](/windows/desktop/SecGloss/p-gly) 儲存在檔案中。</span><span class="sxs-lookup"><span data-stu-id="4a26e-107">The [**createFilePFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createfilepfxwstr) function in Xenroll.dll saves a certificate chain and [*private key*](/windows/desktop/SecGloss/p-gly) in a file by using the PFX format.</span></span>

<span data-ttu-id="4a26e-108">CertEnroll.dll 程式庫不會直接執行將 PFX 訊息複製到檔案的功能。</span><span class="sxs-lookup"><span data-stu-id="4a26e-108">The CertEnroll.dll library does not directly implement functionality to copy the PFX message to a file.</span></span> <span data-ttu-id="4a26e-109">不過，您可以使用 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)介面上的 [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx)方法來建立已編碼的 PFX 訊息，並撰寫自訂函式，以將訊息儲存在檔案中。</span><span class="sxs-lookup"><span data-stu-id="4a26e-109">You can, however, use the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method on the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to create an encoded PFX message and write a custom function to save the message in a file.</span></span>

## <a name="createpfxwstr"></a><span data-ttu-id="4a26e-110">createPFXWStr</span><span class="sxs-lookup"><span data-stu-id="4a26e-110">createPFXWStr</span></span>

<span data-ttu-id="4a26e-111">Xenroll.dll 中的 [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) 函式會以 PFX 格式字串儲存憑證鏈和私密金鑰。</span><span class="sxs-lookup"><span data-stu-id="4a26e-111">The [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr) function in Xenroll.dll saves a certificate chain and private key in a PFX format string.</span></span>

<span data-ttu-id="4a26e-112">您可以使用 [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)介面上的 [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx)方法來建立編碼的 PFX 訊息，其中包含憑證鏈和金鑰。</span><span class="sxs-lookup"><span data-stu-id="4a26e-112">You can use the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method on the [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) interface to create an encoded PFX message that contains the certificate chain and key.</span></span> <span data-ttu-id="4a26e-113">您可以指定密碼、匯出選項和編碼類型。</span><span class="sxs-lookup"><span data-stu-id="4a26e-113">You can specify a password, export options, and encoding type.</span></span> <span data-ttu-id="4a26e-114">若要取出相當於 [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr)所傳回的字串，請在 \_ \_ \_ [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx)方法的 *編碼* 參數中傳遞 XCN CRYPT 字串二進位旗標。</span><span class="sxs-lookup"><span data-stu-id="4a26e-114">To retrieve a string that is equivalent to that returned from [**createPFXWStr**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-createpfxwstr), pass the XCN\_CRYPT\_STRING\_BINARY flag in the in the *Encoding* parameter of the [**CreatePFX**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-createpfx) method.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a26e-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="4a26e-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a26e-116">將 Xenroll.dll 對應至 CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="4a26e-116">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="4a26e-117">**IX509Enrollment**</span><span class="sxs-lookup"><span data-stu-id="4a26e-117">**IX509Enrollment**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)
</dt> </dl>

 

 
