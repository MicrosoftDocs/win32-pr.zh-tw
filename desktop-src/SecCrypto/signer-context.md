---
description: 包含已簽署的 BLOB。
ms.assetid: c12d9007-c779-4363-8e28-6387a665a0d6
title: SIGNER_CONTEXT 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_CONTEXT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 4ebc7d5380438fc6cd28a43136273387c1919713
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106971588"
---
# <a name="signer_context-structure"></a><span data-ttu-id="eba66-103">簽署者 \_ 內容結構</span><span class="sxs-lookup"><span data-stu-id="eba66-103">SIGNER\_CONTEXT structure</span></span>

<span data-ttu-id="eba66-104">**簽署者 \_ 內容** 結構包含已簽署的 [*BLOB*](../secgloss/b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="eba66-104">The **SIGNER\_CONTEXT** structure contains a signed [*BLOB*](../secgloss/b-gly.md).</span></span>

> [!Note]  
> <span data-ttu-id="eba66-105">此結構未定義于任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="eba66-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="eba66-106">若要使用這個結構，您必須自行定義，如本主題所示。</span><span class="sxs-lookup"><span data-stu-id="eba66-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="eba66-107">語法</span><span class="sxs-lookup"><span data-stu-id="eba66-107">Syntax</span></span>


```C++
typedef struct _SIGNER_CONTEXT {
  DWORD cbSize;
  DWORD cbBlob;
  BYTE  *pbBlob;
} SIGNER_CONTEXT, *PSIGNER_CONTEXT;
```



## <a name="members"></a><span data-ttu-id="eba66-108">成員</span><span class="sxs-lookup"><span data-stu-id="eba66-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="eba66-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="eba66-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="eba66-110">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="eba66-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="eba66-111">**cbBlob**</span><span class="sxs-lookup"><span data-stu-id="eba66-111">**cbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="eba66-112">**PbBlob** 成員的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="eba66-112">The size, in bytes, of the **pbBlob** member.</span></span>

</dd> <dt>

<span data-ttu-id="eba66-113">**pbBlob**</span><span class="sxs-lookup"><span data-stu-id="eba66-113">**pbBlob**</span></span>
</dt> <dd>

<span data-ttu-id="eba66-114">已簽署 BLOB 的指標。</span><span class="sxs-lookup"><span data-stu-id="eba66-114">A pointer to the signed BLOB.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="eba66-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="eba66-115">Requirements</span></span>



| <span data-ttu-id="eba66-116">需求</span><span class="sxs-lookup"><span data-stu-id="eba66-116">Requirement</span></span> | <span data-ttu-id="eba66-117">值</span><span class="sxs-lookup"><span data-stu-id="eba66-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="eba66-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eba66-118">Minimum supported client</span></span><br/> | <span data-ttu-id="eba66-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eba66-119">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="eba66-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eba66-120">Minimum supported server</span></span><br/> | <span data-ttu-id="eba66-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eba66-121">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="eba66-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eba66-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eba66-123">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="eba66-123">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="eba66-124">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="eba66-124">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
