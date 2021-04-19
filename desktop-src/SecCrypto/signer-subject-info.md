---
description: 指定要簽署的主旨。
ms.assetid: ba569443-e50f-450b-82cc-b7328f0ca25a
title: SIGNER_SUBJECT_INFO 結構
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SIGNER_SUBJECT_INFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: 05b5d780e50f8ea10fcf68cc90ae7092bbc2c473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989357"
---
# <a name="signer_subject_info-structure"></a><span data-ttu-id="5c0d8-103">簽署者 \_ 主體 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="5c0d8-103">SIGNER\_SUBJECT\_INFO structure</span></span>

<span data-ttu-id="5c0d8-104">**簽署者 \_ 主體 \_ 資訊** 結構會指定要簽署的主旨。</span><span class="sxs-lookup"><span data-stu-id="5c0d8-104">The **SIGNER\_SUBJECT\_INFO** structure specifies a subject to sign.</span></span>

> [!Note]  
> <span data-ttu-id="5c0d8-105">此結構未定義于任何標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="5c0d8-105">This structure is not defined in any header file.</span></span> <span data-ttu-id="5c0d8-106">若要使用這個結構，您必須自行定義，如本主題所示。</span><span class="sxs-lookup"><span data-stu-id="5c0d8-106">To use this structure, you must define it yourself as shown in this topic.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5c0d8-107">語法</span><span class="sxs-lookup"><span data-stu-id="5c0d8-107">Syntax</span></span>


```C++
typedef struct _SIGNER_SUBJECT_INFO {
  DWORD cbSize;
  DWORD *pdwIndex;
  DWORD dwSubjectChoice;
  union {
    SIGNER_FILE_INFO *pSignerFileInfo;
    SIGNER_BLOB_INFO *pSignerBlobInfo;
  };
} SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
```



## <a name="members"></a><span data-ttu-id="5c0d8-108">成員</span><span class="sxs-lookup"><span data-stu-id="5c0d8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="5c0d8-109">**cbSize**</span><span class="sxs-lookup"><span data-stu-id="5c0d8-109">**cbSize**</span></span>
</dt> <dd>

<span data-ttu-id="5c0d8-110">結構的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="5c0d8-110">The size, in bytes, of the structure.</span></span>

</dd> <dt>

<span data-ttu-id="5c0d8-111">**pdwIndex**</span><span class="sxs-lookup"><span data-stu-id="5c0d8-111">**pdwIndex**</span></span>
</dt> <dd>

<span data-ttu-id="5c0d8-112">這個成員是保留的。</span><span class="sxs-lookup"><span data-stu-id="5c0d8-112">This member is reserved.</span></span> <span data-ttu-id="5c0d8-113">它必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="5c0d8-113">It must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="5c0d8-114">**dwSubjectChoice**</span><span class="sxs-lookup"><span data-stu-id="5c0d8-114">**dwSubjectChoice**</span></span>
</dt> <dd>

<span data-ttu-id="5c0d8-115">指定主體是否為檔案或 [*BLOB*](../secgloss/b-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="5c0d8-115">Specifies whether the subject is a file or a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="5c0d8-116">這個成員可以是下列一或多個值。</span><span class="sxs-lookup"><span data-stu-id="5c0d8-116">This member can be one or more of the following values.</span></span>



| <span data-ttu-id="5c0d8-117">值</span><span class="sxs-lookup"><span data-stu-id="5c0d8-117">Value</span></span>                                                                                                                                                                                                                                         | <span data-ttu-id="5c0d8-118">意義</span><span class="sxs-lookup"><span data-stu-id="5c0d8-118">Meaning</span></span>                           |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="SIGNER_SUBJECT_BLOB"></span><span id="signer_subject_blob"></span><dl> <span data-ttu-id="5c0d8-119"><dt>**簽署者 \_主體 \_ BLOB**</dt> <dt>2 (0x2)</dt></span><span class="sxs-lookup"><span data-stu-id="5c0d8-119"><dt>**SIGNER\_SUBJECT\_BLOB**</dt> <dt>2 (0x2)</dt></span></span> </dl> | <span data-ttu-id="5c0d8-120">主體是 BLOB。</span><span class="sxs-lookup"><span data-stu-id="5c0d8-120">The subject is a BLOB.</span></span><br/> |
| <span id="SIGNER_SUBJECT_FILE"></span><span id="signer_subject_file"></span><dl> <span data-ttu-id="5c0d8-121"><dt>**簽署者 \_主題 \_**</dt>檔案 <dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="5c0d8-121"><dt>**SIGNER\_SUBJECT\_FILE**</dt> <dt>1 (0x1)</dt></span></span> </dl> | <span data-ttu-id="5c0d8-122">主體是一個檔案。</span><span class="sxs-lookup"><span data-stu-id="5c0d8-122">The subject is a file.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="5c0d8-123">**pSignerFileInfo**</span><span class="sxs-lookup"><span data-stu-id="5c0d8-123">**pSignerFileInfo**</span></span>
</dt> <dd>

<span data-ttu-id="5c0d8-124">[**簽署者檔案 \_ \_ 資訊**](signer-file-info.md)結構的指標，指定要簽署的檔案。</span><span class="sxs-lookup"><span data-stu-id="5c0d8-124">A pointer to a [**SIGNER\_FILE\_INFO**](signer-file-info.md) structure that specifies the file to sign.</span></span>

</dd> <dt>

<span data-ttu-id="5c0d8-125">**pSignerBlobInfo**</span><span class="sxs-lookup"><span data-stu-id="5c0d8-125">**pSignerBlobInfo**</span></span>
</dt> <dd>

<span data-ttu-id="5c0d8-126">[**簽署者 \_ BLOB \_ 資訊**](signer-blob-info.md)結構的指標，指定要簽署的 blob。</span><span class="sxs-lookup"><span data-stu-id="5c0d8-126">A pointer to a [**SIGNER\_BLOB\_INFO**](signer-blob-info.md) structure that specifies the BLOB to sign.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5c0d8-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c0d8-127">Requirements</span></span>



| <span data-ttu-id="5c0d8-128">需求</span><span class="sxs-lookup"><span data-stu-id="5c0d8-128">Requirement</span></span> | <span data-ttu-id="5c0d8-129">值</span><span class="sxs-lookup"><span data-stu-id="5c0d8-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c0d8-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c0d8-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5c0d8-131">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c0d8-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="5c0d8-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c0d8-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5c0d8-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5c0d8-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c0d8-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c0d8-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c0d8-135">**SignerSign**</span><span class="sxs-lookup"><span data-stu-id="5c0d8-135">**SignerSign**</span></span>](signersign.md)
</dt> <dt>

[<span data-ttu-id="5c0d8-136">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="5c0d8-136">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
