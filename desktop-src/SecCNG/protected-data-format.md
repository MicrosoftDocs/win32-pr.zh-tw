---
description: 受保護的資料會儲存為 asn.1 編碼的 BLOB。
ms.assetid: 8E287A1F-4EDF-4068-85F7-59A1D73F7BCD
title: 受保護的資料格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bafa230efd704536e9e30b946e5fbf2d403e664
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115184"
---
# <a name="protected-data-format"></a><span data-ttu-id="428ab-103">受保護的資料格式</span><span class="sxs-lookup"><span data-stu-id="428ab-103">Protected Data Format</span></span>

<span data-ttu-id="428ab-104">受保護的資料會儲存為 asn.1 編碼的 BLOB。</span><span class="sxs-lookup"><span data-stu-id="428ab-104">Protected data is stored as an ASN.1 encoded BLOB.</span></span> <span data-ttu-id="428ab-105">資料會格式化為 CMS (憑證訊息語法) 封包的內容。</span><span class="sxs-lookup"><span data-stu-id="428ab-105">The data is formatted as CMS (certificate message syntax) enveloped content.</span></span> <span data-ttu-id="428ab-106">數位信封包含加密的內容、包含加密內容加密金鑰 (CEK) 的收件者資訊，以及包含內容相關資訊的標頭（包括未加密的保護描述項規則字串）。</span><span class="sxs-lookup"><span data-stu-id="428ab-106">The digital envelope contains encrypted content, recipient information that contains an encrypted content encryption key (CEK), and a header that contains information about the content, including the unencrypted protection descriptor rule string.</span></span> <span data-ttu-id="428ab-107">如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="428ab-107">This is shown by the following diagram.</span></span>

![受保護的封包資料](images/protecteddatablob.png)

## <a name="related-topics"></a><span data-ttu-id="428ab-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="428ab-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="428ab-110">CNG DPAPI</span><span class="sxs-lookup"><span data-stu-id="428ab-110">CNG DPAPI</span></span>](cng-dpapi.md)
</dt> <dt>

[<span data-ttu-id="428ab-111">保護描述項</span><span class="sxs-lookup"><span data-stu-id="428ab-111">Protection Descriptors</span></span>](protection-descriptors.md)
</dt> <dt>

[<span data-ttu-id="428ab-112">保護提供者</span><span class="sxs-lookup"><span data-stu-id="428ab-112">Protection Providers</span></span>](protection-providers.md)
</dt> </dl>

 

 



