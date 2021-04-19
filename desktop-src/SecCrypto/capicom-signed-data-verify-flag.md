---
description: 指出驗證數位簽章時要檢查的內容。
ms.assetid: e6259c3f-caed-42f4-832c-250365caa0d7
title: 'CAPICOM_SIGNED_DATA_VERIFY_FLAG 列舉 (Capicom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_SIGNED_DATA_VERIFY_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: bc8db48ee067e8d12bffa9dbff433384058013b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996422"
---
# <a name="capicom_signed_data_verify_flag-enumeration"></a><span data-ttu-id="0a772-103">CAPICOM \_ 簽署的 \_ 資料 \_ 驗證旗標 \_ 列舉</span><span class="sxs-lookup"><span data-stu-id="0a772-103">CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG enumeration</span></span>

<span data-ttu-id="0a772-104">**CAPICOM \_ 帶正負號 \_ 資料 \_ 驗證 \_ 旗** 標列舉指出驗證 [*數位簽章*](../secgloss/d-gly.md)時所檢查的內容。</span><span class="sxs-lookup"><span data-stu-id="0a772-104">The **CAPICOM\_SIGNED\_DATA\_VERIFY\_FLAG** enumeration indicates what is checked when a [*digital signature*](../secgloss/d-gly.md) is verified.</span></span>

## <a name="members"></a><span data-ttu-id="0a772-105">成員</span><span class="sxs-lookup"><span data-stu-id="0a772-105">Members</span></span>



| <span data-ttu-id="0a772-106">member</span><span class="sxs-lookup"><span data-stu-id="0a772-106">Member</span></span>                                           | <span data-ttu-id="0a772-107">描述</span><span class="sxs-lookup"><span data-stu-id="0a772-107">Description</span></span>                                                                                                 | <span data-ttu-id="0a772-108">值</span><span class="sxs-lookup"><span data-stu-id="0a772-108">Value</span></span> |
|--------------------------------------------------|-------------------------------------------------------------------------------------------------------------|-------|
| <span data-ttu-id="0a772-109">**\_ \_ 僅限 CAPICOM 驗證簽章 \_**</span><span class="sxs-lookup"><span data-stu-id="0a772-109">**CAPICOM\_VERIFY\_SIGNATURE\_ONLY**</span></span>             | <span data-ttu-id="0a772-110">只會檢查簽章。</span><span class="sxs-lookup"><span data-stu-id="0a772-110">Only the signature is checked.</span></span><br/>                                                                   | <span data-ttu-id="0a772-111">0</span><span class="sxs-lookup"><span data-stu-id="0a772-111">0</span></span>     |
| <span data-ttu-id="0a772-112">**CAPICOM \_ 驗證簽章 \_ \_ 和 \_ 憑證**</span><span class="sxs-lookup"><span data-stu-id="0a772-112">**CAPICOM\_VERIFY\_SIGNATURE\_AND\_CERTIFICATE**</span></span> | <span data-ttu-id="0a772-113">檢查簽章和用來建立簽章之憑證的有效性。</span><span class="sxs-lookup"><span data-stu-id="0a772-113">Both the signature and the validity of the certificate used to create the signature are checked.</span></span><br/> | <span data-ttu-id="0a772-114">1</span><span class="sxs-lookup"><span data-stu-id="0a772-114">1</span></span>     |



## <a name="requirements"></a><span data-ttu-id="0a772-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a772-115">Requirements</span></span>



| <span data-ttu-id="0a772-116">需求</span><span class="sxs-lookup"><span data-stu-id="0a772-116">Requirement</span></span> | <span data-ttu-id="0a772-117">值</span><span class="sxs-lookup"><span data-stu-id="0a772-117">Value</span></span> |
|----------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0a772-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="0a772-118">Redistributable</span></span><br/> | <span data-ttu-id="0a772-119">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="0a772-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                |
| <span data-ttu-id="0a772-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0a772-120">Header</span></span><br/>          | <dl> <span data-ttu-id="0a772-121"><dt>Capicom</dt></span><span class="sxs-lookup"><span data-stu-id="0a772-121"><dt>Capicom.h</dt></span></span> </dl> |



 

 
