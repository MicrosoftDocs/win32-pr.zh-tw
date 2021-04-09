---
description: ICE81 會驗證 MsiDigitalCertificate 資料表、MsiDigitalSignature 資料表、MsiPatchCertificate 資料表和 MsiPackageCertificate 資料表。
ms.assetid: 83d8bc62-679e-410f-a95c-ffe13952b710
title: ICE81
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2fef8da1027fc739ce8e6e979ca998a1cd053a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691072"
---
# <a name="ice81"></a><span data-ttu-id="31c2f-103">ICE81</span><span class="sxs-lookup"><span data-stu-id="31c2f-103">ICE81</span></span>

<span data-ttu-id="31c2f-104">ICE81 會驗證 [MsiDigitalCertificate 資料表](msidigitalcertificate-table.md)、 [MsiDigitalSignature 資料表](msidigitalsignature-table.md)、 [MsiPatchCertificate 資料表](msipatchcertificate-table.md)和 [MsiPackageCertificate 資料表](msipackagecertificate-table.md)。</span><span class="sxs-lookup"><span data-stu-id="31c2f-104">ICE81 validates the [MsiDigitalCertificate table](msidigitalcertificate-table.md), [MsiDigitalSignature table](msidigitalsignature-table.md), [MsiPatchCertificate table](msipatchcertificate-table.md), and [MsiPackageCertificate Table](msipackagecertificate-table.md).</span></span> <span data-ttu-id="31c2f-105">此 ICE 自訂動作會針對未使用或未參考的數位憑證張貼警告，並在簽署的物件不存在或簽署物件的封包未指向外部資料時張貼錯誤。</span><span class="sxs-lookup"><span data-stu-id="31c2f-105">This ICE custom action posts warnings for digital certificates that are unused or unreferenced, and it posts an error when the signed object does not exist or when the signed object's cabinet does not point to external data.</span></span>

<span data-ttu-id="31c2f-106">請注意，ICE03 會確認 MsiDigitalSignature 資料表的資料表資料行中的專案是 "Media"。</span><span class="sxs-lookup"><span data-stu-id="31c2f-106">Note that ICE03 verifies that the entry in the Table column in the MsiDigitalSignature table is "Media."</span></span>

## <a name="result"></a><span data-ttu-id="31c2f-107">結果</span><span class="sxs-lookup"><span data-stu-id="31c2f-107">Result</span></span>

<span data-ttu-id="31c2f-108">ICE81 會針對未使用或未參考的數位憑證張貼下列警告。</span><span class="sxs-lookup"><span data-stu-id="31c2f-108">ICE81 posts the following warnings for unused or unreferenced Digital Certificates.</span></span>



| <span data-ttu-id="31c2f-109">ICE81 警告</span><span class="sxs-lookup"><span data-stu-id="31c2f-109">ICE81 warning</span></span>                                                                                                                                                      | <span data-ttu-id="31c2f-110">Description</span><span class="sxs-lookup"><span data-stu-id="31c2f-110">Description</span></span>                                                        |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="31c2f-111">在 MsiDigitalSignature、MsiPackageCertificate 或 MsiPatchCertificate 資料表中，找不到 MsiDigitalCertificate 資料表中任何記錄的參考。</span><span class="sxs-lookup"><span data-stu-id="31c2f-111">No reference to any of the records in the MsiDigitalCertificate table could be found in MsiDigitalSignature, MsiPackageCertificate, or MsiPatchCertificate tables.</span></span> | <span data-ttu-id="31c2f-112">如果未使用所有記錄，則會傳回此警告。</span><span class="sxs-lookup"><span data-stu-id="31c2f-112">This warning is returned if all records are unused.</span></span>                |
| <span data-ttu-id="31c2f-113">\[ \] 在 MsiDigitalSignature、MsiPackageCertificate 或 MsiPatchCertificate 資料表中，找不到數位憑證1的參考。</span><span class="sxs-lookup"><span data-stu-id="31c2f-113">No reference to the Digital Certificate \[1\] could be found in MsiDigitalSignature, MsiPackageCertificate, or MsiPatchCertificate tables.</span></span>                         | <span data-ttu-id="31c2f-114">如果未使用某些記錄（但不是全部），則會傳回此警告。</span><span class="sxs-lookup"><span data-stu-id="31c2f-114">This warning is returned if some records, but not all, are unused.</span></span> |



 

