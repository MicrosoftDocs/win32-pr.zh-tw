---
description: 下列各節將討論 Xenroll.dll 所匯出的函式。 每個章節也會討論如何使用 CertEnroll.dll 來取代函式，或指出兩個程式庫之間沒有任何對應存在。
ms.assetid: 06d8dd6f-7a8d-4da5-a99d-9c9d8fb90cfa
title: " (憑證註冊 API) 的 Helper 函式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ee272e7b11c3fccf7975c5356302a2961b32ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320075"
---
# <a name="helper-functions-certificate-enrollment-api"></a><span data-ttu-id="0850f-104"> (憑證註冊 API) 的 Helper 函式</span><span class="sxs-lookup"><span data-stu-id="0850f-104">Helper Functions (Certificate Enrollment API)</span></span>

<span data-ttu-id="0850f-105">下列各節將討論 Xenroll.dll 所匯出的函式。</span><span class="sxs-lookup"><span data-stu-id="0850f-105">Each of the following sections discusses a function exported by Xenroll.dll.</span></span> <span data-ttu-id="0850f-106">每個章節也會討論如何使用 CertEnroll.dll 來取代函式，或指出兩個程式庫之間沒有任何對應存在。</span><span class="sxs-lookup"><span data-stu-id="0850f-106">Each section also discusses how to use CertEnroll.dll to replace the function or indicates that no mapping between the two libraries exists.</span></span>

## <a name="binaryblobtostring"></a><span data-ttu-id="0850f-107">binaryBlobToString</span><span class="sxs-lookup"><span data-stu-id="0850f-107">binaryBlobToString</span></span>

<span data-ttu-id="0850f-108">Xenroll.dll 中的 [**binaryBlobToString**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) 函數會將位元組陣列轉換成字串。</span><span class="sxs-lookup"><span data-stu-id="0850f-108">The [**binaryBlobToString**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-binaryblobtostring) function in Xenroll.dll converts a byte array to a string.</span></span>

<span data-ttu-id="0850f-109">使用 CertEnroll.dll，您就可以在 [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)介面上呼叫 [**VariantByteArrayToString**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring)方法。</span><span class="sxs-lookup"><span data-stu-id="0850f-109">Using CertEnroll.dll, you can call the [**VariantByteArrayToString**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-variantbytearraytostring) method on the [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) interface.</span></span>

## <a name="stringtobinaryblob"></a><span data-ttu-id="0850f-110">stringToBinaryBlob</span><span class="sxs-lookup"><span data-stu-id="0850f-110">stringToBinaryBlob</span></span>

<span data-ttu-id="0850f-111">Xenroll.dll 中的 [**stringToBinaryBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) 函數會將字串轉換為位元組陣列。</span><span class="sxs-lookup"><span data-stu-id="0850f-111">The [**stringToBinaryBlob**](/windows/desktop/api/xenroll/nf-xenroll-ienroll4-stringtobinaryblob) function in Xenroll.dll converts a string to a byte array.</span></span>

<span data-ttu-id="0850f-112">使用 CertEnroll.dll，您就可以在 [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)介面上呼叫 [**StringToVariantByteArray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray)方法。</span><span class="sxs-lookup"><span data-stu-id="0850f-112">Using CertEnroll.dll, you can call the [**StringToVariantByteArray**](/windows/desktop/api/CertEnroll/nf-certenroll-ibinaryconverter-stringtovariantbytearray) method on the [**IBinaryConverter**](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0850f-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="0850f-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0850f-114">將 Xenroll.dll 對應至 CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="0850f-114">Mapping Xenroll.dll to CertEnroll.dll</span></span>](mapping-xenroll-dll-to-certenroll-dll.md)
</dt> <dt>

[<span data-ttu-id="0850f-115">**IBinaryConverter**</span><span class="sxs-lookup"><span data-stu-id="0850f-115">**IBinaryConverter**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ibinaryconverter)
</dt> </dl>

 

 