<span data-ttu-id="31c2f-115">ICE81 會張貼下列錯誤。</span><span class="sxs-lookup"><span data-stu-id="31c2f-115">ICE81 posts the following errors.</span></span>



| <span data-ttu-id="31c2f-116">ICE81 錯誤</span><span class="sxs-lookup"><span data-stu-id="31c2f-116">ICE81 error</span></span>                                                                                                                                                              | <span data-ttu-id="31c2f-117">Description</span><span class="sxs-lookup"><span data-stu-id="31c2f-117">Description</span></span>                                                                                                                                                    |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31c2f-118">媒體資料表不存在。</span><span class="sxs-lookup"><span data-stu-id="31c2f-118">Media Table does not exist.</span></span> <span data-ttu-id="31c2f-119">因此，MsiDigitalSignature 中的所有專案都不正確</span><span class="sxs-lookup"><span data-stu-id="31c2f-119">Hence all the entries in MsiDigitalSignature are incorrect</span></span>                                                                                   | <span data-ttu-id="31c2f-120">簽署的物件不存在。</span><span class="sxs-lookup"><span data-stu-id="31c2f-120">The signed object does not exist.</span></span> <span data-ttu-id="31c2f-121">如果媒體資料表不存在，但 MsiDigitalSignature 有專案，則會傳回此錯誤。</span><span class="sxs-lookup"><span data-stu-id="31c2f-121">This error is returned if the Media table does not exist but MsiDigitalSignature has entries.</span></span>                                |
| <span data-ttu-id="31c2f-122">\[媒體資料表中缺少已簽署的物件 2 \]</span><span class="sxs-lookup"><span data-stu-id="31c2f-122">Missing signed object \[2\] in Media Table</span></span>                                                                                                                               | <span data-ttu-id="31c2f-123">簽署的物件 \[ 2 不 \] 存在。</span><span class="sxs-lookup"><span data-stu-id="31c2f-123">The signed object \[2\] does not exist.</span></span> <span data-ttu-id="31c2f-124">如果媒體資料表存在，就會傳回此錯誤，但在 MsiDigitalSignature 中的此專案不會出現在媒體資料表中。</span><span class="sxs-lookup"><span data-stu-id="31c2f-124">This error is returned if the Media table exists, but this entry in MsiDigitalSignature is not present in Media table.</span></span> |
| <span data-ttu-id="31c2f-125">具有金鑰2的表1中的專案 \[ \] \[ \] 已簽署。</span><span class="sxs-lookup"><span data-stu-id="31c2f-125">The entry in table \[1\] with key \[2\] is signed.</span></span> <span data-ttu-id="31c2f-126">因此，封包應該指向封裝外的物件， (封包的值不應加上前置詞 \#) </span><span class="sxs-lookup"><span data-stu-id="31c2f-126">Hence the cabinet should point to an object outside the package (the value of Cabinet should NOT be prefixed with \#)</span></span> | <span data-ttu-id="31c2f-127">簽署物件的封包不會指向外部資料。</span><span class="sxs-lookup"><span data-stu-id="31c2f-127">The signed object's cabinet does not point to external data.</span></span> <span data-ttu-id="31c2f-128">\[1 \] 是資料表名稱。</span><span class="sxs-lookup"><span data-stu-id="31c2f-128">\[1\] is table name.</span></span> <span data-ttu-id="31c2f-129">\[2 \] 是媒體資料表中的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="31c2f-129">\[2\] is key in the Media table.</span></span>                                             |



 

## <a name="related-topics"></a><span data-ttu-id="31c2f-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="31c2f-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31c2f-131">ICE 參考</span><span class="sxs-lookup"><span data-stu-id="31c2f-131">ICE Reference</span></span>](ice-reference.md)
</dt> </dl>

 

 



